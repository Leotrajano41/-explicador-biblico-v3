Crie uma ferramenta web completa em um único arquivo HTML (index.html) com CSS embutido e JavaScript embutido, seguindo o design e as funcionalidades do "Explicador Bíblico Pro".

**Requisitos Gerais:**
1.  **Estrutura:** Um único arquivo `index.html` com `<style>` para CSS e `<script>` para JavaScript.
2.  **Design:** Tema escuro com detalhes em dourado, cabeçalho fixo, abas de navegação, cards para seções e campos de entrada/saída.
3.  **Responsividade:** O layout deve ser adaptável para dispositivos móveis.
4.  **Notificações:** Sistema de toasts (mensagens pop-up) para feedback ao usuário (sucesso, erro, informação).

**Funcionalidades Específicas (abas):**

**1. Aba "Config" (Configurações):**
    *   **Configuração da API:**
        *   Seleção de Provedor de IA: OpenRouter (padrão), OpenAI, Anthropic (Claude), Google Gemini.
        *   Campo para Chave API (tipo password com botão de toggle para mostrar/esconder). Placeholder deve mudar conforme o provedor.
        *   Seleção de Modelo de IA: Grupos para Google (Gemini 2.5 Flash, Gemini 2.5 Pro), Anthropic (Claude Sonnet 4.5, Claude Opus 4), OpenAI (GPT-4o, GPT-4o Mini), Outros (Llama 3.3 70B, DeepSeek R1). Opção "Digitar manualmente..." para modelo customizado.
        *   Botões "Salvar API" e "Testar Conexão".
        *   Área de status da API (ok, erro, info).
    *   **Configurações Gerais:**
        *   Seleção de Duração do Vídeo (Curto, Médio, Longo, Estendido).
        *   Seleção de Tom da Narrativa (Cinematográfico, Didático, Devocional, Investigativo, Épico).
        *   Seleção de Público-Alvo (Geral, Iniciantes, Estudantes Bíblicos, Líderes/Pastores, Jovens).
        *   Seleção de Estilo Visual (Cinematográfico, Moderno, Artístico, Documental).
        *   Seleção de Idioma de Geração:
            *   Português BR (pt)
            *   Inglês (en)
            *   Espanhol (es)
            *   Espanhol LatAm (es-LA)
            *   Francês (fr)
            *   Alemão (de)
            *   Italiano (it)
            *   Russo (ru)
            *   Mandarim (zh)
            *   Japonês (ja)
            *   Árabe (ar)
        *   Botão "Salvar Configurações".
    *   **Persistência:** Todas as configurações (API e Gerais) devem ser salvas e carregadas do `localStorage`.

**2. Aba "Narrativa":**
    *   **Biblioteca de Temas:**
        *   Campo de busca para filtrar temas.
        *   Lista de temas bíblicos pré-definidos, agrupados por categoria (Histórias Épicas, Mistérios Bíblicos, Profecias, Vida de Jesus, Guerras e Batalhas, Origens e Criação, Personagens Marcantes, Arqueologia Bíblica).
        *   Ao clicar em um tema, ele deve preencher o campo "Tema" e ser aplicado a todas as abas.
    *   **Gerador de Narrativa:**
        *   Campo de entrada "Tema".
        *   Seleção de "Ângulo" (Histórico-Cultural, Teológico, Aplicação Prática, Profético, Arqueológico).
        *   Seleção de "Extras" (Nenhum, + Curiosidades, + Arqueologia, + Contexto Cultural).
        *   Botão "Gerar Narrativa Completa".
    *   **Resultado:** Área de output com botão "Copiar".
    *   **Prompt da IA para Narrativa:** Deve instruir a IA a atuar como "roteirista bíblico profissional do canal Explicador Bíblico no YouTube", criar uma narrativa completa com a duração, tom, público, ângulo e extras selecionados, seguindo uma estrutura específica (Gancho, Introdução, Desenvolvimento, Análise Profunda, Aplicação Contemporânea, Conclusão, CTA), e responder no idioma de geração selecionado.

**3. Aba "Ideias":**
    *   **Biblioteca de Temas:** Igual à aba "Narrativa".
    *   **Gerador de Ideias:**
        *   Campo de entrada "Tema".
        *   Seleção de "Quantidade" (5, 10, 20 ideias).
        *   Seleção de "Formato" (Potencial Viral, Série Temática, Perguntas Intrigantes, Mistérios Bíblicos).
        *   Botão "Gerar Ideias".
    *   **Resultado:** Área de output com botão "Copiar".
    *   **Prompt da IA para Ideias:** Deve instruir a IA a atuar como "estrategista de conteúdo do canal Explicador Bíblico no YouTube", gerar ideias de vídeos com a quantidade e formato selecionados, incluindo para cada ideia: Título Principal, Título Alternativo, Descrição, Gancho e Potencial, e responder no idioma de geração selecionado.

