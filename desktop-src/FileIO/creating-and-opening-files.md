---
description: Рекомендации по созданию или открытию файла с помощью функции CreateFile.
ms.assetid: 094cac29-c66d-409e-8928-878dc693d393
title: Создание и открытие файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1430675862b10f9e9221d968242481525dc7632f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664286"
---
# <a name="creating-and-opening-files"></a>Создание и открытие файлов

Функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) может создать новый файл или открыть существующий файл. Необходимо указать имя файла, инструкции по созданию и другие атрибуты. Когда приложение создает новый файл, операционная система добавляет его в указанный каталог.

Операционная система назначает уникальный идентификатор, называемый *маркером*, каждому файлу, который открывается или создается с помощью [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Приложение может использовать этот обработчик с функциями, считывающими из, записывающими и описывающими файл. Он действителен до тех пор, пока не будут закрыты все ссылки на этот обработчик. При запуске приложение наследует все открытые дескрипторы от процесса, запустившего его, если дескрипторы были созданы как наследуемые.

Приложение должно проверить значение маркера, возвращенного [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , прежде, чем пытаться использовать этот маркер для доступа к файлу. При возникновении ошибки значение обработчика будет **недопустимым \_ \_ значением Handle** , и приложение сможет использовать функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) для получения расширенных сведений об ошибке.

Когда приложение использует [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea), оно должно использовать параметр *двдесиредакцесс* , чтобы указать, будет ли он считывать из файла, записывать его в файл, как для чтения, так и для записи, или ни для того ни другого. Это называется запросом *режима доступа*. Приложение также должно использовать параметр *двкреатиондиспоситион* , чтобы указать, какое действие следует предпринять, если файл уже существует, называемый методом *обработки создания*. Например, приложение может вызвать **CreateFile** с параметром *двкреатиондиспоситион* **, чтобы всегда \_ создавать новый** файл, даже если файл с таким именем уже существует (таким образом перезаписывая существующий файл). Успешность этого или не зависит от таких факторов, как атрибуты предыдущего файла и параметры безопасности (Дополнительные сведения см. в следующих разделах).

Приложение также использует [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , чтобы указать, требуется ли совместное использование файла для чтения, записи, как, так и ни одного. Это называется *режимом общего доступа*. Открытый файл, который не является общим (*двшаремоде* ), не может быть открыт повторно в приложении, которое его открыло или другим приложением, пока его обработчик не закроется. Это также называется монопольным доступом.

Если процесс использует [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) для открытия файла, который уже был открыт в режиме общего доступа (для *двшаремоде* задано допустимое ненулевое значение), система сравнивает запрошенные режимы доступа и общего доступа с теми, которые указаны при открытии файла. Если указать режим доступа или совместного использования, который конфликтует с режимами, указанными в предыдущем вызове, то **CreateFile** завершается ошибкой.

В следующей таблице показаны допустимые сочетания двух вызовов функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) с использованием различных режимов доступа и режима общего доступа (*двдесиредакцесс*, *двшаремоде* соответственно). Не имеет значения, в каком порядке выполняются вызовы **CreateFile** . Однако все последующие операции файлового ввода-вывода для каждого из этих файлов по-прежнему будут ограничены текущими режимами доступа и совместного доступа, связанными с этим конкретным маркером файла.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Первый вызов <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a></th>
<th>Допустимые вторые вызовы <a href="/windows/desktop/api/FileAPI/nf-fileapi-createfilea"> <strong>CreateFile</strong></a></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong><br/></td>
<td><ul>
<li><strong>GENERIC_READ</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
<li><strong>GENERIC_READ</strong>  |  <strong>GENERIC_WRITE</strong>, <strong>FILE_SHARE_READ</strong>  |  <strong>FILE_SHARE_WRITE</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

В дополнение к стандартным атрибутам файлов можно также указать атрибуты безопасности, включив указатель на структуру [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) в качестве четвертого параметра [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea). Однако базовая файловая система должна поддерживать безопасность для этого, чтобы иметь любой результат (например, файловая система NTFS поддерживает ее, но различные файловые системы FAT — нет). Дополнительные сведения об атрибутах безопасности см. в разделе [Access Control](/windows/desktop/SecAuthZ/access-control).

Приложение, создающее новый файл, может предоставить дополнительный обработчик для файла шаблона, от которого [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) принимает атрибуты файлов и расширенные атрибуты для создания нового файла.

## <a name="createfile-scenarios"></a>Сценарии CreateFile

Существует несколько фундаментальных сценариев для инициализации доступа к файлу с помощью функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) . Они представлены в виде:

