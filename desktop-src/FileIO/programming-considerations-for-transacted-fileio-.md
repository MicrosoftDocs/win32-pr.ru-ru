---
description: Описывает различные вопросы программирования транзакционной NTFS.
ms.assetid: a1ef1ce1-42f6-4627-ab64-e7f41fa23e94
title: Рекомендации по программированию для транзакционной NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd3150746b1cb34495178cc8318805587f3d08f17e04cb8227e95a9c52ddce3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047944"
---
# <a name="programming-considerations-for-transactional-ntfs"></a>Рекомендации по программированию для транзакционной NTFS

Описание различных аспектов программирования транзакционной NTFS см. в следующих разделах:

-   [Какие изменения в файлах являются транзакционными](#which-file-changes-are-transacted)
-   [Сжатие](#compression)
-   [Создание файла или каталога](#creating-a-file-or-directory)
-   [Удаление файла](#deleting-a-file)
-   [Удаление каталога](#deleting-a-directory)
-   [Проблемы с блокировкой каталога](#directory-locking-issues)
-   [Перечисление каталогов](#directory-enumeration)
-   [Отображенные в памяти файлы](#memory-mapped-files)
-   [Именованные потоки](#named-streams)
-   [Переименование файла или каталога](#renaming-a-file-or-directory)
-   [Точки повторного синтаксического анализа](#reparse-points)
-   [Код ошибки](#error-codes)
-   [Зашифрованная файловая система](#encrypted-file-system)
-   [Функции файлового ввода-вывода и транзакционная NTFS](#file-io-functions-and-transactional-ntfs)
    -   [Транзакционные функции](#transacted-functions)
    -   [Функции файлового ввода-вывода, измененные системой TxF](#file-io-functions-changed-by-txf)

## <a name="which-file-changes-are-transacted"></a>Какие изменения в файлах являются транзакционными

Большинство изменений файлов, таких как изменения в содержимом файлов, потоках, точках повторного анализа, атрибутах и пространстве имен файловой системы, являются транзакционными. При выполнении одного из этих изменений в транзакционном файле обрабатывается изменение, изолированное от других транзакций, и изменение отменяется, если откат транзакции выполнен.

Изменения, которые не влияют на содержимое файла, метаданные или пространство имен файловой системы, такие как изменения в сжатии или дефрагментации, не являются транзакционными. Эти изменения не изолированы от других транзакций и не отменяются, если откат транзакции выполнен.

## <a name="compression"></a>Сжатие

Не удается изменить состояние сжатия файла, открытого в транзакции.

## <a name="creating-a-file-or-directory"></a>Создание файла или каталога

Файл или каталог, созданный в транзакции, невидим для всех элементов за пределами текущей транзакции. За пределами этой транзакции любая попытка создать файл с тем же именем завершается ошибкой **с \_ \_ конфликтом транзакций**, что позволяет эффективно передать имя файла при фиксации или откате транзакции.

## <a name="deleting-a-file"></a>Удаление файла

Файл или каталог, который удаляется путем вызова функции [**делетефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) , остается видимым для всех внешних читателей.

> [!Note]  
> Все дескрипторы транзакций файла должны быть закрыты до завершения транзакции. Если дескрипторы не закрыты должным образом, удаление не выполняется. Все открытые дескрипторы файла должны быть закрыты перед выполнением фиксации, чтобы считаться частью транзакции. это обусловлено тем, что система фактически не удаляет файл до тех пор, пока не будет закрыт последний обработчик, даже если операция не является транзакционной, как часть подсистемы Windows файлового ввода-вывода.

 

## <a name="deleting-a-directory"></a>Удаление каталога

Каталог, который удаляется путем вызова функции [**ремоведиректоритрансактед**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) , остается видимым для всех внешних читателей.

> [!Note]  
> Те же ограничения существуют для открытых дескрипторов операций с каталогами транзакций, как и в файлах. Дополнительные сведения см. [в разделе Удаление файла](#deleting-a-file).

 

## <a name="directory-locking-issues"></a>Проблемы с блокировкой каталога

Если файл изменяется в транзакции, все компоненты каталога пути к файлу называются *закрепленными по переименованию* до завершения транзакции. Это значит, что система не позволяет переименование, пока транзакция не будет зафиксирована или отменена. Попытка переименования каталога, который является предком файла, который был изменен в текущей транзакции, завершится ошибкой, и ошибка не сможет **\_ \_ прервать \_ транзакционную \_ зависимость**.

## <a name="directory-enumeration"></a>Перечисление каталогов

Содержимое каталога может быть изменено, когда перечисление выполняется в результате использования интерфейсов API для перечисления, например функций [**финдфирстфилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) и [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) .

Изменения в каталоге за пределами транзакции не изолируются от транзакции и сразу же отображаются в пределах транзакции. Например, если модуль записи, не поддерживающей транзакции, добавляет файл в каталог, новый файл сразу же становится видимым внутри транзакции таким образом, что вызов функции [**финдфирстфилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) или [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) вернет новый файл.

Изменения, вносимые в каталог внутри транзакции, изолируются до тех пор, пока не будет выполнена фиксация транзакции. Например, файл, созданный в каталоге как часть транзакции. Нетранзакционный модуль чтения, вызывающий функцию [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) или [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) , не увидит созданный файл до тех пор, пока не будет выполнена фиксация транзакции.

## <a name="memory-mapped-files"></a>Сопоставленные в памяти файлы

Клиент должен вызвать функцию [**флушвиевоффиле**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile) , закрыть объект сопоставления файлов и закрыть этот файл перед фиксацией связанной транзакции в размещенном в памяти файле.

## <a name="named-streams"></a>Именованные потоки

Именованные потоки являются полностью транзакционными, но блокировка выполняется на уровне файлов, а не на уровне потока. Модули записи извне транзакции, которые пытаются изменить любой поток в заблокированном файле, получают сообщение об ошибке **\_ общего доступа \_**.

Вторичный поток нельзя переименовать в транзакции.

## <a name="renaming-a-file-or-directory"></a>Переименование файла или каталога

Чтобы переименовать файл как транзакционную операцию, вызовите [**мовефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) , чтобы переместить файл.

## <a name="reparse-points"></a>Точки повторного синтаксического анализа

Изменения точек повторного анализа являются транзакционными. Это означает, что если новая точка повторного анализа назначена файлу в транзакции, она не будет видна другим транзакциям. Аналогично, изменения или удаление существующей точки повторного анализа не видны до фиксации.

## <a name="error-codes"></a>Коды ошибок

Диспетчер транзакций ядра (KTM) использует коды системных ошибок в диапазоне от 6700 до 6799. транзакционная NTFS (TxF) использует Windows коды ошибок в диапазоне от 6800 до 6899. Дополнительные сведения см. в разделе WinError. h и коды системных ошибок (6000-8199).

## <a name="encrypted-file-system"></a>Зашифрованная файловая система

TxF не поддерживает операции с файлами EFS. Для транзакций нельзя открыть зашифрованный с помощью EFS файл. Вызов функции [**креатефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) для файла EFS завершится ошибкой, если **\_ \_ \_ \_ в \_ транзакции не разрешена ошибка EFS**. Аналогично, вызов функции [**енкриптфиле**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) для файла в транзакции завершится ошибкой, если **\_ \_ \_ \_ в \_ транзакции не разрешена ошибка EFS**.

## <a name="file-io-functions-and-transactional-ntfs"></a>Функции файлового ввода-вывода и транзакционная NTFS

TxF предоставляет новые транзакционные функции, которые принимают имя файла и изменяет поведение существующих функций API файлового ввода-вывода, которые принимают маркер файла.

### <a name="transacted-functions"></a>Транзакционные функции

Если не выполняется вызов одной из следующих транзакционных функций вместо ее версии, не поддерживающей транзакции, операция не будет транзакционной:

-   [**копифилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
-   [**креатедиректоритрансактед**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)
-   [**креатефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
-   [**креатехардлинктрансактед**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
-   [**креатесимболиклинктрансактед**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinktransacteda)
-   [**делетефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
-   [**финдфирстфиленаметрансактедв**](/windows/desktop/api/WinBase/nf-winbase-findfirstfilenametransactedw)
-   [**финдфирстфилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
-   [**финдфирстстреамтрансактедв**](/windows/desktop/api/WinBase/nf-winbase-findfirststreamtransactedw)
-   [**жеткомпресседфилесизетрансактед**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
-   [**жетфилеаттрибутестрансактед**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
-   [**жетфуллпаснаметрансактед**](/windows/desktop/api/WinBase/nf-winbase-getfullpathnametransacteda)
-   [**жетлонгпаснаметрансактед**](/windows/desktop/api/WinBase/nf-winbase-getlongpathnametransacteda)
-   [**мовефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)
-   [**ремоведиректоритрансактед**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)
-   [**сетфилеаттрибутестрансактед**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)

Например, функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) теперь имеет транзакционную версию: [**креатефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).

### <a name="file-io-functions-changed-by-txf"></a>Функции файлового ввода-вывода, измененные системой TxF

В следующей таблице перечислены функции, поведение которых зависит от транзакционной NTFS. Например, поведение функции [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) будет зависеть от того, был ли параметр *HFile* создан функцией [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) или функцией [**креатефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) .



| Функция                                                                                                                                                                                                                                                                                                                                                                                                                                             | Описание                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CloseHandle"></span><span id="closehandle"></span><span id="CLOSEHANDLE"></span>[**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/>                                                                                                                                                                                                                                                                                                             | Приложения должны закрывать все дескрипторы, привязанные к транзакции, до фиксации транзакции. Приложение должно закрыть обработчик транзакций, Открытый с помощью **\_ флага file \_ DELETE, \_ в \_ Close** перед фиксацией транзакции, чтобы операция удаления была выполнена.<br/>                                                                                                                                     |
| <span id="CreateFileMapping"></span><span id="createfilemapping"></span><span id="CREATEFILEMAPPING"></span>[**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                 | Если существует транзакция, связанная с *hFile*, то объект сопоставления файлов, создаваемый этой функцией, будет связан с той же транзакцией. Изменения, вносимые в представления этого объекта сопоставления файлов, являются транзакционными. Приложения должны вызвать [**флушвиевоффиле**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), отменить сопоставление всех представлений и закрыть все дескрипторы объекта сопоставления файлов перед фиксацией изменений в транзакциях.<br/> |
| <span id="FindNextFile"></span><span id="findnextfile"></span><span id="FINDNEXTFILE"></span>[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)<br/>                                                                                                                                                                                                                                                                                                         | Если имеется транзакция, привязанная к обработчику перечисления файлов, то возвращаемые файлы подвергаются правилам изоляции транзакций.<br/>                                                                                                                                                                                                                                                                    |
| <span id="FSCTL_SET_COMPRESSION"></span><span id="fsctl_set_compression"></span>[**ФСКТЛ \_ Установка \_ сжатия**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                                                                                                                                                                                                                                                                                                  | Нельзя изменить состояние сжатия файла, открытого с помощью [**креатефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).<br/>                                                                                                                                                                                                                                                                                               |
| <span id="GetFileInformationByHandle__________and__________GetFileInformationByHandleEx"></span><span id="getfileinformationbyhandle__________and__________getfileinformationbyhandleex"></span><span id="GETFILEINFORMATIONBYHANDLE__________AND__________GETFILEINFORMATIONBYHANDLEEX"></span>[**Жетфилеинформатионбихандле**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) и [ **жетфилеинформатионбихандликс**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)<br/> | При наличии транзакции, привязанной к этому файлу, функция возвращает сведения для изолированного представления файлов.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetFileSize_and__________GetFileSizeEx"></span><span id="getfilesize_and__________getfilesizeex"></span><span id="GETFILESIZE_AND__________GETFILESIZEEX"></span>[**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) и [ **жетфилесизикс**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesizeex)<br/>                                                                                                                                                                                  | При наличии транзакции, привязанной к этому файлу, функция возвращает сведения для изолированного представления файлов.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetVolumeInformation"></span><span id="getvolumeinformation"></span><span id="GETVOLUMEINFORMATION"></span>[**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                                                                                                                                                                                                                 | Если том поддерживает транзакции файловой системы, функция возвращает файл, **\_ поддерживающий \_ транзакции** в *лпфилесистемфлагс*.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="MapViewOfFile_and__________MapViewOfFileEx"></span><span id="mapviewoffile_and__________mapviewoffileex"></span><span id="MAPVIEWOFFILE_AND__________MAPVIEWOFFILEEX"></span>[**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) и [ **MapViewOfFileEx**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex)<br/>                                                                                                                                                                | Если существует транзакция, связанная с этим маркером файла, который используется для создания сопоставляемого объекта сопоставления файлов, то связанное представление будет транзакционным. Если представление используется для внесения транзакционных изменений в файл, пользователь должен вызвать [**флушвиевоффиле**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), закрыть объект сопоставления файлов и закрыть этот файл перед фиксацией связанной транзакции.<br/>              |
| <span id="ReadDirectoryChangesW"></span><span id="readdirectorychangesw"></span><span id="READDIRECTORYCHANGESW"></span>[**реаддиректоричанжесв**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>                                                                                                                                                                                                                                                            | При наличии транзакции, привязанной к обработчику каталога, уведомления отправляют изолированное представление каталога. Изменения, вносимые в файлы за пределами транзакционного представления каталога, не включаются в уведомления.<br/>                                                                                                                                                                                |
| <span id="ReadFile___________ReadFileEx__and__________ReadFileScatter"></span><span id="readfile___________readfileex__and__________readfilescatter"></span><span id="READFILE___________READFILEEX__AND__________READFILESCATTER"></span>[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**реадфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)и [**реадфилескаттер**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter)<br/>                                                                                  | При наличии транзакции, привязанной к этому файлу, функция возвращает данные из транзакционного представления файла. Транзакционный маркер чтения гарантирует отображение того же представления файла в течение срока действия маркера.<br/>                                                                                                                                                                                 |
| <span id="SetEndOfFile"></span><span id="setendoffile"></span><span id="SETENDOFFILE"></span>[**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                                                                                                                                                                                                                                                                                                         | Если к этому маркеру привязана транзакция, то изменение в положении конца файла будет транзакционным.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="SetFileInformationByHandle"></span><span id="setfileinformationbyhandle"></span><span id="SETFILEINFORMATIONBYHANDLE"></span>[**сетфилеинформатионбихандле**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)<br/>                                                                                                                                                                                                                                   | При наличии транзакции, привязанной к этому маркеру, внесенные изменения будут транзакционными для классов сведений **филебасиЦинфо**, **филеренамеинфо**, **филеаллокатионинфо**, **филиндоффилеинфо** и **филедиспоситионинфо**.<br/>                                                                                                                                                                          |
| <span id="SetFileShortName"></span><span id="setfileshortname"></span><span id="SETFILESHORTNAME"></span>[**сетфилешортнаме**](/windows/desktop/api/WinBase/nf-winbase-setfileshortnamea)<br/>                                                                                                                                                                                                                                                                                     | При наличии транзакции, привязанной к этому маркеру, изменение краткого имени файла будет транзакционным.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="SetFileTime"></span><span id="setfiletime"></span><span id="SETFILETIME"></span>[**сетфилетиме**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)<br/>                                                                                                                                                                                                                                                                                                             | При наличии транзакции, привязанной к этому маркеру, изменение времени файла будет транзакционным.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="WriteFile__________WriteFileEx__and_________WriteFileGather"></span><span id="writefile__________writefileex__and_________writefilegather"></span><span id="WRITEFILE__________WRITEFILEEX__AND_________WRITEFILEGATHER"></span>[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), [**вритефиликс**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)и [**вритефилегасер**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)<br/>                                                                              | Если существует транзакция, привязанная к этому файлу, запись файла будет транзакционной.<br/>                                                                                                                                                                                                                                                                                                                          |



 

 

