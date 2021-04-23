---
description: Указывает, выполняет ли подавление шума при захвате голоса DSP.
ms.assetid: d63e9ac1-9584-4f74-8404-c95d17eb8c2d
title: Свойство MFPKEY_WMAAECMA_FEATR_NS (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02218ce621123066e5e61435d93f8539de95e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701813"
---
# <a name="mfpkey_wmaaecma_featr_ns-property"></a><span data-ttu-id="39c26-103">МФПКЭЙ \_ вмааекма \_ Феатр, \_ свойство NS</span><span class="sxs-lookup"><span data-stu-id="39c26-103">MFPKEY\_WMAAECMA\_FEATR\_NS Property</span></span>

<span data-ttu-id="39c26-104">Указывает, выполняет ли подавление шума при захвате голоса DSP.</span><span class="sxs-lookup"><span data-stu-id="39c26-104">Specifies whether the Voice Capture DSP performs noise suppression.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="39c26-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="39c26-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="39c26-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="39c26-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="39c26-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="39c26-107">Data Type</span></span>

<span data-ttu-id="39c26-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="39c26-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="39c26-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="39c26-109">Default Value</span></span>

<span data-ttu-id="39c26-110">1</span><span class="sxs-lookup"><span data-stu-id="39c26-110">1</span></span>

## <a name="applies-to"></a><span data-ttu-id="39c26-111">Применение</span><span class="sxs-lookup"><span data-stu-id="39c26-111">Applies To</span></span>

-   [<span data-ttu-id="39c26-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="39c26-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="39c26-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39c26-113">Remarks</span></span>

<span data-ttu-id="39c26-114">Подавление шума является компонентом обработки цифровых сигналов (DSP), который подавляет или сокращает стационарные фоновые шумы в звуковом сигнале.</span><span class="sxs-lookup"><span data-stu-id="39c26-114">Noise suppression is a digital signal processing (DSP) component that suppresses or reduces stationary background noise in the audio signal.</span></span> <span data-ttu-id="39c26-115">Подавление шума применяется после подавления акустического эха (AEC) и обработки массива микрофона.</span><span class="sxs-lookup"><span data-stu-id="39c26-115">Noise suppression is applied after the acoustic echo cancellation (AEC) and microphone array processing.</span></span>

<span data-ttu-id="39c26-116">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="39c26-116">This property can have the following values.</span></span>



| <span data-ttu-id="39c26-117">Значение</span><span class="sxs-lookup"><span data-stu-id="39c26-117">Value</span></span> | <span data-ttu-id="39c26-118">Описание</span><span class="sxs-lookup"><span data-stu-id="39c26-118">Description</span></span>                |
|-------|----------------------------|
| <span data-ttu-id="39c26-119">0</span><span class="sxs-lookup"><span data-stu-id="39c26-119">0</span></span>     | <span data-ttu-id="39c26-120">Отключить подавление шума.</span><span class="sxs-lookup"><span data-stu-id="39c26-120">Disable noise suppression.</span></span> |
| <span data-ttu-id="39c26-121">1</span><span class="sxs-lookup"><span data-stu-id="39c26-121">1</span></span>     | <span data-ttu-id="39c26-122">Включить подавление шума.</span><span class="sxs-lookup"><span data-stu-id="39c26-122">Enable noise suppression.</span></span>  |



 

<span data-ttu-id="39c26-123">Значение этого свойства по умолчанию равно 1 (включено).</span><span class="sxs-lookup"><span data-stu-id="39c26-123">The default value of this property is 1 (enabled).</span></span> <span data-ttu-id="39c26-124">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="39c26-124">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c26-125">Требования</span><span class="sxs-lookup"><span data-stu-id="39c26-125">Requirements</span></span>



| <span data-ttu-id="39c26-126">Требование</span><span class="sxs-lookup"><span data-stu-id="39c26-126">Requirement</span></span> | <span data-ttu-id="39c26-127">Значение</span><span class="sxs-lookup"><span data-stu-id="39c26-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39c26-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="39c26-128">Minimum supported client</span></span><br/> | <span data-ttu-id="39c26-129">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39c26-129">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="39c26-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="39c26-130">Minimum supported server</span></span><br/> | <span data-ttu-id="39c26-131">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="39c26-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="39c26-132">Header</span><span class="sxs-lookup"><span data-stu-id="39c26-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="39c26-133"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="39c26-133"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c26-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="39c26-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c26-135">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="39c26-135">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="39c26-136">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="39c26-136">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