-   Создание нового файла, если файл с таким именем еще не существует.
-   Создание нового файла, даже если файл с таким именем уже существует, очистка его данных и запуск пустой.
-   Открытие существующего файла только в том случае, если он существует и не изменяется.
-   Открытие существующего файла только в том случае, если он существует, усекает его до пустого.
-   Открытие файла всегда: как есть, если он существует, создает новый, если он не существует.

Эти сценарии управляются правильным использованием параметра *двкреатиондиспоситион* . Ниже приведена разбивка этих сценариев на значения этого параметра и то, что происходит при их использовании.

При создании или открытии нового файла, если файл с таким именем еще не существует (для *двкреатиондиспоситион* задано значение **создать \_ Новый**, **создать \_ всегда** или **открыть \_ всегда**), функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) выполняет следующие действия:

-   Объединяет атрибуты файлов и флаги, заданные параметром *двфлагсандаттрибутес* , с **\_ \_ архивом атрибута файла**.
-   Задает нулевую длину файла.
-   Копирует расширенные атрибуты, предоставленные файлом шаблона, в новый файл, если указан параметр *хтемплатефиле* (это переопределяет все флаги **File \_ Attribute \_ \** _, указанные ранее).
-   Устанавливает флаг наследования, заданный членом _ *бинхерисандле**, и дескриптор безопасности, заданный членом **лпсекуритидескриптор** параметра *лпсекуритяттрибутес* ([**Структура \_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), если он предоставлен.

При создании нового файла, даже если файл с таким именем уже существует (*двкреатиондиспоситион* настроен для **создания \_ Always**), функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) выполняет следующие действия:

-   Проверяет текущие атрибуты файлов и параметры безопасности для доступа на запись, если она запрещена.
-   Объединяет атрибуты файлов и флаги, заданные параметром *двфлагсандаттрибутес* , с **\_ \_ архивным атрибутом файла** и существующими атрибутами файла.
-   Устанавливает нулевую длину файла (т. е. все данные, которые были в файле, больше не доступны и файл пуст).
-   Копирует расширенные атрибуты, предоставленные файлом шаблона, в новый файл, если указан параметр *хтемплатефиле* (это переопределяет все флаги **File \_ Attribute \_ \** _, указанные ранее).
-   Устанавливает флаг наследования, заданный членом _ *бинхерисандле** параметра *лпсекуритяттрибутес* (структура [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), если он предоставлен, но игнорирует элемент **лпсекуритидескриптор** структуры **\_ атрибутов безопасности** .
-   Если в противном случае ничего не происходит (то есть функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) возвращает допустимый маркер), вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) приведет к тому, что **Ошибка кода \_ уже \_ существует**, хотя в данном конкретном случае это не является ошибкой (если вы хотите создать "новый" (пустой) файл вместо существующего).

При открытии существующего файла (*двкреатиондиспоситион* , установленного как **Open \_ existing**, **Open \_ Always** или **Truncate \_ existing**), функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) выполняет следующие действия:

-   Проверяет текущие атрибуты файлов и параметры безопасности для запрошенного доступа, если это запрещено.
-   Объединяет флаги файла (**\_ флаг \_ \* файла* _), заданные _dwFlagsAndAttributes * с существующими атрибутами файлов, и игнорирует все атрибуты файлов (* * \_ атрибут \_ \* файла* _), заданные параметром _dwFlagsAndAttributes *.
-   Устанавливает нулевую длину файла, только если для *двкреатиондиспоситион* задано **усечение \_ существующего**, в противном случае сохраняется текущая длина файла и файл открывается как есть.
-   Игнорирует параметр *хтемплатефиле* .
-   Устанавливает флаг наследования, заданный членом **бинхерисандле** параметра *лпсекуритяттрибутес* (структура [**\_ атрибутов безопасности**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) ), если он предоставлен, но игнорирует элемент **лпсекуритидескриптор** структуры **\_ атрибутов безопасности** .

