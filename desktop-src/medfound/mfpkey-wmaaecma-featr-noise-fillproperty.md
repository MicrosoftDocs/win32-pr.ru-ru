---
description: Указывает, выполняется ли заполнение сигнала DSP для записи речи.
ms.assetid: 8bb64686-8f02-4e0d-a664-aeee1744fc8e
title: Свойство MFPKEY_WMAAECMA_FEATR_NOISE_FILL (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c0af2b47767a7798d9b583ac55ad5112ddf1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701814"
---
# <a name="mfpkey_wmaaecma_featr_noise_fill-property"></a><span data-ttu-id="63331-103">МФПКЭЙ \_ вмааекма \_ Феатр \_ , \_ свойство заливки шума</span><span class="sxs-lookup"><span data-stu-id="63331-103">MFPKEY\_WMAAECMA\_FEATR\_NOISE\_FILL Property</span></span>

<span data-ttu-id="63331-104">Указывает, выполняется ли заполнение сигнала DSP для записи речи.</span><span class="sxs-lookup"><span data-stu-id="63331-104">Specifies whether the Voice Capture DSP performs noise filling.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="63331-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="63331-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="63331-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="63331-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="63331-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="63331-107">Data Type</span></span>

<span data-ttu-id="63331-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="63331-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="63331-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="63331-109">Default Value</span></span>

<span data-ttu-id="63331-110">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="63331-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="63331-111">Применение</span><span class="sxs-lookup"><span data-stu-id="63331-111">Applies To</span></span>

-   [<span data-ttu-id="63331-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="63331-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="63331-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="63331-113">Remarks</span></span>

<span data-ttu-id="63331-114">При заполнении шума в части сигнала добавляется небольшой шум, при котором обрезка по центру удалила остаточные выводы.</span><span class="sxs-lookup"><span data-stu-id="63331-114">Noise filling adds a small amount of noise to portions of the signal where center clipping has removed the residual echoes.</span></span> <span data-ttu-id="63331-115">Это приводит к повышению удобства работы пользователя, чем при отсутствии пропусков в сигнале.</span><span class="sxs-lookup"><span data-stu-id="63331-115">This results in a better experience for the user than leaving silent gaps in the signal.</span></span>

<span data-ttu-id="63331-116">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="63331-116">This property can have the following values.</span></span>



| <span data-ttu-id="63331-117">Значение</span><span class="sxs-lookup"><span data-stu-id="63331-117">Value</span></span>          | <span data-ttu-id="63331-118">Описание</span><span class="sxs-lookup"><span data-stu-id="63331-118">Description</span></span>            |
|----------------|------------------------|
| <span data-ttu-id="63331-119">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="63331-119">VARIANT\_TRUE</span></span>  | <span data-ttu-id="63331-120">Включить заполнение шума.</span><span class="sxs-lookup"><span data-stu-id="63331-120">Enable noise filling.</span></span>  |
| <span data-ttu-id="63331-121">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="63331-121">VARIANT\_FALSE</span></span> | <span data-ttu-id="63331-122">Отключить заполнение шума.</span><span class="sxs-lookup"><span data-stu-id="63331-122">Disable noise filling.</span></span> |



 

<span data-ttu-id="63331-123">Значением этого свойства по умолчанию является вариант \_ true (включено).</span><span class="sxs-lookup"><span data-stu-id="63331-123">The default value of this property is VARIANT\_TRUE (enabled).</span></span> <span data-ttu-id="63331-124">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="63331-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

<span data-ttu-id="63331-125">DSP использует это свойство только в том случае, если включена обработка AEC.</span><span class="sxs-lookup"><span data-stu-id="63331-125">The DSP uses this property only when AEC processing is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="63331-126">Требования</span><span class="sxs-lookup"><span data-stu-id="63331-126">Requirements</span></span>



| <span data-ttu-id="63331-127">Требование</span><span class="sxs-lookup"><span data-stu-id="63331-127">Requirement</span></span> | <span data-ttu-id="63331-128">Значение</span><span class="sxs-lookup"><span data-stu-id="63331-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63331-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="63331-129">Minimum supported client</span></span><br/> | <span data-ttu-id="63331-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="63331-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="63331-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="63331-131">Minimum supported server</span></span><br/> | <span data-ttu-id="63331-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="63331-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="63331-133">Header</span><span class="sxs-lookup"><span data-stu-id="63331-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="63331-134"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="63331-134"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63331-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="63331-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63331-136">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="63331-136">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="63331-137">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="63331-137">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
