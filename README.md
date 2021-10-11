# Vault Shamir

[Hashicorp Vault's Shamir](https://github.com/hashicorp/vault/tree/master/shamir) implementation as a standalone go module.

## Example

```golang
import (
    "gitlab.com/unit410/vault-shamir/shamir"
)

func main() {
    secret := []byte{...}
    numShares := 5
    numThreshold := 3

    shares, err := shamir.Split(secret, numShares, numThreshold)
    // usual err handling
    recombinedSecret, err := shamir.Combine(shares)
}
```
