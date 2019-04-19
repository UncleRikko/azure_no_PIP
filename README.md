# azure_no_PIP
disallows public IP creation in an azure subscription
{
    "policyRule": {
    "if": {
      "anyOf": [
        {
          "source": "action",
          "like": "Microsoft.Network/publicIPAddresses/*"
        }
      ]
    },
    "then": {
      "effect": "deny"
    }
  }
  }
