# Página de assinatura de revisão de PR

Página estática usada pelo fluxo de emails da mbtech. O botão do email abre
esta página com `?t=<token>`; ela consulta a Edge Function `assinatura` no
Supabase, mostra os dados do PR e envia o nome e o parecer de quem assina.

Está aqui, e não no Supabase, porque o domínio `supabase.co` devolve todo HTML
como `text/plain` com CSP `sandbox`.

Não contém segredo: o token vem na URL e toda a gravação acontece na Edge
Function, que usa a chave de serviço do lado do servidor.
