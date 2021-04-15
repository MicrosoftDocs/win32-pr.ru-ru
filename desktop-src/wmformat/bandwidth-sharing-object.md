---
title: Объект, совместно использующие пропускную способность
description: Объект, совместно использующие пропускную способность
ms.assetid: 9dc863da-1842-41e7-b66c-c97e0140046d
keywords:
- Windows Media Format SDK, объекты для совместного использования пропускной способности
- Расширенный формат систем (ASF), объекты совместного использования пропускной способности
- ASF (Расширенный системный формат), объекты совместного использования пропускной способности
- объекты, объекты для совместного использования пропускной способности
- Совместное использование пропускной способности, сведения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d29048e3094f1a12775dfbec7422baf349c18be7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412537"
---
# <a name="bandwidth-sharing-object"></a><span data-ttu-id="fb2ee-108">Объект, совместно использующие пропускную способность</span><span class="sxs-lookup"><span data-stu-id="fb2ee-108">Bandwidth Sharing Object</span></span>

<span data-ttu-id="fb2ee-109">Объект совместного использования пропускной способности используется для указания того, что два или больше потоков, независимо от их отдельных ставок, никогда не будут использовать больше указанного объема пропускной способности между ними.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-109">A bandwidth sharing object is used to indicate that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth between them.</span></span> <span data-ttu-id="fb2ee-110">Это чисто информационный объект; заданные в ней битовые скорости не применяются программными средствами ни одним из объектов этого пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-110">This is a purely informational object; the bit rates set within it are not enforced programmatically by any object of this SDK.</span></span>

<span data-ttu-id="fb2ee-111">Сведения о совместном использовании пропускной способности являются необязательной частью профиля.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-111">Bandwidth sharing information is an optional part of a profile.</span></span> <span data-ttu-id="fb2ee-112">Объекты совместного использования пропускной способности можно создавать для существующих сведений о пропускной способности в профиле или создавать пустые, готовые к получению новых данных.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-112">Bandwidth sharing objects can be created for existing bandwidth sharing information in a profile or can be created empty, ready to receive new data.</span></span> <span data-ttu-id="fb2ee-113">Объекты совместного использования пропускной способности не могут существовать независимо от объекта профиля.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-113">Bandwidth sharing objects cannot exist independently of a profile object.</span></span> <span data-ttu-id="fb2ee-114">Чтобы сохранить содержимое объекта, совместно используемой пропускной способностью, необходимо вызвать [**IWMProfile3:: аддбандвидсшаринг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span><span class="sxs-lookup"><span data-stu-id="fb2ee-114">To save the contents of a bandwidth sharing object, you must call [**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing).</span></span>

<span data-ttu-id="fb2ee-115">Чтобы создать объект для общего доступа к пропускной способности, вызовите один из следующих методов.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-115">To create a bandwidth sharing object, call one of the following methods.</span></span>



| <span data-ttu-id="fb2ee-116">Метод</span><span class="sxs-lookup"><span data-stu-id="fb2ee-116">Method</span></span>                                                                                  | <span data-ttu-id="fb2ee-117">Описание</span><span class="sxs-lookup"><span data-stu-id="fb2ee-117">Description</span></span>                                                                                                                                                    |
|-----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb2ee-118">**IWMProfile3:: Креатеневбандвидсшаринг**</span><span class="sxs-lookup"><span data-stu-id="fb2ee-118">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing) | <span data-ttu-id="fb2ee-119">Создает объект совместного использования пропускной способности без каких-либо данных.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-119">Creates a bandwidth sharing object without any data.</span></span>                                                                                                           |
| [<span data-ttu-id="fb2ee-120">**IWMProfile3:: Жетбандвидсшаринг**</span><span class="sxs-lookup"><span data-stu-id="fb2ee-120">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)             | <span data-ttu-id="fb2ee-121">Создает объект совместного использования пропускной способности, заполненный данными из профиля.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-121">Creates a bandwidth sharing object populated with data from a profile.</span></span> <span data-ttu-id="fb2ee-122">Использует индекс общего доступа к пропускной способности для поиска информации о требуемой пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-122">Uses the bandwidth sharing index to identify the desired bandwidth sharing information.</span></span> |



 

<span data-ttu-id="fb2ee-123">Оба метода в приведенной выше таблице устанавливают указатель на интерфейс **ивмбандвидсшаринг** .</span><span class="sxs-lookup"><span data-stu-id="fb2ee-123">Both methods in the preceding table set a pointer to an **IWMBandwidthSharing** interface.</span></span> <span data-ttu-id="fb2ee-124">Интерфейс **ивмстреамлист** наследуется **ивмбандвидсшаринг**, поэтому нет необходимости вызывать **QueryInterface** с этим объектом.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-124">The **IWMStreamList** interface is inherited by **IWMBandwidthSharing**, so there is no need to call **QueryInterface** with this object.</span></span>

<span data-ttu-id="fb2ee-125">Следующие интерфейсы поддерживаются каждым объектом совместного использования пропускной способности.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-125">The following interfaces are supported by every bandwidth sharing object.</span></span>



| <span data-ttu-id="fb2ee-126">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="fb2ee-126">Interface</span></span>                                          | <span data-ttu-id="fb2ee-127">Описание</span><span class="sxs-lookup"><span data-stu-id="fb2ee-127">Description</span></span>                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="fb2ee-128">**ивмбандвидсшаринг**</span><span class="sxs-lookup"><span data-stu-id="fb2ee-128">**IWMBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing) | <span data-ttu-id="fb2ee-129">Управляет свойствами группы потоков, которые будут совместно использовать пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-129">Manages the properties of a group of streams that will share bandwidth.</span></span> |
| [<span data-ttu-id="fb2ee-130">**ивмстреамлист**</span><span class="sxs-lookup"><span data-stu-id="fb2ee-130">**IWMStreamList**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamlist)             | <span data-ttu-id="fb2ee-131">Управляет списком потоков, которые будут совместно использовать пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="fb2ee-131">Manages the list of streams that will share bandwidth.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="fb2ee-132">См. также</span><span class="sxs-lookup"><span data-stu-id="fb2ee-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb2ee-133">**Совместное использование пропускной способности**</span><span class="sxs-lookup"><span data-stu-id="fb2ee-133">**Bandwidth Sharing**</span></span>](bandwidth-sharing.md)
</dt> <dt>

[<span data-ttu-id="fb2ee-134">**Объект диспетчера профилей**</span><span class="sxs-lookup"><span data-stu-id="fb2ee-134">**Profile Manager Object**</span></span>](profile-manager-object.md)
</dt> <dt>

[<span data-ttu-id="fb2ee-135">**Объект Profile**</span><span class="sxs-lookup"><span data-stu-id="fb2ee-135">**Profile Object**</span></span>](profile-object.md)
</dt> </dl>

 

 




