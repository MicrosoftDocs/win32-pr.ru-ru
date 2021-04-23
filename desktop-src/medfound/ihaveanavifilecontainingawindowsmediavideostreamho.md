---
description: У меня есть файл AVI, содержащий поток видео Windows Media.
ms.assetid: 0b4c5bf2-caa6-4e14-be5f-9e25ec918cf0
title: У меня есть файл AVI, содержащий поток видео Windows Media. Как преобразовать его в WMV-файл?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c770a8355e92c6cfe052d86a17c6638a7a9948
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105703429"
---
# <a name="i-have-an-avi-file-containing-a-windows-media-video-stream-how-can-i-convert-it-to-a-wmv-file"></a><span data-ttu-id="7f952-104">У меня есть файл AVI, содержащий поток видео Windows Media.</span><span class="sxs-lookup"><span data-stu-id="7f952-104">I have an AVI file containing a Windows Media Video stream.</span></span> <span data-ttu-id="7f952-105">Как преобразовать его в WMV-файл?</span><span class="sxs-lookup"><span data-stu-id="7f952-105">How can I convert it to a WMV file?</span></span>

<span data-ttu-id="7f952-106">Интерфейсы кодеков аудио и видео Windows Media не предоставляют методы для создания файлов с использованием формата ASF, который используется для файлов WMV.</span><span class="sxs-lookup"><span data-stu-id="7f952-106">The Windows Media Audio and Video codec interfaces do not provide methods to create files using the Advanced Systems Format (ASF), which is the format used for WMV files.</span></span> <span data-ttu-id="7f952-107">Если требуется преобразовать файл (с помощью любого контейнера) в файл ASF, необходимо использовать объекты пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="7f952-107">If you want to convert a file (using any container) to an ASF file, you must use the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="7f952-108">Получите сжатые образцы Windows Media из исходного файла и передайте их в объект модуля записи в виде потоковых примеров.</span><span class="sxs-lookup"><span data-stu-id="7f952-108">Retrieve the compressed Windows Media samples from the source file and pass them to the writer object as stream samples.</span></span> <span data-ttu-id="7f952-109">Дополнительные сведения см. в документации по пакету SDK серии Windows Media Format 9.</span><span class="sxs-lookup"><span data-stu-id="7f952-109">For more information, see the Windows Media Format 9 Series SDK documentation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f952-110">См. также</span><span class="sxs-lookup"><span data-stu-id="7f952-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f952-111">Часто задаваемые вопросы</span><span class="sxs-lookup"><span data-stu-id="7f952-111">Frequently Asked Questions</span></span>](frequentlyaskedquestions.md)
</dt> </dl>

 

 



