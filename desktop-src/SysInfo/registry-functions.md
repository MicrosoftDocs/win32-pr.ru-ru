---
description: Ниже перечислены функции реестра.
ms.assetid: a490b748-42e8-462b-9a7f-a8b21438ea79
title: Функции реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc2cfadd3753b7a269667fee22955f8465495458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264813"
---
# <a name="registry-functions"></a>Функции реестра

Ниже перечислены функции реестра.



| Функция                                                           | Описание                                                                                                                                    |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**жетсистемрегистрикуота**](/windows/desktop/api/Winbase/nf-winbase-getsystemregistryquota)           | Извлекает текущий размер реестра и максимальный размер, который может достичь реестр в системе.                          |
| [**Ошибка RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey)                                 | Закрывает маркер указанного раздела реестра.                                                                                                 |
| [**регконнектрегистри**](/windows/desktop/api/Winreg/nf-winreg-regconnectregistrya)                   | Устанавливает соединение с предопределенным маркером реестра на другом компьютере.                                                                  |
| [**регкопитри**](/windows/desktop/api/Winreg/nf-winreg-regcopytreea)                                 | Копирует указанный раздел реестра вместе со значениями и подразделами в указанный целевой ключ.                                        |
| [**регкреатекэйекс**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa)                           | Создает указанный раздел реестра.                                                                                                            |
| [**регкреатекэйтрансактед**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeytransacteda)           | Создает указанный раздел реестра и связывает его с транзакцией.                                                                       |
| [**регделетекэй**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeya)                               | Удаляет подраздел и его значения.                                                                                                               |
| [**регделетекэйекс**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyexa)                           | Удаляет подраздел и его значения из указанного представления реестра для конкретной платформы.                                                     |
| [**регделетекэйтрансактед**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeytransacteda)           | Удаляет подраздел и его значения из указанного представления реестра для конкретной платформы в качестве транзакционной операции.                           |
| [**регделетекэйвалуе**](/windows/desktop/api/Winreg/nf-winreg-regdeletekeyvaluea)                     | Удаляет указанное значение из указанного раздела реестра и подраздела.                                                                        |
| [**регделететри**](/windows/desktop/api/Winreg/nf-winreg-regdeletetreea)                             | Рекурсивно удаляет подразделы и значения указанного ключа.                                                                               |
| [**регделетевалуе**](/windows/desktop/api/Winreg/nf-winreg-regdeletevaluea)                           | Удаляет именованное значение из указанного раздела реестра.                                                                                         |
| [**регдисаблепредефинедкаче**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcache)     | Отключает кэширование обработки для предопределенного маркера реестра для текущего **\_ \_ пользователя hKey** для текущего процесса.                                |
| [**регдисаблепредефинедкачикс**](/windows/desktop/api/Winreg/nf-winreg-regdisablepredefinedcacheex) | Отключает кэширование обработки для всех предопределенных дескрипторов реестра для текущего процесса.                                                           |
| [**регдисаблерефлектионкэй**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey)         | Отключает отражение реестра для указанного ключа.                                                                                            |
| [**реженаблерефлектионкэй**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey)           | Включает отражение реестра для указанного отключенного ключа.                                                                                    |
| [**реженумкэйекс**](/windows/desktop/api/Winreg/nf-winreg-regenumkeyexa)                               | Перечисляет подразделы указанного открытого раздела реестра.                                                                                     |
| [**реженумвалуе**](/windows/desktop/api/Winreg/nf-winreg-regenumvaluea)                               | Перечисляет значения для указанного открытого ключа реестра.                                                                                     |
| [**Функция RegFlushKey вернула**](/windows/desktop/api/Winreg/nf-winreg-regflushkey)                                 | Записывает все атрибуты указанного открытого раздела реестра в реестр.                                                                    |
| [**регжеткэйсекурити**](/windows/desktop/api/winreg/nf-winreg-reggetkeysecurity)                | Извлекает копию дескриптора безопасности, защищающего указанный открытый раздел реестра.                                                        |
| [**регжетвалуе**](/windows/desktop/api/Winreg/nf-winreg-reggetvaluea)                                 | Извлекает тип и данные для указанного значения реестра.                                                                                  |
| [**реглоадкэй**](/windows/desktop/api/Winreg/nf-winreg-regloadkeya)                                   | Создание подраздела в разделе **hKey \_ Users** или **hKey на \_ локальном \_ компьютере** и сохранение сведений о регистрации из указанного файла в этом подразделе. |
| [**реглоадмуистринг**](/windows/desktop/api/Winreg/nf-winreg-regloadmuistringa)                       | Загружает указанную строку из указанного ключа и подраздела.                                                                                  |
| [**регнотифичанжекэйвалуе**](/windows/desktop/api/Winreg/nf-winreg-regnotifychangekeyvalue)         | Уведомляет вызывающей стороне об изменениях атрибутов или содержимого указанного раздела реестра.                                                   |
| [**регопенкуррентусер**](/windows/desktop/api/Winreg/nf-winreg-regopencurrentuser)                   | Извлекает маркер **\_ текущего ключа \_ пользователя hKey** для пользователя, который олицетворяет текущий поток.                                        |
| [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa)                               | Открывает указанный раздел реестра.                                                                                                              |
| [**регопенкэйтрансактед**](/windows/desktop/api/Winreg/nf-winreg-regopenkeytransacteda)               | Открывает указанный раздел реестра и связывает его с транзакцией.                                                                         |
| [**регопенусерклассесрут**](/windows/desktop/api/Winreg/nf-winreg-regopenuserclassesroot)           | Извлекает маркер **\_ \_ корневого ключа классов hKey** для указанного пользователя.                                                                  |
| [**реговерридепредефкэй**](/windows/desktop/api/Winreg/nf-winreg-regoverridepredefkey)               | Сопоставляет предопределенный раздел реестра с указанным ключом реестра.                                                                                    |
| [**регкуеринфокэй**](/windows/desktop/api/Winreg/nf-winreg-regqueryinfokeya)                         | Извлекает сведения об указанном разделе реестра.                                                                                        |
| [**регкуеримултиплевалуес**](/windows/desktop/api/Winreg/nf-winreg-regquerymultiplevaluesa)           | Извлекает тип и данные для списка имен значений, связанных с открытым ключом реестра.                                                    |
| [**регкуерирефлектионкэй**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)             | Определяет, было ли отражение отключено или включено для указанного ключа.                                                              |
| [**Процедура RegQueryValueEx**](/windows/desktop/api/Winreg/nf-winreg-regqueryvalueexa)                         | Извлекает тип и данные для указанного имени, связанного с открытым ключом реестра.                                                   |
| [**регреплацекэй**](/windows/desktop/api/Winreg/nf-winreg-regreplacekeya)                             | Заменяет файл, соответствующий ключу реестра и всем его подразделам, другим файлом.                                                                |
| [**регресторекэй**](/windows/desktop/api/Winreg/nf-winreg-regrestorekeya)                             | Считывает данные реестра в указанном файле и копирует их по указанному ключу.                                                       |
| [**регсавекэй**](/windows/desktop/api/Winreg/nf-winreg-regsavekeya)                                   | Сохраняет указанный ключ и все его подразделы и значения в новом файле.                                                                       |
| [**регсавекэйекс**](/windows/desktop/api/Winreg/nf-winreg-regsavekeyexa)                               | Сохраняет указанный ключ и все его подразделы и значения в новом файле. Можно указать формат для сохраненного ключа или Hive.                 |
| [**регсеткэйвалуе**](/windows/desktop/api/Winreg/nf-winreg-regsetkeyvaluea)                           | Задает данные для указанного значения в указанном разделе реестра и подразделе.                                                                |
| [**регсеткэйсекурити**](/windows/desktop/api/winreg/nf-winreg-regsetkeysecurity)                | Задает безопасность открытого раздела реестра.                                                                                                     |
| [**RegSetValueEx**](/windows/desktop/api/Winreg/nf-winreg-regsetvalueexa)                             | Задает данные и тип указанного значения в разделе реестра.                                                                              |
| [**регунлоадкэй**](/windows/desktop/api/Winreg/nf-winreg-regunloadkeya)                               | Выгружает указанный раздел реестра и его подразделы из реестра.                                                                          |



 

