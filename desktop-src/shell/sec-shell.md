---
description: В этом разделе содержатся сведения о вопросах безопасности, связанных с оболочкой Windows.
ms.assetid: eca31652-2659-456d-b082-c84d6fd39094
title: 'Вопросы безопасности: оболочка Microsoft Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b11a965a36a403b57a3e5229fc758a4ce37252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810936"
---
# <a name="security-considerations-microsoft-windows-shell"></a>Вопросы безопасности: оболочка Microsoft Windows

В этом разделе содержатся сведения о вопросах безопасности, связанных с оболочкой Windows. Этот документ не может предоставить все, что вам нужно знать о проблемах безопасности. вместо этого используйте его в качестве отправной точки и ссылки на эту конкретную область технологий.

Оболочка управляет рядом важных аспектов системы, в том числе несколько, которые представляют потенциальные риски безопасности, если они не обрабатывались должным образом. В этом разделе описаны некоторые из наиболее распространенных проблем и способы их устранения в приложениях. Помните, что безопасность не ограничена Интернет-эксплойтами. В общих системах, включая системы, доступные через службы терминалов, необходимо также убедиться в том, что пользователи не могут выполнять какие-либо действия, которые могут повредить другие пользователи, имеющие доступ к системе.

-   [Правильная установка приложения](#installing-your-application-properly)
-   [Shlwapi](#shlwapi)
-   [Автозавершение](#autocomplete)
-   [ShellExecute, ShellExecuteEx и связанные функции](#shellexecute-shellexecuteex-and-related-functions)
-   [Перемещение и копирование файлов](#moving-and-copying-files)
-   [Создание защищенных расширений пространства имен](#writing-secure-namespace-extensions)
-   [Оповещения системы безопасности](#security-alerts)
-   [См. также](#related-topics)

## <a name="installing-your-application-properly"></a>Правильная установка приложения

Большинство потенциальных проблем безопасности оболочки можно устранить путем правильной установки приложения.

-   Установите приложение в папку Program Files. 

    | Операционная система                             | Расположение                                                                                                                                                                                                                                   |
    |----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows XP, Windows Server 2003 и более ранние версии | \_программные \_ файлы CSid                                                                                                                                                                                                                      |
    | Windows Vista и более поздние версии                      | FOLDERID \_ ProgramFiles, FOLDERID \_ PROGRAMFILESX86, FOLDERID \_ ProgramFilesX64, FOLDERID \_ програмфилескоммон, FOLDERID \_ ProgramFilesCommonX86 или FOLDERID \_ ProgramFilesCommonX64. Дополнительные сведения см. в разделе [**кновнфолдерид**](knownfolderid.md) . |

    

     

-   Не храните данные пользователя в папке Program Files.

    Используйте соответствующую папку данных для данных, общих для всех пользователей.

    

    | Операционная система                             | Расположение               |
    |----------------------------------------------|------------------------|
    | Windows XP, Windows Server 2003 и более ранние версии | \_распространенная папка \_ AppData |
    | Windows Vista и более поздние версии                      | FOLDERID \_ папка ProgramData  |

    

     

    Используйте соответствующую папку данных пользователя для данных, принадлежащих определенному пользователю.

    

    | Операционная система                             | Расположение                                                   |
    |----------------------------------------------|------------------------------------------------------------|
    | Windows XP, Windows Server 2003 и более ранние версии | Выcsid \_ AppData, личный код CSID \_ и др.               |
    | Windows Vista и более поздние версии                      | FOLDERID \_ роамингаппдата, \_ документы FOLDERID и др. |

    

     

-   Если необходимо установить в папку, отличную от папки Program Files, убедитесь, что списки управления доступом (ACL) правильно настроены таким образом, чтобы пользователи не имели доступа к недопустимым частям файловой системы. Все данные, относящиеся к конкретному пользователю, должны иметь список управления доступом, который не позволяет другому пользователю обращаться к нему.
-   При настройке сопоставлений файлов обязательно укажите командную строку. Используйте полный путь и заключите все элементы, содержащие пробелы, в кавычки. Заключите параметры команды в отдельные кавычки. В противном случае строка может быть неверно проанализирована, и приложение не запустится должным образом. Здесь показаны два примера правильно сформированных командных строк.

    ```
    "C:\Program Files\MyApp\MyApp.exe" "%1" "%2"
    C:\MyAppDir\MyApp\MyApp.exe "%1"
    ```

    

> [!Note]  
> Расположение стандартных папок установки может отличаться от системы к системе. Чтобы получить расположение стандартной папки в определенной системе Windows Vista или более поздней версии, вызовите [**шжеткновнфолдерпас**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) с соответствующим значением [**кновнфолдерид**](knownfolderid.md) . В Windows XP, Windows Server 2003 или более ранних версиях вызовите [**шжетфолдерлокатион**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) или [**шжетфолдерпас**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) с соответствующим значением [**CSid**](csidl.md) .

 

## <a name="shlwapi"></a>Shlwapi

Упрощенный API оболочки (Shlwapi) включает ряд функций обработки строк. Неправильное использование этих функций может привести к непредвиденному усечению строк без уведомления о возвращаемом усечении. В следующих случаях не следует использовать функции Shlwapi. Перечисленные альтернативные функции, которые создают меньше рисков, должны использоваться на их месте.



| Shlwapi, функция                                                 | Альтернативная функция                                                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw),[**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)              | [**Стрингкчкат**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**стрингкбкат**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata) и связанные функции             |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw), [ **стркпин**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)             | [**Стрингкчкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**стрингкбкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) и связанные функции         |
| [**внспринтф**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa), [ **ввнспринтф**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa) | [**Стрингкчпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**стрингкбпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa) и связанные функции |



 

При использовании таких функций, как [**пасрелативепасто**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa) , которые возвращают путь к файлу, всегда устанавливайте для буфера максимальный размер \_ символов. Это гарантирует, что буфер достаточно велик для хранения наибольшего возможного пути к файлу, а также завершающего нуль-символа.

Дополнительные сведения о альтернативных строковых функциях см. в разделе [About стрсафе. h](../menurc/strsafe-ovw.md).

## <a name="autocomplete"></a>Автозавершение

Не используйте функцию автозаполнения для паролей.

## <a name="shellexecute-shellexecuteex-and-related-functions"></a>ShellExecute, ShellExecuteEx и связанные функции

Существует несколько функций оболочки, которые можно использовать для запуска приложений: [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), [**винексек**](/windows/win32/api/winbase/nf-winbase-winexec)и [**шкреатепроцессасусерв**](/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw). Убедитесь, что вы предоставляете однозначное определение приложения, которое должно быть выполнено.

-   При указании пути к исполняемому файлу укажите полный путь. Не зависят от оболочки для нахождение файла.
-   Если указать строку командной строки, содержащую пробелы, заключите строку в кавычки. В противном случае средство синтаксического анализа может интерпретировать один элемент, содержащий пробелы, как несколько элементов.

## <a name="moving-and-copying-files"></a>Перемещение и копирование файлов

Одним из ключевых способов обеспечения безопасности системы является правильное назначение ACL. Также можно использовать зашифрованные файлы. Убедитесь, что при перемещении или копировании файлов им назначается правильный список ACL и они не были случайно расшифрованы. Сюда входит перемещение файлов в **корзину**, а также в файловую систему. Используйте [**интерфейс IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) (Windows Vista или более поздней версии) или [**ШФИЛЕОПЕРАТИОН**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) (Windows XP и более ранние версии). Не используйте [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile), который может не задавать ожидаемый список ACL для целевого файла.

## <a name="writing-secure-namespace-extensions"></a>Создание защищенных расширений пространства имен

Расширения пространства имен оболочки — это мощный и гибкий способ предоставления данных пользователю. Однако они могут вызвать сбой системы, если они неправильно написаны. Некоторые ключевые моменты, которые следует учитывать:

-   Не следует рассчитывать на то, что данные, такие как изображения, форматируются правильно.
-   Не следует рассчитывать, что максимальный \_ путь эквивалентен числу *байтов* в строке. Это число *символов*.

## <a name="security-alerts"></a>Оповещения системы безопасности

В следующей таблице перечислены некоторые функции, которые при неправильном использовании могут привести к нарушению безопасности приложений.



| Компонент                                                                        | Меры по снижению риска                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [ **ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) | Поиск, зависящий от проверки ряда расположений по умолчанию для поиска конкретного файла, можно использовать при атаке с подменой. Используйте полный путь, чтобы обеспечить доступ к нужному файлу.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw)                                                       | Первый аргумент, *psz1*, должен быть достаточно большим для хранения *psz2* и закрывающего " \\ 0", в противном случае может произойти переполнение буфера. Вместо этого используйте один из следующих вариантов. [**Стрингкбкат**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**стрингкбкатекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**стрингкбкатн**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**стрингкбкатнекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**стрингкчкат**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**стрингкчкатекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)или [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                             |
| [**стркатбуфф**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa)                                               | Конечная строка не гарантированно завершается нулем. Вместо этого используйте один из следующих вариантов. [**Стрингкбкат**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**стрингкбкатекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**стрингкбкатн**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**стрингкбкатнекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**стрингкчкат**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**стрингкчкатекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)или [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                  |
| [**стркатчаинв**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw)                                           | Конечная строка не гарантированно завершается нулем. Вместо этого используйте один из следующих вариантов. [**Стрингкбкатекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**стрингкбкатнекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**стрингкчкатекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)или [**стрингкчкатнекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw)                                                       | Первый аргумент, *psz1*, должен быть достаточно большим для хранения *psz2* и закрывающего " \\ 0", в противном случае может произойти переполнение буфера. Вместо этого используйте один из следующих вариантов. [**Стрингкбкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**стрингкбкопекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**стрингкбкопин**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**стрингкбкопинекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**стрингкчкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**стрингкчкопекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)или [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                             |
| [**стркпин**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)                                                     | Не гарантируется, что скопированная строка завершается нулем. Вместо этого используйте один из следующих вариантов. [**Стрингкбкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**стрингкбкопекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**стрингкбкопин**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**стрингкбкопинекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**стрингкчкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**стрингкчкопекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna), [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                                                                                                    |
| [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa)                                                       | [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa) предполагает, что *лпсз* является строкой, завершающейся нулем. Кроме того, возвращаемая строка не гарантированно завершается нулем. Вместо этого используйте один из следующих вариантов. [**Стрингкбкат**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**стрингкбкопекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**стрингкбкопин**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**стрингкбкопинекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**стрингкчкопи**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**стрингкчкопекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)или [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                              |
| [**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)                                                     | Первый аргумент, *псзфронт*, должен быть достаточно большим для хранения *псзбакк* и закрывающего " \\ 0", в противном случае может произойти переполнение буфера. Имейте в виду, что последний аргумент, *кчмакс*, — это количество символов, копируемых в *псзфронт*, а не обязательно размер *псзфронт* в байтах. Вместо этого используйте один из следующих вариантов. [**Стрингкбкат**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**стрингкбкатекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**стрингкбкатн**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**стрингкбкатнекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**стрингкчкат**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**стрингкчкатекс**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)или [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa). |
| [**внспринтф**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa)                                                 | Не гарантируется, что скопированная строка завершается нулем. Вместо этого используйте один из следующих вариантов. [**Стрингкбпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**стрингкбпринтфекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**стрингкбвпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**стрингкбвпринтфекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**стрингкчпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)или [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |
| [**ввнспринтф**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa)                                               | Не гарантируется, что скопированная строка завершается нулем. Вместо этого используйте один из следующих вариантов. [**Стрингкбпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**стрингкбпринтфекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**стрингкбвпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**стрингкбвпринтфекс**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**стрингкчпринтф**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)или [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Microsoft Security](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Центр разработчиков безопасности](https://msdn.microsoft.com/security/)
</dt> <dt>

[Ускорители решений от Майкрософт](/previous-versions/tn-archive/cc936627(v=technet.10))
</dt> <dt>

[Технический центр безопасности](https://technet.microsoft.com/security/default.aspx)
</dt> <dt>

[О Стрсафе. h](../menurc/strsafe-ovw.md)
</dt> </dl>

 

 
