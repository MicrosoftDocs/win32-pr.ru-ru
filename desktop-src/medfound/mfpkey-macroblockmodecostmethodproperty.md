---
description: Указывает метод стоимости, используемый кодеком для определения используемого режима макроблокк.
ms.assetid: 2ba9b943-0daa-40c1-87ea-2fa647fb7095
title: Свойство MFPKEY_MACROBLOCKMODECOSTMETHOD (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 289219300a79c67565891c48cec848851c17bd7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692846"
---
# <a name="mfpkey_macroblockmodecostmethod-property"></a><span data-ttu-id="1eb40-103">МФПКЭЙ \_ макроблоккмодекостмесод, свойство</span><span class="sxs-lookup"><span data-stu-id="1eb40-103">MFPKEY\_MACROBLOCKMODECOSTMETHOD Property</span></span>

<span data-ttu-id="1eb40-104">Указывает метод стоимости, используемый кодеком для определения используемого режима макроблокк.</span><span class="sxs-lookup"><span data-stu-id="1eb40-104">Specifies the cost method used by the codec to determine which macroblock mode to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1eb40-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="1eb40-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1eb40-106">g \_ всзвмвкмакроблоккмодекостмесод</span><span class="sxs-lookup"><span data-stu-id="1eb40-106">g\_wszWMVCMacroblockModeCostMethod</span></span>

## <a name="data-type"></a><span data-ttu-id="1eb40-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1eb40-107">Data Type</span></span>

<span data-ttu-id="1eb40-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="1eb40-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="1eb40-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1eb40-109">Default Value</span></span>

<span data-ttu-id="1eb40-110">0</span><span class="sxs-lookup"><span data-stu-id="1eb40-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="1eb40-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1eb40-111">Remarks</span></span>

<span data-ttu-id="1eb40-112">Для этого свойства можно задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1eb40-112">This property may be set to one of the following values.</span></span>



| <span data-ttu-id="1eb40-113">Значение</span><span class="sxs-lookup"><span data-stu-id="1eb40-113">Value</span></span> | <span data-ttu-id="1eb40-114">Используемый метод</span><span class="sxs-lookup"><span data-stu-id="1eb40-114">Method used</span></span>                                                                                            |
|-------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb40-115">0</span><span class="sxs-lookup"><span data-stu-id="1eb40-115">0</span></span>     | <span data-ttu-id="1eb40-116">SAD/Хадамард.</span><span class="sxs-lookup"><span data-stu-id="1eb40-116">SAD/Hadamard.</span></span> <span data-ttu-id="1eb40-117">Этот параметр настраивает кодек для использования только искажений при вычислении затрат.</span><span class="sxs-lookup"><span data-stu-id="1eb40-117">This option configures the codec to use only distortion when computing cost.</span></span>             |
| <span data-ttu-id="1eb40-118">1</span><span class="sxs-lookup"><span data-stu-id="1eb40-118">1</span></span>     | <span data-ttu-id="1eb40-119">Стоимость удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="1eb40-119">RD cost.</span></span> <span data-ttu-id="1eb40-120">Этот параметр настраивает кодек для учета скорости и искажения при вычислении затрат.</span><span class="sxs-lookup"><span data-stu-id="1eb40-120">This option configures the codec to account for both rate and distortion when computing cost.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1eb40-121">Требования</span><span class="sxs-lookup"><span data-stu-id="1eb40-121">Requirements</span></span>



| <span data-ttu-id="1eb40-122">Требование</span><span class="sxs-lookup"><span data-stu-id="1eb40-122">Requirement</span></span> | <span data-ttu-id="1eb40-123">Значение</span><span class="sxs-lookup"><span data-stu-id="1eb40-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eb40-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1eb40-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1eb40-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1eb40-125">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1eb40-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1eb40-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1eb40-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1eb40-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1eb40-128">Header</span><span class="sxs-lookup"><span data-stu-id="1eb40-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1eb40-129"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1eb40-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eb40-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1eb40-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eb40-131">МФПКЭЙ \_ мотионматчмесод</span><span class="sxs-lookup"><span data-stu-id="1eb40-131">MFPKEY\_MOTIONMATCHMETHOD</span></span>](mfpkey-motionmatchmethodproperty.md)
</dt> <dt>

[<span data-ttu-id="1eb40-132">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1eb40-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




