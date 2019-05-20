# Sequelize exercise - Full Stack JavaScript Techdegree

### Sequelize Blog application
A simple blog application built using the Sequelize ORM, which allows us to talk to a SQL database (SQLite in this case) using Node.js

## To view project
1. Download project.
2. Run 'npm install' in the command line.
3. Run 'npm start' in the command line.
4. Go to 'localhost:3000' in your browser.

***
<!-- <img src="https://res.cloudinary.com/dtqevfsxh/image/upload/v1554483544/portfolio/expressFlashcards.png" width="500px"> -->

<!-- ## View project
:mag: Live version available at [nickhericks.github.io/reactScoreboardPremium/](https://nickhericks.github.io/reactScoreboardPremium/) -->

## Tools used
- Sequelize ORM

## Code example
```javascript
/* GET individual article route */
router.get('/:id', function(req, res, next) {
	Article.findByPk(req.params.id)
		.then(function(article) {
			if(article) {
				res.render('articles/show', { article: article, title: article.title });
			} else {
				res.send(404);
			}
		})
		.catch(function(err) {
			res.send(500);
		});
});
```

## Acknowledgements
This project was built as part of the [Full Stack JavaScript Techdegree](https://join.teamtreehouse.com/techdegree/) offered by [Treehouse](https://teamtreehouse.com) :raised_hands:
