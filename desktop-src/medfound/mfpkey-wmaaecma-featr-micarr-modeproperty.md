---
description: Указывает, каким способом в DSP записи голоса выполняется обработка массивов микрофона.
ms.assetid: 5e04fe50-d764-4497-9999-37279e156204
title: Свойство MFPKEY_WMAAECMA_FEATR_MICARR_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25bf8ffcae465e8abfddedb3e6d6dded683bb2bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263526"
---
# <a name="mfpkey_wmaaecma_featr_micarr_mode-property"></a><span data-ttu-id="7c33f-103">МФПКЭЙ \_ вмааекма \_ феатр \_ mode микарр, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="7c33f-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE Property</span></span>

<span data-ttu-id="7c33f-104">Указывает, каким способом в DSP записи голоса выполняется обработка массивов микрофона.</span><span class="sxs-lookup"><span data-stu-id="7c33f-104">Specifies how the Voice Capture DSP performs microphone array processing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="7c33f-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="7c33f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="7c33f-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="7c33f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="7c33f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7c33f-107">Data Type</span></span>

<span data-ttu-id="7c33f-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7c33f-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="7c33f-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="7c33f-109">Default Value</span></span>

<span data-ttu-id="7c33f-110">\_ \_ однообразная микаррай</span><span class="sxs-lookup"><span data-stu-id="7c33f-110">MICARRAY\_SINGLE\_BEAM</span></span>

## <a name="applies-to"></a><span data-ttu-id="7c33f-111">Применение</span><span class="sxs-lookup"><span data-stu-id="7c33f-111">Applies To</span></span>

-   [<span data-ttu-id="7c33f-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="7c33f-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="7c33f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7c33f-113">Remarks</span></span>

<span data-ttu-id="7c33f-114">Значение этого свойства является членом перечисления [ \_ \_ режима массива MIC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) .</span><span class="sxs-lookup"><span data-stu-id="7c33f-114">The value of this property is a member of the [MIC\_ARRAY\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-mic_array_mode) enumeration.</span></span> <span data-ttu-id="7c33f-115">Значение по умолчанию — МИКАРРАЙ \_ Single- \_ образная.</span><span class="sxs-lookup"><span data-stu-id="7c33f-115">The default value is MICARRAY\_SINGLE\_BEAM.</span></span> <span data-ttu-id="7c33f-116">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="7c33f-116">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="7c33f-117">DSP использует это свойство только в том случае, если включена обработка массива микрофона.</span><span class="sxs-lookup"><span data-stu-id="7c33f-117">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c33f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7c33f-118">Requirements</span></span>



| <span data-ttu-id="7c33f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7c33f-119">Requirement</span></span> | <span data-ttu-id="7c33f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7c33f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c33f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7c33f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7c33f-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7c33f-122">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7c33f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7c33f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7c33f-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7c33f-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7c33f-125">Header</span><span class="sxs-lookup"><span data-stu-id="7c33f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c33f-126"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c33f-126"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c33f-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7c33f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c33f-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7c33f-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="7c33f-129">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="7c33f-129">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
