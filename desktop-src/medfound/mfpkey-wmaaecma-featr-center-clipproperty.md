---
description: Указывает, выполняет ли DSP для записи звука вырезание по центру.
ms.assetid: 6830cadd-fa8d-41e1-ac11-a6c8f2795941
title: Свойство MFPKEY_WMAAECMA_FEATR_CENTER_CLIP (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0936ddfe9e34664e55a20efea35a3c06dd6990e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263528"
---
# <a name="mfpkey_wmaaecma_featr_center_clip-property"></a><span data-ttu-id="46900-103">МФПКЭЙ \_ вмааекма \_ Феатр \_ , \_ свойство Clip</span><span class="sxs-lookup"><span data-stu-id="46900-103">MFPKEY\_WMAAECMA\_FEATR\_CENTER\_CLIP Property</span></span>

<span data-ttu-id="46900-104">Указывает, выполняет ли DSP для записи звука вырезание по центру.</span><span class="sxs-lookup"><span data-stu-id="46900-104">Specifies whether the Voice Capture DSP performs center clipping.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="46900-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="46900-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="46900-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="46900-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="46900-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="46900-107">Data Type</span></span>

<span data-ttu-id="46900-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="46900-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="46900-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="46900-109">Default Value</span></span>

<span data-ttu-id="46900-110">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="46900-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="46900-111">Применение</span><span class="sxs-lookup"><span data-stu-id="46900-111">Applies To</span></span>

-   [<span data-ttu-id="46900-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="46900-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="46900-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46900-113">Remarks</span></span>

<span data-ttu-id="46900-114">Вырезание по центру — это процесс, который удаляет небольшие остатки эха, остающиеся после обработки AEC, в одноразговорных ситуациях (когда речь идет только на одном конце строки).</span><span class="sxs-lookup"><span data-stu-id="46900-114">Center clipping is a process that removes small echo residuals that remain after AEC processing, in single-talk situations (when speech occurs only on one end of the line).</span></span>

<span data-ttu-id="46900-115">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="46900-115">This property can have the following values.</span></span>



| <span data-ttu-id="46900-116">Значение</span><span class="sxs-lookup"><span data-stu-id="46900-116">Value</span></span>          | <span data-ttu-id="46900-117">Описание</span><span class="sxs-lookup"><span data-stu-id="46900-117">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="46900-118">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="46900-118">VARIANT\_FALSE</span></span> | <span data-ttu-id="46900-119">Отключить вырезание по центру.</span><span class="sxs-lookup"><span data-stu-id="46900-119">Disable center clipping.</span></span> |
| <span data-ttu-id="46900-120">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="46900-120">VARIANT\_TRUE</span></span>  | <span data-ttu-id="46900-121">Включить вырезание по центру.</span><span class="sxs-lookup"><span data-stu-id="46900-121">Enable center clipping.</span></span>  |



 

<span data-ttu-id="46900-122">Значением этого свойства по умолчанию является вариант \_ true (включено).</span><span class="sxs-lookup"><span data-stu-id="46900-122">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="46900-123">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="46900-123">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="46900-124">DSP использует это свойство только в том случае, если включена обработка AEC.</span><span class="sxs-lookup"><span data-stu-id="46900-124">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="46900-125">Требования</span><span class="sxs-lookup"><span data-stu-id="46900-125">Requirements</span></span>



| <span data-ttu-id="46900-126">Требование</span><span class="sxs-lookup"><span data-stu-id="46900-126">Requirement</span></span> | <span data-ttu-id="46900-127">Значение</span><span class="sxs-lookup"><span data-stu-id="46900-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46900-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46900-128">Minimum supported client</span></span><br/> | <span data-ttu-id="46900-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46900-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="46900-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46900-130">Minimum supported server</span></span><br/> | <span data-ttu-id="46900-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="46900-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="46900-132">Header</span><span class="sxs-lookup"><span data-stu-id="46900-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="46900-133"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="46900-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46900-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46900-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46900-135">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="46900-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="46900-136">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="46900-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
