---
description: Как символьные ссылки влияют на стандартные функции файлов, использующие имена путей для указания одного или нескольких файлов.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Символьные эффекты ссылок в функциях файловых систем
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1c5d140dc70de8ebc255b779b226b6da156aa2b8961c49d86f466ac01b26ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078463"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a>Символьные эффекты ссылок в функциях файловых систем

Несколько стандартных файловых функций, использующих имена путей для указания одного или нескольких файлов, зависят от использования символических ссылок. В этом разделе перечислены эти функции и описаны изменения в поведении.

-   [CopyFile и Копифилетрансактед](#copyfile-and-copyfiletransacted)
-   [копифиликс](#copyfileex)
-   [CreateFile и Креатефилетрансактед](#createfile-and-createfiletransacted)
-   [Креатехардлинк и Креатехардлинктрансактед](#createhardlink-and-createhardlinktransacted)
-   [DeleteFile и Делетефилетрансактед](#deletefile-and-deletefiletransacted)
-   [финдфирстчанженотификатион](#findfirstchangenotification)
-   [FindFirstFile и Финдфирстфилетрансактед](#findfirstfile-and-findfirstfiletransacted)
-   [финдфирстфиликс](#findfirstfileex)
-   [FindNextFile](#findnextfile)
-   [жетбинаритипе](#getbinarytype)
-   [Жеткомпресседфилесизе и Жеткомпресседфилесизетрансактед](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [жетдискфриспаце](#getdiskfreespaceex)
-   [жетдискфриспацеекс](#getdiskfreespaceex)
-   [GetFileAttributes](#getfileattributesex)
-   [Сбой getfileattributesex](#getfileattributesex)
-   [жетфилесекурити](#getfilesecurity)
-   [жеттемппас](#gettemppath)
-   [жетволумеинформатион](#getvolumeinformation)
-   [сетфилеаттрибутес](#setfileattributes)
-   [сетфилесекурити](#setfilesecurity)
-   [Связанные темы](#related-topics)

В приведенных ниже описаниях используются следующие термины.

-   Исходный файл — исходный копируемый файл.
-   Целевой файл — созданная копия файла.
-   Target — сущность, на которую указывает символьная ссылка.

> [!Note]  
> Поведение функций, которые принимают маркер, созданный с помощью функции [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , например функции [**функции getFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , будет различаться в зависимости от того, была ли вызвана функция **CreateFile** с помощью флага **файла \_ флаг \_ открытия \_ \_ точки** повторной обработки. Дополнительные сведения см. в разделах [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) и следующие разделы [CreateFile и креатефилетрансактед](#createfile-and-createfiletransacted) .

 

## <a name="copyfile-and-copyfiletransacted"></a>CopyFile и Копифилетрансактед

Если исходный файл является символьной ссылкой, то фактически скопированный файл является целевым объектом символьной ссылки.

Если конечный файл уже существует и является символьной ссылкой, то символьная ссылка перезаписывается исходным файлом.

## <a name="copyfileex"></a>копифиликс

Если задано копирование **\_ файла Copy \_ \_ символьную ссылку** и:

-   Если исходный файл является символьной ссылкой, копируется символьная ссылка, а не целевой файл.
-   Если исходный файл не является символьной ссылкой, поведение не изменяется.
-   Если целевой файл является существующей символьной ссылкой, то символьная ссылка перезаписывается, а не на целевой файл.
-   Если также указан параметр exist (если **\_ \_ \_ \_ существует** ) и файл назначения является существующей символьной ссылкой, то операция завершается ошибкой во всех случаях.

Если **копия \_ файла \_ Copy \_ символьную ссылку** не указана и:

-   Если также задан параметр **\_ \_ \_ \_ Exists** if, а файл назначения является существующей символьной ссылкой, операция завершается ошибкой, только если существует целевой объект символьной ссылки.
-   Если не задано значение **\_ \_ \_ \_ Exists** , то поведение при копировании файла не изменяется.

**Windows Server 2003 и Windows XP:** Флаг **\_ копирования файла \_ Copy \_ символьную ссылку** не поддерживается. Если исходный файл является символьной ссылкой, то фактически скопированный файл является целевым объектом символьной ссылки.

## <a name="createfile-and-createfiletransacted"></a>CreateFile и Креатефилетрансактед

Если вызов этой функции создает новый файл, поведение не изменяется.

Если указан параметр **\_ \_ открыть \_ \_ точку** повторного анализа, используется значение, и:

-   Если существующий файл открыт и является символьной ссылкой, возвращаемый маркер является маркером для символьной ссылки.
-   Если задан параметр **создать \_ всегда**, **усекать \_ существующий** или **\_ удалить флаг \_ файла \_ при \_ закрытии** , то затронутый файл является символьной ссылкой.

Если не задана **\_ \_ открытая \_ \_ точка** повторного анализа, если не указан флаг файла и:

-   Если существующий файл открыт и является символьной ссылкой, возвращаемый маркер является обработкой целевого объекта.
-   Если задан параметр **создать \_ всегда**, **усекать \_ существующий** или **\_ удалить флаг \_ файла \_ при \_ закрытии** , то затронутый файл является целевым объектом.

## <a name="createhardlink-and-createhardlinktransacted"></a>Креатехардлинк и Креатехардлинктрансактед

Если путь указывает на символьную ссылку, функция создает жесткую связь с целевым объектом.

## <a name="deletefile-and-deletefiletransacted"></a>DeleteFile и Делетефилетрансактед

Если путь указывает на символьную ссылку, то символьная ссылка удаляется, а не на целевой объект. Чтобы удалить целевой объект, необходимо вызвать [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) и указать параметр **\_ удалить флаг \_ файла \_ при \_ закрытии**.

## <a name="findfirstchangenotification"></a>финдфирстчанженотификатион

Если путь указывает на символьную ссылку, для целевого объекта создается маркер уведомления. Если приложение зарегистрировано для получения уведомлений об изменениях каталога, содержащего символьные ссылки, приложение уведомляется только при изменении символьных ссылок, а не на целевых файлах.

## <a name="findfirstfile-and-findfirstfiletransacted"></a>FindFirstFile и Финдфирстфилетрансактед

Если путь указывает на символьную ссылку, буфер [**Win32 \_ Find \_**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) содержит сведения о символьной ссылке, а не целевом объекте.

## <a name="findfirstfileex"></a>финдфирстфиликс

Если путь указывает на символьную ссылку, буфер [**Win32 \_ Find \_**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) содержит сведения о символьной ссылке, а не целевом объекте.

## <a name="findnextfile"></a>FindNextFile

Если путь указывает на символьную ссылку, буфер [**Win32 \_ Find \_**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) содержит сведения о символьной ссылке, а не целевом объекте.

## <a name="getbinarytype"></a>жетбинаритипе

Если путь указывает на символьную ссылку, используется целевой файл.

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a>Жеткомпресседфилесизе и Жеткомпресседфилесизетрансактед

Если путь указывает на символьную ссылку, функция возвращает размер файла целевого объекта.

## <a name="getdiskfreespace"></a>жетдискфриспаце

Если путь указывает на символьную ссылку, операция выполняется на целевом объекте.

## <a name="getdiskfreespaceex"></a>жетдискфриспацеекс

Если путь указывает на символьную ссылку, операция выполняется на целевом объекте.

## <a name="getfileattributes"></a>GetFileAttributes

Если путь указывает на символьную ссылку, функция возвращает атрибуты для символьной ссылки.

## <a name="getfileattributesex"></a>Сбой getfileattributesex

Если путь указывает на символьную ссылку, функция возвращает атрибуты для символьной ссылки.

## <a name="getfilesecurity"></a>жетфилесекурити

Если путь указывает на символьную ссылку, функция возвращает атрибуты для символьной ссылки.

## <a name="gettemppath"></a>жеттемппас

Если путь указывает на символьную ссылку, то имя временного пути поддерживает все символьные ссылки.

## <a name="getvolumeinformation"></a>жетволумеинформатион

Если путь указывает на символьную ссылку, функция возвращает сведения о томе для целевого объекта.

## <a name="setfileattributes"></a>сетфилеаттрибутес

Если путь указывает на символьную ссылку, функция получает атрибуты для символьной ссылки.

## <a name="setfilesecurity"></a>сетфилесекурити

Если путь указывает на символьную ссылку, функция возвращает атрибуты для символьной ссылки.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[**копифилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[**копифиликс**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**креатефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**креатехардлинк**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[**креатехардлинктрансактед**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[**делетефилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[**финдфирстчанженотификатион**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[**финдфирстфилетрансактед**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[**жетбинаритипе**](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[**жеткомпресседфилесизе**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[**жеткомпресседфилесизетрансактед**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[**жетдискфриспаце**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[**жетдискфриспацеекс**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**Сбой getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**жетфилесекурити**](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**жеттемппас**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[**жетволумеинформатион**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[**сетфилеаттрибутес**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**сетфилесекурити**](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
