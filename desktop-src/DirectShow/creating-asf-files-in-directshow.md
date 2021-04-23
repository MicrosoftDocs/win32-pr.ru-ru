---
description: Создание файлов ASF в DirectShow
ms.assetid: dffda43a-5831-4889-864f-81351b9e2bb3
title: Создание файлов ASF в DirectShow (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11f5c9ebac0b14b736c47599ee25a1c1c28dd8f0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105662055"
---
# <a name="creating-asf-files-in-directshow-directshow"></a><span data-ttu-id="df8f4-103">Создание файлов ASF в DirectShow (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="df8f4-103">Creating ASF Files in DirectShow (DirectShow)</span></span>

<span data-ttu-id="df8f4-104">В этом разделе описывается, как использовать фильтр [модуля записи DirectShow WM ASF](wm-asf-writer-filter.md) для создания файлов в расширенном системном формате (ASF).</span><span class="sxs-lookup"><span data-stu-id="df8f4-104">This section describes how to use the DirectShow [WM ASF Writer](wm-asf-writer-filter.md) filter to create files in Advanced Systems Format (ASF).</span></span> <span data-ttu-id="df8f4-105">ASF — это формат контейнера, который может содержать любой тип сжатых или несжатых данных.</span><span class="sxs-lookup"><span data-stu-id="df8f4-105">ASF is a container format that can contain any type of compressed or uncompressed data.</span></span> <span data-ttu-id="df8f4-106">Файлы формата Windows Media — это файлы ASF, которые используют определенные кодеки, как указано в пакете средств разработки программного обеспечения (SDK) Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="df8f4-106">Windows Media Format files are ASF files that use certain codecs as specified in the Windows Media Format Software Development Kit (SDK).</span></span> <span data-ttu-id="df8f4-107">Эти файлы используют расширения WMA для звуковых файлов Windows Media и WMV для видеофайлов Windows Media.</span><span class="sxs-lookup"><span data-stu-id="df8f4-107">These files use the extensions ".wma" for Windows Media Audio files and ".wmv" for Windows Media Video files.</span></span>

<span data-ttu-id="df8f4-108">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="df8f4-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="df8f4-109">Пакет SDK для DirectShow и пакет SDK Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="df8f4-109">The DirectShow SDK and the Windows Media Format SDK</span></span>](the-directshow-sdk-and-the-windows-media-format-sdk.md)
-   [<span data-ttu-id="df8f4-110">Настройка модуля записи ASF</span><span class="sxs-lookup"><span data-stu-id="df8f4-110">Configuring the ASF Writer</span></span>](configuring-the-asf-writer.md)
-   [<span data-ttu-id="df8f4-111">Создание графов фильтра для записи файлов ASF</span><span class="sxs-lookup"><span data-stu-id="df8f4-111">Building Filter Graphs to Write ASF Files</span></span>](building-filter-graphs-to-write-asf-files.md)
-   [<span data-ttu-id="df8f4-112">Настройка профилей и других свойств ASF-файлов</span><span class="sxs-lookup"><span data-stu-id="df8f4-112">Configuring Profiles and Other ASF File Properties</span></span>](configuring-profiles-and-other-asf-file-properties.md)
-   [<span data-ttu-id="df8f4-113">Разблокировка пакета SDK Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="df8f4-113">Unlocking the Windows Media Format SDK</span></span>](unlocking-the-windows-media-format-sdk.md)

## <a name="related-topics"></a><span data-ttu-id="df8f4-114">См. также</span><span class="sxs-lookup"><span data-stu-id="df8f4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df8f4-115">Использование Windows Media в DirectShow</span><span class="sxs-lookup"><span data-stu-id="df8f4-115">Using Windows Media in DirectShow</span></span>](using-windows-media-in-directshow.md)
</dt> </dl>

 

 



