# Баг-репорты экрана регистрации 

|**ID**|BR-REG001|

|**Исполнитель**| Высоцкий Алексей Владимирович | 22.10.2026 |
|**Заголовок**| [Регистрация] Зависание приложения при валидном email |
|**Окружение**| Android Studio Narwhal 4 Feature Drop | 2025.1.4, Android 16, Pixel 1 | FitEra 0.1.24 |
|**Предусловия**| 1. Приложение запущено <br> 2. Открыт экран регистрации (шаг 1 из 3) <br> 3. Поле email пустое |
|**Шаги воспроизведения**| 1. Ввести email: test@mail.com <br> 2. Нажать кнопку «Продолжить» <br> 3. Наблюдать за реакцией приложения 30 секунд|
|**Ожидаемый результат**| Переход на шаг 2 «Ввод пароля»
| **Фактический результат** | * Появляется индикатор загрузки <br> * Приложение не реагирует на действия <br> * Сообщение об ошибке: «[Что-то пошло не так, повторите попытку или попробуйте позже.]» <br> * Воспроизводимость: 3 из 3 |
|**Severity / Priority**| - Severity: Minor <br> - Priority: Low|<br>
| **Приложения** | Скриншоты и видео воспроизведения <br> [BR-REG001 ошибка](images/br-reg001_error_message.png) <br> [BR-REG001 загрузка](images/br-reg001_loading.png)|<br>
| **Стасус** | Closed |


|**ID**|BR-REG002|
|**Исполнитель**| Высоцкий Алексей Владимирович | 24.10.2026 |
|**Заголовок**| [Регистрация] При вводе email со спецсимволом в доменной части кнопка «Продолжить» становится активной |
|**Окружение**| Android Studio Narwhal 4 Feature Drop | 2025.1.4, Android 16, Pixel 1 | FitEra 0.1.26 |
|**Предусловия**| 1. Пользователь запустил приложение<br>2. Кликнул кнопку «Создать аккаунт»<br>3. Открыт экран регистрации (шаг 1 из 3)<br>4. Поле ввода email — пустое |
|**Шаги воспроизведения**| 1. Ввести email со спецсимволами в доменной части: `testt@mail.ru!`, `testa@email.c№om`, `testi@link.e;u`.<br>2. Проверить состояние кнопки «Продолжить» |
|**Ожидаемый результат**| Кнопка «Продолжить» неактивна
|**Фактический результат**|Кнопка «Продолжить» активна|
|**Severity / Priority**| - Severity: Majior <br> - Priority: Low|<br>
|**Приложения**| Скриншоты и видео воспроизведения <br> [BR-REG002 Ввод email со спецсимволом в домене и состояние кнопки](images/br-reg002_spsimbol_in_dom.png)|<br>
| **Стасус** | Opened |


|**ID**|BR-REG003|
|**Исполнитель**| Высоцкий Алексей Владимирович | 24.10.2026 |
|**Заголовок**| [Регистрация] При длине email 255 символов в поле ввода email кнопка «Продолжить» активна |
|**Окружение**| Android Studio Narwhal 4 Feature Drop | 2025.1.4, Android 16, Pixel 1 | FitEra 0.1.26 |
|**Предусловия**| 1. Пользователь запустил приложение<br>2. Кликнул кнопку «Создать аккаунт»<br>3. Открыт экран регистрации (шаг 1 из 3)<br>4. Поле ввода email — пустое |
|**Шаги воспроизведения**| 1. Ввести email длиной 255 символов: `erblsrenebjlzblgvhvdlyrntxehfzzfnafxkznzuxcdjtxeqqmjiscnthkvqwvjgjhhcnnpljxkmqrqcaewybkyrhrqceyvxgkrxbjbmgtnsjqpwqfnbycmnbqofpaouovvouhnsbqcvhqkwhslutjddmdwuctbneqjyvuovzthzyhxlnwcbeqknkozgbyvpbxhcdvvmcktwucmcldjbgcrjkwlytznbehqmcbfecclvbruhbqhc@mail.ru` <br>2. Проверить состояние кнопки «Продолжить» |
|**Ожидаемый результат**| Кнопка «Продолжить» неактивна
| **Фактический результат** |Кнопка «Продолжить» активна|
|**Severity / Priority**| - Severity: Majior <br> - Priority: Low|<br>
| **Приложения** | Скриншоты и видео воспроизведения <br> [BR-REG003 Ввод email с длиной 255 символов](images/br-reg003_225_symbols.png) |<br>
| **Стасус** | Opened |


|**ID**|BR-REG004|
|**Исполнитель**| Высоцкий Алексей Владимирович | 24.10.2026 |
|**Заголовок**| [Регистрация] При вводе невалидного email: 255 символов, спецсимвол в доменной части в поле ввода email Кнопка активна, выполняется переход на шаг 2 «Проверка кода»|
|**Окружение**| Android Studio Narwhal 4 Feature Drop | 2025.1.4, Android 16, Pixel 1 | FitEra 0.1.26 |
|**Предусловия**| 1. Пользователь запустил приложение<br>2. Кликнул кнопку «Создать аккаунт»<br>3. Открыт экран регистрации (шаг 1 из 3)<br>4. Поле ввода email — пустое |
|**Шаги воспроизведения**| 1. Ввести невалидный email: `erblsrenebjlzblgvhvdlyrntxehfzzfnafxkznzuxcdjtxeqqmjiscnthkvqwvjgjhhcnnpljxkmqrqcaewybkyrhrqceyvxgkrxbjbmgtnsjqpwqfnbycmnbqofpaouovvouhnsbqcvhqkwhslutjddmdwuctbneqjyvuovzthzyhxlnwcbeqknkozgbyvpbxhcdvvmcktwucmcldjbgcrjkwlytznbehqmcbfecclvbruhbqhc@mail.ru`<br>  `testt@mail.ru!`, `testa@email.c№om`, `testi@link.e;u` <br>2. Нажать кнопку  «Продолжить» |
|**Ожидаемый результат**| Переход не выполняется пользователь остается на шаге 1 «Регистрация»
| **Фактический результат** |Выполняется переход на шаг 2 «Проверка кода»|
|**Severity / Priority**| - Severity: Majior <br> - Priority: High|<br>
| **Приложения** | Скриншоты и видео воспроизведения <br> [BR-REG004 Ввод email 255 символов](images/br-reg004_step_2_possobility.png) <br> [BR-REG004 Ввод email со спецсимволом в домене](images/br-reg004_step_2_possobility_symbols.png)|<br>
| **Стасус** | Opened |
