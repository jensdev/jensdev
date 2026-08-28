## jensdev

TypeScript at [Craftzing](https://www.craftzing.com), Belgium. Expo apps and the APIs behind them.

Mostly I care that the types are honest at the boundary. On the API side that means generating
them from a TypeSpec contract instead of maintaining them by hand. On the Expo side it means
checking the TypeScript surface against what the Swift and Kotlin actually do — when they
disagree, the types are the bug.

**Working with**
`TypeScript` · `Expo` · `React-Native` · `TypeSpec` / `OpenAPI` · `Zod` · `Effect` · `ts-pattern` · `NestJS`

**Recent upstream work**

- [expo/expo](https://github.com/expo/expo) — `anchor` support for Apple Maps annotations, and
  two fixes to iOS camera barcode scanning where the ZXing fallback path disagreed with
  AVFoundation on type strings
- [microsoft/typespec](https://github.com/microsoft/typespec) — a dropped `discriminator.mapping`
  entry when the first union variant caused a circular emit
- [react-native-passkey](https://github.com/f-23/react-native-passkey) — Android Credentials
  1.6.0 / Android 15 support, and realigning the TypeScript types with what the native
  implementations actually do
- [facebook/react-native](https://github.com/facebook/react-native) — custom fonts rendering the
  heaviest face on iOS Fabric when combined with an explicit `fontWeight`

**How I like to build**

- **Contract-first.** The API is authored in TypeSpec, compiled to OpenAPI, and the types, Zod
  schemas, controller interfaces and SDK are generated from it — implementation and docs can't
  drift apart.
- **Typed domains.** DDD and hexagonal ports & adapters, making illegal states unrepresentable
  rather than validating after the fact.
- **Architecture you can read.** C4 levels as Mermaid in the repo, updated in the same PR as the code.
- **Declarative machines.** Fedora + mise + chezmoi: a laptop is one command from ready.
