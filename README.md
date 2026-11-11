# Privacy Policy — Na Ponta da Língua: Word Game

**Last updated:** November 10, 2026

**Document version:** 1.0

> The Brazilian Portuguese version of this policy is the primary document; this is its English
> counterpart. Where the two differ, the Portuguese text governs in Brazil.

---

## 1. Who we are

**Na Ponta da Língua: Palavras** (Google Play package `com.talero.napontadalngua`) is developed
and published by **Talero** ("we", "us").

- **Data controller (LGPD art. 5, VI; GDPR art. 4(7)):** Talero
- **Privacy contact e-mail:** **talero.dev@gmail.com**
- **Website:** https://github.com/talero-dev/napontadalngua-privacy-policy

Contacting us about privacy is free and we answer within **15 days** of your request.

## 2. One-screen summary

- The game works **offline** and requires **no account, login, e-mail address or phone number**.
- **We do not collect your name, e-mail, phone number, contacts, photos, files, microphone, camera
  or GPS location.** None of those permissions is requested.
- Your **progress, statistics and preferences stay on your device only.** We do not upload them —
  we run no servers of our own.
- What does leave the device goes to **Google services** embedded in the app: advertising
  (Google AdMob) and, where enabled, usage measurement (Firebase Analytics), crash reporting
  (Firebase Crashlytics) and remote configuration (Firebase Remote Config). Those services may
  collect **device identifiers,
  in-app interaction events, diagnostics and your IP address** (which allows an approximate,
  city- or region-level location estimate).
- The app is rated **13+** and is **not directed to children**.
- You can erase everything at any time from **Settings → Privacy → Delete my data**
  ("Apagar meus dados").

## 3. What data is processed

### 3.1 Data that stays on your device

Stored locally (app database and preferences) and **never transmitted**:

