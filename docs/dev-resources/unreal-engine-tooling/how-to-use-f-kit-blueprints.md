# How To Use F-Kit Blueprints

### Create Wallet flow

The flow to create a new wallet is pretty straight forward

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-01-Screen-Shot-2022-10-28-at-2.06.09-PM.png" alt=""><figcaption></figcaption></figure>

It is enough to call the “[*CreateNewWallet*](https://www.notion.so/SolanaWallet-a8095ce998a149d088788c4ebecfcb6f)” function from the SolanaWalletManager.

From the returned Wallet object it is mandatory to set a new password: this can be done with the “[*SetPassword*](https://www.notion.so/SolanaWallet-a8095ce998a149d088788c4ebecfcb6f)” function.

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-02-Screen-Shot-2022-10-28-at-2.11.29-PM.png" alt=""><figcaption></figcaption></figure>

Then it is mandatory to generate a Mnemonic for the given Wallet. This can be done with the “[*GenerateMnemonic*](https://www.notion.so/SolanaWallet-a8095ce998a149d088788c4ebecfcb6f)” function. The Sting returned is the “SeedPhrase” that can be used to restore the wallet.

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-03-Screen-Shot-2022-10-28-at-2.12.08-PM.png" alt=""><figcaption></figcaption></figure>

The new Wallet needs at least an account. An account can be generated with the “*GenerateNewAccount*” function.

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-04-Screen-Shot-2022-10-28-at-2.12.25-PM.png" alt=""><figcaption></figcaption></figure>

Finally, the created wallet can be saved to the local system. This is done with the “*SetSaveSlotName*” and “*SaveWallet*” functions. The SaveSlotName parameter is suggested to be a combination of the wallet name and the public key of the wallet.

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-05-Screen-Shot-2022-10-28-at-2.12.43-PM.png" alt=""><figcaption></figcaption></figure>

### Recover Wallet flow

A wallet can be recovered both with “PrivateKey” or “SeedPhrase”.

In order to restore a wallet you need to create a new Wallet object as shown in the first step of the “Create Wallet Flow”.

### Restore from seed phrase

From the created Wallet object, you need to restore the Mnemonic

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-06-Screen-Shot-2022-10-28-at-2.13.05-PM.png" alt=""><figcaption></figcaption></figure>

Then, in order to retrieve the accounts, a derivation path must be selected

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-07-Screen-Shot-2022-10-28-at-2.13.23-PM.png" alt=""><figcaption></figcaption></figure>

Then it is needed to set a new password for the wallet and save it as seen in the “Create Wallet” flow.

### Restore from private key

From the created wallet object, it is enough to call the “*ImportAccountFromPrivateKey*”

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-08-Screen-Shot-2022-10-28-at-2.13.40-PM.png" alt=""><figcaption></figcaption></figure>

Then it is needed to set a new password for the wallet and save it as seen in the “Create Wallet” flow.

## Unlock an existing wallet

In order to login to an existing wallet it is enought to retrieve the existing wallet from a “SaveSlotName” using the “*GetOrCreateWallet*” and then calll the “*UnlockWallet*” function providing the correct password.

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-09-Screen-Shot-2022-10-28-at-2.14.02-PM.png" alt=""><figcaption></figcaption></figure>

<figure><img src="/images/docs-assets/how-to-use-f-kit-blueprints-10-Screen-Shot-2022-10-28-at-2.14.14-PM.png" alt=""><figcaption></figcaption></figure>
