---
title: Объект свойств входного носителя
description: Объект свойств входного носителя
ms.assetid: e7aa6c99-b6b3-4e5b-869d-3387f70dad87
keywords:
- Windows Media Format SDK, объекты свойств входного носителя
- Расширенный системный формат (ASF), объекты свойств входного носителя
- ASF (Расширенный системный формат), объекты свойств входного носителя
- объекты, объекты свойств входных данных мультимедиа
- объекты свойств входного носителя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beddda23ab7be86c3cb522edb8e811978c0c9ed9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103890228"
---
# <a name="input-media-properties-object"></a><span data-ttu-id="b045c-108">Объект свойств входного носителя</span><span class="sxs-lookup"><span data-stu-id="b045c-108">Input Media Properties Object</span></span>

<span data-ttu-id="b045c-109">Входной объект свойств носителя, созданный объектом Writer, поддерживает следующие интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b045c-109">An input media properties object created by the writer object supports the following interfaces.</span></span> <span data-ttu-id="b045c-110">Доступ к этим интерфейсам осуществляется путем вызова **QueryInterface** в одном из интерфейсов объекта модуля записи.</span><span class="sxs-lookup"><span data-stu-id="b045c-110">These interfaces are accessed by a call to **QueryInterface** on one of the interfaces of the writer object.</span></span>



| <span data-ttu-id="b045c-111">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="b045c-111">Interface</span></span>                                        | <span data-ttu-id="b045c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b045c-112">Description</span></span>                                                                                                |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b045c-113">**ивминпутмедиапропс**</span><span class="sxs-lookup"><span data-stu-id="b045c-113">**IWMInputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) | <span data-ttu-id="b045c-114">Извлекает свойства входного потока.</span><span class="sxs-lookup"><span data-stu-id="b045c-114">Retrieves the properties of an input stream.</span></span>                                                               |
| [<span data-ttu-id="b045c-115">**ивммедиапропс**</span><span class="sxs-lookup"><span data-stu-id="b045c-115">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)           | <span data-ttu-id="b045c-116">Используется в качестве базового интерфейса для других интерфейсов свойств мультимедиа (входные, выходные и видео).</span><span class="sxs-lookup"><span data-stu-id="b045c-116">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="b045c-117">**ивмвидеомедиапропс**</span><span class="sxs-lookup"><span data-stu-id="b045c-117">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops) | <span data-ttu-id="b045c-118">Управляет свойствами потока видео.</span><span class="sxs-lookup"><span data-stu-id="b045c-118">Manages the properties of a video stream.</span></span> <span data-ttu-id="b045c-119">Это необязательный интерфейс, доступный только для потоков видео.</span><span class="sxs-lookup"><span data-stu-id="b045c-119">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b045c-120">См. также</span><span class="sxs-lookup"><span data-stu-id="b045c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b045c-121">**Объекты**</span><span class="sxs-lookup"><span data-stu-id="b045c-121">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="b045c-122">**Объект модуля записи**</span><span class="sxs-lookup"><span data-stu-id="b045c-122">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