**4. Aba "Keywords":**
    *   **Pesquisa de Keywords:**
        *   Campo de entrada "Tema".
        *   Seleção de "Idioma" para as keywords (Português BR, Inglês, Espanhol).
        *   Seleção de "Tipo" (YouTube, Blog/SEO, Ambos).
        *   Botão "Pesquisar Keywords".
    *   **Keywords Geradas:**
        *   Área de output mostrando keywords agrupadas (Principais, Secundárias, Long Tail, Hashtags).
        *   Keywords devem ser clicáveis para seleção.
        *   Área "Selecionadas" para exibir e copiar as keywords clicadas.
    *   **Prompt da IA para Keywords:** Deve instruir a IA a atuar como "especialista em SEO para canais bíblicos no YouTube", gerar keywords para o tema, idioma e tipo selecionados, separando-as em grupos específicos, e responder no idioma de geração selecionado.

**5. Aba "IA Visual":**
    *   **Prompts Visuais:**
        *   Campo de entrada "Cena Bíblica".
        *   Seleção de "Estilo" (Cinematográfico, Pintura Épica, Arte Digital, Arte Antiga, Aquarela).
        *   Seleção de "Ferramenta" (Midjourney, DALL-E 3, Stable Diffusion, Adobe Firefly).
        *   Seleção de "Quantidade" (3, 5, 10 prompts).
        *   Botão "Gerar Prompts Visuais".
    *   **Resultado:** Área de output com botão "Copiar".
    *   **Prompt da IA para Prompts Visuais:** Deve instruir a IA a atuar como "especialista em prompts de imagem IA", criar prompts visuais para a cena, estilo, ferramenta e quantidade selecionados, incluindo para cada prompt: PROMPT [numero] (em inglês), TRADUÇÃO e DICA, e responder no idioma de geração selecionado.

**6. Aba "Thumbnails":**
    *   **Conceitos de Thumbnails:**
        *   Campo de entrada "Tema".
        *   Seleção de "Estilo" (Choque e Impacto, Mistério, Épico, Moderno).
        *   Seleção de "Paleta" (Dourado/Preto, Vermelho/Laranja, Azul/Dourado, Escuro/Dramático).
        *   Botão "Gerar Conceitos".
    *   **Resultado:** Área de output.
    *   **Prompt da IA para Thumbnails:** Deve instruir a IA a atuar como "designer de thumbnails para o canal Explicador Bíblico no YouTube", gerar 3 conceitos de thumbnail para o tema, estilo e paleta selecionados, incluindo para cada conceito: Nome, Elemento Central, Fundo, Texto Principal, Texto Secundário, Efeitos e PROMPT IA (em inglês), e responder no idioma de geração selecionado.

**7. Aba "SEO":**
    *   **SEO Completo:**
        *   Campo de entrada "Tema".
        *   Seleção de "Plataforma" (YouTube, Blog, Ambos).
        *   Seleção de "Objetivo" (Maximizar Views, Ganhar Inscritos, Ranquear no Search).
        *   Botão "Gerar SEO Completo".
    *   **Resultado:** Área de output com botão "Copiar".
    *   **Prompt da IA para SEO:** Deve instruir a IA a atuar como "especialista em SEO para o canal Explicador Bíblico no YouTube", gerar SEO completo para o tema, plataforma e objetivo selecionados, incluindo: Títulos (3 opções), Descrição (200-300 palavras com keywords), Tags (30 separadas por vírgula), Hashtags (10), Categoria Recomendada e Análise de Competitividade, e responder no idioma de geração selecionado.

**8. Aba "Fórmula":**
    *   **Fórmula Viral:**
        *   Campo de entrada "Tema".
        *   Botão "Gerar Fórmula Viral".
    *   **Resultado:** Área de output.
    *   **Prompt da IA para Fórmula Viral:** Deve instruir a IA a atuar como "estrategista de vídeos virais do canal Explicador Bíblico no YouTube", gerar uma fórmula completa de vídeo viral para o tema, incluindo: Gancho (script exato), Problema/Tensão, Desenvolvimento, Loops de Retenção, Revelação Principal, CTA Estratégico, Métricas Alvo e Palavras-chave do Roteiro, e responder no idioma de geração selecionado.

**Instruções Adicionais:**
*   A variável `TEMAS` deve conter a lista de temas bíblicos fornecida anteriormente.
*   As funções `callAI` devem ser robustas para lidar com diferentes provedores de API e modelos, e devem injetar o idioma de geração no prompt final.
*   Todos os elementos HTML devem ter IDs únicos para fácil manipulação via JavaScript.
*   O CSS deve garantir uma interface limpa, moderna e funcional.
