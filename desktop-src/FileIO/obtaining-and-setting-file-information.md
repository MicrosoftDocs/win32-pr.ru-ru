---
description: Функции, используемые для получения и задания сведений о файле.
ms.assetid: 3b5fb709-c699-4651-8072-97210c8cf763
title: Получение и установка сведений о файле
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c6eb6abf2554e1945e0782c667245ea0eaa99be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913531"
---
# <a name="obtaining-and-setting-file-information"></a><span data-ttu-id="74d66-103">Получение и установка сведений о файле</span><span class="sxs-lookup"><span data-stu-id="74d66-103">Obtaining and Setting File Information</span></span>

<span data-ttu-id="74d66-104">В следующих разделах описывается, как получить и задать сведения о файле.</span><span class="sxs-lookup"><span data-stu-id="74d66-104">The following topics describe how to get and set file information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="74d66-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="74d66-105">In this section</span></span>



| <span data-ttu-id="74d66-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="74d66-106">Topic</span></span>                                                                                                             | <span data-ttu-id="74d66-107">Описание</span><span class="sxs-lookup"><span data-stu-id="74d66-107">Description</span></span>                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="74d66-108">Получение сведений о типе файла</span><span class="sxs-lookup"><span data-stu-id="74d66-108">Retrieving File Type Information</span></span>](retrieving-file-type-information.md)<br/>                               | <span data-ttu-id="74d66-109">Функция [**жетфилетипе**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) Извлекает тип файла: диск, символ (например, консоль), Pipe или Unknown.</span><span class="sxs-lookup"><span data-stu-id="74d66-109">The [**GetFileType**](/windows/desktop/api/FileAPI/nf-fileapi-getfiletype) function retrieves the type of a file: disk, character (such as a console), pipe, or unknown.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="74d66-110">Определение размера файла</span><span class="sxs-lookup"><span data-stu-id="74d66-110">Determining the Size of a File</span></span>](determining-the-size-of-a-file.md)<br/>                                   | <span data-ttu-id="74d66-111">Функция [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) получает размер файла.</span><span class="sxs-lookup"><span data-stu-id="74d66-111">The [**GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) function retrieves the size of a file.</span></span><br/>                                                                                                                                                                                                      |
| [<span data-ttu-id="74d66-112">Поиск одного или нескольких файлов</span><span class="sxs-lookup"><span data-stu-id="74d66-112">Searching for One or More Files</span></span>](searching-for-one-or-more-files.md)<br/>                                 | <span data-ttu-id="74d66-113">Приложение может искать в текущем каталоге все имена файлов, соответствующие заданному шаблону, с помощью функций [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)и [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="74d66-113">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span><br/> |
| [<span data-ttu-id="74d66-114">Установка и получение метки времени файла</span><span class="sxs-lookup"><span data-stu-id="74d66-114">Setting and Getting the Timestamp of a File</span></span>](setting-and-getting-the-timestamp-of-a-file.md)<br/>         | <span data-ttu-id="74d66-115">Приложения могут извлекать и задавать дату и время создания файла, последнего изменения или последнего доступа с помощью функций [**функции getFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) и [**сетфилетиме**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) .</span><span class="sxs-lookup"><span data-stu-id="74d66-115">Applications can retrieve and set the date and time a file is created, last modified, or last accessed by using the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) and [**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime) functions.</span></span><br/>                                                                         |
| [<span data-ttu-id="74d66-116">Определение кодовой страницы текущей кодировки</span><span class="sxs-lookup"><span data-stu-id="74d66-116">Determining the Current Character Set Code Page</span></span>](determining-the-current-character-set-code-page.md)<br/> | <span data-ttu-id="74d66-117">Функция [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) определяет, использует ли функция файлового ввода-вывода кодовую страницу кодировки ANSI или OEM.</span><span class="sxs-lookup"><span data-stu-id="74d66-117">The [**AreFileApisANSI**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) function determines whether the file I/O functions are using the ANSI or OEM character set code page.</span></span><br/>                                                                                                                               |



 

 

