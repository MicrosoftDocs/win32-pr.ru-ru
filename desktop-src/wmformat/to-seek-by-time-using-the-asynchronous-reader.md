---
title: Поиск по времени с помощью асинхронного модуля чтения
description: Поиск по времени с помощью асинхронного модуля чтения
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Расширенный формат систем (ASF), поиск по времени
- ASF (Расширенный системный формат), поиск по времени
- Расширенный системный формат (ASF), асинхронный читатель
- ASF (Расширенный системный формат), асинхронный читатель
- асинхронные читатели, поиск по времени
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788814"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a><span data-ttu-id="abed9-108">Поиск по времени с помощью асинхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="abed9-108">To Seek By Time Using the Asynchronous Reader</span></span>

<span data-ttu-id="abed9-109">Если вы хотите найти определенное время презентации в файле ASF, необходимо правильно настроить файл.</span><span class="sxs-lookup"><span data-stu-id="abed9-109">If you want to seek to a specific presentation time in an ASF file, the file must be properly configured.</span></span> <span data-ttu-id="abed9-110">По умолчанию можно выполнять поиск по файлам только по звуку, но перед поиском необходимо проиндексировать видеофайлы.</span><span class="sxs-lookup"><span data-stu-id="abed9-110">You can seek in audio only files by default, but video files need to be indexed before seeking.</span></span> <span data-ttu-id="abed9-111">Если вы не знаете, как создать файл, можно проверить \_ атрибут g всзвмсикабле в заголовке файла, вызвав [**ивмхеадеринфо:: жетаттрибутебинаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="abed9-111">If you are not sure about how a file has been created, you can check the g\_wszWMSeekable attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="abed9-112">Чтобы найти данные в файле ASF с помощью асинхронного модуля чтения, вызовите [**ивмреадер:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), передав требуемое время и длительность части файла, который требуется считать *кнсстарт* и *кнсдуратион* соответственно.</span><span class="sxs-lookup"><span data-stu-id="abed9-112">To seek to data in an ASF file by presentation time using the asynchronous reader, call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passing the desired time and duration of the part of the file you want to read as *cnsStart* and *cnsDuration* respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="abed9-113">См. также</span><span class="sxs-lookup"><span data-stu-id="abed9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="abed9-114">**Интерфейс Ивмреадер**</span><span class="sxs-lookup"><span data-stu-id="abed9-114">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="abed9-115">**Чтение файлов с помощью асинхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="abed9-115">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="abed9-116">**Считывание метаданных при воспроизведении**</span><span class="sxs-lookup"><span data-stu-id="abed9-116">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="abed9-117">**Работа с индексами**</span><span class="sxs-lookup"><span data-stu-id="abed9-117">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




