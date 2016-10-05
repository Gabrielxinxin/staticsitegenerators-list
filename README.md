<!-- TITLE/ -->

<h1>Static Site Generators Listing</h1>

<!-- /TITLE -->


<!-- BADGES/ -->

<span class="badge-travisci"><a href="http://travis-ci.org/bevry/staticsitegenerators-list" title="Check this project's build status on TravisCI"><img src="https://img.shields.io/travis/bevry/staticsitegenerators-list/master.svg" alt="Travis CI Build Status" /></a></span>
<span class="badge-npmversion"><a href="https://npmjs.org/package/staticsitegenerators" title="View this project on NPM"><img src="https://img.shields.io/npm/v/staticsitegenerators.svg" alt="NPM version" /></a></span>
<span class="badge-npmdownloads"><a href="https://npmjs.org/package/staticsitegenerators" title="View this project on NPM"><img src="https://img.shields.io/npm/dm/staticsitegenerators.svg" alt="NPM downloads" /></a></span>
<span class="badge-daviddm"><a href="https://david-dm.org/bevry/staticsitegenerators-list" title="View the status of this project's dependencies on DavidDM"><img src="https://img.shields.io/david/bevry/staticsitegenerators-list.svg" alt="Dependency Status" /></a></span>
<span class="badge-daviddmdev"><a href="https://david-dm.org/bevry/staticsitegenerators-list#info=devDependencies" title="View the status of this project's development dependencies on DavidDM"><img src="https://img.shields.io/david/dev/bevry/staticsitegenerators-list.svg" alt="Dev Dependency Status" /></a></span>
<br class="badge-separator" />
<span class="badge-slackin"><a href="https://slack.bevry.me" title="Join this project's slack community"><img src="https://slack.bevry.me/badge.svg" alt="Slack community badge" /></a></span>
<span class="badge-patreon"><a href="http://patreon.com/bevry" title="Donate to this project using Patreon"><img src="https://img.shields.io/badge/patreon-donate-yellow.svg" alt="Patreon donate button" /></a></span>
<span class="badge-gratipay"><a href="https://www.gratipay.com/bevry" title="Donate weekly to this project using Gratipay"><img src="https://img.shields.io/badge/gratipay-donate-yellow.svg" alt="Gratipay donate button" /></a></span>
<span class="badge-flattr"><a href="https://flattr.com/profile/balupton" title="Donate to this project using Flattr"><img src="https://img.shields.io/badge/flattr-donate-yellow.svg" alt="Flattr donate button" /></a></span>
<span class="badge-paypal"><a href="https://bevry.me/paypal" title="Donate to this project using Paypal"><img src="https://img.shields.io/badge/paypal-donate-yellow.svg" alt="PayPal donate button" /></a></span>
<span class="badge-bitcoin"><a href="https://bevry.me/bitcoin" title="Donate once-off to this project using Bitcoin"><img src="https://img.shields.io/badge/bitcoin-donate-yellow.svg" alt="Bitcoin donate button" /></a></span>
<span class="badge-wishlist"><a href="https://bevry.me/wishlist" title="Buy an item on our wishlist for us"><img src="https://img.shields.io/badge/wishlist-donate-yellow.svg" alt="Wishlist browse button" /></a></span>

<!-- /BADGES -->


<!-- DESCRIPTION/ -->

A comprehensive, partially automatically generated comparison of static site generators with some minimal meta data about them

<!-- /DESCRIPTION -->


