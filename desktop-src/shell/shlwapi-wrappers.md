---
description: В таблицах этого документа перечислены функции-оболочки из Shlwapi.dll, которые предоставляют ограниченную функциональность Юникода для Windows 95, Windows 98 и Windows Millennium Edition (Windows Me).
title: Функции программы-оболочки SHLWAPI
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3c428c89-b650-48c1-9f91-b94f9f8e10e2
api_name:
- SHLWAPI Wrapper Functions
- AppendMenuWrapW
- CallWindowProcWrapW
- CharLowerWrapW
- CharUpperBufWrapW
- CharUpperWrapW
- CompareStringWrapW
- CopyFileWrapW
- CreateEventWrapW
- CreateFileWrapW
- CreateWindowExWrapW
- DefWindowProcWrapW
- DeleteFileWrapW
- DialogBoxParamWrapW
- DispatchMessageWrapW
- DragQueryFileWrapW
- DrawTextExWrapW
- DrawTextWrapW
- ExtTextOutWrapW
- FormatMessageWrapW
- GetClassInfoWrapW
- GetDateFormatW
- GetDateFormatWrapW
- GetDlgItemTextWrapW
- GetFileAttributesWrapW
- GetLocaleInfoWrapW
- GetMenuItemInfoWrapW
- GetModuleFileNameWrapW
- GetModuleHandleWrapW
- GetObjectWrapW
- GetOpenFileNameWrapW
- GetSaveFileNameWrapW
- GetSystemDirectoryWrapW
- GetTimeFormatWrapW
- GetWindowLongWrapW
- GetWindowsDirectoryWrapW
- GetWindowTextLengthWrapW
- GetWindowTextWrapW
- InsertMenuItemWrapW
- IsCharAlphaNumericWrapW
- IsCharAlphaWrapW
- IsCharUpperWrapW
- LoadLibraryWrapW
- LoadStringWrapW
- MessageBoxWrapW
- MLGetUILanguage
- MoveFileWrapW
- OutputDebugStringWrapW
- PeekMessageWrapW
- PostMessageWrapW
- RegCreateKeyExWrapW
- RegisterClassWrapW
- RegOpenKeyExWrapW
- RegQueryValueExW
- RegQueryValueExWrapW
- RegQueryValueWrapW
- RegSetValueExWrapW
- SendMessageWrapW
- SetDlgItemTextWrapW
- SetWindowLongWrapW
- SetWindowTextWrapW
- SHCancelTimerQueueTimer
- SHDeleteTimerQueue
- ShellExecuteExWrapW
- ShellMessageBoxWrapW
- SHGetFileInfoWrapW
- SHGetPathFromIDListWrapW
- SHInterlockedCompareExchange
- SHQueueUserWorkItem
- SHSetTimerQueueTimer
- TranslateAcceleratorWrapW
- UnregisterClassWrapW
api_type:
- NA
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d928228873b893228c7fddc22fc1ca29ca511cd
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549756"
---
# <a name="shlwapi-wrapper-functions"></a>Функции программы-оболочки SHLWAPI

\[Эти функции доступны в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003. Они могут быть изменены или недоступны в последующих версиях Windows.\]

В таблицах этого документа перечислены функции-оболочки из Shlwapi.dll, которые предоставляют ограниченную функциональность Юникода для Windows 95, Windows 98 и Windows Millennium Edition (Windows Me).

Windows 95, Windows 98 и Windows Millennium Edition (Windows Me) называются "собственными платформами ANSI". На собственных платформах ANSI эти функции-оболочки преобразуют входные строковые параметры Юникода в ANSI и вызывают версии ANSI функций в столбце **пересылки на** . Например, **аппендменуврапв** вызывает **аппендменуа**, который является версией ANSI [**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua). Другие функции следуют той же схеме. Все строки, возвращаемые функцией ANSI, преобразуются в Юникод и возвращаются вызывающему приложению. Помимо исключений, указанных в столбце « **Примечания** », функция-оболочка имеет тот же синтаксис и предоставляет те же функциональные возможности, что и функция в столбце « **Пересылка** ». Подробные сведения об использовании см. на этой справочной странице.

**Предупреждение системы безопасности:** Несколько строк Юникода могут быть преобразованы в одну и ту же строку ANSI. Непредвиденные конфликты после преобразования могут привести к непредвиденному поведению. Например, если **креативентврапв** используется для создания двух событий с разными именами, имена которых совпадают после преобразования из Юникода в ANSI, второй вызов возвратит обработчик к тому же событию, что и первый вызов, несмотря на то, что исходные строки в Юникоде были разными.

Операционные системы Microsoft Windows NT, Windows 2000, Windows XP, Windows Server 2003 и более поздних версий называются "собственными платформами Юникода". В большинстве случаев на собственных платформах Юникода эти функции-оболочки просто пересылают входные строковые параметры в версию Юникода функции в столбце **Пересылка в** . Например, **аппендменуврапв** пересылается в **аппендменув**, который является версией Юникода [**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua). Другие функции следуют той же схеме. Все строки, возвращаемые функцией Юникода, возвращаются вызывающему приложению. Помимо исключений, указанных в столбце « **Примечания** », функция-оболочка имеет тот же синтаксис и предоставляет те же функциональные возможности, что и функция в столбце « **Пересылка** ». Подробные сведения об использовании см. на этой справочной странице.

**Предупреждение системы безопасности:** Проблемы безопасности, указанные для функций в столбце **пересылки в** , также применяются к соответствующим функциям-оболочкам. Дополнительные сведения см. в справочной документации по функции в столбце **пересылки в** .

