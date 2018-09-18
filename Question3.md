---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: 
question: Playing with others ?
left_image: Q3A.jpg
left_text: Gaming solo
right_image: Q3B.jpg
right_text: Gaming multi

next_link: "resultat"
---
<html lang="en">
<head>
  <title>{{ page.question }}</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css">
  <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>
  <script type="text/javascript">
	function gen_url(choice) {
		var result = /[&?]result=([^&]+)/.exec(location.search);
		result = result ? result[1].replace(/"/g, '&quot;') : '';
		result = "<a href=\"{{ page.next_link }}".concat(result,choice).concat("\">");
		document.write(result);
	}
  </script>
</head>
<body>

	<div class="jumbotron text-center">
	  <h1>{{ page.question }}</h1>
	</div>

	<div class="container">
	  <div class="row">
		<div class="col-sm-6">
		  <script>gen_url(0);</script>
			<img src="{{ page.left_image }}" class="img-responsive" alt="{{ page.left_text }}" width="700" height="700"> 
		</div>
		<div class="col-sm-6">
		  <script>gen_url("1");</script>
			<img src="{{ page.right_image }}" class="img-responsive" alt="{{ page.right_text }}" width="700" height="700"> 
		</div>
	  </div>
	</div>

</body>
</html>