С реестром можно использовать следующие функции оболочки:

-   [**ассоккреате**](/windows/desktop/api/shlwapi/nf-shlwapi-assoccreate)
-   [**ассоккуерикэй**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerykeya)
-   [**ассоккуеристринг**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringa)
-   [**ассоккуеристрингбикэй**](/windows/desktop/api/shlwapi/nf-shlwapi-assocquerystringbykeya)
-   [**шкопикэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shcopykeya)
-   [**шделетимптикэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeleteemptykeya)
-   [**шделетекэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletekeya)
-   [**шделетевалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shdeletevaluea)
-   [**шенумкэйекс**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumkeyexa)
-   [**шенумвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shenumvaluea)
-   [**шжетвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shgetvaluea)
-   [**шкуеринфокэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryinfokeya)
-   [**шкуеривалуикс**](/windows/desktop/api/shlwapi/nf-shlwapi-shqueryvalueexa)
-   [**шрегклосеускэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcloseuskey)
-   [**шрегкреатеускэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shregcreateuskeya)
-   [**шрегделетимптюскэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteemptyuskeya)
-   [**шрегделетеусвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shregdeleteusvaluea)
-   [**шрегдупликатехкэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shregduplicatehkey)
-   [**шреженумускэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumuskeya)
-   [**шреженумусвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shregenumusvaluea)
-   [**шрегжетбулусвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetboolusvaluea)
-   [**шрегжетинтв**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetintw)
-   [**шрегжетпас**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetpatha)
-   [**шрегжетусвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shreggetusvaluea)
-   [**шрегопенускэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shregopenuskeya)
-   [**шрегкуеринфаускэй**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryinfouskeya)
-   [**шрегкуерюсвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shregqueryusvaluea)
-   [**шрегсетпас**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetpatha)
-   [**шрегсетусвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shregsetusvaluea)
-   [**шрегвритеусвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shregwriteusvaluea)
-   [**шсетвалуе**](/windows/desktop/api/shlwapi/nf-shlwapi-shsetvaluea)

