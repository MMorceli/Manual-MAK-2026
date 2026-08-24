# Segurança e publicação do Manual do Colaborador

## Conclusão

O GitHub Pages em uma conta gratuita **não oferece controle de acesso por funcionário**. Ao publicar este pacote no GitHub Pages gratuito, o HTML, o PDF e o arquivo `manual-data.js` ficarão disponíveis publicamente para qualquer pessoa que obtenha ou descubra o endereço.

Um repositório privado, quando disponível em outro plano, também não torna automaticamente o site do GitHub Pages privado. A publicação privada com controle de acesso é um recurso do GitHub Enterprise Cloud para sites de projeto de organizações.

## Proteções já incluídas

- `robots.txt` bloqueando o rastreamento de todo o site;
- metadados `noindex`, `nofollow`, `noarchive`, `nosnippet` e `noimageindex`;
- política de conteúdo que impede conexões externas e limita scripts, imagens e estilos ao próprio site;
- política de referência para não enviar o endereço da página a outros sites;
- nenhuma biblioteca, fonte, ferramenta de análise ou serviço externo;
- página de erro sem indexação;
- identificação visual de “Uso interno”.

Essas medidas reduzem exposição acidental e indexação por buscadores que respeitam as regras. Elas **não são autenticação**, não impedem download e não garantem sigilo.

## O que não deve ser feito

- Não adicionar senha diretamente no HTML ou JavaScript. O código e a senha seriam enviados ao navegador e poderiam ser visualizados ou contornados.
- Não considerar um endereço difícil de adivinhar como proteção.
- Não colocar senhas, tokens, chaves ou dados pessoais no repositório.
- Não usar apenas `robots.txt` como mecanismo de confidencialidade.

## Publicação recomendada para acesso exclusivo

Use uma plataforma com autenticação no servidor, exigindo a conta corporativa do funcionário antes de entregar qualquer arquivo. Alternativas adequadas incluem:

1. GitHub Enterprise Cloud com GitHub Pages privado e usuários da organização autorizados; ou
2. intranet/SharePoint da empresa com acesso restrito; ou
3. hospedagem protegida por um serviço de identidade corporativa e autenticação no servidor.

Se a empresa permanecer obrigatoriamente no GitHub gratuito, a recomendação de segurança é manter este repositório privado apenas como armazenamento do código e **não ativar o GitHub Pages com o conteúdo interno**.

## Verificações antes de publicar

- confirmar que somente pessoas autorizadas conseguem obter uma resposta do servidor;
- testar o acesso em uma janela anônima: o conteúdo não pode aparecer antes da autenticação;
- exigir HTTPS;
- remover acessos imediatamente quando um funcionário sair da empresa;
- revisar periodicamente quem possui permissão;
- confirmar que o PDF e `manual-data.js` também exigem autenticação quando acessados diretamente.
