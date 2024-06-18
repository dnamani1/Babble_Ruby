# Ruby Babble Game

## Overview
The Ruby Babble game is a single-player text-based game inspired by Scrabble. The player tries to form words from a set of seven randomly selected letters. Each valid word formed scores points based on the letters used. The game continues until the player chooses to quit or the tile bag is empty.

## Game Rules
- **Tile Rack**: The player has a rack of seven letters to form words.
- **Tile Bag**: The game starts with a tile bag containing 98 tiles, following the standard Scrabble distribution (excluding blank tiles).
- **Scoring**: Points are awarded based on the Scrabble values of the letters used in the word.
- **Word Formation**: Valid words remove their letters from the rack, which are then replenished from the tile bag.
- **Game End**: The game ends when the tile bag is empty or the player types `:QUIT`.

## Setup Instructions
1. **Clone Repository**:
   ```bash
   git clone https://github.com/yourusername/rubybabble.git
   cd rubybabble
   ```

2. **Install Dependencies**:
   - Create a `Gemfile` with the following content:
     ```ruby
     source "https://rubygems.org"
     gem 'spellchecker'
     ```
   - Run `bundle install` to install the required gem.

3. **Configure Rake**:
   - Create a `Rakefile` with the following content:
     ```ruby
     require 'rake/testtask'

     Rake::TestTask.new do |t|
         t.pattern = "tests/*/test_*.rb"
     end

     task :babble do |t|
       ruby "babble.rb"
     end
     ```

4. **Run Tests**:
   ```bash
   rake test
   ```

5. **Play the Game**:
   ```bash
   rake babble
   ```

## How to Play
1. Run the game using `rake babble`.
2. The game will display your tile rack.
3. Enter a word using the letters from your tile rack.
4. The game will check the word and update your score.
5. Type `:QUIT` to end the game.

## Contributing
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a new Pull Request.
