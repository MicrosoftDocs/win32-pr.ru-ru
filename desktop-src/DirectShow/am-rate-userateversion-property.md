---
description: Это свойство используется для сигнализации о версии свойства изменения скорости, которую должен использовать декодер.
ms.assetid: 49d1bfda-749b-4614-9a75-1f76fa8b320d
title: Свойство AM_RATE_UseRateVersion (Двдмедиа. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd33ef96c50ecc3da0711f08f0c7ffbf0a20825
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910222"
---
# <a name="am_rate_userateversion-property"></a><span data-ttu-id="1aade-103">\_ \_ Свойство усератеверсион Rate</span><span class="sxs-lookup"><span data-stu-id="1aade-103">AM\_RATE\_UseRateVersion Property</span></span>

<span data-ttu-id="1aade-104">Это свойство используется для сигнализации о версии свойства изменения скорости, которую должен использовать декодер.</span><span class="sxs-lookup"><span data-stu-id="1aade-104">This property is used to signal which version of the Rate Change property set the decoder should use.</span></span> <span data-ttu-id="1aade-105">Значение является типом **слова** .</span><span class="sxs-lookup"><span data-stu-id="1aade-105">The value is a **WORD** type.</span></span> <span data-ttu-id="1aade-106">Байт высокого порядка содержит дополнительный номер версии, а младший байт содержит младший байт.</span><span class="sxs-lookup"><span data-stu-id="1aade-106">The high-order byte contains the minor version number, and the low-order byte contains the low-order byte.</span></span> <span data-ttu-id="1aade-107">Таким же значением версии 1,1 будет сигнальное значение 0x0101.</span><span class="sxs-lookup"><span data-stu-id="1aade-107">Thus, version 1.1 is signaled with the value 0x0101.</span></span>

<span data-ttu-id="1aade-108">Если декодер не поддерживает указанную версию, он должен вызвать сбой вызова [**икспропертисет:: Set**](ikspropertyset-set.md) и Return E без \_ интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1aade-108">If the decoder does not support the specified version, it should fail the call to [**IKsPropertySet::Set**](ikspropertyset-set.md) and return E\_NOINTERFACE.</span></span> <span data-ttu-id="1aade-109">Если в фильтре источника не задана версия, декодеру следует по умолчанию установить версию 1,0.</span><span class="sxs-lookup"><span data-stu-id="1aade-109">If the source filter does not set the version, the decoder should default to version 1.0.</span></span>



| <span data-ttu-id="1aade-110">Метка</span><span class="sxs-lookup"><span data-stu-id="1aade-110">Label</span></span> | <span data-ttu-id="1aade-111">Значение</span><span class="sxs-lookup"><span data-stu-id="1aade-111">Value</span></span> |
|-------------------|-------------------------------|
| <span data-ttu-id="1aade-112">Идентификатор GUID набора свойств</span><span class="sxs-lookup"><span data-stu-id="1aade-112">Property Set GUID</span></span> | <span data-ttu-id="1aade-113">\_Кспропсетид \_ тсратечанже</span><span class="sxs-lookup"><span data-stu-id="1aade-113">AM\_KSPROPSETID\_TSRateChange</span></span> |
| <span data-ttu-id="1aade-114">Идентификатор свойства</span><span class="sxs-lookup"><span data-stu-id="1aade-114">Property ID</span></span>       | <span data-ttu-id="1aade-115">\_Ставка \_ усератеверсион</span><span class="sxs-lookup"><span data-stu-id="1aade-115">AM\_RATE\_UseRateVersion</span></span>      |
| <span data-ttu-id="1aade-116">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1aade-116">Data Type</span></span>         | <span data-ttu-id="1aade-117">**WORD**</span><span class="sxs-lookup"><span data-stu-id="1aade-117">**WORD**</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="1aade-118">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="1aade-118">Requirements</span></span>



| <span data-ttu-id="1aade-119">Требование</span><span class="sxs-lookup"><span data-stu-id="1aade-119">Requirement</span></span> | <span data-ttu-id="1aade-120">Значение</span><span class="sxs-lookup"><span data-stu-id="1aade-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1aade-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1aade-121">Header</span></span><br/> | <dl> <span data-ttu-id="1aade-122"><dt>Двдмедиа. h</dt></span><span class="sxs-lookup"><span data-stu-id="1aade-122"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1aade-123">См. также</span><span class="sxs-lookup"><span data-stu-id="1aade-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1aade-124">**Набор свойств изменения скорости**</span><span class="sxs-lookup"><span data-stu-id="1aade-124">**Rate Change Property Set**</span></span>](rate-change-property-set.md)
</dt> </dl>

 

 




