---
description: Приложение может искать в текущем каталоге все имена файлов, соответствующие заданному шаблону, с помощью функций FindFirstFile, Финдфирстфиликс, FindNextFile и Финдклосе.
ms.assetid: 7edd6c6e-7e8a-415c-866b-2283e5596a62
title: Поиск одного или нескольких файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3c5825b418221b1af429c6c0a731446d627701c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682916"
---
# <a name="searching-for-one-or-more-files"></a><span data-ttu-id="243a5-103">Поиск одного или нескольких файлов</span><span class="sxs-lookup"><span data-stu-id="243a5-103">Searching for One or More Files</span></span>

<span data-ttu-id="243a5-104">Приложение может искать в текущем каталоге все имена файлов, соответствующие заданному шаблону, с помощью функций [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)и [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) .</span><span class="sxs-lookup"><span data-stu-id="243a5-104">An application can search the current directory for all file names that match a given pattern by using the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea), [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa), [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea), and [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) functions.</span></span> <span data-ttu-id="243a5-105">Шаблон должен быть допустимым именем файла и может содержать подстановочные знаки.</span><span class="sxs-lookup"><span data-stu-id="243a5-105">The pattern must be a valid file name and can include wildcard characters.</span></span>

<span data-ttu-id="243a5-106">Функции [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) и [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) создают дескрипторы, которые **финдфирстфиликс** использует для поиска других файлов с тем же шаблоном.</span><span class="sxs-lookup"><span data-stu-id="243a5-106">The [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) functions create handles that **FindFirstFileEx** uses to search for other files with the same pattern.</span></span> <span data-ttu-id="243a5-107">Все функции возвращают сведения о найденном файле.</span><span class="sxs-lookup"><span data-stu-id="243a5-107">All functions return information about the file that was found.</span></span> <span data-ttu-id="243a5-108">Эти сведения включают имя файла, его размер, атрибуты и время.</span><span class="sxs-lookup"><span data-stu-id="243a5-108">This information includes the file name, size, attributes, and time.</span></span>

<span data-ttu-id="243a5-109">Функция [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) также позволяет приложению искать файлы на основе дополнительных условий поиска.</span><span class="sxs-lookup"><span data-stu-id="243a5-109">The [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa) function also allows an application to search for files based on additional search criteria.</span></span> <span data-ttu-id="243a5-110">Функция может ограничить поиск именами устройств или каталогов.</span><span class="sxs-lookup"><span data-stu-id="243a5-110">The function can limit searches to device names or directory names.</span></span>

<span data-ttu-id="243a5-111">Функция [**финдклосе**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) уничтожает дескрипторы, созданные с помощью [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) и [**финдфирстфиликс**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span><span class="sxs-lookup"><span data-stu-id="243a5-111">The [**FindClose**](/windows/desktop/api/FileAPI/nf-fileapi-findclose) function destroys handles created by [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa).</span></span>

<span data-ttu-id="243a5-112">Приложение может выполнять поиск одного файла по указанному пути с помощью функции [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) .</span><span class="sxs-lookup"><span data-stu-id="243a5-112">An application can search for a single file on a specific path by using the [**SearchPath**](/windows/win32/api/processenv/nf-processenv-searchpatha) function.</span></span>

 

 
