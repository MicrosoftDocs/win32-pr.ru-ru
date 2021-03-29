---
description: Это свойство используется для сигнализации о версии свойства изменения скорости, которую должен использовать декодер.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: Свойство AM_RATE_UseRateVersion (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ab609d2d38dc28257d13994e6cd464094b714be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657670"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="887b6-103">\_ \_ Свойство усератеверсион Rate</span><span class="sxs-lookup"><span data-stu-id="887b6-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="887b6-104">Это свойство используется для сигнализации о версии свойства изменения скорости, которую должен использовать декодер.</span><span class="sxs-lookup"><span data-stu-id="887b6-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="887b6-105">Значение является типом **слова** .</span><span class="sxs-lookup"><span data-stu-id="887b6-105">The value is a **WORD** type.</span></span> <span data-ttu-id="887b6-106">Байт высокого порядка содержит дополнительный номер версии, а младший байт содержит младший байт.</span><span class="sxs-lookup"><span data-stu-id="887b6-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="887b6-107">Таким же значением версии 1,1 будет сигнальное значение 0x0101.</span><span class="sxs-lookup"><span data-stu-id="887b6-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="887b6-108">Если декодер не поддерживает указанную версию, он должен вызвать сбой вызова [**икспропертисет:: Set**](ikspropertyset-set.md) и Return E без \_ интерфейса.</span><span class="sxs-lookup"><span data-stu-id="887b6-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="887b6-109">Если в фильтре источника не задана версия, декодеру следует по умолчанию установить версию 1,0.</span><span class="sxs-lookup"><span data-stu-id="887b6-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



|                   |                               |
|-------------------|-------------------------------|
| <span data-ttu-id="887b6-110">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="887b6-110">Property Set GUID</span></span> | <span data-ttu-id="887b6-111">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="887b6-111">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="887b6-112">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="887b6-112">Property ID</span></span>       | <span data-ttu-id="887b6-113">\_Ставка \_ усератеверсион</span><span class="sxs-lookup"><span data-stu-id="887b6-113">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="887b6-114">Тип данных</span><span class="sxs-lookup"><span data-stu-id="887b6-114">Data Type</span></span>         | <span data-ttu-id="887b6-115">**WORD**</span><span class="sxs-lookup"><span data-stu-id="887b6-115">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="887b6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="887b6-116">Requirements</span></span>



| <span data-ttu-id="887b6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="887b6-117">Requirement</span></span> | <span data-ttu-id="887b6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="887b6-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="887b6-119">Header</span><span class="sxs-lookup"><span data-stu-id="887b6-119">Header</span></span><br/> | <dl> <span data-ttu-id="887b6-120"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="887b6-120"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="887b6-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="887b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="887b6-122">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="887b6-122">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