Ниже приведены функции инициализации файлов. Они получают информацию из и копируют данные в системный или определяемый приложением файл инициализации. Эти функции предоставляются только для обеспечения совместимости с 16-разрядными версиями Windows. Новые приложения должны использовать реестр.



| Функция                                                               | Описание                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**жетприватепрофилеинт**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofileint)                   | Извлекает целое число, связанное с ключом в указанном разделе файла инициализации.     |
| [**жетприватепрофилесектион**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesection)           | Извлекает все ключи и значения для указанного раздела файла инициализации.             |
| [**жетприватепрофилесектионнамес**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilesectionnames) | Извлекает имена всех разделов в файле инициализации.                                     |
| [**жетприватепрофилестринг**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestring)             | Извлекает строку из указанного раздела в файле инициализации.                           |
| [**жетприватепрофилеструкт**](/windows/desktop/api/Winbase/nf-winbase-getprivateprofilestruct)             | Извлекает данные, связанные с ключом в указанном разделе файла инициализации.       |
| [**жетпрофилеинт**](/windows/desktop/api/Winbase/nf-winbase-getprofileinta)                                 | Извлекает целое число из ключа в указанном разделе файла Win.ini.                      |
| [**жетпрофилесектион**](/windows/desktop/api/Winbase/nf-winbase-getprofilesectiona)                         | Извлекает все ключи и значения для указанного раздела файла Win.ini.                   |
| [**жетпрофилестринг**](/windows/desktop/api/Winbase/nf-winbase-getprofilestringa)                           | Извлекает строку, связанную с ключом в указанном разделе файла Win.ini.           |
| [**вритеприватепрофилесектион**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilesectiona)       | Заменяет ключи и значения для указанного раздела в файле инициализации.                  |
| [**вритеприватепрофилестринг**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestringa)         | Копирует строку в указанный раздел файла инициализации.                              |
| [**вритеприватепрофилеструкт**](/windows/desktop/api/Winbase/nf-winbase-writeprivateprofilestructa)         | Копирует данные в ключ в указанном разделе файла инициализации.                         |
| [**вритепрофилесектион**](/windows/desktop/api/Winbase/nf-winbase-writeprofilesectiona)                     | Заменяет содержимое указанного раздела в файле Win.ini указанными ключами и значениями. |
| [**вритепрофилестринг**](/windows/desktop/api/Winbase/nf-winbase-writeprofilestringa)                       | Копирует строку в указанный раздел файла Win.ini.                                    |



 

## <a name="obsolete-functions"></a>Устаревшие функции

Эти функции предоставляются только для обеспечения совместимости с 16-разрядными версиями Windows:

-   [**регкреатекэй**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeya)
-   [**реженумкэй**](/windows/desktop/api/Winreg/nf-winreg-regenumkeya)
-   [**регопенкэй**](/windows/desktop/api/Winreg/nf-winreg-regopenkeya)
-   [**регкуеривалуе**](/windows/desktop/api/Winreg/nf-winreg-regqueryvaluea)
-   [**регсетвалуе**](/windows/desktop/api/Winreg/nf-winreg-regsetvaluea)

 

 
