
```markdown
## EasyPlayfab.Friends

### `public static List<FriendInfo> friends`

This property retrieves the current friend list for the local user.

### `public static void AddFriend(string targetPlayfabId)`

Adds the PlayFab user, based on the `targetPlayfabId`, to the friend list of the local user.

Example:

```
EasyUsages.EasyPlayfab.Friends.AddFriend("TargetPlayerID");
```

### `public static void RemoveFriend(string targetPlayfabId)`

Removes a specified user from the friend list of the local user.

Example:

```
EasyUsages.EasyPlayfab.Friends.RemoveFriend("TargetPlayerID");
```

### `public static void SetFriendTag(string targetPlayfabId, params string[] tags)`

Updates the tag list for a specified user in the friend list of the local user.

Example:

```
EasyUsages.EasyPlayfab.Friends.SetFriendTag("TargetPlayerID", "tag1", "tag2");
```

## EasyPlayfab.PlayerItemManagement

### `public static List<ItemInstance> ownedItems`

This property retrieves the user's owned items.

### `public static void AddUserVirtualCurrency(int amount, string currencyCode, string playfabId = "")`

Adds the user's virtual currency.

Example:

```
EasyUsages.EasyPlayfab.PlayerItemManagement.AddUserVirtualCurrency(100, "Gold");
```

### `public static void SubtractUserVirtualCurrency(int amount, string currencyCode, string playfabId = "")`

Subtracts the user's virtual currency.

Example:

```
EasyUsages.EasyPlayfab.PlayerItemManagement.SubtractUserVirtualCurrency(50, "Gold");
```

### `public static void GrantItemToPlayer(string itemId, string catalogVer, string playfabId = "")`

Grants a PlayFab item to the player.

Example:

```
EasyUsages.EasyPlayfab.PlayerItemManagement.GrantItemToPlayer("ItemID123", "CatalogVersion", "PlayerID");
```

## EasyPlayfab.PlayerDataManagement

### `public static string playfab_username`

This property gets or sets the user's PlayFab username.

### `public static List<ItemInstance> player_ownedItems`

This property retrieves the user's owned PlayFab items.

### `public static Dictionary<string, UserDataRecord> UserData`

This property retrieves the user's data.

### `public static void UpdateUserData(Dictionary<string, string> data, List<string> keysToRemove)`

Updates the user's data.

Example:

```
Dictionary<string, string> data = new Dictionary<string, string>
{
    { "Key1", "Value1" },
    { "Key2", "Value2" }
};
List<string> keysToRemove = new List<string> { "KeyToRemove" };
EasyUsages.EasyPlayfab.PlayerDataManagement.UpdateUserData(data, keysToRemove);
```

## EasyPlayfab.TitleDataManagement

### `public static List<CatalogItem> catalogItems`

This property retrieves the title's catalog items.

### `public static Dictionary<string, string> TitleData`

This property retrieves the title's data.

### `public static List<TitleNewsItem> titleNews`

This property retrieves the title's news items.

## EasyOculus.IAP

### `public static System.Action OnPurchase`

This action is triggered when a purchase is completed.

### `public static void PurchaseSKU(string sku)`

Purchase an Oculus SKU securely.

Example:

```
EasyUsages.EasyOculus.IAP.PurchaseSKU("YourSKU");
```
