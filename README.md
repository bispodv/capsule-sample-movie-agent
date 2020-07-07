<p align="Center">
  <img src="https://bixbydevelopers.com/dev/docs-assets/resources/dev-guide/bixby_logo_github-11221940070278028369.png">
  <br/>
  <h1 align="Center">Bixby Movie Agent Sample Capsule</h1>
</p>

Watching movies is a way to travel to new worlds.
This Capsule is like a travel agent to help you find your next movie adventure.

## Usage

1. Clone this repo.
1. Get started with the [Bixby Studio](https://bixbydevelopers.com/dev/docs/dev-guide/developers/ide).
1. Run a query in the [Simulator](https://bixbydevelopers.com/dev/docs/dev-guide/developers/ide.simulator).
   1. Open the Simulator window.
   1. Pick a target device and locale.
   1. Compile NL.
   1. Enter your query by text or voice. See use cases below for example utterances.

## Use Cases

| Use Cases | Example Utterances |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Recommend a movie: <br> When no other inputs are specified, prompt for a genre <br> - Provide a selection of genres, with the "genre of the day" highlighted at the top <br> - Display a conversation driver "Help me choose" to launch the quiz to infer a genre | "What movie should I watch?" |
| Play a quiz: <br> - Launch a quiz to infer a genre by asking a series of personality type questions <br> - The genre will be used to recommend a movie. | "Play the movie quiz" <br> "Help me choose" when on the genre prompt |
| Recommend a movie by genre | "Recommend a fantasy movie" |
| Browse movies by release window | "Show me movies released last spring" |
| Find movies involving person (cast or crew member) <br> When multiple people share the same name, disambiguate with a selection prompt | "What movies feature Emma Watson" <br> "Find movies by James Cameron" |
| Find movies with a combination of inputs | "What movies did Xavier Dolan work on last year?" <br> "What documentaries came out last spring?" |

## Code Puzzles
For hands-on exercises that build upon this Capsule, head over to the [Code
Puzzles](./codelab/CODELAB.md).

## Device- And Locale-Specific Views

### File Structure

All views and layouts belong in a subfolder of the Resources subfolder. These subfolders can be the `base` folder, a device-specific folder such as `bixby-watch`, a locale-specific folder such as `en`, or a device- and locale-specific folder such as `bixby-watch-en`. 

In this capsule, there are two subfolders that contain views and layouts: 

1. `base`
1. `bixby-watch`

The `base` folder contains the views and layouts that are common across all targets. This means that a view or layout does not need to be customized if the information does not need to be presented differently depending on the user's device.

The `bixby-watch` folder contain views and layouts for their respective devices. These will be used to provide users with the experience intended for the watch target when invoking this capsule from their watch device.

### Design Decisions

There are two methods of customizing views for each target: dedicated views and in-line routing. [This article](https://bixbydevelopers.zendesk.com/knowledge/articles/360047341294) in our Help Center provides more information on how to do both.

The method used in this capsule is defining dedicated views for each target rather than in-line device-specific routing. The reason for this is the stark difference between the mobile and watch views. If done in-line, the resulting view would be bloated and quite hard to maintain moving forward. In-line changes should be limited to small tweaks rather than for large customizations.

## References

### Data Source

The Movie DB (TMDb). This product uses the TMDb API but is not endorsed or certified by TMDb.

https://www.themoviedb.org

https://www.themoviedb.org/documentation/api

https://developers.themoviedb.org/3

https://www.themoviedb.org/documentation/api/terms-of-use

---

## Additional Resources

### Your Source for Everything Bixby
* [Bixby Developer Center](http://bixbydevelopers.com) - Everything you need to get started with Bixby Development!
* [Bixby News, Blogs and Tutorials](https://bixby.developer.samsung.com/) - Bixby News, Tutorials, Blogs and Events

### Guides & Best Practices
* [Quick Start Guide](https://bixbydevelopers.com/dev/docs/get-started/quick-start) - Build your first capsule
* [Design Guides](https://bixbydevelopers.com/dev/docs/dev-guide/design-guides) - Best practices for designing your capsules
* [Developer Guides](https://bixbydevelopers.com/dev/docs/dev-guide/developers) - Guides that take you from design and modeling all the way through deployment of your capsules

### Bixby Videos
* [Bixby Developers YouTube Channel](https://www.youtube.com/c/bixbydevelopers) - Tutorial videos, Presentations, Capsule Demos and more

### Bixby Podcast
* [Bixby Developers Chat](http://bixbydev.buzzsprout.com/) - Voice, Conversational AI and Bixby discussions 

### Bixby on Social Media
* [@BixbyDevelopers](https://twitter.com/bixbydevelopers) - Twitter
* [Facebook](https://facebook.com/BixbyDevelopers)
* [Instagram](https://www.instagram.com/bixbydevelopers/)

### Need Support?
* Have a feature request? Please suggest it in our [Support Community](https://support.bixbydevelopers.com/hc/en-us/community/topics/360000183273-Feature-Requests) to help us prioritize.
* Have a technical question? Ask on [Stack Overflow](https://stackoverflow.com/questions/tagged/bixby) with tag “bixby”