| Data | Purpose |
|---|---|
| In-progress round (guesses already made on today's word) | Resume where you left off, even after closing the app |
| Finished rounds, streaks and guess distribution | Build the Statistics screen |
| Recently used practice answers | Avoid repeating the same word immediately |
| Unlocked Archive puzzles | Keep an unlock permanent |
| Preferences: theme, colour-blind mode, hard mode, haptics, sound, language, reminder time | Keep the app configured the way you set it |
| Ad consent state and ad frequency counters | Honour your choice and avoid over-serving ads |

All of it is erased when you use **Delete my data** or uninstall the app.

> Android Auto Backup may copy progress, statistics and preferences to your Google account if you
> have backup enabled. That backup is controlled by you and Google, not by us; ad consent state
> and Google library identifiers are **excluded** from it. To turn it off: **Android Settings →
> Google → Backup**.

### 3.2 Data processed by the Google services inside the app

The Firebase services listed below are used only where they are enabled in the app; where they are,
they may process the data described.

| Category | Concrete examples | Collected by |
|---|---|---|
| Device or other identifiers | Android Advertising ID (AAID), App Set ID, Firebase installation ID, Crashlytics installation UUID, Analytics instance ID | AdMob, Firebase Analytics, Crashlytics, Firebase Installations |
| App interactions | app opens, screens viewed, round start and end, ad taps, rewarded video views, result shares | AdMob, Firebase Analytics |
| Diagnostics and crash logs | stack traces, app state, device model, Android version, app version, free memory, time to crash, ad SDK performance | Crashlytics, AdMob |
| IP address and approximate location derived from it | estimated region/city, used to select the ad and to localise reporting | AdMob, Firebase |

**Location:** the app **neither requests nor uses** a location permission
(`ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION`) and does not use GPS. The "approximate
location" above is only the estimate any internet service can make from the connection's IP
address.

**Never transmitted:** the words you type, the day's answer, individual letters, or any free text.
Usage events record only the shape of the game (mode, word length, won or lost, number of
attempts) — never the content.

### 3.3 What the app does not do

We do not use contacts, calendar, camera, microphone, files, SMS, call logs, biometrics, health or
financial data, nor any permanent device identifier (IMEI, serial number). There are no in-app
purchases, no subscriptions and no user accounts.

## 4. Permissions the app declares

The installed package declares the permissions below. A few are ours; most come from Google
libraries and appear in the merged manifest whether or not we wrote them. All are "normal"
permissions — Android shows no dialog for any of them except notifications.

| Permission | Why | Source |
|---|---|---|
| `INTERNET` | Load ads, fetch remote configuration, send metrics and crash reports. The game itself works offline. | Ours + SDKs |
| `ACCESS_NETWORK_STATE` | Check connectivity before attempting a network request | Ours + SDKs |
| `POST_NOTIFICATIONS` | Optional daily reminder. Requested **in context**, after a win, never on first launch; declining removes no game functionality | Ours |
| `com.google.android.gms.permission.AD_ID` | Access the Android Advertising ID, required by Google for apps targeting Android 13 or higher | Google Mobile Ads SDK; also declared by Firebase Analytics |
| `android.permission.READ_BASIC_PHONE_STATE` | Basic network signals used by the ads SDK (carrier / connection type). Grants no access to the phone number or IMEI | Google Mobile Ads SDK |
| `android.permission.ACCESS_ADSERVICES_AD_ID`, `android.permission.ACCESS_ADSERVICES_ATTRIBUTION` | Android Privacy Sandbox APIs used by Google measurement for privacy-preserving attribution | Firebase Analytics (play-services-measurement) |
| `com.google.android.finsky.permission.BIND_GET_INSTALL_REFERRER_SERVICE` | Read the Google Play install referrer (campaign) once | Firebase Analytics (play-services-measurement) |
| `android.permission.WAKE_LOCK` | Keep the CPU awake while a short metrics upload completes | Firebase Analytics (play-services-measurement) |
| `android.permission.FOREGROUND_SERVICE` | Required by the AndroidX WorkManager library that schedules the daily reminder. **We run no foreground service.** | AndroidX WorkManager |
| `com.talero.napontadalngua.DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION` | Internal signature-protection permission created by the AndroidX Core library; it grants access to nothing of yours | AndroidX Core |

We request no location, contacts, camera, microphone, storage, phone, SMS, exact alarm or
`QUERY_ALL_PACKAGES` permission.

## 5. Third-party services and their policies

Every service below is Google's. Each has its own policy, which governs what it collects.

| Service | Role in the app | What it processes | Policy |
|---|---|---|---|
| **Google AdMob / Google Mobile Ads SDK** | Serves the ads (banner, interstitial, rewarded video) | Advertising ID, App Set ID, IP address (approximate location), ad interactions, SDK diagnostics | <https://policies.google.com/technologies/partner-sites> and <https://support.google.com/admob/answer/6128543> |
| **Google User Messaging Platform (UMP)** | Presents and records the privacy consent form (GDPR / US states) and stores your choice | Consent choices, approximate country by IP | <https://developers.google.com/admob/android/privacy> |
| **Firebase Analytics** | Measures aggregate usage (screens, rounds, ad funnel) so we can improve the game | Analytics instance ID, Advertising ID, usage events, device model/language/country, IP address | <https://firebase.google.com/support/privacy> |
| **Firebase Crashlytics** | Reports crashes and freezes so we can fix them | Stack traces, app state, device metadata, Crashlytics installation UUID | <https://firebase.google.com/support/privacy> |
| **Firebase Remote Config** | Adjusts game parameters (ad frequency, daily-word epoch) without an app update | Firebase installation ID, basic device data, IP address | <https://firebase.google.com/support/privacy> |
| **Firebase Installations** | Provides the installation identifier used by Analytics, Crashlytics and Remote Config | Installation ID, basic app and device data | <https://firebase.google.com/support/privacy> |
| **Google Play In-App Review / In-App Update** | Shows the review invitation and the update prompt, both rendered by Google Play itself | Handled by Google Play; the app receives nothing back beyond "completed" | <https://policies.google.com/privacy> |

Google's general privacy policy: <https://policies.google.com/privacy>.
How Google uses data from apps and sites that use its services:
<https://policies.google.com/technologies/partner-sites>.

We use no ad mediation networks, no third-party analytics SDKs, no embedded social networks, no
tracking pixels and no attribution tools beyond those listed.

## 6. Advertising, consent and the Advertising ID

### 6.1 How ads work here

The app is free and funded by advertising. We follow the rules we set for ourselves: ads never
cover content, never appear during an active round, never sit next to the game keyboard, never
appear on app exit, and rewarded videos are always started by you with the reward stated up front.

The ads SDK is configured with a maximum ad content rating of **PG**, tagged as **not directed to
children** and **not for users under the age of consent**.

### 6.2 Personalised ads and your choice

- **In the European Economic Area, the United Kingdom and Switzerland**, and in US states with
  their own privacy legislation, the app shows a Google (UMP) consent form **before** any ad
  request. We request ads only if consent allows it.
- You can review or change that choice at any time in **Settings → Privacy → Privacy options**
  (the entry appears when your region requires the form).
- Your consent choice is also forwarded to Firebase Analytics through **Consent Mode v2**
  (`analytics_storage`, `ad_storage`, `ad_user_data`, `ad_personalization`).
- **In Brazil** the Google form may not appear, because the LGPD allows legal bases other than
  consent for advertising. You still control ad personalisation through Android itself
  (section 6.3).

### 6.3 Advertising ID: what it is and how to reset it

The **Android Advertising ID (AAID)** is a resettable identifier Google provides for advertising.
It contains no name or e-mail address, but it is personal data under both the LGPD and the GDPR.

To reset or delete it:

1. Open Android **Settings**.
2. Go to **Privacy → Ads** (on some devices: **Google → Ads**, or **Security & privacy → More
   privacy → Ads**).
3. Tap **Reset advertising ID** for a fresh identifier, or **Delete advertising ID** so apps
   receive no identifier at all.

Deleting the advertising ID removes no game functionality: ads simply become non-personalised.

## 7. How long data is kept

| Where | Retention |
|---|---|
| On your device (progress, statistics, preferences) | Until you erase it in the app or uninstall. No automatic expiry. |
| Firebase Analytics — user-level and event-level data | For the retention period set in the Firebase console, the shortest of which is **2 months**. Aggregate reports, which identify no one, are kept by Google indefinitely. |
| Firebase Crashlytics — crash reports | Approximately **90 days**, per Firebase documentation. |
| Firebase Remote Config / Installations | For as long as the app is installed; the installation ID is regenerated on reinstall. |
| Google AdMob | Per Google's own retention policies for advertising data. We have neither access to the raw logs nor control over that period. |

## 8. Legal bases and your rights

### 8.1 LGPD — Law 13.709/2018 (Brazil)

Brazil is our primary market and the LGPD governs this processing.

**Legal bases we rely on:**

| Processing | Legal basis |
|---|---|
| Storing progress, statistics and preferences on the device | Performance of the service you asked for by installing and opening the game (art. 7, V) |
| Crash reporting and diagnostics | Legitimate interest in keeping the app working and secure (art. 7, IX), with minimal, non-identifying data |
| Aggregate usage measurement | Legitimate interest in improving the product (art. 7, IX) |
| Personalised advertising | Consent where the Google form is shown (art. 7, I); outside those regions, legitimate interest (art. 7, IX), always with the option to opt out through the Advertising ID — see 6.2 |
| Daily reminder | Consent, given through the notification permission (art. 7, I) |

**Your rights (art. 18):** confirmation that processing exists; access; correction of incomplete,
inaccurate or outdated data; anonymisation, blocking or deletion of unnecessary or unlawfully
processed data; portability; information about whom we share data with; information about the
option not to consent and its consequences; and withdrawal of consent.

Because there is no account or sign-up, **we cannot link any data to you by name or e-mail.** To
exercise rights over data held by Google you will need your Advertising ID (section 6.3) — or you
can simply use **Delete my data** and reset that ID, which achieves the same result in practice.
Write to **talero.dev@gmail.com** and we will walk you through it.

Complaints may be addressed to the Brazilian data protection authority,
**ANPD**: <https://www.gov.br/anpd>.

### 8.2 GDPR / UK GDPR (EEA, United Kingdom and Switzerland)

If you are in those regions, the legal bases are **consent** (art. 6(1)(a)) for personalised
advertising and the purposes covered by the UMP form, and **legitimate interests** (art. 6(1)(f))
for crash reporting, security and aggregate measurement.

You have the right of access, rectification, erasure, restriction, portability, objection to
processing based on legitimate interests, and withdrawal of consent at any time (which does not
affect processing already carried out). You may also lodge a complaint with your national
supervisory authority.

Because Google's servers are located in, among other places, the United States, international
transfers occur. Google states that it relies on Standard Contractual Clauses and the Data Privacy
Framework for those transfers — details at <https://business.safety.google/privacy/>.

### 8.3 United States (CCPA/CPRA and equivalent state laws)

We do not sell personal information for money. Sharing identifiers with Google for personalised
advertising may qualify as a "sale" or "share" under some of those laws; in the regions covered,
the Google form presents an opt-out, and deleting the Advertising ID through Android has the same
effect.

### 8.4 Other regions

If the app is distributed in regions covered by laws such as Türkiye's KVKK or Indonesia's UU PDP,
the same mechanisms apply: the UMP form controls, the Advertising ID and the **Delete my data**
function.

## 9. Children and teenagers

**The app is not directed to children.** The target audience declared on Google Play is **13 and
over** (age bands 13–15, 16–17 and 18+). **We do not participate in the Google Play Designed for
Families programme** and we use no ads SDK self-certified for child audiences.

We do not knowingly collect data from children under 13. The icon, feature graphic, screenshots
and store copy are deliberately designed not to appeal to children.

If you are a parent or guardian and believe a child under 13 used the app, write to
**talero.dev@gmail.com**: we will guide you through the local deletion (section 10) and
the Advertising ID reset, which is the entirety of what is identifiable.

## 10. How to delete your data

### 10.1 In the app (recommended)

1. Open **Na Ponta da Língua**.
2. Tap the **gear** icon (Settings) in the top app bar.
3. Scroll to the **Privacy** section.
4. Tap **Delete my data** ("Apagar meus dados").
5. Confirm in the **"Delete your data?"** dialog by tapping **Delete**.

This immediately and permanently erases:

- the local database (progress, finished rounds, statistics, streaks, Archive unlocks);
- all preferences (theme, colour-blind mode, hard mode, haptics, sound, language, reminder);
- Firebase Analytics data held on the device, via `resetAnalyticsData()`, which also generates a
  new instance ID;
- the **Firebase installation ID**, which disassociates the device from earlier data in Analytics,
  Crashlytics and Remote Config;
- crash reports not yet uploaded;
- the ad consent state (the form reappears when your region requires it).

It cannot be undone.

### 10.2 By uninstalling

Uninstalling removes all local storage. If Android Auto Backup is enabled, a copy of your progress
may remain in your Google account — delete it under **Android Settings → Google → Backup**.

### 10.3 Data already held by Google

Once you have deleted locally and reset the Advertising ID (section 6.3), earlier data can no
longer be associated with your device and expires within the periods in section 7. For requests
made directly to Google, use <https://myactivity.google.com> and
<https://policies.google.com/privacy>.

### 10.4 By e-mail

Write to **talero.dev@gmail.com** with the subject **"Delete my data"**. Since there is no
sign-up, we will ask for your Advertising ID and the approximate dates of use in order to locate
any record. We answer within 15 days.

## 11. Security

- All network traffic uses **HTTPS/TLS**. The app disables cleartext traffic
  (`cleartextTrafficPermitted="false"`) and trusts only system certificate authorities.
- Local data lives in the app's private storage, isolated by the Android sandbox and protected by
  device encryption.
- We log no personal data; debug logging is stripped from the production build.
- No component of the app is exported except the launcher screen, which must be.

No system is perfectly secure, but since we operate no servers and hold no personal data, the
exposure surface is small by construction.

## 12. Game content

The word lists are derived from open-licensed Brazilian Portuguese sources and are filtered
through a blocklist that removes offensive, sexual, violent and discriminatory terms. Sources,
versions, licences and attributions are listed in the in-app **About → Word sources** screen.

## 13. Changes to this policy

When this policy changes materially we update the date at the top, publish the new version at this
same URL and notify you inside the app on next launch. Continuing to use the app after a change
means you are aware of the new version.

## 14. Contact us

**Data controller:** Talero
**Privacy contact:** talero.dev@gmail.com

---

# Política de Privacidade (Português) — Na Ponta da Língua: Palavras

**Última atualização:** 10 de novembro de 2026

**Versão do documento:** 1.0

---

## 1. Quem somos

O aplicativo **Na Ponta da Língua: Palavras** (identificador na Google Play:
`com.talero.napontadalngua`) é desenvolvido e publicado por **Talero**, doravante "nós".

- **Controlador dos dados (LGPD, art. 5º, VI):** Talero
- **E-mail de contato para privacidade:** **talero.dev@gmail.com**
- **Site:** https://github.com/talero-dev/napontadalngua-privacy-policy

Falar com a gente sobre privacidade é de graça e a resposta sai em até **15 dias** a contar do
pedido.

## 2. Resumo em uma tela

- O jogo funciona **offline** e **não exige cadastro, login, e-mail nem número de telefone**.
- **Nós não coletamos seu nome, e-mail, telefone, agenda, fotos, arquivos, microfone, câmera nem
  localização por GPS.** Nenhuma dessas permissões é pedida.
- Seu **progresso, estatísticas e preferências ficam guardados apenas no seu aparelho**. Não
  enviamos nada disso para servidores nossos — aliás, não temos servidores próprios.
- O que sai do aparelho vai para **serviços do Google** que usamos dentro do app: anúncios
  (Google AdMob) e, quando ativos, medição de uso (Firebase Analytics), relatórios de falha
  (Firebase Crashlytics) e configuração remota (Firebase Remote Config). Esses serviços podem
  coletar **identificadores do
  aparelho, eventos de uso, dados de diagnóstico e o endereço IP** (que permite estimar a
  localização aproximada, no nível de cidade ou região).
- O app é para **maiores de 13 anos** e **não é direcionado a crianças**.
- Você pode apagar tudo a qualquer momento em **Configurações → Privacidade → Apagar meus dados**.

## 3. Que dados são tratados

### 3.1 Dados que ficam só no seu aparelho

Guardados localmente (banco de dados do app e preferências), **sem transmissão**:

| Dado | Para quê |
|---|---|
| Progresso da partida em andamento (tentativas já feitas na palavra do dia) | Continuar de onde você parou, inclusive depois de fechar o app |
| Histórico de rodadas concluídas, sequência (streak) e distribuição de tentativas | Montar a tela de Estatísticas |
| Palavras já sorteadas no Treino | Evitar repetir a mesma palavra logo em seguida |
| Puzzles do Arquivo desbloqueados | Manter o desbloqueio permanente |
| Preferências: tema, modo daltônico, modo difícil, vibração, som, idioma, horário do lembrete | Deixar o app do jeito que você configurou |
| Estado do consentimento de anúncios e contadores de frequência de anúncios | Respeitar sua escolha e não exagerar na quantidade de anúncios |

Esses dados são apagados quando você usa **Apagar meus dados** ou desinstala o aplicativo.

> O backup automático do Android (Auto Backup) pode copiar progresso, estatísticas e preferências
> para a sua conta Google, se você tiver o backup ligado no aparelho. Esse backup é controlado por
> você e pelo Google, não por nós; os dados de consentimento de anúncios e os identificadores das
> bibliotecas do Google ficam **excluídos** do backup. Para desligar: **Configurações do Android →
> Google → Backup**.

### 3.2 Dados tratados pelos serviços do Google dentro do app

Os serviços do Firebase listados abaixo só são usados quando estão ativos no app; nesse caso, podem
tratar os dados descritos.

| Categoria | Exemplos concretos | Quem coleta |
|---|---|---|
| Identificadores do aparelho ou outros identificadores | ID de publicidade do Android (AAID), App Set ID, ID de instalação do Firebase, UUID de instalação do Crashlytics, ID de instância do Analytics | AdMob, Firebase Analytics, Crashlytics, Firebase Installations |
| Interações no app | abertura do app, telas visitadas, início e fim de rodada, toques em anúncios, visualizações de vídeo recompensado, compartilhamento de resultado | AdMob, Firebase Analytics |
| Diagnóstico e registros de falha | pilha de chamadas (stack trace) da falha, modelo do aparelho, versão do Android, versão do app, memória livre, tempo até a falha, desempenho do SDK de anúncios | Crashlytics, AdMob |
| Endereço IP e localização aproximada derivada dele | região/cidade estimada a partir do IP, para escolher o anúncio e a moeda/idioma do relatório | AdMob, Firebase |

**Localização:** o app **não pede e não usa** permissão de localização (`ACCESS_FINE_LOCATION`
ou `ACCESS_COARSE_LOCATION`) nem GPS. A "localização aproximada" acima é apenas a estimativa que
qualquer serviço de internet faz a partir do endereço IP da conexão.

**Nunca são enviados:** as palavras que você digita, a palavra-resposta do dia, letras
individuais, nem qualquer texto livre. Os eventos de uso registram só o formato do jogo (modo,
número de letras, acertou ou não, quantas tentativas) — nunca o conteúdo.

### 3.3 O que o app não faz

Não usamos contatos, agenda, câmera, microfone, arquivos, SMS, histórico de chamadas,
biometria, saúde, dados financeiros nem qualquer identificador permanente do aparelho (IMEI,
número de série). Não há compras dentro do app, nem assinaturas, nem contas de usuário.

## 4. Permissões que o app declara

O pacote instalado declara as permissões abaixo. Algumas são nossas; a maioria vem das
bibliotecas do Google e aparece no manifesto mesclado mesmo sem termos escrito uma linha sobre
elas. Todas são permissões "normais" — o Android não mostra caixa de diálogo para nenhuma delas,
exceto notificações.

| Permissão | Por quê | Origem |
|---|---|---|
| `INTERNET` | Carregar anúncios, buscar configuração remota, enviar métricas e relatórios de falha. O jogo em si funciona sem internet. | Nossa + SDKs |
| `ACCESS_NETWORK_STATE` | Saber se há conexão antes de tentar uma requisição de rede | Nossa + SDKs |
| `POST_NOTIFICATIONS` | Lembrete diário opcional. Pedimos isso **em contexto**, depois de uma vitória, nunca na primeira abertura; recusar não tira nenhuma função do jogo | Nossa |
| `com.google.android.gms.permission.AD_ID` | Acessar o ID de publicidade do Android, exigido pelo Google para apps que miram o Android 13 ou superior | Google Mobile Ads SDK; também declarada pelo Firebase Analytics |
| `android.permission.READ_BASIC_PHONE_STATE` | Sinais básicos de rede usados pelo SDK de anúncios (tipo de operadora/conexão). Não dá acesso ao número de telefone nem ao IMEI | Google Mobile Ads SDK |
| `android.permission.ACCESS_ADSERVICES_AD_ID`, `android.permission.ACCESS_ADSERVICES_ATTRIBUTION` | APIs do Android Privacy Sandbox usadas pela medição do Google para atribuição com preservação de privacidade | Firebase Analytics (play-services-measurement) |
| `com.google.android.finsky.permission.BIND_GET_INSTALL_REFERRER_SERVICE` | Ler, uma única vez, a origem da instalação na Google Play (campanha) | Firebase Analytics (play-services-measurement) |
| `android.permission.WAKE_LOCK` | Manter o processador acordado enquanto um envio de métricas curto termina | Firebase Analytics (play-services-measurement) |
| `android.permission.FOREGROUND_SERVICE` | Exigida pela biblioteca WorkManager do Android, que agenda o lembrete diário. **Não executamos nenhum serviço em primeiro plano.** | AndroidX WorkManager |
| `com.talero.napontadalngua.DYNAMIC_RECEIVER_NOT_EXPORTED_PERMISSION` | Permissão interna de proteção criada pela biblioteca AndroidX Core; não dá acesso a nada seu | AndroidX Core |

Não pedimos localização, contatos, câmera, microfone, armazenamento, telefone, SMS, alarmes
exatos nem `QUERY_ALL_PACKAGES`.

## 5. Serviços de terceiros e as políticas deles

Todos os serviços abaixo são do Google. Cada um tem a própria política, que se aplica ao que ele
coleta.

| Serviço | O que faz no app | O que trata | Política |
|---|---|---|---|
| **Google AdMob / Google Mobile Ads SDK** | Exibe os anúncios (banner, intersticial, vídeo recompensado) | ID de publicidade, App Set ID, endereço IP (localização aproximada), interações com o anúncio, diagnóstico do SDK | <https://policies.google.com/technologies/partner-sites> e <https://support.google.com/admob/answer/6128543> |
| **Google User Messaging Platform (UMP)** | Mostra e registra o formulário de consentimento de privacidade (GDPR/estados dos EUA) e guarda sua escolha | Escolhas de consentimento, país aproximado por IP | <https://developers.google.com/admob/android/privacy> |
| **Firebase Analytics** | Mede uso agregado (telas, rodadas, funil de anúncios) para melhorar o jogo | ID de instância do Analytics, ID de publicidade, eventos de uso, modelo/idioma/país do aparelho, endereço IP | <https://firebase.google.com/support/privacy> |
| **Firebase Crashlytics** | Relata falhas e travamentos para corrigirmos | Pilha de chamadas, estado do app, metadados do aparelho, UUID de instalação do Crashlytics | <https://firebase.google.com/support/privacy> |
| **Firebase Remote Config** | Ajusta parâmetros do jogo (frequência de anúncios, data-base da palavra do dia) sem atualizar o app | ID de instalação do Firebase, dados básicos do aparelho, endereço IP | <https://firebase.google.com/support/privacy> |
| **Firebase Installations** | Fornece o identificador de instalação que o Analytics, o Crashlytics e o Remote Config usam | ID de instalação, dados básicos do app e do aparelho | <https://firebase.google.com/support/privacy> |
| **Google Play In-App Review / In-App Update** | Mostra o convite de avaliação e o aviso de atualização, ambos renderizados pela própria Google Play | Tratados pela Google Play; o app não recebe dado nenhum de volta além de "concluído" | <https://policies.google.com/privacy> |

Política de privacidade geral do Google: <https://policies.google.com/privacy>.
Como o Google usa dados de apps e sites parceiros: <https://policies.google.com/technologies/partner-sites>.

Não usamos redes de mediação de anúncios, SDKs de análise de terceiros, redes sociais embutidas,
pixels de rastreamento nem ferramentas de atribuição além das listadas.

## 6. Anúncios, consentimento e o ID de publicidade

### 6.1 Como os anúncios funcionam aqui

O app é gratuito e se sustenta com anúncios. Seguimos as regras que prometemos no produto:
anúncios nunca cobrem o conteúdo, nunca aparecem durante uma partida em andamento, nunca ficam
colados no teclado do jogo, nunca surgem ao sair do app e os vídeos recompensados são sempre
iniciados por você, com o prêmio anunciado antes.

Configuramos o SDK de anúncios com classificação máxima de conteúdo **PG**, marcado como **não
direcionado a crianças** e **não destinado a usuários abaixo da idade de consentimento**.

### 6.2 Anúncios personalizados e sua escolha

- **Na União Europeia, no Reino Unido e na Suíça**, e em estados dos EUA com legislação própria de
  privacidade, o app mostra um formulário de consentimento do Google (UMP) **antes** de qualquer
  requisição de anúncio. Só pedimos anúncios se o consentimento permitir.
- Você pode rever ou mudar essa escolha a qualquer momento em **Configurações → Privacidade →
  Opções de privacidade** (a entrada aparece quando a sua região exige o formulário).
- Sua escolha de consentimento também é repassada ao Firebase Analytics através do **Consent Mode
  v2** (`analytics_storage`, `ad_storage`, `ad_user_data`, `ad_personalization`).
- **No Brasil**, o formulário do Google pode não ser exibido, porque a LGPD admite bases legais
  diferentes do consentimento para publicidade. Ainda assim, você controla a personalização de
  anúncios pelo próprio Android (item 6.3).

### 6.3 ID de publicidade: o que é e como resetar

O **ID de publicidade do Android (AAID)** é um identificador reconfigurável que o Google fornece
para publicidade. Ele não contém seu nome nem seu e-mail, mas é um identificador pessoal para
efeitos da LGPD e do GDPR.

Para redefinir ou apagar:

1. Abra **Configurações** do Android.
2. Vá em **Privacidade → Anúncios** (em alguns aparelhos: **Google → Anúncios**, ou
   **Segurança e privacidade → Mais privacidade → Anúncios**).
3. Toque em **Redefinir ID de publicidade** para receber um identificador novo, ou em
   **Excluir ID de publicidade** para que os apps deixem de receber qualquer identificador.

Excluir o ID de publicidade não tira nenhuma função do jogo: os anúncios passam a ser não
personalizados.

## 7. Por quanto tempo os dados ficam guardados

| Onde | Retenção |
|---|---|
| No seu aparelho (progresso, estatísticas, preferências) | Até você apagar pelo app ou desinstalar. Não há expiração automática. |
| Firebase Analytics — dados no nível do usuário e do evento | Pelo prazo de retenção definido no console do Firebase, cujo menor valor é **2 meses**. Relatórios agregados, que não identificam ninguém, são mantidos pelo Google por prazo indeterminado. |
| Firebase Crashlytics — relatórios de falha | Cerca de **90 dias**, conforme a documentação do Firebase. |
| Firebase Remote Config / Installations | Enquanto o app estiver instalado; o ID de instalação é recriado se o app for reinstalado. |
| Google AdMob | Conforme as políticas de retenção do Google para dados de publicidade. Não temos acesso aos registros brutos nem controle sobre esse prazo. |

## 8. Bases legais e seus direitos

### 8.1 LGPD — Lei nº 13.709/2018 (Brasil)

O Brasil é o nosso mercado principal e a LGPD é a lei que rege este tratamento.

**Bases legais que invocamos:**

| Tratamento | Base legal |
|---|---|
| Guardar progresso, estatísticas e preferências no aparelho | Execução do próprio serviço que você pediu ao instalar e abrir o jogo (art. 7º, V) |
| Relatórios de falha e diagnóstico | Legítimo interesse em manter o app funcionando e seguro (art. 7º, IX), com dados mínimos e sem identificação direta |
| Medição de uso agregado | Legítimo interesse em melhorar o produto (art. 7º, IX) |
| Publicidade personalizada | Consentimento onde o formulário do Google é exibido (art. 7º, I); fora dessas regiões, legítimo interesse (art. 7º, IX), sempre com a opção de desativar pelo ID de publicidade — ver 6.2 |
| Lembrete diário | Consentimento, dado na permissão de notificações (art. 7º, I) |

**Seus direitos (art. 18):** confirmação de que existe tratamento; acesso aos dados; correção de
dados incompletos, inexatos ou desatualizados; anonimização, bloqueio ou eliminação de dados
desnecessários ou tratados fora da lei; portabilidade; informação sobre com quem compartilhamos;
informação sobre a possibilidade de não consentir e o que acontece se você não consentir; e
revogação do consentimento.

Como a gente não tem conta nem cadastro, **não conseguimos ligar nenhum dado a você pelo nome ou
e-mail**. Para exercer os direitos sobre os dados guardados pelo Google, você precisa do seu ID de
publicidade (item 6.3) — ou pode simplesmente usar **Apagar meus dados** e resetar o ID, o que
resolve na prática. Escreva para **talero.dev@gmail.com** que a gente ajuda no passo a passo.

Reclamações podem ser dirigidas à **Autoridade Nacional de Proteção de Dados (ANPD)**:
<https://www.gov.br/anpd>.

### 8.2 GDPR / UK GDPR (Espaço Econômico Europeu, Reino Unido e Suíça)

Se você estiver nessas regiões, as bases legais são: **consentimento** (art. 6º(1)(a)) para
publicidade personalizada e para as finalidades cobertas pelo formulário UMP; e **interesse
legítimo** (art. 6º(1)(f)) para relatórios de falha, segurança e medição agregada.

Você tem direito de acesso, retificação, apagamento, limitação, portabilidade, oposição ao
tratamento baseado em interesse legítimo e de retirar o consentimento a qualquer momento (o que
não afeta o tratamento já realizado). Também pode reclamar à autoridade de proteção de dados do
seu país.

Como os servidores do Google ficam, entre outros lugares, nos Estados Unidos, há transferência
internacional de dados. O Google declara utilizar Cláusulas Contratuais Padrão e o Data Privacy
Framework para essas transferências — detalhes em <https://business.safety.google/privacy/>.

### 8.3 Estados Unidos (CCPA/CPRA e leis estaduais equivalentes)

Nós não vendemos dados pessoais por dinheiro. O compartilhamento de identificadores com o Google
para publicidade personalizada pode ser considerado "venda" ou "compartilhamento" por algumas
dessas leis; nas regiões abrangidas, o formulário do Google apresenta a opção de recusa, e a
exclusão do ID de publicidade pelo Android tem o mesmo efeito.

### 8.4 Outras regiões

Quando o app for distribuído em regiões cobertas por leis como a KVKK (Turquia) ou a UU PDP
(Indonésia), valem os mesmos mecanismos: os controles do formulário UMP, o ID de publicidade e a
função **Apagar meus dados**.

## 9. Crianças e adolescentes

**O app não é direcionado a crianças.** O público-alvo declarado na Google Play é de **13 anos ou
mais** (faixas 13–15, 16–17 e 18+). **Não participamos do programa Designed for Families / Famílias
da Google Play** e não usamos SDKs de anúncios autocertificados para públicos infantis.

Não coletamos intencionalmente dados de menores de 13 anos. O ícone, o gráfico de destaque, as
capturas de tela e o texto da loja foram feitos para não atrair crianças.

Se você é responsável e acredita que uma criança menor de 13 anos usou o app, escreva para
**talero.dev@gmail.com**: orientamos o apagamento local (item 10) e o reset do ID de
publicidade, que é tudo o que existe de identificável.

## 10. Como apagar seus dados

### 10.1 Pelo app (recomendado)

1. Abra o **Na Ponta da Língua**.
2. Toque no ícone de **engrenagem** (Configurações) na barra superior.
3. Desça até a seção **Privacidade**.
4. Toque em **Apagar meus dados**.
5. Confirme na caixa de diálogo **"Apagar seus dados?"** tocando em **Apagar**.

Isso apaga, na hora e de forma definitiva:

- o banco de dados local (progresso, rodadas concluídas, estatísticas, sequências, desbloqueios do
  Arquivo);
- todas as preferências (tema, modo daltônico, modo difícil, vibração, som, idioma, lembrete);
- os dados do Firebase Analytics guardados no aparelho, com `resetAnalyticsData()`, que também
  gera um ID de instância novo;
- o **ID de instalação do Firebase**, o que desassocia o aparelho dos dados anteriores no
  Analytics, no Crashlytics e no Remote Config;
- relatórios de falha ainda não enviados;
- o estado de consentimento de anúncios (o formulário volta a aparecer quando a sua região exigir).

Não dá para desfazer.

### 10.2 Desinstalando

Desinstalar o app remove todo o armazenamento local. Se o Auto Backup do Android estiver ligado,
uma cópia do progresso pode continuar na sua conta Google — apague-a em
**Configurações do Android → Google → Backup**.

### 10.3 Dados que já estão com o Google

Depois de apagar localmente e resetar o ID de publicidade (item 6.3), os dados antigos deixam de
ser associáveis ao seu aparelho e expiram nos prazos do item 7. Para pedidos diretamente ao
Google, use <https://myactivity.google.com> e <https://policies.google.com/privacy>.

### 10.4 Por e-mail

Escreva para **talero.dev@gmail.com** com o assunto **"Apagar meus dados"**. Como não há
cadastro, vamos pedir o seu ID de publicidade e a data aproximada de uso para localizar qualquer
registro. Respondemos em até 15 dias.

## 11. Segurança

- Todo o tráfego de rede usa **HTTPS/TLS**. O app desabilita tráfego em texto puro
  (`cleartextTrafficPermitted="false"`) e confia apenas nas autoridades certificadoras do sistema.
- Os dados locais ficam no armazenamento privado do app, isolado pelo sandbox do Android e
  protegido pela criptografia do aparelho.
- Não registramos dados pessoais em log; os logs de depuração são removidos na versão de produção.
- Nenhum componente do app é exportado, exceto a tela inicial, que precisa ser para o ícone
  funcionar.

Nenhum sistema é perfeitamente seguro, mas como não temos servidores nem guardamos dados pessoais,
a superfície de exposição é pequena por construção.

## 12. Conteúdo do jogo

As listas de palavras são derivadas de fontes abertas de português brasileiro e passam por uma
lista de bloqueio que remove termos ofensivos, sexuais, violentos e discriminatórios. As fontes,
versões, licenças e atribuições estão na tela **Sobre → Origem das palavras**, dentro do app.

## 13. Mudanças nesta política

Quando esta política mudar de forma relevante, atualizamos a data no topo, publicamos a versão
nova nesta mesma URL e avisamos dentro do app na próxima abertura. Continuar usando o app depois
da mudança significa que você tomou conhecimento da versão nova.

## 14. Fale com a gente

**Controlador dos dados:** Talero
**Contato de privacidade:** talero.dev@gmail.com
