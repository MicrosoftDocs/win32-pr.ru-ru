---
description: Рекомендации по перемещению и замене файлов с помощью функций Копифиликс, CreateFile, Реплацефиле и Мовефиликс.
ms.assetid: 4872af0d-42e8-4576-9aa9-4b8671375f2e
title: Перемещение и замена файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d7f08d2bd8d07645076620e839d7d12f5969502
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "105684800"
---
# <a name="moving-and-replacing-files"></a><span data-ttu-id="e13d1-103">Перемещение и замена файлов</span><span class="sxs-lookup"><span data-stu-id="e13d1-103">Moving and Replacing Files</span></span>

<span data-ttu-id="e13d1-104">Прежде чем можно будет выполнить операцию копирования, исходный файл должен быть закрыт или открыт только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e13d1-104">Before a copy operation can be performed, the source file must be closed or opened only for reading.</span></span> <span data-ttu-id="e13d1-105">Ни один поток не может иметь исходный файл, Открытый для записи.</span><span class="sxs-lookup"><span data-stu-id="e13d1-105">No thread can have the the source file opened for writing.</span></span> <span data-ttu-id="e13d1-106">Чтобы скопировать существующий файл в новый, используйте функцию [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) или [**копифиликс**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) .</span><span class="sxs-lookup"><span data-stu-id="e13d1-106">To copy an existing file to a new one, use the [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile) or [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function.</span></span> <span data-ttu-id="e13d1-107">Приложения могут указать, завершается ли ошибка **CopyFile** и **копифиликс** , если конечный файл уже существует.</span><span class="sxs-lookup"><span data-stu-id="e13d1-107">Applications can specify whether **CopyFile** and **CopyFileEx** fail if the destination file already exists.</span></span> <span data-ttu-id="e13d1-108">Если конечный файл существует и открыт, он должен быть открыт с соответствующими разрешениями на общий доступ.</span><span class="sxs-lookup"><span data-stu-id="e13d1-108">If the destination file does exist and is open, it must have been opened with applicable sharing permissions.</span></span> <span data-ttu-id="e13d1-109">Дополнительные сведения см. в разделе [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span><span class="sxs-lookup"><span data-stu-id="e13d1-109">For more information, see [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea).</span></span>

<span data-ttu-id="e13d1-110">Функция [**копифиликс**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) также позволяет приложению указать адрес функции обратного вызова (см. [**копипрогрессраутине**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)), который вызывается каждый раз при копировании другой части файла.</span><span class="sxs-lookup"><span data-stu-id="e13d1-110">The [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function also allows an application to specify the address of a callback function (see [**CopyProgressRoutine**](/windows/desktop/api/WinBase/nc-winbase-lpprogress_routine)) that is called each time another portion of the file has been copied.</span></span> <span data-ttu-id="e13d1-111">Приложение может использовать эти сведения для отображения индикатора, показывающего общее количество байтов, скопированных в процентах от общего размера файла.</span><span class="sxs-lookup"><span data-stu-id="e13d1-111">The application can use this information to display an indicator that shows the total number of bytes copied as a percent of the total file size.</span></span>

<span data-ttu-id="e13d1-112">Функция [**реплацефиле**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) заменяет один файл другим файлом с возможностью создания резервной копии исходного файла.</span><span class="sxs-lookup"><span data-stu-id="e13d1-112">The [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea) function replaces one file with another file, with the option of creating a backup copy of the original file.</span></span> <span data-ttu-id="e13d1-113">Функция сохраняет атрибуты исходного файла, например время создания, списки ACL и атрибут шифрования.</span><span class="sxs-lookup"><span data-stu-id="e13d1-113">The function preserves attributes of the original file, such as its creation time, ACLs, and encryption attribute.</span></span>

<span data-ttu-id="e13d1-114">Файл также должен быть закрыт, прежде чем приложение сможет его переместить.</span><span class="sxs-lookup"><span data-stu-id="e13d1-114">A file must also be closed before an application can move it.</span></span> <span data-ttu-id="e13d1-115">Функции [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile) и [**мовефиликс**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) копируют существующий файл в новое расположение и удаляют оригинал.</span><span class="sxs-lookup"><span data-stu-id="e13d1-115">The [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile) and [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) functions copy an existing file to a new location and deletes the original.</span></span>

<span data-ttu-id="e13d1-116">Функция [**мовефиликс**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) также позволяет приложению указать способ перемещения файла.</span><span class="sxs-lookup"><span data-stu-id="e13d1-116">The [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa) function also allows an application to specify how to move the file.</span></span> <span data-ttu-id="e13d1-117">Функция может заменить существующий файл, переместить файл по томам и отложить перемещение файла до перезапуска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="e13d1-117">The function can replace an existing file, move a file across volumes, and delay moving the file until the operating system is restarted.</span></span>

 

 



