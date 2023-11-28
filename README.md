# gymcontrol




## step-by-step

>npm init -y (cria package.json)

npm i typescript @types/node tsx tsup -D
	tsx - executar typescript em node
	tsup - criar build da aplicação -> ts to js
	-D	dev dependences

npx tsc --init
	ts config
	npx executor de pacotes binarios
	mudar target para es2020

npm i fastify
	framework já possui suporte a ts

dividir server.ts com app.ts
	ajuda a nao subir um server rodando test
	passar no listen	host: '0.0.0.0' ajuda fastify a ter acessar front futuro

.npmrc
	save-exact=true //salva versao exata dos pacotes

npm i dotenv
	.env

npm i zod
	validação

npm i prisma -D
	interface de linha de cmd ORM
	npx prisma init
	npx prisma generate //

npm i @prisma/client
	acessar o banco

npx prisma migrate dev
	compara as alterações e atualiza o banco
npx prisma migrate deploy
	para produção

npx prisma studio
	visualizar banco

npm i bcryptjs
	@types/bcryptjs -D
	hashing senhas

npm i vitest vite-tsconfig-paths @vitest/coverage-v8 -D
	//vite-tsconfig-paths entender os paths @/

	tests
	package.json
		"test": "vitest run", roda test uma vez
    "test:watch": "vitest" monitora e roda qlquer alteração
		"test:coverage": "vistest run --coverage" // relatorio de cobertura de tests
		colocar courage gitignore
