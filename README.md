The Midgard RPG Server soruce

adding changes to server:
1)so that only mods will make villnila mobs spawn.
2)all worlds will be defualt Void , this makes it easyer for RPG servers since most use a custom map.
3) anything else i need to change for The Midgard Project including Porting plugins or Mods to work.

Compilation
-----------

We use Gradle to handle our dependencies.

1. Checkout project.
2. Init submodules : git submodule update --init --recursive
3. Setup workspace : gradlew setupCauldron
4. Build binaries  : gradlew buildPackages
Note: all binaries will be in distributions folder

Optional
---------
5: After doing Build binaries and testing then Run "gradlew genPatches" (in the Cauldron-Reloaded root) to generate patch files for Minecraft base classes in the Cauldron-Reloaded root Patches Folder. (only do this if your pushing to github to update your Fork Source or making a Pull Request to add to Main Repo, so when ppl update there forks or do new clone and do gradlew setupCauldron they will get the source patched in the Eclipse Workspace folder) 

Profiling
---------

We use YourKit as our Java Profiler.

YourKit is kindly supporting open source projects with its full-featured Java Profiler.
YourKit, LLC is the creator of innovative and intelligent tools for profiling
Java. Take a look at YourKit's leading software products:
* [YourKit Java Profiler](http://www.yourkit.com/java/profiler/index.jsp)


Coding and Pull Request Conventions
-----------

* We generally follow the Sun/Oracle coding standards.
* No tabs; use 4 spaces instead.
* No trailing whitespaces.
* No CRLF line endings, LF only; will be converted automatically by git
* No 80 column limit or 'weird' midstatement newlines.
* The number of commits in a pull request should be kept to a minimum (squish them into one most of the time - use common sense!).
* No merges should be included in pull requests unless the pull request's purpose is a merge.
* Pull requests should be tested (does it compile? AND does it work?) before submission.
* Any major additions should have documentation ready and provided if applicable (this is usually the case).
* Most pull requests should be accompanied by a corresponding GitHub ticket so we can associate commits with GitHub issues (this is primarily for changelog generation on ci.md-5.net).
* Try to follow test driven development where applicable.

If you make changes to or add upstream classes (net.minecraft, net.minecraftforge, cpw.mods.fml, org.bukkit, org.spigotmc) it is mandatory to:

* Make a separate commit adding the new net.minecraft classes (commit message: "Added x for diff visibility" or so).
* Then make further commits with your changes.
* Mark your changes with:
    * 1 line; add a trailing: `// Cauldron [- Optional reason]`
    * 2+ lines; add
        * Before: `// Cauldron start [- Optional comment]`
        * After: `// Cauldron end`
* Keep the diffs to a minimum (*somewhat* important)

Tips to get your pull request accepted
-----------
Making sure you follow the above conventions is important, but just the beginning. Follow these tips to better the chances of your pull request being accepted and pulled.

* Make sure you follow all of our conventions to the letter.
* Make sure your code compiles under Java 6.
* Provide proper JavaDocs where appropriate.
* Provide proper accompanying documentation where appropriate.
* Test your code.
* Make sure to follow coding best practices.
* Provide a test plugin/mod binary and source for us to test your code with.
* Your pull request should link to accompanying pull requests.
* The description of your pull request should provide detailed information on the pull along with justification of the changes where applicable.

Credits
-------

* [MCP](http://mcp.ocean-labs.de) - permission to use data to make Cauldron.
* [Forge](http://www.minecraftforge.net) - mod support.
* [CraftBukkit](http://bukkit.org) - plugin support.
* [Spigot](http://www.spigotmc.org) - performance optimizations.
* Blood and the MinecraftPortCentral Team.
