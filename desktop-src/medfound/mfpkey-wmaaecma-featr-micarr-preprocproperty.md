---
description: Указывает, выполняет ли система DSP для записи голоса предварительную обработку массива микрофонов.
ms.assetid: 0f197165-e6e5-456b-9615-1edc8ada7bb5
title: Свойство MFPKEY_WMAAECMA_FEATR_MICARR_PREPROC (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f992d8d26ba547eb1b5d1eac470536a963209f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701815"
---
# <a name="mfpkey_wmaaecma_featr_micarr_preproc-property"></a><span data-ttu-id="a1569-103">МФПКЭЙ \_ вмааекма \_ феатр \_ микарр, \_ свойство</span><span class="sxs-lookup"><span data-stu-id="a1569-103">MFPKEY\_WMAAECMA\_FEATR\_MICARR\_PREPROC Property</span></span>

<span data-ttu-id="a1569-104">Указывает, выполняет ли система DSP для записи голоса предварительную обработку массива микрофонов.</span><span class="sxs-lookup"><span data-stu-id="a1569-104">Specifies whether the Voice Capture DSP performs microphone array preprocessing.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="a1569-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="a1569-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="a1569-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="a1569-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="a1569-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a1569-107">Data Type</span></span>

<span data-ttu-id="a1569-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="a1569-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="a1569-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a1569-109">Default Value</span></span>

<span data-ttu-id="a1569-110">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="a1569-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="a1569-111">Применение</span><span class="sxs-lookup"><span data-stu-id="a1569-111">Applies To</span></span>

-   [<span data-ttu-id="a1569-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="a1569-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="a1569-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a1569-113">Remarks</span></span>

<span data-ttu-id="a1569-114">Предварительная обработка может удалить стационарные звуки, мешающие обработке, например тон с фиксированным шагом.</span><span class="sxs-lookup"><span data-stu-id="a1569-114">Preprocessing can remove stationary tones that interfere with processing, such as a tone with a fixed pitch.</span></span>

<span data-ttu-id="a1569-115">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="a1569-115">This property can have the following values.</span></span>



| <span data-ttu-id="a1569-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a1569-116">Value</span></span>          | <span data-ttu-id="a1569-117">Описание</span><span class="sxs-lookup"><span data-stu-id="a1569-117">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="a1569-118">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="a1569-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="a1569-119">Отключить предварительную обработку.</span><span class="sxs-lookup"><span data-stu-id="a1569-119">Disable preprocessing.</span></span> |
| <span data-ttu-id="a1569-120">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="a1569-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="a1569-121">Включить предварительную обработку.</span><span class="sxs-lookup"><span data-stu-id="a1569-121">Enable preprocessing.</span></span>  |



 

<span data-ttu-id="a1569-122">Значением этого свойства по умолчанию является вариант \_ true (включено).</span><span class="sxs-lookup"><span data-stu-id="a1569-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="a1569-123">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="a1569-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="a1569-124">DSP использует это свойство только в том случае, если включена обработка массива микрофона.</span><span class="sxs-lookup"><span data-stu-id="a1569-124">The DSP uses this property only when microphone array processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1569-125">Требования</span><span class="sxs-lookup"><span data-stu-id="a1569-125">Requirements</span></span>



| <span data-ttu-id="a1569-126">Требование</span><span class="sxs-lookup"><span data-stu-id="a1569-126">Requirement</span></span> | <span data-ttu-id="a1569-127">Значение</span><span class="sxs-lookup"><span data-stu-id="a1569-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1569-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1569-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a1569-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1569-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="a1569-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1569-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a1569-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1569-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a1569-132">Header</span><span class="sxs-lookup"><span data-stu-id="a1569-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1569-133"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1569-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1569-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a1569-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1569-135">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a1569-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="a1569-136">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="a1569-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
