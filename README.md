# Failing test case with importmap-rails 1.1.0 and React Native WebView

The following breaks on React Native WebView (JS isn't loaded):

```
<WebView
  source={{
    uri: "http://localhost:3000",
    originWhitelist={[
      'https://*',
      'blob:*',
      'http://localhost:3000',
    ]}
  }}
/>
```

This used to work with importmap-rails 1.0.3.

Might be linked to https://github.com/rails/importmap-rails/pull/128
