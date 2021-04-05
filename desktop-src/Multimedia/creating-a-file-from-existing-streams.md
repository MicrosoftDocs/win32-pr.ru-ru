---
title: Создание файла из существующих потоков
description: Создание файла из существующих потоков
ms.assetid: 5149a766-7809-42b7-8e5c-b67b847b9218
keywords:
- Функция Ависаве
- Функция Ависавев
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc422d2170ccd49b8a9746666db7ebbcd7dff14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986397"
---
# <a name="creating-a-file-from-existing-streams"></a><span data-ttu-id="0bbbf-105">Создание файла из существующих потоков</span><span class="sxs-lookup"><span data-stu-id="0bbbf-105">Creating a File from Existing Streams</span></span>

<span data-ttu-id="0bbbf-106">Один из способов создания файла, содержащего потоки данных, заключается в объединении существующих потоков в новый файл.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-106">One way to create a file that contains data streams is to combine existing streams into a new file.</span></span> <span data-ttu-id="0bbbf-107">Потоки, предоставляющие данные для нового файла, могут находиться в памяти или в одном или нескольких файлах.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-107">The streams that provide data for the new file can reside in memory or in one or more files.</span></span>

<span data-ttu-id="0bbbf-108">Вы можете создать файл из нескольких потоков с помощью функции [**ависаве**](/windows/desktop/api/Vfw/nf-vfw-avisavea) .</span><span class="sxs-lookup"><span data-stu-id="0bbbf-108">You can build a file from several streams by using the [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) function.</span></span> <span data-ttu-id="0bbbf-109">Эта функция создает файл и записывает потоки данных, указанные в его вызывающей последовательности, в файл.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-109">This function creates a file and writes the data streams specified in its calling sequence to the file.</span></span> <span data-ttu-id="0bbbf-110">Вызывающая последовательность для **ависаве** использует переменное число аргументов, которые включают в себя интерфейсы для потоков, Объединенных в новый файл.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-110">The calling sequence for **AVISave** uses a variable number of arguments that include interfaces for the streams combined in the new file.</span></span>

<span data-ttu-id="0bbbf-111">Кроме того, потоки данных можно объединять в новый файл с помощью функции [**ависавев**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) .</span><span class="sxs-lookup"><span data-stu-id="0bbbf-111">You can also combine data streams in a new file by using the [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) function.</span></span> <span data-ttu-id="0bbbf-112">Эта функция предоставляет те же функциональные возможности, что и **ависаве**, но при использовании **ависавев** приложение указывает потоки данных в виде массива, а не переменное число аргументов.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-112">This function provides the same functionality as **AVISave**, but when you use **AVISaveV**, your application specifies the data streams as an array, not as a variable number of arguments.</span></span>

<span data-ttu-id="0bbbf-113">Можно создать диалоговое окно, в котором пользователь может выбрать параметры сжатия для нового файла с помощью функции [**ависавеоптионс**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) .</span><span class="sxs-lookup"><span data-stu-id="0bbbf-113">You can create a dialog box in which the user can select compression settings for the new file by using the [**AVISaveOptions**](/windows/desktop/api/Vfw/nf-vfw-avisaveoptions) function.</span></span> <span data-ttu-id="0bbbf-114">Диалоговое окно отображает текущие параметры сжатия и позволяет пользователю изменять их.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-114">The dialog box displays the current compression settings and lets the user edit them.</span></span> <span data-ttu-id="0bbbf-115">Изменения параметров сжатия хранятся в структуре [**авикомпрессоптионс**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) .</span><span class="sxs-lookup"><span data-stu-id="0bbbf-115">Compression setting changes are stored in an [**AVICOMPRESSOPTIONS**](/windows/desktop/api/Vfw/ns-vfw-avicompressoptions) structure.</span></span>

<span data-ttu-id="0bbbf-116">Можно также включить функцию обратного вызова с [**ависаве**](/windows/desktop/api/Vfw/nf-vfw-avisavea) и [**ависавев**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) , которую приложение может использовать для просмотра хода выполнения записи файла и при необходимости позволить пользователю отменить операцию сохранения.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-116">You can also include a callback function with [**AVISave**](/windows/desktop/api/Vfw/nf-vfw-avisavea) and [**AVISaveV**](/windows/desktop/api/Vfw/nf-vfw-avisaveva) that your application can use to display the progress of writing the file and, if needed, let the user cancel the save operation.</span></span> <span data-ttu-id="0bbbf-117">Можно включить адрес функции обратного вызова в вызывающей последовательности **ависаве** или **ависавев**.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-117">You can include the address of the callback function in the calling sequence of **AVISave** or **AVISaveV**.</span></span>

<span data-ttu-id="0bbbf-118">Можно позволить пользователю выбрать имя файла для нового файла с помощью функции [**жетсавефиленамепревиев**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) .</span><span class="sxs-lookup"><span data-stu-id="0bbbf-118">You can let the user select a filename for the new file by using the [**GetSaveFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) function.</span></span> <span data-ttu-id="0bbbf-119">Эта функция отображает диалоговое окно Сохранить как, в котором пользователь может просматривать первый поток (обычно это видеопоток) AVI-файла.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-119">This function displays the Save As dialog box in which the user can preview the first stream (normally the video stream) of an AVI file.</span></span>

<span data-ttu-id="0bbbf-120">Можно создать указатель на файловый интерфейс (и виртуальный файл) для группы потоков с помощью функции [**авимакефилефромстреамс**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) .</span><span class="sxs-lookup"><span data-stu-id="0bbbf-120">You can create a file interface pointer (and a virtual file) for a group of streams by using the [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) function.</span></span> <span data-ttu-id="0bbbf-121">Другие функции Авифиле могут использовать указатель на файловый интерфейс, возвращаемый этой функцией, для доступа к потокам в виртуальном файле.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-121">Other AVIFile functions can use the file interface pointer returned by this function to access the streams in the virtual file.</span></span> <span data-ttu-id="0bbbf-122">После завершения использования виртуального файла удалите указатель на файловый интерфейс с помощью функции [**авифилерелеасе**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) .</span><span class="sxs-lookup"><span data-stu-id="0bbbf-122">After you finish using the virtual file, delete the file interface pointer by using the [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) function.</span></span>

> [!Note]  
> <span data-ttu-id="0bbbf-123">Чтобы уменьшить качество изображения и звука, старайтесь не сжимать файл AVI более одного раза.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-123">To minimize image and audio degradation, avoid compressing an AVI file more than once.</span></span> <span data-ttu-id="0bbbf-124">Объедините несжатые фрагменты видео в систему редактирования, а затем выполните сжатие окончательного продукта.</span><span class="sxs-lookup"><span data-stu-id="0bbbf-124">Combine uncompressed pieces of video in your editing system and then compress the final product.</span></span> <span data-ttu-id="0bbbf-125">Дополнительные сведения о параметрах сжатия см. в разделе [Диспетчер сжатия видео](video-compression-manager.md).</span><span class="sxs-lookup"><span data-stu-id="0bbbf-125">For information about compression options, see [Video Compression Manager](video-compression-manager.md).</span></span>

 

 

 




