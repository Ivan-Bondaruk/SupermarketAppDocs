#User Model
Code below show you a model of user that used for user details.
<pre>
```swift
struct UserModel: Codable {
    let id: UUID
    let firstName: String
    let middleName: String
    let lastName: String
    let phone: String
    let points: Int
    let birthday: Date
    
    enum CodingKeys: String, CodingKey {
        case id
        case firstName = "first_name"
        case middleName = "middle_name"
        case lastName = "last_name"
        case phone
        case points
        case birthday
    }
}
```
</pre>

Enum in code below used for supabase coding:
<pre>
```swift
enum CodingKeys: String, CodingKey {
    case id
    case firstName = "first_name"
    case middleName = "middle_name"
    case lastName = "last_name"
    case phone
    case points
    case birthday
}
```
</pre>

All variables names that used in model needs to be same in table columns, but not all variables
we can create with same name so we need to provide coding key - how variable in model looks like in table column.

??? warning "Pay attention to provide right variables declaration" 
    If your variable name not much like in table column you must to provide codingkey.