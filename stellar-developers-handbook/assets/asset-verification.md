## Asset verification

When you issue an asset, it is important to provide clear information about what your asset represents. This info can be discovered and displayed by clients so users know exactly what they are getting when they hold your asset.

#### Step-by-step guide to the basic asset verification:

1. Set [`home_domain`](https://www.stellar.org/developers/guides/concepts/accounts.html#home-domain) field for your asset issuing account. Clients can look up a `stellar.toml` from this domain. 
   - This should be in the format of a [fully qualified domain name](https://en.wikipedia.org/wiki/Fully_qualified_domain_name) such as `example.com`, `anchor.example.com` etc.  
   - DO NOT include scheme (i.e. `http` or `https`) and trailing relative path: `https://example.com` or `example.com/tokens` won't work.  
   - Find more details and code samples [here](https://www.stellar.org/developers/guides/issuing-assets.html#discoverablity-and-meta-information).
2. Create `stellar.toml` following directions from the official Stellar [guide](https://www.stellar.org/developers/guides/concepts/stellar-toml.html).  
   - Do not forget to add the `[[CURRENCIES]]` for each of your assets.
   - Provide a short meaningful asset description (parameters `name`,
    `desc` and `conditions`) to tell your users what it's all about
    (optional).
3. Publish your `stellar.toml` file, clients will search it at the following location: `https://your_domain.com/.well-known/stellar.toml`. 
   - Make sure that CORS (cross-origin resource sharing) is [enabled](https://www.stellar.org/developers/guides/concepts/stellar-toml.html#enabling-cross-origin-resource-sharing-cors).
   - Also check the content type, should be `content-type: text/plain; charset=utf-8`.  Some clients/browsers may not handle it correctly if content is transferred as `application/octet-stream`, not `text/plain` as expected.
 
#### References
 
1. [Stellar Guides - Issuing Assets](https://www.stellar.org/developers/guides/issuing-assets.html#discoverablity-and-meta-information).
2. [Stellar Guides - Accounts](https://www.stellar.org/developers/guides/concepts/accounts.html#home-domain).
3. [Stellar Guides - stellar.toml](https://www.stellar.org/developers/guides/concepts/stellar-toml.html).
4. [Wikipedia - Fully qualified domain names](https://en.wikipedia.org/wiki/Fully_qualified_domain_name).
5. [Enable CORS](https://enable-cors.org/server.html)
6. [Stellar StackExchange - Asset not verified](https://stellar.stackexchange.com/q/1378/366).
7. [Table of Contents](../index)