# 🎬 Movie Explorer

<div align="center">
  <img src="https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white" alt="Android">
  <img src="https://img.shields.io/badge/Kotlin-0095D5?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin">
  <img src="https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white" alt="Jetpack Compose">
  <img src="https://img.shields.io/badge/Material%20Design-757575?style=for-the-badge&logo=material-design&logoColor=white" alt="Material Design">
</div>

<br>

<div align="center">
  <h3>🎭 Descubra seus filmes favoritos com um design moderno e elegante</h3>
  <p>Um aplicativo Android nativo desenvolvido com Jetpack Compose para explorar filmes usando a API do OMDb</p>
</div>

---

## ✨ Características

### 🎨 **Design Moderno**
- **Interface elegante** seguindo Material Design 3
- **Gradientes vibrantes** e cores personalizadas
- **Animações suaves** e transições fluidas
- **Tipografia hierárquica** para melhor legibilidade
- **Tema escuro/claro** com suporte automático

### 🔍 **Funcionalidades**
- **Busca de filmes** em tempo real
- **Interface em português** totalmente localizada
- **Cards informativos** com posters e detalhes
- **Estados visuais** para loading, erro e vazio
- **Feedback visual** interativo

### 🛠 **Tecnologias**
- **Jetpack Compose** para UI moderna
- **Material Design 3** para componentes
- **Retrofit** para comunicação com API
- **Coil** para carregamento de imagens
- **MVVM Architecture** com ViewModel
- **Coroutines** para operações assíncronas

---

## 📱 Screenshots

<div align="center">
  <img src="https://via.placeholder.com/300x600/6C5CE7/FFFFFF?text=Tela+Principal" alt="Tela Principal" width="200">
  <img src="https://via.placeholder.com/300x600/74B9FF/FFFFFF?text=Resultados" alt="Resultados" width="200">
  <img src="https://via.placeholder.com/300x600/E17055/FFFFFF?text=Detalhes" alt="Detalhes" width="200">
</div>

---

## 🚀 Como Executar

### Pré-requisitos
- Android Studio Hedgehog ou superior
- Android SDK 24+ (Android 7.0)
- Kotlin 1.8.0+
- Gradle 8.0+

### Instalação

1. **Clone o repositório**
   ```bash
   git clone https://github.com/seu-usuario/movie-explorer.git
   cd movie-explorer
   ```

2. **Abra no Android Studio**
   - Abra o Android Studio
   - Selecione "Open an existing project"
   - Navegue até a pasta do projeto

3. **Configure a API Key**
   - Obtenha uma chave gratuita em [OMDb API](http://www.omdbapi.com/apikey.aspx)
   - Substitua `8f785fa1` pela sua chave em `MovieViewModel.kt`

4. **Execute o projeto**
   - Conecte um dispositivo Android ou inicie um emulador
   - Clique em "Run" ou use `Shift + F10`

---

## 🏗 Arquitetura

```
app/
├── src/main/java/com/example/movieexplorer/
│   ├── data/                    # Modelos de dados
│   │   ├── Movie.kt
│   │   ├── MovieDetail.kt
│   │   └── MovieSearchResponse.kt
│   ├── di/                      # Injeção de dependência
│   │   └── Module.kt
│   ├── ui/
│   │   ├── theme/               # Tema e cores
│   │   │   ├── Color.kt
│   │   │   ├── Theme.kt
│   │   │   └── Type.kt
│   │   └── viewmodel/           # ViewModels
│   │       └── MovieViewModel.kt
│   └── MainActivity.kt          # Activity principal
└── src/main/res/
    ├── values/
    │   ├── colors.xml           # Cores do Android
    │   └── strings.xml          # Strings localizadas
    └── drawable/                # Recursos visuais
```

---

## 🎨 Design System

### Cores Principais
- **Primary**: `#6C5CE7` (Roxo vibrante)
- **Secondary**: `#74B9FF` (Azul claro)
- **Tertiary**: `#E17055` (Laranja)
- **Background**: Gradiente suave
- **Surface**: Cards elevados

### Tipografia
- **Display**: 32sp, Bold
- **Headline**: 22sp, Bold
- **Title**: 16sp, SemiBold
- **Body**: 14sp, Regular
- **Label**: 12sp, Medium

---

## 🔧 Configuração da API

### OMDb API
Este projeto usa a [OMDb API](http://www.omdbapi.com/) para buscar informações sobre filmes.

1. Acesse [OMDb API](http://www.omdbapi.com/apikey.aspx)
2. Registre-se para obter uma chave gratuita
3. Substitua a chave no arquivo `MovieViewModel.kt`:

```kotlin
private val apiKey = "SUA_CHAVE_AQUI"
```

### Limitações da API Gratuita
- 1.000 requisições por dia
- Apenas busca básica de filmes
- Sem detalhes completos (plot, diretor, etc.)

---

## 📦 Dependências

```kotlin
dependencies {
    // Core Android
    implementation("androidx.core:core-ktx:1.12.0")
    implementation("androidx.lifecycle:lifecycle-runtime-ktx:2.7.0")
    implementation("androidx.activity:activity-compose:1.8.2")
    
    // Jetpack Compose
    implementation(platform("androidx.compose:compose-bom:2023.08.00"))
    implementation("androidx.compose.ui:ui")
    implementation("androidx.compose.ui:ui-graphics")
    implementation("androidx.compose.material3:material3")
    implementation("androidx.lifecycle:lifecycle-viewmodel-compose:2.7.0")
    
    // Networking
    implementation("com.squareup.retrofit2:retrofit:2.9.0")
    implementation("com.squareup.retrofit2:converter-gson:2.9.0")
    implementation("com.squareup.okhttp3:logging-interceptor:4.12.0")
    
    // Image Loading
    implementation("io.coil-kt:coil-compose:2.5.0")
}
```

---

## 🤝 Contribuindo

Contribuições são sempre bem-vindas! Para contribuir:

1. **Fork** o projeto
2. **Crie** uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. **Push** para a branch (`git push origin feature/AmazingFeature`)
5. **Abra** um Pull Request

---

## 📄 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

## 👨‍💻 Autor

**Seu Nome**
- GitHub: [@seu-usuario](https://github.com/seu-usuario)
- LinkedIn: [Seu LinkedIn](https://linkedin.com/in/seu-perfil)

---

## 🙏 Agradecimentos

- [OMDb API](http://www.omdbapi.com/) por fornecer dados de filmes
- [Jetpack Compose](https://developer.android.com/jetpack/compose) pela framework moderna
- [Material Design](https://material.io/) pelo sistema de design
- Comunidade Android por todo o suporte

---

<div align="center">
  <p>Feito com ❤️ e Jetpack Compose</p>
  <p>⭐ Se gostou do projeto, deixe uma estrela!</p>
</div>