---
description: Пример Дмоенум
ms.assetid: afd7853e-b0ab-42f6-8c2e-c2b0b40d989b
title: Пример Дмоенум
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c413b7787ba12785758cffed89be15229373643d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262460"
---
# <a name="dmoenum-sample"></a><span data-ttu-id="b0288-103">Пример Дмоенум</span><span class="sxs-lookup"><span data-stu-id="b0288-103">DMOEnum Sample</span></span>

## <a name="description"></a><span data-ttu-id="b0288-104">Описание</span><span class="sxs-lookup"><span data-stu-id="b0288-104">Description</span></span>

<span data-ttu-id="b0288-105">Этот пример приложения перечисляет все [объекты DirectX Media](directx-media-objects.md) (дмос), зарегистрированные в системе пользователя, и отображает сведения о них.</span><span class="sxs-lookup"><span data-stu-id="b0288-105">This sample application enumerates all of the [DirectX Media Objects](directx-media-objects.md) (DMOs) registered in the user's system, and displays information about them.</span></span>

<span data-ttu-id="b0288-106">В примере используется функция [**дмоенум**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) и интерфейс [**Иенумдмо**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) для перечисления дмос.</span><span class="sxs-lookup"><span data-stu-id="b0288-106">The sample uses the [**DMOEnum**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoenum) function and the [**IEnumDMO**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-ienumdmo) interface to enumerate the DMOs.</span></span> <span data-ttu-id="b0288-107">Он использует интерфейс [**имедиаобжект**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) и другие интерфейсы DMO для получения сведений о каждом DMO.</span><span class="sxs-lookup"><span data-stu-id="b0288-107">It uses the [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject) interface and other DMO interfaces to retrieve information about each DMO.</span></span>

## <a name="usage"></a><span data-ttu-id="b0288-108">Использование</span><span class="sxs-lookup"><span data-stu-id="b0288-108">Usage</span></span>

<span data-ttu-id="b0288-109">При запуске приложения перечисляются все установленные дмос.</span><span class="sxs-lookup"><span data-stu-id="b0288-109">When the application launches, it enumerates all of the installed DMOs.</span></span> <span data-ttu-id="b0288-110">Если выбрана конкретная категория DMO, приложение отображает только дмос в этой категории.</span><span class="sxs-lookup"><span data-stu-id="b0288-110">If you select a specific DMO category, the application displays only the DMOs in that category.</span></span> <span data-ttu-id="b0288-111">Чтобы просмотреть сведения о DMO, выберите DMO из списка.</span><span class="sxs-lookup"><span data-stu-id="b0288-111">To view information about a DMO, select the DMO from the list.</span></span> <span data-ttu-id="b0288-112">Приложение отображает число потоков, предпочтительные типы носителей, сервер DLL для этого DMO и другие сведения о DMO.</span><span class="sxs-lookup"><span data-stu-id="b0288-112">The application displays the number of streams, the preferred media types, the DLL server for that DMO, and other information about the DMO.</span></span> <span data-ttu-id="b0288-113">Чтобы включить или исключить ключ дмос, установите флажок **включить ключ дмос?** .</span><span class="sxs-lookup"><span data-stu-id="b0288-113">To include or exclude keyed DMOs, toggle the **Include Keyed DMOs?** checkbox.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="b0288-114">Загрузка образца</span><span class="sxs-lookup"><span data-stu-id="b0288-114">Downloading the Sample</span></span>

<span data-ttu-id="b0288-115">Чтобы скачать примеры пакета SDK для DirectShow, установите последнюю версию [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="b0288-115">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="b0288-116">Этот пример устанавливается по следующему пути: *\[ \] корневые примеры SDK* \\ \\ мультимедиа \\ DirectShow \\ Прочие \\ дмоенум.</span><span class="sxs-lookup"><span data-stu-id="b0288-116">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Misc\\DMOEnum.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0288-117">См. также</span><span class="sxs-lookup"><span data-stu-id="b0288-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0288-118">Примеры DirectShow</span><span class="sxs-lookup"><span data-stu-id="b0288-118">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



