<div align="center">
  <h1>Hello, World! Me chamo Altieris Souza, tenho 20 anos e sou desenvolvedor Front-end!</h1>
  <a href="https://github.com/Altieris-Souza">
  <div>
  <br/>
  </div>
    <img height="170em" width="490px" src="https://github-readme-stats.vercel.app/api?username=Altieris-Souza&show_icons=true&theme=dark&include_all_commits=true&count_private=true"/>
    <img height="170em" width="400px" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Altieris-Souza&layout=compact&langs_count=7&theme=dark"/>
  </div>

##

<div align="center"><br>
  <img align="center" alt="Alt-Ts" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg">
  <img align="center" alt="Alt-Ts" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/typescript/typescript-plain.svg">
  <img align="center" alt="Alt-React" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg">
  <img align="center" alt="Alt-CSS" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg">
  <img align="center" alt="Alt-HTML" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
  <img align="center" alt="Alt-CSS" height="50" width="60" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
  <img align="center" alt="Alt-node" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-plain-wordmark.svg">
</div>
  
  <br>

<div align="center"><br>
  <img align="center" alt="Alt-postgres" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-plain.svg" />
  <img align="center" alt="Alt-mySql" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-plain-wordmark.svg" />
  <img align="center" alt="Alt-figma" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/figma/figma-original.svg" />
  <img align="center" alt="Alt-django" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/django/django-plain.svg" />
  <img align="center" alt="Alt-python" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" />
  <img align="center" alt="Alt-jquery" height="50" width="60" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jquery/jquery-plain-wordmark.svg" />
 </div>
 
<div align="center"><br>
  <a href="https://instagram.com/altieris.sf" target="_blank"><img src="https://img.shields.io/badge/-Instagram-%23E4405F?style=for-the-badge&logo=instagram&logoColor=white" target="_blank"></a>
  <a href = "mailto:altmsf15@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/altierissouza/" target="_blank"><img src="https://img.shields.io/badge/-LinkedIn-%230077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
  
  ##
  <html>
<head>
	<meta charset=utf-8 />
	<title>Contador de Visitas</title>

</head>
<body>

<?php

	function get_num_visitas(){
		//conectar
		$link = mysql_connect('localhost', 'root', '');
		if (!$link) {
			die('Não foi possível conectar: ' . mysql_error());
		}
		
		mysql_select_db("contador");
		$query = "SELECT total " .
				 "FROM `visitas` " .
				 "ORDER BY total ASC LIMIT 1";
		$result = mysql_query($query);
		if (!$result) {
			$message  = 'Invalid query: ' . mysql_error() . "\n";
			$message .= 'Whole query: ' . $query;
			die($message);
		}
		if (mysql_num_rows($result) == 0) {
			echo "No rows found, nothing to print so am exiting";
			exit;
		}
		$row = mysql_fetch_array($result);
		mysql_close($link);
		return $row["total"];
		//fazer consulta
		//retornar total
	}

	function imprime_visitas($contador){
		return "<h1>" . $contador . "</h1>";
	}
	
	function contar_visita(){
		//conectar
		$link = mysql_connect('localhost', 'root', '');
		if (!$link) {
			die('Não foi possível conectar: ' . mysql_error());
		}
		
		mysql_select_db("contador");
		$query = "UPDATE `visitas` " .
				 "SET total = total + 1";
		$result = mysql_query($query);
		if (!$result) {
			$message  = 'Invalid query: ' . mysql_error() . "\n";
			$message .= 'Whole query: ' . $query;
			die($message);
		}
		mysql_close($link);
	}

	contar_visita();
	$contador = get_num_visitas();
	echo imprime_visitas($contador);

?>

 
</body>
</html>
  
 
  ![Snake animation](https://github.com/Altieris-Souza/Altieris-Souza/blob/output/github-contribution-grid-snake.svg)
</div>


