---
layout: marketing
path: /postgraphile/
title: PostGraphile - full GraphQL API server in an instant from PostgreSQL database
---

<!-- **************************************** -->

<header class='hero simple'>
<div class='hero-block center'>

# PostGraphile: instant GraphQL API for PostgreSQL database

<div class='d-flex justify-content-center'>
<br />
<a class='button button--outline-white' href='/postgraphile/introduction/'>Documentation &rarr;</a>
</div>


</div><!-- /container -->
</header>



<!-- **************************************** -->

<section>
<div class='container center'>
<div class='row'>
<div class='col-xs-12'>
<div class='hero-block'>

## Solves N+1 queries issues

Using graphile-build's [look-ahead](/graphile-build/look-ahead/) features a
single root level GraphQL query, no matter how nested, can become just one SQL
query.

</div>
</div><!-- /col-xs-12 -->

</div><!-- /row -->
</div><!-- /container -->
</section>

<!-- **************************************** -->

<section>
<div class='container center'>

<div class='row'>
<div class='col-xs-12'>
<div class='hero-block'>

## Customisable with SQL

We support [custom queries](/postgraphile/custom-queries/), [custom
mutations](/postgraphile/custom-mutations/) and [computed
columns](/postgraphile/computed-columns/) in your PostgreSQL
database automatically.

</div>
</div>
</div>

</div>
</section>

<!-- **************************************** -->

<section>
<div class='container center'>

<div class='row'>
<div class='col-xs-12'>
<div class='hero-block'>

## Customisable with JS plugins

The GraphQL schema PostGraphile uses is entirely built from [Graphile Build
plugins](https://github.com/graphile/graphile-build/tree/master/packages/graphile-build-pg/src/plugins),
you can disable any of the built in plugins to restrict the functionality or
add additional plugins to extended or enhanced your generated schema.

This allows you to add (or remove) fields, create new types, add functionality,
replace functionality or or even tweak existing functionality (e.g. wrapping an
existing resolver with your own higher-order function) to gain powerful control
over your API.

</div>
<div class='row'>
<div class='col-lg-6 col-xs-12'>

##### Build your schema with plugins
```js
buildSchema(plugins)
 
```

```graphql{2}
type Person {
  # @deprecated Use 'name' instead
  # The person's first name
  firstName: String

  #...
```

</div><!-- /col-6 -->
<div class='col-lg-6 col-xs-12'>

##### Transform your schema with ease
```js
buildSchema([...plugins,
  DeprecateFromCommentPlugin])
```

```graphql{3-4}
type Person {
  # The person's first name
  firstName: String @deprecated(
    reason: "Use 'name' instead")

  #...
```

</div>
</div>
</div>
</section>

<!-- **************************************** -->

<!-- **************************************** -->

<section>
<div class='container center'>
<div class='row'>
<div class='col-xs-12'>
<div class='hero-block'>

## Fully compatible

Graphile uses the <a href="http://graphql.org/graphql-js/">reference GraphQL implementation</a>
under the hood, so you know it's spec compliant.

You can use regular GraphQL objects from other libraries in your generated
schema - you only need to change the parts of your code that you wish to trigger hooks for.

</div>
</div>
</div><!-- /row -->
</div><!-- /container -->
</section>

<!-- **************************************** -->

<section>
<div class='container center'>

<div class='row'>
<div class='col-xs-12'>
<div class='hero-block'>

## GraphiQL with auto-generated documentation

![GraphiQL displaying allSuperheroes](./graphiql-superheroes.png)

</div>
</div>
</div>

</div>
</section>

<!-- **************************************** -->

<section>
<div class='container center'>
<div class='row'>
<div class='col-xs-12'>
<div class='hero-block'>

## PostgreSQL schema watching

PostGraphile has an excellent developer experience (DX) when you use the
`--watch` CLI flag - it will automatically re-generate the GraphQL schema when
your database changes. What's more, it will automatically reload GraphiQL's
documentation too, so you can see your new schema features right away! No need
to restart the server!

</div>
</div><!-- /col-9 -->

</div><!-- /row -->
</div><!-- /container -->
</section>



<!-- **************************************** -->

<section>
<div class='container center'>
<div class='row justify-content-center'>
<div class='text-center col-xs-12'>
<div class='hero-block'>

## Quick to start

</div>


```js
npm install -g postgraphile
postgraphile -c postgres://user:pass@host/dbname --schema schema_name
```

<br />
<div class='d-flex justify-content-center'>
<a class='button button--outline' href='/graphile-build/getting-started/'>Get started &rarr;</a>
</div>

</div><!-- /col-xs-12 -->
</div><!-- /container -->
</section>


<section class='mailinglist'>
<div class='container'>

<div class='row justify-content-center'>
<div class='col-xs-12'>
<div class='hero-block center'>

  ## Questions, comments or feedback? <a href='mailto:info@graphile.org?subject=Graphile%20question%2Fcomment%2Ffeedback%3A'>info@graphile.org</a></h2>

</div>
</div>
</div>

<div class='row justify-content-center'>
<div class='col-xs-12 center'>
<div class='hero-block'>
<div>
<form action="//graphile.us16.list-manage.com/subscribe/post?u=d103f710cf00a9273b55e8e9b&amp;id=c3a9eb5c4e" method="post"
id="mc-embedded-subscribe-form" name="mc-embedded-subscribe-form" class="validate" target="_blank" novalidate>
  <div id="mc_embed_signup_scroll center hero-block">
    <p>Keep up to date on Grapile and PostGraphile features/changes.
    Subscribe to our occasional announcements newsletter:</p>
    <div class="mc-field-group form-inline justify-content-center">
      <div class='form-group'>
        <label for="mce-EMAIL">Email address</label>
        <input
          autocapitalize="off"
          autocomplete="off"
          autocorrect="off"
          class="required email signup-field form-control mx-sm-3"
          id="mce-EMAIL"
          name="EMAIL"
          spellcheck="false"
          type="email"
          value=""
        />
        <!-- real people should not fill this in and expect good things - do not remove this or risk form bot signups-->
        <div style="position: absolute; left: -5000px;" aria-hidden="true"><input type="text" name="b_d103f710cf00a9273b55e8e9b_c3a9eb5c4e" tabindex="-1" value=""></div>
        <input
          class="button btn btn-primary signup-button"
          id="mc-embedded-subscribe"
          name="subscribe"
          type="submit"
          value="Subscribe"
        />
        </div>
      </div>
      <div id="mce-responses" class="clear">
        <div class="response" id="mce-error-response" style="display:none"></div>
        <div class="response" id="mce-success-response" style="display:none"></div>
      </div>
    </div>
  </div>
</form>
</div>
<!--End mc_embed_signup-->
</div>
</div>
</div>

</div>
</section>

<!-- **************************************** -->