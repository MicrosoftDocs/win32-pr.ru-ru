---
description: Задает конец прохода кодирования.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: Свойство MFPKEY_ENDOFPASS (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908780"
---
# <a name="mfpkey_endofpass-property"></a><span data-ttu-id="553c3-103">МФПКЭЙ \_ ендофпасс, свойство</span><span class="sxs-lookup"><span data-stu-id="553c3-103">MFPKEY\_ENDOFPASS Property</span></span>

<span data-ttu-id="553c3-104">Задает конец прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="553c3-104">Specifies the end of an encoding pass.</span></span>

## <a name="data-type"></a><span data-ttu-id="553c3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="553c3-105">Data Type</span></span>

<span data-ttu-id="553c3-106">**Логическое значение VT \_**</span><span class="sxs-lookup"><span data-stu-id="553c3-106">**VT\_BOOL**</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="553c3-107">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="553c3-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="553c3-108">g \_ всзвмвцендофпасс</span><span class="sxs-lookup"><span data-stu-id="553c3-108">g\_wszWMVCEndOfPass</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="553c3-109">Тип данных для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="553c3-109">Data Type for IPropertyBag</span></span>

<span data-ttu-id="553c3-110">Тип данных не требуется.</span><span class="sxs-lookup"><span data-stu-id="553c3-110">No data type is required.</span></span> <span data-ttu-id="553c3-111">Чтобы задать это свойство, передайте неинициализированный **вариант**.</span><span class="sxs-lookup"><span data-stu-id="553c3-111">To set this property, pass an uninitialized **VARIANT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="553c3-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="553c3-112">Remarks</span></span>

<span data-ttu-id="553c3-113">Это свойство не является нормальным, так как оно имеет тот же результат, независимо от того, имеет ли значение вариант \_ true или Variant \_ false.</span><span class="sxs-lookup"><span data-stu-id="553c3-113">This property is not a normal property because it has the same effect regardless of whether the value is VARIANT\_TRUE or VARIANT\_FALSE.</span></span> <span data-ttu-id="553c3-114">Это свойство необходимо задать после обработки последних входных образцов для прохода предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="553c3-114">You must set this property after you process the last input samples for a preprocessing pass.</span></span> <span data-ttu-id="553c3-115">Если выполняется несколько проходов, необходимо задать это свойство в конце каждого этапа предварительной обработки (в настоящее время ни один из кодеков не поддерживает больше одного).</span><span class="sxs-lookup"><span data-stu-id="553c3-115">If you are performing multiple passes, you must set this property at the end of each preprocessing pass (at present none of the codecs supports more than one).</span></span> <span data-ttu-id="553c3-116">Если это свойство не задано, кодек предполагает, что вы все еще передаете образцы для предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="553c3-116">If you do not set this property, the codec will assume that you are still passing samples for preprocessing.</span></span>

## <a name="requirements"></a><span data-ttu-id="553c3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="553c3-117">Requirements</span></span>



| <span data-ttu-id="553c3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="553c3-118">Requirement</span></span> | <span data-ttu-id="553c3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="553c3-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="553c3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="553c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="553c3-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="553c3-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="553c3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="553c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="553c3-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="553c3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="553c3-124">Header</span><span class="sxs-lookup"><span data-stu-id="553c3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="553c3-125"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="553c3-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="553c3-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="553c3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="553c3-127">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="553c3-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




