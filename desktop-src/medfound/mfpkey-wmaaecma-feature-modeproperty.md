---
description: Позволяет приложению переопределять параметры по умолчанию в различных свойствах схемы DSP для записи речи.
ms.assetid: 1c11e817-36bd-4a5d-9c2b-6a91e86f623f
title: Свойство MFPKEY_WMAAECMA_FEATURE_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9a47ef86a2acf83131800e9cb55b86de2cd3d98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811620"
---
# <a name="mfpkey_wmaaecma_feature_mode-property"></a><span data-ttu-id="1940f-103">\_ \_ Свойство режима компонента мфпкэй вмааекма \_</span><span class="sxs-lookup"><span data-stu-id="1940f-103">MFPKEY\_WMAAECMA\_FEATURE\_MODE Property</span></span>

<span data-ttu-id="1940f-104">Позволяет приложению переопределять параметры по умолчанию в различных свойствах схемы DSP для записи речи.</span><span class="sxs-lookup"><span data-stu-id="1940f-104">Enables the application to override the default settings on various properties of the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="1940f-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="1940f-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="1940f-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="1940f-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="1940f-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="1940f-107">Data Type</span></span>

<span data-ttu-id="1940f-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="1940f-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="1940f-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="1940f-109">Default Value</span></span>

<span data-ttu-id="1940f-110">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="1940f-110">VARIANT\_FALSE</span></span>

## <a name="applies-to"></a><span data-ttu-id="1940f-111">Применение</span><span class="sxs-lookup"><span data-stu-id="1940f-111">Applies To</span></span>

-   [<span data-ttu-id="1940f-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="1940f-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="1940f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1940f-113">Remarks</span></span>

<span data-ttu-id="1940f-114">Если это свойство имеет значение VARIANT \_ true, приложение может установить следующие свойства в DSP:</span><span class="sxs-lookup"><span data-stu-id="1940f-114">If this property is VARIANT\_TRUE, the application can set the following properties on the DSP:</span></span>

-   [<span data-ttu-id="1940f-115">МФПКЭЙ \_ вмааекма \_ феатр \_ AES</span><span class="sxs-lookup"><span data-stu-id="1940f-115">MFPKEY\_WMAAECMA\_FEATR\_AES</span></span>](mfpkey-wmaaecma-featr-aesproperty.md)
-   [<span data-ttu-id="1940f-116">МФПКЭЙ \_ вмааекма \_ феатр \_ АГК</span><span class="sxs-lookup"><span data-stu-id="1940f-116">MFPKEY\_WMAAECMA\_FEATR\_AGC</span></span>](mfpkey-wmaaecma-featr-agcproperty.md)
-   [<span data-ttu-id="1940f-117">МФПКЭЙ \_ вмааекма \_ феатр \_ \_</span><span class="sxs-lookup"><span data-stu-id="1940f-117">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP</span></span>](mfpkey-wmaaecma-featr-center-clipproperty.md)
-   [<span data-ttu-id="1940f-118">МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Длина эхо</span><span class="sxs-lookup"><span data-stu-id="1940f-118">MFPKEY\_WMAAECMA\_FEATR\_ECHO\_LENGTH</span></span>](mfpkey-wmaaecma-featr-echo-lengthproperty.md)
-   [<span data-ttu-id="1940f-119">МФПКЭЙ \_ вмааекма \_ феатр \_ \_ Размер кадра</span><span class="sxs-lookup"><span data-stu-id="1940f-119">MFPKEY\_WMAAECMA\_FEATR\_FRAME\_SIZE</span></span>](mfpkey-wmaaecma-featr-frame-sizeproperty.md)
-   [<span data-ttu-id="1940f-120">МФПКЭЙ \_ вмааекма \_ феатр \_ микарр \_ mode</span><span class="sxs-lookup"><span data-stu-id="1940f-120">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_MODE</span></span>](mfpkey-wmaaecma-featr-micarr-modeproperty.md)
-   [<span data-ttu-id="1940f-121">МФПКЭЙ \_ вмааекма \_ феатр \_ микарр \_</span><span class="sxs-lookup"><span data-stu-id="1940f-121">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC</span></span>](mfpkey-wmaaecma-featr-micarr-preprocproperty.md)
-   [<span data-ttu-id="1940f-122">МФПКЭЙ \_ вмааекма \_ феатр \_ , \_ Заливка шума</span><span class="sxs-lookup"><span data-stu-id="1940f-122">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL</span></span>](mfpkey-wmaaecma-featr-noise-fillproperty.md)
-   [<span data-ttu-id="1940f-123">МФПКЭЙ \_ вмааекма \_ феатр \_ NS</span><span class="sxs-lookup"><span data-stu-id="1940f-123">MFPKEY\_WMAAECMA\_FEATR\_NS</span></span>](mfpkey-wmaaecma-featr-nsproperty.md)
-   [<span data-ttu-id="1940f-124">МФПКЭЙ \_ вмааекма \_ феатр \_ Вад</span><span class="sxs-lookup"><span data-stu-id="1940f-124">MFPKEY\_WMAAECMA\_FEATR\_VAD</span></span>](mfpkey-wmaaecma-featr-vadproperty.md)

<span data-ttu-id="1940f-125">Если это свойство имеет значение VARIANT \_ false, то DSP игнорирует эти свойства и использует параметры по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1940f-125">If this property is VARIANT\_FALSE, the DSP ignores these properties and uses its default settings.</span></span> <span data-ttu-id="1940f-126">Значение этого свойства по умолчанию — VARIANT \_ false.</span><span class="sxs-lookup"><span data-stu-id="1940f-126">The default value of this property is VARIANT\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="1940f-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1940f-127">Requirements</span></span>



| <span data-ttu-id="1940f-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1940f-128">Requirement</span></span> | <span data-ttu-id="1940f-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1940f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1940f-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1940f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1940f-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1940f-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1940f-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1940f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1940f-133">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1940f-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1940f-134">Header</span><span class="sxs-lookup"><span data-stu-id="1940f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1940f-135"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="1940f-135"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1940f-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1940f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1940f-137">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1940f-137">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="1940f-138">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="1940f-138">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