- [View the listing](https://github.com/bevry/staticsitegenerators-list/blob/master/list.json) | [Edit the listing](https://github.com/bevry/staticsitegenerators-list/edit/master/list.json)
- [View the rendered listing](https://staticsitegenerators.net/list.json)
- [View the website](http://staticsitegenerators.net) | [View the website source](https://github.com/bevry/staticsitegenerators-website)


## Contributing

### Requirements

There are generally three types of Content Management Systems:

1. Dynamic Servers (e.g. WordPress, Ghost, DocPad, Harp) — these allow you to have re-render on every request abilities
2. Flat File Content Management Systems (e.g. Yellow, Techy) — these allow you to write your content as files
3. Static Site Generators (e.g. Jekyll, DocPad) — these generate a static website from your input that you can deploy anywhere

Currently, this listing is only for projects that relate to Flat File Content Management Systems and/or Static Site Generators, but not for projects which relate only to Dynamic Servers (such as WordPress and Ghost).

### Adding

Entries are stored within the `list.json` file.

#### Fields

Accepted project fields:

- `name` the project's name
- `github` the slug of the GitHub repository if applicable
- `gitlab` the slug of the GitLab repository if applicable
- `bitbucket` the slug of BitBucket repository if applicable
- `website` the project's website if they have one
- `language` the project's primary programming language if applicable
- `description` the project's description
- `created_at` the project's date of creation in ISO format
- `updated_at` the project's date of last update in ISO format
- `license` the project's [SPDX license code](https://spdx.org/licenses/)
  - if license is missing, omit this field
  - if license is not applicable because it is a commercial service, use `false`
  - if multiple licenses, see the [SPDX parser](https://www.npmjs.com/package/spdx) for formatting
- `tags` at least one or more of the following tags that apply to the project (if no tags apply, it probably isn't related to static site generators):
  - `flat-file` for projects that import file content into a database
  - `generator` for projects that export content to a static website
  - `editor` for projects that provide a custom editing experience for content, e.g. Contentful.com, Prose.io
  - `host` for projects that host generated static content, e.g. GitHub Pages, Surge.sh
  - `extensible` for projects that provide users with directives for adding new features

Dates should be in ISO format which looks like this `2006-08-18T16:00:00.000Z`. Conversion can be done with JavaScript using `console.log(new Date('19-Aug-2006').toISOString())` or via the command line using Node.js via `node -e "console.log(new Date('19-Aug-2006').toISOString())"`.

At the very least, the following fields are required:

- `name`
- `tags`
- `github` or `gitlab` or `bitbucket` or `website`

If `github` is specified, the following fields should only be specified if GitHub's data is incorrect:

- `license`
- `website`
- `language`
- `description`
- `created_at`
- `updated_at`

If `gitlab` is specified, the following fields should only be specified if GitLab's data is incorrect:

- `language`
- `description`
- `created_at`
- `updated_at`

The following fields are automatic and only apply to our rendered listing:

- `stars`
- `forks`
- `watchers`


#### Testing

When you submit your pull request, your submission will be automatically tested, so no need to test locally, however if you do wish to, you can:

1. Install [Node.js](https://learn.bevry.me/node/install) (5-15 minutes)

1. Fork the project and clone your fork - [guide](https://help.github.com/articles/fork-a-repo/) (5 minutes)

1. Install local dependencies (1 minute)

  ``` bash
  npm install
  ```

1. Running the tests (1 minute)

  ``` bash
  npm test
  ```

1. Make any changes that the tests indicate, commit your changes, and submit

<!-- HISTORY/ -->

<h2>History</h2>

<a href="https://github.com/bevry/staticsitegenerators-list/releases">Discover the release history by heading on over to the releases page.</a>

<!-- /HISTORY -->


<!-- BACKERS/ -->

<h2>Backers</h2>

<h3>Maintainers</h3>

These amazing people are maintaining this project:

<ul><li><a href="http://jaspervdj.be">Jasper Van der Jeugt</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=jaspervdj" title="View the GitHub contributions of Jasper Van der Jeugt on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://balupton.com">Benjamin Lupton</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=balupton" title="View the GitHub contributions of Benjamin Lupton on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/davisonio">Craig Davison</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=davisonio" title="View the GitHub contributions of Craig Davison on repository bevry/staticsitegenerators-list">view contributions</a></li></ul>

<h3>Sponsors</h3>

No sponsors yet! Will you be the first?

<span class="badge-patreon"><a href="http://patreon.com/bevry" title="Donate to this project using Patreon"><img src="https://img.shields.io/badge/patreon-donate-yellow.svg" alt="Patreon donate button" /></a></span>
<span class="badge-gratipay"><a href="https://www.gratipay.com/bevry" title="Donate weekly to this project using Gratipay"><img src="https://img.shields.io/badge/gratipay-donate-yellow.svg" alt="Gratipay donate button" /></a></span>
<span class="badge-flattr"><a href="https://flattr.com/profile/balupton" title="Donate to this project using Flattr"><img src="https://img.shields.io/badge/flattr-donate-yellow.svg" alt="Flattr donate button" /></a></span>
<span class="badge-paypal"><a href="https://bevry.me/paypal" title="Donate to this project using Paypal"><img src="https://img.shields.io/badge/paypal-donate-yellow.svg" alt="PayPal donate button" /></a></span>
<span class="badge-bitcoin"><a href="https://bevry.me/bitcoin" title="Donate once-off to this project using Bitcoin"><img src="https://img.shields.io/badge/bitcoin-donate-yellow.svg" alt="Bitcoin donate button" /></a></span>
<span class="badge-wishlist"><a href="https://bevry.me/wishlist" title="Buy an item on our wishlist for us"><img src="https://img.shields.io/badge/wishlist-donate-yellow.svg" alt="Wishlist browse button" /></a></span>

<h3>Contributors</h3>

These amazing people have contributed code to this project:

<ul><li><a href="http://jaspervdj.be">Jasper Van der Jeugt</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=jaspervdj" title="View the GitHub contributions of Jasper Van der Jeugt on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://balupton.com">Benjamin Lupton</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=balupton" title="View the GitHub contributions of Benjamin Lupton on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://davison.io">Craig Davison</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=davisonio" title="View the GitHub contributions of Craig Davison on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/LomigLavnek">Lomig Lavnek</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=LomigLavnek" title="View the GitHub contributions of Lomig Lavnek on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/SurajShukla">Suraj Shukla</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=SurajShukla" title="View the GitHub contributions of Suraj Shukla on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://stoneship.org/">Denis Defreyne</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=ddfreyne" title="View the GitHub contributions of Denis Defreyne on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/ipavl">ipavl</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=ipavl" title="View the GitHub contributions of ipavl on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://klml.de">Klaus Mueller</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=klml" title="View the GitHub contributions of Klaus Mueller on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://japh.com.au">Japh</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=Japh" title="View the GitHub contributions of Japh on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="mixu.net">Mikito Takada</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=mixu" title="View the GitHub contributions of Mikito Takada on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://dbohdan.com/">dbohdan</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=dbohdan" title="View the GitHub contributions of dbohdan on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://tuxproject.de">Cthulhux</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=dertuxmalwieder" title="View the GitHub contributions of Cthulhux on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://davidsiaw.github.io/">David Siaw</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=davidsiaw" title="View the GitHub contributions of David Siaw on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://wikismith.com">Jeffrey Hicks</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=wikismith" title="View the GitHub contributions of Jeffrey Hicks on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.mattlayman.com">Matt Layman</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=mblayman" title="View the GitHub contributions of Matt Layman on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://appernetic.io">Göran</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=appernetic" title="View the GitHub contributions of Göran on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/vikrantrathore">vikrantrathore</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=vikrantrathore" title="View the GitHub contributions of vikrantrathore on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://narno.org">Arnaud Ligny</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=Narno" title="View the GitHub contributions of Arnaud Ligny on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://blog.coolaj86.com">AJ ONeal</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=coolaj86" title="View the GitHub contributions of AJ ONeal on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.bennyklotz.at">Benjamin Klotz</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=tak1n" title="View the GitHub contributions of Benjamin Klotz on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.csslab.cl">Jorge Epuñan</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=juanbrujo" title="View the GitHub contributions of Jorge Epuñan on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://medium.com/@tarkus">Konstantin Tarkus</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=koistya" title="View the GitHub contributions of Konstantin Tarkus on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://datenstrom.se">Mark Seuffert</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=markseu" title="View the GitHub contributions of Mark Seuffert on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://moox.io/">Maxime Thirouin</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=MoOx" title="View the GitHub contributions of Maxime Thirouin on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://pawandubey.com">Pawan Dubey</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=pawandubey" title="View the GitHub contributions of Pawan Dubey on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://ramiro.org/">Ramiro Gómez</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=yaph" title="View the GitHub contributions of Ramiro Gómez on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://robloach.net">Rob Loach</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=RobLoach" title="View the GitHub contributions of Rob Loach on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://emitter.io">Roman Atachiants</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=Kelindar" title="View the GitHub contributions of Roman Atachiants on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.adnetinc.com/">Rudy Affandi</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=lesaff" title="View the GitHub contributions of Rudy Affandi on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="www.micrypt.com">Seyi Ogunyemi</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=micrypt" title="View the GitHub contributions of Seyi Ogunyemi on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.dte.web.id">Taufik Nurrohman</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=tovic" title="View the GitHub contributions of Taufik Nurrohman on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/tomtom">Tom Link</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=tomtom" title="View the GitHub contributions of Tom Link on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://wcm1.web.rice.edu">W. Caleb McDaniel</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=wcaleb" title="View the GitHub contributions of W. Caleb McDaniel on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="harijs.me">harijs.me</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=harijsm" title="View the GitHub contributions of harijs.me on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/jandecaluwe">jandecaluwe</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=jandecaluwe" title="View the GitHub contributions of jandecaluwe on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://chriswarrick.com/">Chris Warrick</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=Kwpolska" title="View the GitHub contributions of Chris Warrick on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="www.isnowfy.com">Rui Wang</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=isnowfy" title="View the GitHub contributions of Rui Wang on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://bomberstudios.com">Ale Muñoz</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=bomberstudios" title="View the GitHub contributions of Ale Muñoz on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://razbakov.com/">Aleksey Razbakov</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=razbakov" title="View the GitHub contributions of Aleksey Razbakov on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://lexoyo.me">Alex Hoyau</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=lexoyo" title="View the GitHub contributions of Alex Hoyau on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://opoo.org/">Alex Lin</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=opoo" title="View the GitHub contributions of Alex Lin on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="www.primoca.com">Alex Thompson</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=pierogitus" title="View the GitHub contributions of Alex Thompson on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://agonzalezro.github.io">Alexandre González</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=agonzalezro" title="View the GitHub contributions of Alexandre González on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://grison.me">Alexandre Grison</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=agrison" title="View the GitHub contributions of Alexandre Grison on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/rudyryk">Alexey Kinev</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=rudyryk" title="View the GitHub contributions of Alexey Kinev on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://amitu.com/">Amit Upadhyay</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=amitu" title="View the GitHub contributions of Amit Upadhyay on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/Aisbergg">Aisbergg</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=Aisbergg" title="View the GitHub contributions of Aisbergg on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/andrewjamesmurray">Andrew Murray</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=andrewjamesmurray" title="View the GitHub contributions of Andrew Murray on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.kalamuna.com">Andrew_Mallis</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=andrewmallis" title="View the GitHub contributions of Andrew_Mallis on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://getgrav.org">Andy Miller</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=rhukster" title="View the GitHub contributions of Andy Miller on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="ankushg.com">Ankush Gupta</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=ankushg" title="View the GitHub contributions of Ankush Gupta on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.anthonnyquerouil.fr">Anthonny Quérouil</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=anthonny" title="View the GitHub contributions of Anthonny Quérouil on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://hashobject.com">Anton Podviaznikov</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=podviaznikov" title="View the GitHub contributions of Anton Podviaznikov on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/anton-iarchuk-sysgears">Anton Iarchuk</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=anton-iarchuk-sysgears" title="View the GitHub contributions of Anton Iarchuk on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://artem.krylysov.com/">Artem Krylysov</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=akrylysov" title="View the GitHub contributions of Artem Krylysov on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://arty.name">Artemy Tregubenko</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=arty-name" title="View the GitHub contributions of Artemy Tregubenko on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.0x743.com">Brett Estrade</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=estrabd" title="View the GitHub contributions of Brett Estrade on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.barryclark.co">Barry Clark</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=barryclark" title="View the GitHub contributions of Barry Clark on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/grv87">Basil Peace</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=grv87" title="View the GitHub contributions of Basil Peace on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://venthur.de">Bastian Venthur</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=venthur" title="View the GitHub contributions of Bastian Venthur on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.zoobab.com">Benjamin Henrion</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=zoobab" title="View the GitHub contributions of Benjamin Henrion on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="www.icir.org/johanna">Johanna</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=0xxon" title="View the GitHub contributions of Johanna on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://whump.com/">Bill Humphries</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=whump" title="View the GitHub contributions of Bill Humphries on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://boscoh.com">Bosco Ho</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=boscoh" title="View the GitHub contributions of Bosco Ho on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://byronkellett.github.io">Byron Kellett</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=ByronKellett" title="View the GitHub contributions of Byron Kellett on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/bullpizzle">Byron LK</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=bullpizzle" title="View the GitHub contributions of Byron LK on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://celehner.com/">Charles Lehner</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=clehner" title="View the GitHub contributions of Charles Lehner on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://webiphany.com">Chris Dawson</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=xrd" title="View the GitHub contributions of Chris Dawson on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="adam-bien.com">Adam Bien</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=AdamBien" title="View the GitHub contributions of Adam Bien on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://lumeh.org/">Colin Chan</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=kalgynirae" title="View the GitHub contributions of Colin Chan on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/elaOnMars">Daniela Knoll</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=elaOnMars" title="View the GitHub contributions of Daniela Knoll on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://dario.im">Dario Castañé</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=imdario" title="View the GitHub contributions of Dario Castañé on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://daveaglick.com">Dave Glick</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=daveaglick" title="View the GitHub contributions of Dave Glick on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.webhook.com">dave.snider@gmail.com</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=snide" title="View the GitHub contributions of dave.snider@gmail.com on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://porkrind.org">David Caldwell</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=caldwell" title="View the GitHub contributions of David Caldwell on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/eads">David Eads</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=eads" title="View the GitHub contributions of David Eads on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://davidherron.com">David Herron</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=robogeek" title="View the GitHub contributions of David Herron on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://davidpennington.me">David Pennington</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=Xeoncross" title="View the GitHub contributions of David Pennington on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="appliedscala.com">Denis</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=denisftw" title="View the GitHub contributions of Denis on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/deber">Denis Bernard</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=deber" title="View the GitHub contributions of Denis Bernard on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/denis-soundcloud">Denis Defreyne</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=denis-soundcloud" title="View the GitHub contributions of Denis Defreyne on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://preaction.me">Doug Bell</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=preaction" title="View the GitHub contributions of Doug Bell on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://aaemnnost.tv">Evan Mattson</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=aaemnnosttv" title="View the GitHub contributions of Evan Mattson on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://rpy.xyz">Evan Sonderegger</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=esonderegger" title="View the GitHub contributions of Evan Sonderegger on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://helpfulsheep.com/">Gabi Nagy</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=g4b1nagy" title="View the GitHub contributions of Gabi Nagy on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.gar1t.com">Garrett Smith</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=gar1t" title="View the GitHub contributions of Garrett Smith on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://shapeshed.com">George Ornbo</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=shapeshed" title="View the GitHub contributions of George Ornbo on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://mhlakhani.com">Hasnain Lakhani</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=mhlakhani" title="View the GitHub contributions of Hasnain Lakhani on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="Saint Aardvark the Carpeted) <aardvark@saintaardvarkthecarpeted.com> (http://saintaardvarkthecarpeted.com">Hugh Brown</a></li>
<li><a href="http://imelnikov.ru">Ivan Melnikov</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=melnikov-ivan" title="View the GitHub contributions of Ivan Melnikov on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.janpecha.cz/">Jan Pecha</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=janpecha" title="View the GitHub contributions of Jan Pecha on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://grow.io">Jeremy Weinstein</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=jeremydw" title="View the GitHub contributions of Jeremy Weinstein on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://jex.im/">Jex</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=JexCheng" title="View the GitHub contributions of Jex on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://campbell.fm">Jim Campbell</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=j1mc" title="View the GitHub contributions of Jim Campbell on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://www.m0ngr31.us">Joe Ipson</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=m0ngr31" title="View the GitHub contributions of Joe Ipson on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://boyne.tech/">Johannes Boyne</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=johannesboyne" title="View the GitHub contributions of Johannes Boyne on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://genehack.org">John SJ Anderson</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=genehack" title="View the GitHub contributions of John SJ Anderson on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/johngtait">John Tait</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=johngtait" title="View the GitHub contributions of John Tait on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="https://github.com/jonschlinkert">Jon Schlinkert</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=jonschlinkert" title="View the GitHub contributions of Jon Schlinkert on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://jonathanbullock.com">Jonathan Bullock</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=jonbullock" title="View the GitHub contributions of Jonathan Bullock on repository bevry/staticsitegenerators-list">view contributions</a></li>
<li><a href="http://saintaardvarkthecarpeted.com">Hugh Brown (Saint Aardvark the Carpeted)</a> — <a href="https://github.com/bevry/staticsitegenerators-list/commits?author=saintaardvark" title="View the GitHub contributions of Hugh Brown (Saint Aardvark the Carpeted) on repository bevry/staticsitegenerators-list">view contributions</a></li></ul>



<!-- /BACKERS -->


<!-- LICENSE/ -->

<h2>License</h2>

Unless stated otherwise all works are:

<ul><li>Copyright &copy; <a href="http://jaspervdj.be">Jasper Van der Jeugt</a></li>
<li>Copyright &copy; 2013+ <a href="http://bevry.me">Bevry Pty Ltd</a></li></ul>

and licensed under:

<ul><li><a href="http://spdx.org/licenses/Unlicense.html">The Unlicense</a></li></ul>

<!-- /LICENSE -->
