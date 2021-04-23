---
description: Когда фильтр навигации по DVD переходит в режим Караоке, он информирует звуковой декодер через \_ \_ свойство AM двдкараоке \_ Enable.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Набор свойств караоке для DVD (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909072"
---
# <a name="dvd-karaoke-property-set"></a><span data-ttu-id="7f786-103">Набор свойств караоке для DVD</span><span class="sxs-lookup"><span data-stu-id="7f786-103">DVD Karaoke Property Set</span></span>

<span data-ttu-id="7f786-104">Когда фильтр [навигации по DVD](dvd-navigator-filter.md) переходит в режим Караоке, он информирует звуковой декодер через свойство **AM \_ \_ двдкараоке \_ Enable** .</span><span class="sxs-lookup"><span data-stu-id="7f786-104">When the [DVD Navigator](dvd-navigator-filter.md) filter goes into karaoke mode, it informs the audio decoder through the **AM\_PROPERTY\_DVDKARAOKE\_ENABLE** property.</span></span> <span data-ttu-id="7f786-105">После этого декодер должен отключить звуковые каналы с 2 по 5, пока он не будет получен из свойства **\_ \_ \_ данных двдкараоке** в DVD Navigator с указателем на структуру данных [**AM \_ двдкараокедата**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) , указывающую, как должны быть смешаны вспомогательные каналы.</span><span class="sxs-lookup"><span data-stu-id="7f786-105">The decoder should then mute audio channels 2 through 5 until it receives from the DVD Navigator an **AM\_PROPERTY\_DVDKARAOKE\_DATA** property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) data structure indicating how the auxiliary channels are to be mixed.</span></span>



| <span data-ttu-id="7f786-106">Метка</span><span class="sxs-lookup"><span data-stu-id="7f786-106">Label</span></span> | <span data-ttu-id="7f786-107">Значение</span><span class="sxs-lookup"><span data-stu-id="7f786-107">Value</span></span> |
|-------------------|-----------------------------|
| <span data-ttu-id="7f786-108">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="7f786-108">Property Set GUID</span></span> | <span data-ttu-id="7f786-109">\_Кспропсетид \_ двдкараоке</span><span class="sxs-lookup"><span data-stu-id="7f786-109">AM\_KSPROPSETID\_DvdKaraoke</span></span> |



 



| <span data-ttu-id="7f786-110">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="7f786-110">Property ID</span></span>                      | <span data-ttu-id="7f786-111">Описание</span><span class="sxs-lookup"><span data-stu-id="7f786-111">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f786-112">\_включить свойство AM \_ двдкараоке \_</span><span class="sxs-lookup"><span data-stu-id="7f786-112">AM\_PROPERTY\_DVDKARAOKE\_ENABLE</span></span> | <span data-ttu-id="7f786-113">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="7f786-113">BOOLEAN value.</span></span> <span data-ttu-id="7f786-114">Навигатор DVD отправляет декодеру свойство AM двдкараоке, которое \_ \_ \_ включает значение **true** , чтобы включить довнмиксинг караоке или **false** для отключения.</span><span class="sxs-lookup"><span data-stu-id="7f786-114">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_ENABLE with a value of **TRUE** to enable karaoke downmixing or **FALSE** to disable it.</span></span>                                                                                                                                    |
| <span data-ttu-id="7f786-115">\_данные свойства \_ двдкараоке \_</span><span class="sxs-lookup"><span data-stu-id="7f786-115">AM\_PROPERTY\_DVDKARAOKE\_DATA</span></span>   | <span data-ttu-id="7f786-116">Навигатор DVD-диска отправляет декодеру \_ \_ свойство данных AM Property двдкараоке \_ с указателем на структуру [**AM \_ двдкараокедата**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) для изменения конфигурации довнмикс; то есть для включения или отключения определенных каналов караоке и направления их к правому или левому каналу вывода.</span><span class="sxs-lookup"><span data-stu-id="7f786-116">The DVD Navigator sends the decoder an AM\_PROPERTY\_DVDKARAOKE\_DATA property with a pointer to an [**AM\_DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) structure to change the downmix configuration; that is, to turn certain karaoke channels on or off and direct them to the right or left output channel.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7f786-117">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="7f786-117">Requirements</span></span>



| <span data-ttu-id="7f786-118">Требование</span><span class="sxs-lookup"><span data-stu-id="7f786-118">Requirement</span></span> | <span data-ttu-id="7f786-119">Значение</span><span class="sxs-lookup"><span data-stu-id="7f786-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7f786-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7f786-120">Header</span></span><br/> | <dl> <span data-ttu-id="7f786-121"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f786-121"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f786-122">См. также</span><span class="sxs-lookup"><span data-stu-id="7f786-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f786-123">Наборы свойств</span><span class="sxs-lookup"><span data-stu-id="7f786-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




