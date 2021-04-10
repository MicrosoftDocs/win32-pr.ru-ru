---
title: Создание файлов ASF в DirectShow (пакет SDK для формата Windows Media 11)
description: Создание файлов ASF в DirectShow
ms.assetid: 8b7af340-934d-43a9-88e9-7bbb2d3a38e0
keywords:
- Windows Media Format SDK, создание файлов ASF в DirectShow
- Пакет SDK для Windows Media Format, DirectShow
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный системный формат (ASF), создание в DirectShow
- ASF (Расширенный системный формат), создание в DirectShow
- DirectShow, создание файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbe4a6a37a508e5d7c713ae4cf38d771d075cefa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104134898"
---
# <a name="creating-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="08e5c-110">Создание файлов ASF в DirectShow (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="08e5c-110">Creating ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="08e5c-111">С помощью DirectShow можно создавать файлы ASF непосредственно из источников захвата, таких как видеокамеры или перекодировать другие файлы в формат Windows Media.</span><span class="sxs-lookup"><span data-stu-id="08e5c-111">You can use DirectShow to create ASF files directly from capture sources such as DV camcorders or to transcode other files into Windows Media Format.</span></span> <span data-ttu-id="08e5c-112">В любом сценарии приложения создают графы фильтров, в которых в качестве модуля подготовки отчетов включен фильтр [записи WM ASF](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="08e5c-112">In either scenario, applications create filter graphs that include the [WM ASF Writer](wm-asf-writer-filter.md) filter as the renderer.</span></span>

<span data-ttu-id="08e5c-113">Модуль записи WM ASF предоставляет частичную оболочку для пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="08e5c-113">The WM ASF Writer provides a partial wrapper for the Windows Media Format SDK.</span></span> <span data-ttu-id="08e5c-114">Приложения могут использовать интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) фильтра для передачи системного профиля (версии 4, 7 или 8) или напрямую использовать пакет SDK формата Windows Media для создания настраиваемого профиля для передачи в фильтр.</span><span class="sxs-lookup"><span data-stu-id="08e5c-114">Applications can use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface of the filter to pass in a system profile (versions 4, 7, or 8), or use the Windows Media Format SDK directly to create a custom profile to pass to the filter.</span></span> <span data-ttu-id="08e5c-115">Чтобы добавить метаданные и другие сведения о заголовке, приложение использует интерфейс [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) , который можно получить из фильтра.</span><span class="sxs-lookup"><span data-stu-id="08e5c-115">To add metadata and other header information, the application uses the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface, which can be obtained from the filter.</span></span> <span data-ttu-id="08e5c-116">После настройки профиля и метаданных приложение может просто запустить граф фильтра.</span><span class="sxs-lookup"><span data-stu-id="08e5c-116">After the profile and metadata have been configured, the application can simply run the filter graph.</span></span> <span data-ttu-id="08e5c-117">На внутреннем уровне фильтр использует пакет SDK Windows Media Format для записи файла.</span><span class="sxs-lookup"><span data-stu-id="08e5c-117">Internally, the filter uses the Windows Media Format SDK to write the file.</span></span> <span data-ttu-id="08e5c-118">Фильтр обрабатывает все данные синхронизации аудио-видео, которые в противном случае были бы ответственными за приложение.</span><span class="sxs-lookup"><span data-stu-id="08e5c-118">The filter handles all the audio-video synchronization details, which would otherwise be the responsibility of the application.</span></span>

<span data-ttu-id="08e5c-119">Этот процесс более подробно описывается в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="08e5c-119">This process is explained in more detail in the following sections.</span></span>



| <span data-ttu-id="08e5c-120">Section</span><span class="sxs-lookup"><span data-stu-id="08e5c-120">Section</span></span>                                                                                                           | <span data-ttu-id="08e5c-121">Описание</span><span class="sxs-lookup"><span data-stu-id="08e5c-121">Description</span></span>                                                                            |
|-------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="08e5c-122">Настройка модуля записи WM ASF (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="08e5c-122">Configuring the WM ASF Writer (QASF)</span></span>](configuring-the-wm-asf-writer--qasf.md)                                   | <span data-ttu-id="08e5c-123">Описание настройки фильтра модуля записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="08e5c-123">Describes how to configure the WM ASF Writer filter.</span></span>                                   |
| [<span data-ttu-id="08e5c-124">Создание графов фильтров для записи файлов ASF (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="08e5c-124">Building Filter Graphs to Write ASF Files (QASF)</span></span>](building-filter-graphs-to-write-asf-files--qasf.md)           | <span data-ttu-id="08e5c-125">Описывает, как создавать графы для перекодирования и записи файлов.</span><span class="sxs-lookup"><span data-stu-id="08e5c-125">Describes how to create file-transcoding and capture graphs.</span></span>                           |
| [<span data-ttu-id="08e5c-126">Настройка профилей и других свойств файлов (КАСФ)</span><span class="sxs-lookup"><span data-stu-id="08e5c-126">Configuring Profiles and Other File Properties (QASF)</span></span>](configuring-profiles-and-other-file-properties--qasf.md) | <span data-ttu-id="08e5c-127">Описывает, как выполнять различные задачи настройки файлов ASF с помощью модуля записи WM ASF.</span><span class="sxs-lookup"><span data-stu-id="08e5c-127">Describes how to perform various ASF file-configuration tasks using the WM ASF Writer.</span></span> |



 

 

 
