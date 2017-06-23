# twitter

## Hide advertising tweets

1. Install [Stylish](https://userstyles.org/) extension
2. Visit [Twitter](http://twitter.com)
3. Click on User Styles button and select Write new style -> For this URL
4. Copy and paste the following and click Save.

``` javascript
@namespace url(http://www.w3.org/1999/xhtml);

@-moz-document domain("twitter.com") {
  .promoted-tweet { display: none; }

}
```
