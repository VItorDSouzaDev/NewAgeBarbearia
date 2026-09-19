# The Modern Cut

Crie o projeto inicial de um site completo para uma barbearia moderna, com agendamento online para os clientes. Identidade visual premium, masculina e boutique, com toque contemporâneo: paleta escura (grafite/preto), acentos em dourado/âmbar e couro, uma serifada de destaque nos títulos e sans-serif limpa no corpo. Invente um nome de barbearia e conteúdo realista (serviços, preços, depoimentos, endereço) — nada de lorem ipsum. Inclua um botão flutuante de contato via WhatsApp.
Stack
React + TypeScript + Tailwind CSS + shadcn/ui
Supabase para autenticação e dados (clientes, barbeiros, serviços, agendamentos)
Motion (Framer Motion) para transições e microinterações
GSAP para a animação inicial da hero
Mobile-first, responsivo em todos os breakpoints padrão do Tailwind/shadcn
Páginas
Home — hero com a animação em GSAP, serviços e preços, equipe de barbeiros, galeria, depoimentos, localização e horário de funcionamento, footer
Agendamento — fluxo serviço → barbeiro → data/horário → revisão → confirmação
Autenticação — login e cadastro do cliente
Área do cliente — meus agendamentos (ver, cancelar, remarcar), perfil, alterar senha
Painel admin (barbeiro/dono) — gerenciar agenda, serviços e clientes
Camada de UX (vale para o app inteiro)
Modais em toda ação que peça senha ou confirme algo sensível: login, alteração de senha, cancelamento de agendamento, exclusão de conta, exclusões no painel admin.
Toasts para feedback de sucesso, erro e conclusão de qualquer ação (agendamento confirmado, erro ao salvar, cancelamento concluído, etc.).
Motion (Framer Motion) para transições de página e microinterações em todo o app — hover em botões e cards, entrada/saída de elementos, troca de estados.
Animações rápidas, discretas e profissionais. Sem exagero: devem parecer resposta imediata, não espetáculo.
Acessibilidade, sem exceção:
Respeitar prefers-reduced-motion (use useReducedMotion ou <MotionConfig reducedMotion="user">)
Foco correto nos modais: vai para o modal ao abrir, fica retido dentro dele (focus trap) e volta ao elemento que o abriu ao fechar
Fechar com ESC sempre que apropriado
Use os componentes Dialog e Toast/Sonner do shadcn/ui como base — eles já nascem acessíveis, então herde esse comportamento em vez de recriar do zero
Animação inicial (GSAP)
Ao carregar a Home, anime a entrada da hero com GSAP — por exemplo, reveal do título e stagger nos elementos seguintes. Curta (cerca de 1 a 1,5s), elegante, e que não bloqueie a interação: o usuário precisa conseguir clicar em qualquer botão mesmo durante a animação. Use o hook useGSAP (@gsap/react) para o cleanup correto dentro do ciclo de vida do React.
Skeleton Loaders
Para todo dado assíncrono (horários disponíveis, lista de agendamentos, galeria, etc.), crie skeletons com o mesmo layout e as mesmas dimensões dos componentes finais — mesma estrutura de card, mesma proporção de imagem. Efeito de shimmer suave, e responsivos nos mesmos breakpoints dos componentes reais.
Antes de gerar o código, me pergunte qualquer coisa que precise para entender exatamente como eu imagino cada funcionalidade.

This project was built with [Lovable](https://lovable.dev).

## Build with Lovable

Continue developing this project in the [Lovable editor](https://lovable.dev/projects/8df8d0f9-18ad-4b62-97f5-d4f75494138a).

- **Ship faster**: describe what you want to build and Lovable handles the code.
- **Stay in sync**: every change made in Lovable is committed straight to this repository.
- **Full ownership**: this code is yours. Push to `main` on GitHub and your changes sync back into Lovable, ready for your next prompt.

## Development

Prefer working locally? You need Node.js and npm — [install with nvm](https://github.com/nvm-sh/nvm#installing-and-updating).

```sh
git clone <this-repository-url>
cd <repository-name>
npm i
npm run dev
```
