# Aula-08-ES

Exercício Prático
Sistema de Streaming (tipo Netflix/Prime)
Contexto: Você vai modelar um sistema simples de streaming.

# 📋 Etapa 1 — Miro + Draw.io

Monte o diagrama de classes com:

Classes:
- Plataforma (nome, pais)
- Usuario (nome, email, plano)
- Catalogo (titulo, qtdFilmes)
- Filme (titulo, duracao, genero)
- Avaliacao (nota, comentario)
  
Relacionamentos para você descobrir e justificar:
1. Plataforma → Catalogo
2. Catalogo → Filme
3. Usuario → Avaliacao
4. Avaliacao → Filme
   
🧠 Pergunta-chave: Se a Plataforma fechar, o Catálogo some? E os Filmes?
Use isso para decidir: Agregação ou Composição?

# 💻 Etapa 2 — Google Colab / VS Code
Implemente as classes em Python seguindo o diagrama que você criou no Miro.

Deve funcionar assim:

    """
    netflix = Plataforma("Netflix", "EUA")
    catalogo = Catalogo("Filmes em Destaque", 0)
    filme1 = Filme("Oppenheimer", 180, "Drama")
    filme2 = Filme("Barbie", 114, "Comédia")
    catalogo.add_filme(filme1)
    catalogo.add_filme(filme2)
    usuario = Usuario("Ana", "ana@email.com", "Premium")
    avaliacao = Avaliacao(9.5, "Incrível! Assisti duas vezes")
    usuario.avaliar(filme1, avaliacao)
    catalogo.listar_filmes()
    usuario.ver_avaliacoes()