## <a name="file-attributes-and-directories"></a>Атрибуты и каталоги файлов

Атрибуты файлов являются частью метаданных, связанных с файлом или каталогом, каждый из которых имеет собственную цель и правила, определяющие, как он может быть задан и изменен. Некоторые из этих атрибутов применяются только к файлам, а некоторые — только к каталогам. Например, атрибут **File \_ Attribute \_ Directory** применяется только к каталогам: он используется файловой системой для определения того, является ли объект на диске каталогом, но он не может быть изменен для существующего объекта файловой системы.

Некоторые атрибуты файлов могут быть заданы для каталога, но имеют значение только для файлов, созданных в этом каталоге, в качестве атрибутов по умолчанию. Например, **\_ \_ сжатый атрибут файла** может быть задан для объекта каталога, но поскольку сам объект каталога не содержит фактических данных, он не сжимается полностью. Однако каталоги, отмеченные этим атрибутом, сообщают файловой системе о необходимости сжатия новых файлов, добавленных в этот каталог. Любой атрибут файла, который может быть установлен в каталоге и будет установлен для новых файлов, добавленных в этот каталог, называется *наследуемым атрибутом*.

Функция [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) предоставляет параметр для установки определенных атрибутов файла при создании файла. Как правило, эти атрибуты наиболее распространены для использования приложением во время создания файла, но не все возможные атрибуты файлов доступны для **CreateFile**. Некоторые атрибуты файлов должны использовать другие функции, такие как [**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa), [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)или [**декриптфиле**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea) , после того как файл уже существует. В случае с **\_ \_ каталогом атрибутов файла** функция [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) необходима во время создания, так как **CreateFile** не может создавать каталоги. Другими атрибутами файлов, требующими специальной обработки, являются **\_ \_ \_ точка повторного анализа атрибутов файлов** и **\_ \_ разреженный \_ файл атрибута файла**, для которого требуется **DeviceIoControl**. Дополнительные сведения см. в разделе [**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa).

Как упоминалось ранее, наследование атрибутов файла происходит при создании файла с атрибутами файлов, считанными из атрибутов каталога, в которых будет расположен файл. В следующей таблице перечислены унаследованные атрибуты и их связь с возможностями функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .



| Состояние атрибута каталога                                      | Возможность переопределения наследования [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) для новых файлов      |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| **Файл \_ \_Сжатый набор атрибутов** .<br/>                | Нет элемента управления. Используйте [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) для очистки.<br/>    |
| **Файл \_ \_Сжатый атрибут** не задан.<br/>            | Нет элемента управления. Используйте [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) , чтобы задать.<br/>      |
| **Файл \_ \_Зашифрованный набор атрибутов** .<br/>                 | Нет элемента управления. Используйте [**декриптфиле**](/windows/desktop/api/WinBase/nf-winbase-decryptfilea).<br/>                      |
| **Файл \_ \_Зашифрованный атрибут** не задан.<br/>             | Можно задать с помощью [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).<br/>                       |
| **Файл \_ \_ \_ \_ Неиндексированный набор атрибутов Content** .<br/>     | Нет элемента управления. Используйте [**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) для очистки.<br/> |
| **Файл \_ АТРИБУТ \_ не \_ \_ индексировано содержимого** не задан.<br/> | Нет элемента управления. Используйте [**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa) для установки.<br/>   |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Управление доступом](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)
</dt> <dt>

[**Константы атрибутов файлов**](file-attribute-constants.md)
</dt> <dt>

[Сжатие и распаковка файлов](file-compression-and-decompression.md)
</dt> <dt>

[Шифрование файлов](file-encryption.md)
</dt> <dt>

[Функции управления файлами](file-management-functions.md)
</dt> <dt>

[Дескрипторы и объекты](/windows/desktop/SysInfo/handles-and-objects)
</dt> <dt>

[Наследование в обработке](/windows/desktop/SysInfo/handle-inheritance)
</dt> <dt>

[Открытие файла для чтения или записи](opening-a-file-for-reading-or-writing.md)
</dt> <dt>

[**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> </dl>

 