В этой таблице содержатся все функции-оболочки, содержащиеся в Shlwapi.dll. Чтобы вызвать их, необходимо использовать порядковый номер, указанный в таблице.

> [!Note]  
> Эти функции-оболочки доступны в Windows XP, но не предоставляют функций-оболочек в Windows XP с пакетом обновления 2 (SP2) и более поздних версий. Они также не предоставляют функции-оболочки в Windows Server 2003. Вместо этого следует использовать функции, перечисленные в столбце **Пересылка в** .

 



| Функция                  | Порядковый номер | Пересылает                                             | DLL      | Remarks                                                                                                                             |
|---------------------------|---------|---------------------------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| аппендменуврапв           | 36      | [**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua)                     | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(меню)](#menu)                                                           |
| каллвиндовпрокврапв       | 37      | [**каллвиндовпрок**](/windows/win32/api/winuser/nf-winuser-callwindowproca)             | USER32   | [сохранении](#shlwapi-wrapper-functions)                                                                                                   |
| чарловерврапв            | 38      | [**чарловер**](/windows/win32/api/winuser/nf-winuser-charlowera)                       | KERNEL32 | [&](#shlwapi-wrapper-functions)                                                                                                   |
| чаруппербуфврапв         | 44      | [**чаруппербуфф**](/windows/win32/api/winuser/nf-winuser-charupperbuffa)               | KERNEL32 | [&](#shlwapi-wrapper-functions)                                                                                                   |
| чарупперврапв            | 43      | [**чаруппер**](/windows/win32/api/winuser/nf-winuser-charuppera)                       | KERNEL32 | [&](#shlwapi-wrapper-functions)                                                                                                   |
| компарестрингврапв        | 45      | [**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)                 | KERNEL32 | [CompareString](#comparestring)                                                                                                   |
| копифилеврапв             | 112     | [**CopyFile**](/windows/win32/api/winbase/nf-winbase-copyfile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| креативентврапв          | 51      | [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)                     | KERNEL32 | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |
| креатефилеврапв           | 52      | [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| креатевиндовексврапв       | 55      | [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)             | USER32   | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |
| дефвиндовпрокврапв        | 56      | [**дефвиндовпрок**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)               | USER32   | [сохранении](#shlwapi-wrapper-functions)                                                                                                   |
| делетефилеврапв           | 57      | [**DeleteFile**](/windows/win32/api/fileapi/nf-fileapi-deletefilea)                         | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| диалогбокспарамврапв       | 59      | [**диалогбокспарам**](/windows/win32/api/winuser/nf-winuser-dialogboxparama)             | USER32   | [(f)](#dragqueryfile), [(i)](#shlwapi-wrapper-functions), [(диалогбокспарам)](#dialogboxparam)                                       |
| диспатчмессажеврапв      | 60      | [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)           | USER32   | [сохранении](#shlwapi-wrapper-functions)                                                                                                   |
| драгкуерифилеврапв        | 318     | [**драгкуерифиле**](/windows/win32/api/Shellapi/nf-shellapi-dragqueryfilea)                  | БИБЛИОТЕКИ  | [(b)](#dialogboxparam), [(c)](#shlwapi-wrapper-functions), ( [g)](#compareexchange), [(драгкуерифиле)](#dragqueryfile)               |
| дравтекстексврапв           | 301     | [**дравтекстекс**](/windows/win32/api/winuser/nf-winuser-drawtextexa)                        | USER32   | [(a)](#shlwapi-wrapper-functions), [(d)](#shlwapi-wrapper-functions)                                                                |
| дравтекстврапв             | 61      | [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext)                            | USER32   | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |
| ексттекстаутврапв           | 299     | [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta)                        | GDI32    | [(d)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(ExtTextOut)](#exttextout)                                               |
| форматмессажеврапв        | 68      | [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(FormatMessage)](#formatmessage)                                       |
| жетклассинфоврапв         | 69      | [**жетклассинфо**](/windows/win32/api/winuser/nf-winuser-getclassinfoa)                 | USER32   | [(Жетклассинфо)](#getclassinfo)                                                                                                     |
| жетдатеформатврапв        | 311     | [**жетдатеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-getdateformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| жетдлгитемтекстврапв       | 74      | [**жетдлгитемтекст**](/windows/win32/api/winuser/nf-winuser-getdlgitemtexta)             | USER32   | [модуле](#compareexchange)                                                                                                             |
| жетфилеаттрибутесврапв    | 75      | [**GetFileAttributes**](/windows/win32/api/fileapi/nf-fileapi-getfileattributesa)           | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| жетлокалеинфоврапв        | 77      | [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa)                 | KERNEL32 | [модуле](#compareexchange)                                                                                                             |
| жетменуитеминфоврапв      | 302     | [**жетменуитеминфо**](/windows/win32/api/winuser/nf-winuser-getmenuiteminfoa)           | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange), [(объектами menuiteminfo)](#menuiteminfo)                                                     |
| жетмодулефиленамеврапв    | 80      | [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)         | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| жетмодулехандлеврапв      | 83      | [**Ошибка GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea)             | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| жетобжектврапв            | 84      | [**GetObject**](/windows/win32/api/wingdi/nf-wingdi-getobject)                          | GDI32    | [модуле](#compareexchange)                                                                                                             |
| жетопенфиленамеврапв      | 403     | [**GetOpenFileName**](/windows/win32/api/commdlg/nf-commdlg-getopenfilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| жетсавефиленамеврапв      | 389     | [**жетсавефиленаме**](/windows/win32/api/commdlg/nf-commdlg-getsavefilenamea)           | COMDLG32 | [(a)](#shlwapi-wrapper-functions), [(b)](#dialogboxparam), [(g)](#compareexchange), [(OpenFileName)](#openfilename)                 |
| жетсистемдиректориврапв   | 81      | [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)       | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| жеттимеформатврапв        | 310     | [**жеттимеформат**](/windows/win32/api/datetimeapi/nf-datetimeapi-gettimeformata)                 | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(DateTime)](#datetime)                                                 |
| жетвиндовлонгврапв        | 94      | [**жетвиндовлонг**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)               | USER32   | [(Виндовлонг)](#windowlong)                                                                                                         |
| жетвиндовсдиректориврапв  | 97      | [**жетвиндовсдиректори**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya)     | KERNEL32 | [(c)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| жетвиндовтекстленгсврапв  | 96      | [**жетвиндовтекстленгс**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)   | USER32   | [б](#j)                                                                                                                           |
| жетвиндовтекстврапв        | 95      | [**жетвиндовтекст**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)               | USER32   | [(f)](#dragqueryfile), [(g)](#compareexchange)                                                                                      |
| инсертменуитемврапв       | 98      | [**инсертменуитем**](/windows/win32/api/winuser/nf-winuser-insertmenuitema)             | USER32   | [(a)](#shlwapi-wrapper-functions), [(f)](#dragqueryfile), [(меню)](#menu), [(объектами menuiteminfo)](#menuiteminfo)                          |
| исчаралфаврапв          | 25      | [**исчаралфа**](/windows/win32/api/winuser/nf-winuser-ischaralphaa)                   | USER32   | [&](#shlwapi-wrapper-functions)                                                                                                   |
| исчаралфанумерикврапв   | 28      | [**исчаралфанумерик**](/windows/win32/api/winuser/nf-winuser-ischaralphanumerica)     | KERNEL32 | [&](#shlwapi-wrapper-functions)                                                                                                   |
| исчарупперврапв          | 26      | [**исчаруппер**](/windows/win32/api/winuser/nf-winuser-ischaruppera)                   | USER32   | [&](#shlwapi-wrapper-functions)                                                                                                   |
| лоадлибрариврапв          | 105     | [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)                     | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| лоадстрингврапв           | 107     | [**лоадстринг**](/windows/win32/api/winuser/nf-winuser-loadstringa)                     | KERNEL32 | [&](#shlwapi-wrapper-functions)                                                                                                   |
| мессажебоксврапв           | 340     | [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox)                     | USER32   | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |
| мовефилеврапв             | 113     | [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile)                             | KERNEL32 | [(a)](#shlwapi-wrapper-functions), [(c)](#shlwapi-wrapper-functions)                                                                |
| аутпутдебугстрингврапв    | 115     | [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)         | KERNEL32 | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |
| пикмессажеврапв          | 116     | [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)                   | USER32   | [(PeekMessage и сообщение)](#peekmessage-and-postmessage)                                                                       |
| постмессажеврапв          | 117     | [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea)                   | USER32   | [(PeekMessage и сообщение)](#peekmessage-and-postmessage)                                                                       |
| регкреатекэйексврапв       | 120     | [**регкреатекэйекс**](/windows/win32/api/winreg/nf-winreg-regcreatekeyexa)               | ADVAPI32 | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |
| регистерклассврапв        | 131     | [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)               | USER32   | [(a)](#shlwapi-wrapper-functions), [(registerClass)](#registerclass)                                                                |
| регопенкэйексврапв         | 125     | [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)                   | ADVAPI32 | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |
| регкуеривалуиксврапв      | 128     | [**Процедура RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa)             | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange), [(валуикс)](#regqueryvalueexw), [(регкуеривалуиксв)](#regqueryvalueexw) |
| регкуеривалуеврапв        | 127     | [**регкуеривалуе**](/windows/win32/api/winreg/nf-winreg-regqueryvaluea)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(g)](#compareexchange)                                                                          |
| регсетвалуиксврапв        | 130     | [**RegSetValueEx**](/windows/win32/api/winreg/nf-winreg-regsetvalueexa)                 | ADVAPI32 | [(a)](#shlwapi-wrapper-functions), [(валуикс)](#regqueryvalueexw)                                                                   |
| сендмессажеврапв          | 136     | [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)                   | USER32   | [SendMessage](#sendmessage)                                                                                                       |
| сетдлгитемтекстврапв       | 138     | [**сетдлгитемтекст**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)             | USER32   | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |
| сетвиндовлонгврапв        | 141     | [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)               | USER32   | [(Виндовлонг)](#windowlong)                                                                                                         |
| сетвиндовтекстврапв        | 143     | [**SetWindowText**](/windows/win32/api/winuser/nf-winuser-setwindowtexta)               | USER32   | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |
| шеллексекутиксврапв       | 35      | [**ShellExecuteEx**](/windows/win32/api/Shellapi/nf-shellapi-shellexecuteexa)                | БИБЛИОТЕКИ  | [(a)](#shlwapi-wrapper-functions), [(б)](#dialogboxparam), [(ShellExecuteEx)](#shellexecuteex)                                      |
| шеллмессажебоксврапв      | 388     | [**шеллмессажебокс**](/windows/win32/api/Shellapi/nf-shellapi-shellmessageboxa)              | SHLWAPI  | [(a)](#shlwapi-wrapper-functions), [(FormatMessage)](#formatmessage)                                                                |
| шжетфилеинфоврапв        | 313     | [**шжетфилеинфо**](/windows/win32/api/Shellapi/nf-shellapi-shgetfileinfoa)                  | БИБЛИОТЕКИ  | [(a)](#shlwapi-wrapper-functions), [(б)](#dialogboxparam), [(g)](#compareexchange)                                                  |
| шжетпасфромидлистврапв  | 334     | [**шжетпасфромидлист**](/windows/win32/api/shlobj_core/nf-shlobj_core-shgetpathfromidlista)      | USER32   | [модуле](#compareexchange)                                                                                                             |
| транслатеакцелераторврапв | 146     | [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) | USER32   | [сохранении](#shlwapi-wrapper-functions)                                                                                                   |
| унрегистерклассврапв      | 147     | [**унрегистеркласс**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)           | USER32   | [конкретного](#shlwapi-wrapper-functions)                                                                                                   |



 

Функции-оболочки в следующей таблице не выполняют преобразование наборов символов. Вместо этого они предоставляют ограниченную поддержку функций операционной системы, недоступных на более ранних платформах.



| Функция                     | Порядковый номер | Пересылает                                                                     | DLL      | Remarks                                                                        |
|------------------------------|---------|---------------------------------------------------------------------------------|----------|--------------------------------------------------------------------------------|
| млжетуилангуаже              | 376     | [**жетусердефаултуилангуаже**](/windows/win32/api/winnls/nf-winnls-getuserdefaultuilanguage)                   | KERNEL32 | [высоты](#shlwapi-wrapper-functions)                                              |
| шканцелтимеркуеуетимер      | 265     | [**DeleteTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueuetimer)                         | KERNEL32 | [высоты](#shlwapi-wrapper-functions)                                              |
| шделететимеркуеуе           | 262     | [**DeleteTimerQueue**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-deletetimerqueue)                                   | KERNEL32 | [высоты](#shlwapi-wrapper-functions)                                              |
| шинтерлоккедкомпариксчанже | 342     | [**интерлоккедкомпариксчанжепоинтер**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer) | KERNEL32 | [CompareExchange](#compareexchange)                                          |
| шкуеуеусерворкитем          | 260     | [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem)                                 | KERNEL32 | [(QueueUserWorkItem)](#queueuserworkitem), [(h)](#shlwapi-wrapper-functions)   |
| шсеттимеркуеуетимер         | 263     | [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer)                         | KERNEL32 | [(Сеттимеркуеуетимер)](#settimerqueuetimer), [(h)](#shlwapi-wrapper-functions) |



 

## <a name="remarks"></a>Remarks

### <a name="a"></a>конкретного

Если требуется преобразование строки, все строки преобразуются через \_ кодовую страницу CP ACP.

Эти функции используют символы наилучшего соответствия и не выполняют проверку по умолчанию при преобразовании из Юникода в ANSI. Более того, если строка не может быть преобразована из Юникода в ANSI, функция-оболочка передает строку **со значением NULL** в базовую функцию ANSI. Это может произойти, например, при нехватке памяти. Передача **пустой** строки может привести к сбою некоторых функций с ошибкой недопустимого параметра, но другие функции принимают строку **null** и обрабатывают ее как предполагаемый параметр. Например, ошибка возникает, когда функция **креатевиндовексврапв** пытается преобразовать параметр *лпвиндовнаме* в ANSI, а [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) создает окно с пустым заголовком. Программа-оболочка не уведомляет вас о возникновении этих проблем.

Уровень Майкрософт для Юникода (МСЛУ) проверяет наличие ошибок во время преобразования из Юникода в ANSI и возвращает соответствующие значения ошибок. Например, функция-оболочка [**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua) в мслу возвращает 0, если элемент не был успешно добавлен.

### <a name="b"></a>&

Эти функции используют ссылку с отложенной загрузкой на соответствующую функцию. Это означает, что библиотека DLL, содержащая функцию в столбце "пересылается", не загружается Shlwapi.dll до тех пор, пока не будет вызвана функция в этой библиотеке DLL. Компоновщик Microsoft Visual C++ поддерживает эту функцию более широко с помощью параметра параметр/DELAYLOAD.

### <a name="c"></a>ц

Эта функция управляет именами файлов. Как отмечалось в [(а)](#shlwapi-wrapper-functions), функции преобразуют все строки через \_ кодовую страницу CP ACP. Они не проверяют, заданы ли для файловых операций ввода-вывода режим ANSI. Если функции файлового ввода-вывода находятся в режиме изготовителя оборудования, строки будут преобразованы в неправильную кодировку и из нее. Приложение может явно задать функции ввода-вывода в режиме изготовителя оборудования, вызвав функцию [**SetFileApisToOEM**](/windows/win32/api/fileapi/nf-fileapi-setfileapistooem) .

* * Предупреждение системы безопасности. * * Использование этих функций-оболочек для имен файлов может привести к нарушению безопасности приложения. Поскольку проверка по умолчанию не выполняется и используются символы наилучшего соответствия, символы имени файла могут быть преобразованы непредвиденным образом. Это может привести к атакам с подменой файловой системы. Кроме того, при преобразовании из Юникода в ANSI могут возникать неуспешные потери данных.

МСЛУ не имеет этих ограничений.

### <a name="d"></a>четырехмерного

Если для рисуемой строки требуется набор символов, недоступный в шрифте, выбранном в контексте устройства, эти функции-оболочки используют функцию [связывания шрифтов](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767872(v=vs.85)) Библиотеки [MLang](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767865(v=vs.85)) для отображения каждого символа в соответствующем шрифте. В отличие от большинства других функций-оболочек, они работают в Microsoft Windows NT 4,0 в дополнение к собственным платформам ANSI.

### <a name="e"></a>&

Полные реализации этих функций в Юникоде доступны на собственных платформах ANSI. Эти функции не вызывают связанную функцию ANSI.

### <a name="f"></a>ж

Если язык пользовательского интерфейса по умолчанию использует набор символов, отличный от набора по умолчанию системного интерфейса, система пытается переписать шаблоны диалоговых окон и элементов управления-подкласс, а также преобразовать элементы меню в прорисовку владельцем, чтобы строки в языке пользовательского интерфейса по умолчанию отображались правильно. Единственными элементами управления, которые поддерживаются в шаблоне диалогового окна, являются статические элементы управления Button, ListBox и ComboBox. Эти элементы управления являются подклассами таким, что функция **сендмессажеврапв** может получить исходную строку Юникода без преобразования с помощью кодировки ANSI. В отличие от большинства других функций-оболочек, они работают в Microsoft Windows NT 4,0, а также в собственных платформах ANSI. Дополнительные сведения о том, как определяются язык пользовательского интерфейса по умолчанию и язык пользовательского интерфейса по умолчанию, см. в комментариях к документации по функции [**мллоадлибрари**](./callbacks.md) .

### <a name="g"></a>модуле

Если требуется преобразование строки, все строки преобразуются через \_ кодовую страницу CP ACP.

При преобразовании из ANSI в Юникод для вывода, если возвращаемая строка не помещается в предоставленный буфер, функции-оболочки усекаются. Эти функции, возвращающие количество символов, копируемых в буфер или количество символов, необходимое для предотвращения усечения, не возвращают число символов Юникода, копируемых в буфер, предоставленный или требуемый из вызывающей стороны функции-оболочки. Они возвращают количество символов ANSI, скопированных в буфер или требуемых базовой функцией ANSI. МСЛУ не имеет этих ограничений.

### <a name="h"></a>высоты

В системах до Windows XP эти функции реализуют упрощенный пул потоков и очередь таймера. В Windows XP и более поздних версиях эти функции используют системный пул потоков и очередь системных таймеров. Для функций очереди таймера параметр *хкуеуе* должен иметь значение **null** , чтобы указать, что операция должна выполняться в очереди таймера по умолчанию.

### <a name="i"></a>сохранении

На платформах Юникода эти функции преобразуют сообщение из Юникода в ANSI, если окно назначения — ANSI. Эти функции не выполняют преобразование сообщений на собственных платформах ANSI. Таким образом, вызывающие приложения, вызывающие эту функцию, должны убедиться, что сообщение имеет формат Юникода на платформах Юникода и в формате ANSI на платформах ANSI. Например, в следующем вызове функции параметр *wParam* должен быть кодовой точкой Юникода, если программа выполняется на платформе Юникода и должна быть символом ANSI, если программа выполняется на платформе ANSI.

``` syntax
CallWindowProcWrapW(prevWndProc, hwnd, WM_CHAR, wParam, lParam);
```

МСЛУ отслеживает кодировку окна назначения и при необходимости преобразует сообщение.

### <a name="j"></a>б

На платформах ANSI эти функции возвращают длину базовой строки ANSI, а не длину переведенной строки в Юникоде. МСЛУ не имеет этих ограничений.

### <a name="compareexchange"></a>CompareExchange

Синтаксис для **шинтерлоккедкомпариксчанже** несколько отличается от типа [**интерлоккедкомпариксчанжепоинтер**](/windows/win32/api/winnt/nf-winnt-interlockedcompareexchangepointer), но он работает одинаково.

``` syntax
void* SHInterlockedCompareExchange(void **ppDest, void *pExch, void *pComp);
```

### <a name="comparestring"></a>CompareString

Помните, что на собственных платформах ANSI обе строки преобразуются в ANSI и сравниваются как строки ANSI. Если строки в Юникоде содержат символы, которые не могут быть представлены в формате ANSI, результаты могут быть неожиданными. Например, если кодовая страница ANSI по умолчанию не поддерживает ККЯ-символы, строки L " \\ x66F0" и l " \\ x6708" будут сравниваться как равные на собственных платформах ANSI, так как они сопоставляются со строкой ANSI "?".

### <a name="datetime"></a>DateTime

В Shlwapi.dll версии 5,0, поставляемой вместе с Windows 2000, кодовая страница идентификатора локали, которая передается в качестве первого параметра **жетдатеформатврапв** и **жеттимеформатврапв** , должна соответствовать текущей кодовой странице ANSI. В противном случае возвращаемая строка может быть преобразована неправильно. Это ограничение не распространяется на Shlwapi.dll версии 5,5 и выше. Это означает, что это ограничение не распространяется на системы Windows XP и более поздних версий. МСЛУ не имеет этого ограничения.

### <a name="dialogboxparam"></a>(Диалогбокспарам)

Параметр *лптемплатенаме* для функции **диалогбокспарамврапв** не может быть строкой. Он должен быть порядковым номером, созданным с помощью макроса [**макеинтресаурце**](/windows/win32/api/winuser/nf-winuser-makeintresourcea) . Процедура диалогового окна, заданная параметром *лпдиалогфунк* , принимает сообщения ANSI на собственных платформах ANSI и сообщениях Юникода на собственных платформах Юникода. Процедура диалогового окна должна быть подготовлена для обработки обоих случаев. МСЛУ не имеет этих ограничений.

### <a name="exttextout"></a>ExtTextOut

Собственные платформы ANSI реализуют функцию [**ексттекстаутв**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) , а также собственные платформы Юникода. Цель **ексттекстаутврапв** заключается в том, чтобы выполнить связывание шрифтов, как описано в отдельном замечании.

### <a name="dragqueryfile"></a>(Драгкуерифиле)

Функция **драгкуерифилеврапв** не позволяет запрашивать длину файла в обработчике перетаскивания, передавая **null** в качестве параметра *лпсзфиле* . МСЛУ не имеет этих ограничений.

### <a name="formatmessage"></a>FormatMessage

На собственных платформах ANSI форматы в строке не преобразуются из Юникода в ANSI. Например, следующий пример кода имеет значение Error.


```
WCHAR szBuffer[MAX_PATH];
DWORD_PTR Arguments[2] = { L"String1", L"String2" };

FormatMessageWrapW(FORMAT_MESSAGE_FROM_STRING, 
               L"%1!s! %2", 
               0, 0, 
               szBuffer, 
               MAX_PATH, 
               (va_list*)Arguments);
```



В этом примере кода используется "! s!" ЧЧ:ММ:СС... На собственных платформах ANSI эта строка передается в версию ANSI функции [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage) . Следовательно, вместо строки в Юникоде ожидается строка ANSI. Аналогично, формат "%2" подразумевает строковый аргумент. При передаче в функцию ANSI **FormatMessage** она интерпретируется как строка ANSI, а не строка Юникода. Правильная строка формата: L "%1! WS! %2! ws! ". Это правильно выводит строки на платформах ANSI и Юникод.

Функция не поддерживает "%0" Строка специального формата.

МСЛУ не имеет этих ограничений.

### <a name="getclassinfo"></a>(Жетклассинфо)

На собственных платформах ANSI члены **лпсзменунаме** и **лпсзкласснаме** структуры [**вндкласс**](/windows/win32/api/winuser/ns-winuser-wndclassa) не преобразуются в Юникод и всегда имеют значение **null**. Кроме того, процедура окна, возвращаемая членом **лпфнвндпрок** структуры **вндкласс** , не преобразуется в Юникод и ссылается на процедуру окна ANSI. МСЛУ не имеет этих ограничений.

### <a name="menu"></a>Меню

В Shlwapi.dll версии 5,0, которая поставляется с Windows 2000, строки пунктов меню, содержащие символы табуляции ( \\ t), могут отображаться неправильно. Это ограничение не распространяется на Shlwapi.dll версии 5,5 и выше. Это означает, что это ограничение не распространяется на системы Windows XP и более поздних версий. МСЛУ не имеет этого ограничения.

### <a name="menuiteminfo"></a>Объектами menuiteminfo

Эта функция поддерживает только версию Microsoft Windows NT 4,0 структуры [**менуитеминфов**](/windows/win32/api/winuser/ns-winuser-menuiteminfoa) . В этой структуре отсутствует элемент **хбмпитем** . Кроме того, функция не поддерживает \_ флаг битовой карты миим. МСЛУ не имеет этих ограничений.

### <a name="openfilename"></a>OpenFileName

Элемент **кбсизе** структуры [**опенфиленамев**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) должен иметь значение sizeof (OpenFileName \_ NT4W).

Элемент **лпстркустомфилтер** структуры [**опенфиленамев**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) должен иметь значение **null**.

Значения элементов **нмаксфиле** и **нмаксфилетитле** структуры [**опенфиленамев**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) не должны превышать максимальное значение \_ path.

Если элемент **лпфнхук** структуры [**Опенфиленамев**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) не равен **null**, он должен ССЫЛАТЬСЯ на процедуру-ловушку ANSI на собственных платформах ANSI и процедуру обработчика Юникода на собственных платформах Юникода.

МСЛУ не имеет этих ограничений.

### <a name="peekmessage-and-postmessage"></a>(PeekMessage и сообщение)

На собственных платформах ANSI для передаваемого или полученного сообщения не выполняется перевод. Передаваемое/полученное сообщение является ANSI на собственных платформах ANSI и Юникод на собственных платформах Юникода. Вызывающее приложение должно быть готово к обработке обоих случаев. Например, если полученное сообщение имеет тип WM \_ char, то параметр *wParam* является кодом символа ANSI на собственных платформах ANSI, но это кодовая точка Юникода на собственных платформах Юникода. МСЛУ не имеет этих ограничений.

### <a name="queueuserworkitem"></a>QueueUserWorkItem

Функция **шкуеуеусерворкитем** немного отличается от соответствующей функции [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem) . Синтаксис для **шкуеуеусерворкитем** показан здесь.

``` syntax
BOOL SHQueueUserWorkItem(LPTHREAD_START_ROUTINE pfnCallback,
                     LPVOID pContext,
                     LONG lPriority,
                     DWORD_PTR dwTag,
                     DWORD_PTR * pdwId,
                     LPCSTR pszModule,
                     DWORD dwFlags);
```

Параметры должны быть установлены следующим образом:

-   Параметры *пфнкаллбакк* и *пконтекст* имеют те же значения, что и параметры *функции* и *контекста* , соответственно, класса [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem).
-   Параметр *двтаг* не используется и должен иметь значение 0.
-   Параметр *пдвлд* не используется и должен иметь значение **null**.
-   Параметр *псзмодуле* указывает на необязательную строку ANSI, завершающуюся нулем, которая указывает имя библиотеки, загружаемой перед началом и выгрузкой рабочего элемента после завершения рабочего элемента. Этот параметр может принимать значение **NULL**.
-   Параметр *dwFlags* поддерживает только подмножество значений, поддерживаемых [**QueueUserWorkItem**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-queueuserworkitem). Распознаются следующие флаги.

    

    | Имя              | Значение      | Значение                          |
    |-------------------|------------|----------------------------------|
    | Техническая спецификация \_ ексекутеио    | 0x00000001 | То же, что и WT \_ ексекутеиниосреад.   |
    | Техническая спецификация \_ лонжексектиме | 0x00000008 | То же, что и WT \_ ексекутелонгфунктион. |

    

     

    > [!Note]  
    > \_Значение флага TPS лонжексектиме не совпадает с числовым значением \_ флага WT ексекутелонгфунктион. При использовании **шкуеуеусерворкитем** параметр dwFlags должен быть сочетанием значений спецификаций \_ \* , а не значений WT \_ \* .

     

**Шкуеуеусерворкитем** возвращает ненулевое значение, если рабочий элемент был успешно поставлен в очередь, и 0 в противном случае. Если функция завершается ошибкой, можно использовать [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) для получения дополнительных сведений.

### <a name="registerclass"></a>RegisterClass

На собственных платформах ANSI миграция элемента **лпфнвндпрок** структуры [**вндклассв**](/windows/win32/api/winuser/ns-winuser-wndclassa) не выполняется. Окно будет принимать сообщения в окне ANSI на собственных платформах ANSI и сообщениях окна Юникода на собственных платформах Юникода. Процедура окна должна быть подготовлена для обработки обоих случаев. МСЛУ не имеет этих ограничений.

### <a name="regqueryvalueexw"></a>(Регкуеривалуиксв)

**Регкуеривалуиксврапв** также был вызван с именем **регкуеривалуиксв**. Как и в случае с любой неименованной функцией, экспортируемой строго по порядковому номеру, можно выбрать имя, известное функции в коде.

### <a name="sendmessage"></a>SendMessage

На собственных платформах Юникода функция **сендмессажеврапв** пересылается функции [**сендмессажев**](/windows/win32/api/winuser/nf-winuser-sendmessage) . На собственных платформах ANSI **сендмессажеврапв** обеспечивает ограниченную поддержку преобразования сообщений в Юникоде в ANSI. Список поддерживаемых сообщений приведен в следующей таблице. Функция не будет переводить другие сообщения.

МСЛУ не имеет этих ограничений.



|                      |                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| \_ADDSTRING CB        | (б) (f) (c)                                                                                               |
| \_FINDSTRING CB       | (б) (f) (c)                                                                                               |
| \_ФИНДСТРИНЖЕКСАКТ CB  | (a) (f) (c)                                                                                               |
| \_ЖЕТЛБТЕКСТ CB        | (b) (f) (c) (o) буфер, переданный в параметре *lParam* , должен содержать пространство не менее 256 символов.   |
| \_ЖЕТЛБТЕКСТЛЕН CB     | конкретного                                                                                                       |
| \_ИНСЕРТСТРИНГ CB     | (б) (f) (c)                                                                                               |
| \_СЕЛЕКТСТРИНГ CB     | (б) (f) (c)                                                                                               |
| EM \_ чарфромпос      |                                                                                                           |
| EM, \_ строка          | (e) возвращаемое значение представляет собой число скопированных символов ANSI.                                             |
| EM \_ жетсел           |                                                                                                           |
| EM \_ реплацесел       | (б) (f)                                                                                                   |
| EM \_ сетпассвордчар  | конкретного                                                                                                       |
| EM \_ сетсел           |                                                                                                           |
| EM \_ сетвордбреакпрок | Это сообщение не действует. Процедура разрыва слов не задана.                                          |
| ADDSTRING балансировки нагрузки \_        | (б) (f) (d)                                                                                               |
| FINDSTRING балансировки нагрузки \_       | (б) (f) (d)                                                                                               |
| финдстринжексакт балансировки нагрузки \_  | (b) (f) (фунта)                                                                                             |
| \_Балансировка нагрузки          | (b) (f) (фунт) (o) буфер, переданный в параметре *lParam* , должен содержать пространство не менее 256 символов. |
| жеттекстлен балансировки нагрузки \_       | конкретного                                                                                                       |
| инсертстринг балансировки нагрузки \_     | (б) (f) (d)                                                                                               |
| селектстринг балансировки нагрузки \_     | (б) (f) (d)                                                                                               |
| WM \_ gettext          | (б) (f)                                                                                                   |
| WM \_ жеттекстленгс    | конкретного                                                                                                       |
| WM \_ SETTEXT          | (б) (f)                                                                                                   |
| WM \_ сеттингчанже    | (а) сообщение отправляется с временем ожидания три секунды.                                                  |



 


-   (а) измеряемая или получаемая строка ANSI должна соответствовать следующему условию: длина соответствующей версии строки в Юникоде не может превышать длину ANSI-версии строки. Если это условие не выполнено, возвращаемая длина будет сокращена. Если недостаточно памяти для определения длины строки Юникода, функция возвращает ноль, а не ошибку балансировки нагрузки \_ или CB \_ Err, как может быть ожидается.
-   (б) Если требуется преобразование строки, все строки преобразуются через \_ кодовую страницу CP ACP.

    Эта функция использует символы наилучшего соответствия и не выполняет проверку по умолчанию при преобразовании из Юникода в ANSI. Кроме того, если строка не может быть преобразована из Юникода в ANSI, функция передает строку со значением NULL в базовую функцию ANSI. Это может произойти, например, при нехватке памяти. Передача пустой строки может привести к сбою некоторых функций с ошибкой недопустимого параметра, но другие функции принимают строку NULL и обрабатывают ее как предполагаемый параметр. Например, если ошибка возникает, когда \_ оболочка WM SETTEXT пытается преобразовать заголовок окна в ANSI, окно будет иметь пустой заголовок. Функция не уведомляет вас при возникновении этих проблем. МСЛУ не имеет этих ограничений.

-   (c) заданный описатель окна должен быть маркером для элемента управления [ComboBox](../controls/combo-boxes.md) или [ComboBoxEx](../controls/comboboxex-controls.md) . Если маркер связан с элементом управления ComboBox, который является владельцем и не был создан с помощью стиля [списка стилей](../controls/list-box-styles.md) , то перевод этого сообщения завершится ошибкой и может даже завершиться сбоем.
-   (d) заданный описатель окна должен быть маркером для элемента управления ListBox. Если ListBox является владельцем и не был создан с помощью стиля [списка стилей](../controls/list-box-styles.md) , то перевод этого сообщения завершится ошибкой и может даже завершиться сбоем.
-   (e) Если требуется преобразование строки, все строки преобразуются через \_ кодовую страницу CP ACP.

    При преобразовании из ANSI в Юникод для вывода функции-оболочки усекаются возвращаемую строку, если она не помещается в предоставленный буфер. Возвращаемое значение для функций, возвращающих количество символов, копируемых в буфер, или количество символов, необходимое для предотвращения усечения, относится к числу символов ANSI, копируемых в буфер или требуемых базовой функцией ANSI, а не к числу символов Юникода, копируемых в буфер, предоставленный или требуемый из вызывающего приложения, вызвавшего функцию-оболочку. МСЛУ не имеет этого ограничения. Дополнительные сведения см. [в статье уровень Майкрософт для Юникода в системах Windows 95/98/Me](/previous-versions/ms812865(v=msdn.10)).

### <a name="settimerqueuetimer"></a>(Сеттимеркуеуетимер)

Функция **шсеттимеркуеуетимер** немного отличается от соответствующей функции [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) . Ее синтаксис выглядит следующим образом:

``` syntax
HANDLE SHSetTimerQueueTimer(HANDLE hQueue,
                        WAITORTIMERCALLBACK pfnCallback,
                        LPVOID pContext,
                        DWORD dwDueTime,
                        DWORD dwPeriod,
                        LPCSTR lpszLibrary,
                        DWORD dwFlags);
```

Параметры должны быть установлены следующим образом:

-   Параметр *хкуеуе* должен иметь значение **null**, указывая очередь таймера по умолчанию.
-   Параметры *пфнкаллбакк*, *пконтекст*, *двдуетиме* и *двпериод* имеют те же значения, что и параметры *обратного вызова*, *параметра*, *DueTime* и *period* , соответственно, из [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).
-   Параметр *лпсзлибрари* не используется и должен иметь значение **null**.
-   Параметр *flags* поддерживает только подмножество значений, поддерживаемых [**CreateTimerQueueTimer**](/windows/win32/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer).

    

    | Имя              | Значение      | Значение                         |
    |-------------------|------------|---------------------------------|
    | Техническая спецификация \_ ексекутеио    | 0x00000001 | То же, что и WT \_ ексекутеиниосреад   |
    | Техническая спецификация \_ лонжексектиме | 0x00000008 | То же, что и WT \_ ексекутелонгфунктион |

    

     

    > [!Note]  
    > \_Значение флага TPS лонжексектиме не совпадает с числовым значением \_ флага WT ексекутелонгфунктион. При использовании **шсеттимеркуеуетимер** параметр *dwFlags* должен быть сочетанием значений спецификаций \_ \* , а не значений WT \_ \* .

     

**Шсеттимеркуеуетимер** возвращает маркер созданного таймера в случае успеха и **значение NULL** в противном случае.

### <a name="shellexecuteex"></a>ShellExecuteEx

Элемент **лпфиле** структуры [**шеллексекутеинфо**](/windows/win32/api/Shellapi/ns-shellapi-shellexecuteinfoa) , переданный в параметре только этой функции, не может превышать \_ Максимальное число \_ символов URL-адреса в Интернете \_ . Если флаг см \_ . в разделе Mask \_ CLASSNAME, то элемент **лпкласс** должен быть инициализирован со **значением NULL**.

### <a name="valueex"></a>(Валуикс)

Поддерживаются только следующие типы данных реестра: REG \_ SZ, REG \_ expand \_ SZ, REG \_ binary и REG \_ DWORD. В отличие от этих функций-оболочек, МСЛУ также поддерживает REG \_ Multi \_ expand \_ SZ.

### <a name="windowlong"></a>(Виндовлонг)

На собственных платформах ANSI функция не выполняет преобразование ни в одном из окон Long. Например, при передаче ГВЛП \_ WndProc функция возвращает окно ANSI, а не преобразователь. МСЛУ не имеет этих ограничений.

 

 
