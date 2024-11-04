# MelScript Termux

O MelScript facilita o desenvolvimento de aplicações web interativas e dinâmicas com sintaxe simples e poderosa.

Ideal para criar interfaces intuitivas, manipular o DOM e interagir com APIs externas.

## Como Instalar no seu Termux

Primeiro você precisa adicionar o repositório ao APT:

```bash
echo 'deb [trusted=yes] https://melscript-termux.github.io/repo stable main' >> $PREFIX/etc/apt/sources.list.d/melscript.list
```

Depois você precisa sincronizar o seu termux:

```bash
yes | apt update -y
```

E então você pode baixar melscript:

```bash
apt install melscript
```

## Como utilizar melscript

O programa mel-exec injeta melscript automaticamente no seu HTML

Tudo o que você precisa, é simplesmente utilizar a linguagem e executar com o comando mel-exec

### Exemplo index.html

```html
<html>
	<head>
		<meta charset="utf-8" />
		<title>MelScript Hello World</title>
	</head>
	<body>
		<mel>
		funcao Saudacao() {
			imprimir("Olá a todos");
		}
		Saudacao();
		</mel>
	</body>
</html>
```

### Exemplo comando

O comando deve ser executado na pasta onde o index.html está:

```bash
cd mel-exemplo
mel-exec --address localhost --port 8080
```
