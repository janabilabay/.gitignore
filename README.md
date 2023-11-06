# .gitignore гайд

Файл `.gitignore` создан для указания файлов и папок, которые не должны быть отслеживаемыми системой контроля версий Git. Это позволяет исключить определенные файлы из отслеживания Git, что полезно, когда некоторые файлы генерируются автоматически или являются результатом компиляции и не являются частью исходного кода проекта.

Основная цель `.gitignore` заключается в следующем:

**Предотвращение случайного отслеживания файлов:** Иногда временные файлы, файлы сборки, личные файлы конфигурации IDE, артефакты сборки и прочие нежелательные файлы могут попадать в систему контроля версий. `.gitignore` позволяет исключить их, что помогает поддерживать репозиторий чистым.

**Улучшение работы в команде:** Если разработчики используют различные среды разработки или операционные системы, то создание общего `.gitignore` файла позволяет исключить файлы, специфичные для каждой среды.

**Уменьшение размера репозитория:** Исключение ненужных файлов помогает уменьшить размер репозитория, что делает его более компактным и улучшает производительность при клонировании или скачивании репозитория.

**Предотвращение конфликтов:** Использование `.gitignore` помогает избежать конфликтов при слиянии изменений между разными ветками разработки.

`.gitignore` является инструментом для управления репозиторием, позволяя исключить ненужные файлы, сохраняя при этом только те, которые необходимы для разработки, обеспечивая чистоту работы с версиями проекта.

**Как создать файл `.gitignore`?**

1. Создайте текстовый файл в проекте.
2. Назовите его `.gitignore`.
3. Добавьте шаблоны и правила исключения файлов и каталогов, такие как временные файлы, настройки пользователя и зависимости, чтобы они не попадали под управление Git.

Ниже `.gitignore` файл предназначен для игнорирования временных и сгенерированных файлов, которые создаются средой разработки Xcode, инструментами управления зависимостями (CocoaPods, Carthage, Swift Package Manager), а также для различных автоматизированных инструментов разработки (например, Fastlane). Также исключает файлы, связанные с конфигурацией проекта и другие файлы, которые обычно не должны храниться в репозитории.

```markdown
# Xcode
.DS_Store                # Finder metadata for version control
*/build/                 # Build folders

# User-specific
*.pbxuser                # Xcode user-specific info
!default.pbxuser         # Exclude default Xcode user info
*.mode1v3                # Xcode state file extension
!default.mode1v3         # Exclude default Xcode state file extension
*.mode2v3                # Another Xcode state file extension
!default.mode2v3         # Exclude default another Xcode state file extension
*.perspectivev3          # Xcode perspective file extension
!default.perspectivev3   # Exclude default Xcode perspective file extension
xcuserdata/              # Xcode user data

# Build products
build/                   # Generated build files

# Pods (CocoaPods dependencies)
Pods/                    # CocoaPods folder
*.xcworkspace            # Xcode workspace file

# Carthage (Carthage dependencies)
/Carthage/               # Carthage folder
/Carthage/Build/         # Carthage built products

# SPM (Swift Package Manager)
.checkouts/              # SPM folder
.build/                  # SPM generated files

# Fastlane (automation tool)
fastlane/report.xml      # Fastlane reports
fastlane/Preview.html    # Fastlane HTML preview
fastlane/screenshots     # Fastlane screenshots
fastlane/test_output     # Fastlane test results

# Other
.DerivedData/            # Generated data
.idea/                   # IntelliJ IDEA project folder
*.hmap                   # Hmap files
*.ipa                    # iOS application files (IPA)
*.xcuserstate            # Xcode user state
```
