```shell
#!/bin/bash

# Hello, World! I'm Angus Macapella 👋
# Let's turn this README into a dynamic command-line experience 🚀

whoami="Developer"
currentLocation="South Africa 🌍"
languages=("Python" "JavaScript" "Java")
tools=("VS Code" "Git" "Terminal")

echo "Welcome to the profile of a $whoami from $currentLocation!"
echo "Here's a bit about me:"

# Print out my favorite programming languages
echo "🚀 My Favorite Languages:"
for lang in "${languages[@]}"; do
  echo "   - $lang"
done

# Highlight my preferred tools
echo "🛠️ Preferred Tools:"
for tool in "${tools[@]}"; do
  echo "   - $tool"
done

# Show some GitHub stats
ghUsername="AMACAFELLA"
githubStats=$(curl -s "https://api.github.com/users/$ghUsername")

repos=$(echo "$githubStats" | jq -r '.public_repos')
followers=$(echo "$githubStats" | jq -r '.followers')
following=$(echo "$githubStats" | jq -r '.following')

echo "📊 GitHub Stats:"
echo "   - Public Repositories: $repos"
echo "   - Followers: $followers"
echo "   - Following: $following"

# Let's connect
echo "🌐 Let's Connect:"
echo "   - [LinkedIn](https://www.linkedin.com/in/angus-macapella)"
echo "   - [Portfolio](https://angusmacapella.netlify.app/)"

# End of the README
echo "Thanks for stopping by! Feel free to connect with me. Let's code the future together! 🚀"

# Exit
exit 0
