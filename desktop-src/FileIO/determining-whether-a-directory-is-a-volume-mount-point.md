---
description: Определение того, является ли указанный каталог подключенной папкой.
ms.assetid: b4a2c3d7-8805-41de-b316-592e77076570
title: Определение того, является ли каталог подключенной папкой
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7492a3114ff0c9c9ce0685c6d3e2b94724457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912315"
---
# <a name="determining-whether-a-directory-is-a-mounted-folder"></a><span data-ttu-id="71ed5-103">Определение того, является ли каталог подключенной папкой</span><span class="sxs-lookup"><span data-stu-id="71ed5-103">Determining Whether a Directory Is a Mounted Folder</span></span>

<span data-ttu-id="71ed5-104">Можно определить, является ли каталог подключенной папкой, если, например, вы используете приложение резервного копирования или поиска, которое ограничено одним томом.</span><span class="sxs-lookup"><span data-stu-id="71ed5-104">It is useful to determine whether a directory is a mounted folder when, for example, you are using a backup or search application that is limited to one volume.</span></span> <span data-ttu-id="71ed5-105">Такое приложение может обращаться к сведениям на нескольких томах, если вы используете такие функции, как [**сетволумемаунтпоинт**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) , для создания подключенных папок для других томов на томе, для которого ограничено приложение.</span><span class="sxs-lookup"><span data-stu-id="71ed5-105">Such an application can reach information on multiple volumes if you use functions such as [**SetVolumeMountPoint**](/windows/desktop/api/WinBase/nf-winbase-setvolumemountpointa) to create mounted folders for the other volumes on the volume that the application is limited to.</span></span> <span data-ttu-id="71ed5-106">Дополнительные сведения см. в разделе [Создание подключенных папок](mounting-and-dismounting-a-volume.md).</span><span class="sxs-lookup"><span data-stu-id="71ed5-106">For more information, see [Creating Mounted Folders](mounting-and-dismounting-a-volume.md).</span></span>

<span data-ttu-id="71ed5-107">Чтобы определить, является ли указанный каталог подключенной папкой, сначала вызовите функцию [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) и проверьте значение флага **\_ \_ \_ точки повторного анализа атрибута файла** в возвращаемом значении, чтобы узнать, имеет ли каталог связанную точку повторного анализа.</span><span class="sxs-lookup"><span data-stu-id="71ed5-107">To determine if a specified directory is a mounted folder, first call the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) function and inspect the **FILE\_ATTRIBUTE\_REPARSE\_POINT** flag in the return value to see if the directory has an associated reparse point.</span></span> <span data-ttu-id="71ed5-108">Если это так, используйте функции [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) и [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) , чтобы получить тег повторного анализа в элементе **dwReserved0** структуры [**\_ \_ данных Win32 Find**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="71ed5-108">If it does, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) and [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) functions to obtain the reparse tag in the **dwReserved0** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="71ed5-109">Чтобы определить, является ли точка повторной обработки подключенной папкой (а не какой-либо другой формой точки повторного анализа), проверьте, совпадает ли значение тега **с \_ \_ \_ \_ точкой подключения к тегу повторного анализа значения IO**.</span><span class="sxs-lookup"><span data-stu-id="71ed5-109">To determine if the reparse point is a mounted folder (and not some other form of reparse point), test whether the tag value equals the value **IO\_REPARSE\_TAG\_MOUNT\_POINT**.</span></span> <span data-ttu-id="71ed5-110">Дополнительные сведения см. в разделе [точки повторного анализа](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="71ed5-110">For more information, see [Reparse Points](reparse-points.md).</span></span>

<span data-ttu-id="71ed5-111">Чтобы получить целевой том подключенной папки, используйте функцию [**жетволуменамефорволумемаунтпоинт**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) .</span><span class="sxs-lookup"><span data-stu-id="71ed5-111">To obtain the target volume of a mounted folder, use the [**GetVolumeNameForVolumeMountPoint**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumenameforvolumemountpointw) function.</span></span>

<span data-ttu-id="71ed5-112">Аналогичным образом можно определить, является ли точка повторной обработки символьной ссылкой, проверяя, является оно **ТЕГОМ повторного анализа ввода-вывода с помощью \_ \_ тега \_ символьную ссылку**.</span><span class="sxs-lookup"><span data-stu-id="71ed5-112">In a similar manner, you can determine if a reparse point is a symbolic link by testing whether the tag value is **IO\_REPARSE\_TAG\_SYMLINK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71ed5-113">См. также</span><span class="sxs-lookup"><span data-stu-id="71ed5-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71ed5-114">**Константы атрибутов файлов**</span><span class="sxs-lookup"><span data-stu-id="71ed5-114">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 



