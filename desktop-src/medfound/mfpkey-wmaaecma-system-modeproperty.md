---
description: Задает режим обработки для схемы DSP для записи голоса.
ms.assetid: 479b3525-5beb-4c6b-b1ad-8fa72c0d0fd0
title: Свойство MFPKEY_WMAAECMA_SYSTEM_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfca745b83c8a73a2eb4c17c8a2206f90255088c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662781"
---
# <a name="mfpkey_wmaaecma_system_mode-property"></a><span data-ttu-id="dd01a-103">МФПКЭЙ \_ вмааекма \_ , \_ свойство системного режима</span><span class="sxs-lookup"><span data-stu-id="dd01a-103">MFPKEY\_WMAAECMA\_SYSTEM\_MODE Property</span></span>

<span data-ttu-id="dd01a-104">Задает режим обработки для схемы DSP для записи голоса.</span><span class="sxs-lookup"><span data-stu-id="dd01a-104">Sets the processing mode for the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="dd01a-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="dd01a-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="dd01a-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="dd01a-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="dd01a-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="dd01a-107">Data Type</span></span>

<span data-ttu-id="dd01a-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="dd01a-108">VT\_I4</span></span>

## <a name="applies-to"></a><span data-ttu-id="dd01a-109">Применение</span><span class="sxs-lookup"><span data-stu-id="dd01a-109">Applies To</span></span>

-   [<span data-ttu-id="dd01a-110">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="dd01a-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="dd01a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd01a-111">Remarks</span></span>

<span data-ttu-id="dd01a-112">Значение этого свойства является членом перечисления [ \_ системного \_ режима AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) .</span><span class="sxs-lookup"><span data-stu-id="dd01a-112">The value of this property is a member of the [AEC\_SYSTEM\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_system_mode) enumeration.</span></span>

<span data-ttu-id="dd01a-113">Свойство должно иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="dd01a-113">The property must be one of the following values.</span></span>



| <span data-ttu-id="dd01a-114">Значение</span><span class="sxs-lookup"><span data-stu-id="dd01a-114">Value</span></span> | <span data-ttu-id="dd01a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="dd01a-115">Description</span></span>                                 |
|-------|---------------------------------------------|
| <span data-ttu-id="dd01a-116">0</span><span class="sxs-lookup"><span data-stu-id="dd01a-116">0</span></span>     | <span data-ttu-id="dd01a-117">Режим "Отмена звукового эха" (AEC)</span><span class="sxs-lookup"><span data-stu-id="dd01a-117">Audio echo cancellation (AEC) only mode</span></span>     |
| <span data-ttu-id="dd01a-118">2</span><span class="sxs-lookup"><span data-stu-id="dd01a-118">2</span></span>     | <span data-ttu-id="dd01a-119">Режим только обработки массива микрофона (MAP)</span><span class="sxs-lookup"><span data-stu-id="dd01a-119">Microphone array processing (MAP) only mode</span></span> |
| <span data-ttu-id="dd01a-120">4</span><span class="sxs-lookup"><span data-stu-id="dd01a-120">4</span></span>     | <span data-ttu-id="dd01a-121">Контекст AEC и режим MAP</span><span class="sxs-lookup"><span data-stu-id="dd01a-121">AEC and MAP mode</span></span>                            |
| <span data-ttu-id="dd01a-122">5</span><span class="sxs-lookup"><span data-stu-id="dd01a-122">5</span></span>     | <span data-ttu-id="dd01a-123">Ни AEC, ни режим MAP</span><span class="sxs-lookup"><span data-stu-id="dd01a-123">Neither AEC nor MAP mode</span></span>                    |



 

<span data-ttu-id="dd01a-124">Это свойство необходимо задать перед использованием схемы DSP для записи голоса.</span><span class="sxs-lookup"><span data-stu-id="dd01a-124">You must set this property before using the Voice Capture DSP.</span></span> <span data-ttu-id="dd01a-125">После задания этого свойства можно использовать DSP с параметрами по умолчанию или задать дополнительные свойства.</span><span class="sxs-lookup"><span data-stu-id="dd01a-125">After you set this property, you can use the DSP with its default settings, or set additional properties.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd01a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="dd01a-126">Requirements</span></span>



| <span data-ttu-id="dd01a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="dd01a-127">Requirement</span></span> | <span data-ttu-id="dd01a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="dd01a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd01a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd01a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dd01a-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="dd01a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="dd01a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd01a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dd01a-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="dd01a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dd01a-133">Header</span><span class="sxs-lookup"><span data-stu-id="dd01a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd01a-134"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd01a-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd01a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd01a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd01a-136">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="dd01a-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="dd01a-137">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="dd01a-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
