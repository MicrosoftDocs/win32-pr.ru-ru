---
description: Константы битовой флага ФОНЕБУТТОНСТАТЕ описывают позиции кнопок.
ms.assetid: f1196e31-65c6-4ade-a0b7-c7758ce97be1
title: Константы PHONEBUTTONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2b1cc2f669fb5c1171834f46e11a161e9390eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689533"
---
# <a name="phonebuttonstate_-constants"></a><span data-ttu-id="b9434-103">Константы PHONEBUTTONSTATE_</span><span class="sxs-lookup"><span data-stu-id="b9434-103">PHONEBUTTONSTATE_ Constants</span></span>

<span data-ttu-id="b9434-104">**PHONEBUTTONSTATE_** константы битовых флагов описывают позиции кнопки.</span><span class="sxs-lookup"><span data-stu-id="b9434-104">The **PHONEBUTTONSTATE_** bit-flag constants describe the button's positions.</span></span>

<dl> <dt>

<span data-ttu-id="b9434-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span><span class="sxs-lookup"><span data-stu-id="b9434-105"><span id="PHONEBUTTONSTATE_DOWN"></span><span id="phonebuttonstate_down"></span>**PHONEBUTTONSTATE_DOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9434-106">Кнопка находится в состоянии "вниз" (нажата вниз).</span><span class="sxs-lookup"><span data-stu-id="b9434-106">The button is in the "down" state (pressed down).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9434-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="b9434-107"><span id="PHONEBUTTONSTATE_UNAVAIL"></span><span id="phonebuttonstate_unavail"></span>**PHONEBUTTONSTATE_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9434-108">Указывает, что состояние кнопки не известно поставщику услуг и не будет известно в будущем.</span><span class="sxs-lookup"><span data-stu-id="b9434-108">Indicates that the up or down state of the button is not known to the service provider, and will not become known at a future time.</span></span> <span data-ttu-id="b9434-109">(TAPI версии 1,4 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="b9434-109">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9434-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="b9434-110"><span id="PHONEBUTTONSTATE_UNKNOWN"></span><span id="phonebuttonstate_unknown"></span>**PHONEBUTTONSTATE_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9434-111">Указывает, что состояние кнопки в данный момент неизвестно, но может быть известно в будущем.</span><span class="sxs-lookup"><span data-stu-id="b9434-111">Indicates that the up or down state of the button is not known at this time, but may become known at a future time.</span></span> <span data-ttu-id="b9434-112">(TAPI версии 1,4 и более поздней)</span><span class="sxs-lookup"><span data-stu-id="b9434-112">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b9434-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span><span class="sxs-lookup"><span data-stu-id="b9434-113"><span id="PHONEBUTTONSTATE_UP"></span><span id="phonebuttonstate_up"></span>**PHONEBUTTONSTATE_UP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b9434-114">Кнопка находится в состоянии "вверх".</span><span class="sxs-lookup"><span data-stu-id="b9434-114">The button is in the "up" state.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9434-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b9434-115">Remarks</span></span>

<span data-ttu-id="b9434-116">Без расширяемости.</span><span class="sxs-lookup"><span data-stu-id="b9434-116">No extensibility.</span></span> <span data-ttu-id="b9434-117">Все 32 бит зарезервированы.</span><span class="sxs-lookup"><span data-stu-id="b9434-117">All 32 bits are reserved.</span></span>

<span data-ttu-id="b9434-118">Для обеспечения обратной совместимости поставщик услуг должен проверить согласованную версию API на телефоне и не использовать эти PHONEBUTTONSTATE_ значения, которые не поддерживает согласованная версия.</span><span class="sxs-lookup"><span data-stu-id="b9434-118">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the phone, and to not use those PHONEBUTTONSTATE_ values that the negotiated version does not support.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9434-119">Требования</span><span class="sxs-lookup"><span data-stu-id="b9434-119">Requirements</span></span>



| <span data-ttu-id="b9434-120">Требование</span><span class="sxs-lookup"><span data-stu-id="b9434-120">Requirement</span></span> | <span data-ttu-id="b9434-121">Значение</span><span class="sxs-lookup"><span data-stu-id="b9434-121">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b9434-122">Версия TAPI</span><span class="sxs-lookup"><span data-stu-id="b9434-122">TAPI version</span></span><br/> | <span data-ttu-id="b9434-123">Требуется TAPI 2,0 или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b9434-123">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b9434-124">Header</span><span class="sxs-lookup"><span data-stu-id="b9434-124">Header</span></span><br/>       | <dl> <span data-ttu-id="b9434-125"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9434-125"><dt>Tapi.h</dt></span></span> </dl> |



 

 




