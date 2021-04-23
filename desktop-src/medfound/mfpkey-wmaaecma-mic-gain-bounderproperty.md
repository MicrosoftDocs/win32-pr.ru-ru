---
description: Указывает, применяет ли схема DSP для записи голоса ограничение на усиление микрофона.
ms.assetid: b9f0bcc7-57ab-4339-bf1d-2b12c8744f01
title: Свойство MFPKEY_WMAAECMA_MIC_GAIN_BOUNDER (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c1b09f2095f5accb44e4e0edaff2b8c94941d3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701811"
---
# <a name="mfpkey_wmaaecma_mic_gain_bounder-property"></a><span data-ttu-id="96dec-103">МФПКЭЙ \_ Вмааекма \_ \_ свойство "граница усиления микрофона" \_</span><span class="sxs-lookup"><span data-stu-id="96dec-103">MFPKEY\_WMAAECMA\_MIC\_GAIN\_BOUNDER Property</span></span>

<span data-ttu-id="96dec-104">Указывает, применяет ли схема DSP для записи голоса ограничение на усиление микрофона.</span><span class="sxs-lookup"><span data-stu-id="96dec-104">Specifies whether the Voice Capture DSP applies microphone gain bounding.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="96dec-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="96dec-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="96dec-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="96dec-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="96dec-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="96dec-107">Data Type</span></span>

<span data-ttu-id="96dec-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="96dec-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="96dec-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="96dec-109">Default Value</span></span>

<span data-ttu-id="96dec-110">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="96dec-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="96dec-111">Применение</span><span class="sxs-lookup"><span data-stu-id="96dec-111">Applies To</span></span>

-   [<span data-ttu-id="96dec-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="96dec-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="96dec-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="96dec-113">Remarks</span></span>

<span data-ttu-id="96dec-114">Граница усиления микрофона обеспечивает правильный уровень прибыли микрофона.</span><span class="sxs-lookup"><span data-stu-id="96dec-114">Microphone gain bounding ensures that the microphone has the correct level of gain.</span></span> <span data-ttu-id="96dec-115">Если увеличение слишком велико, захваченный сигнал может быть перегружен и будет обрезан.</span><span class="sxs-lookup"><span data-stu-id="96dec-115">If gain is too high, the captured signal might be saturated and will be clipped.</span></span> <span data-ttu-id="96dec-116">Обрезка — это нелинейный результат, который приведет к сбою алгоритма отмены акустического эха (AEC).</span><span class="sxs-lookup"><span data-stu-id="96dec-116">Clipping is a non-linear effect, which will cause the acoustic echo cancellation (AEC) algorithm to fail.</span></span> <span data-ttu-id="96dec-117">Если увеличение слишком мало, то коэффициент передачи сигнала на шум низкий, что также может привести к сбою или неправильному выполнению алгоритма AEC.</span><span class="sxs-lookup"><span data-stu-id="96dec-117">If the gain is too low, the signal-to-noise ratio is low, which can also cause the AEC algorithm to fail or not perform well.</span></span>

<span data-ttu-id="96dec-118">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="96dec-118">This property can have the following values.</span></span>



| <span data-ttu-id="96dec-119">Значение</span><span class="sxs-lookup"><span data-stu-id="96dec-119">Value</span></span>          | <span data-ttu-id="96dec-120">Описание</span><span class="sxs-lookup"><span data-stu-id="96dec-120">Description</span></span>                       |
|----------------|-----------------------------------|
| <span data-ttu-id="96dec-121">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="96dec-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="96dec-122">Включить границу усиления микрофона.</span><span class="sxs-lookup"><span data-stu-id="96dec-122">Enable microphone gain bounding.</span></span>  |
| <span data-ttu-id="96dec-123">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="96dec-123">VARIANT\_FALSE</span></span> | <span data-ttu-id="96dec-124">Отключить границу усиления микрофона.</span><span class="sxs-lookup"><span data-stu-id="96dec-124">Disable microphone gain bounding.</span></span> |



 

<span data-ttu-id="96dec-125">Значением этого свойства по умолчанию является вариант \_ true (включено).</span><span class="sxs-lookup"><span data-stu-id="96dec-125">The default value of this property is VARIANT\_TRUE (enabled).</span></span>

<span data-ttu-id="96dec-126">Граница усиления микрофона применяется только в том случае, если DSP работает в режиме исходного кода.</span><span class="sxs-lookup"><span data-stu-id="96dec-126">Microphone gain bounding is applies only when the DSP operates in source mode.</span></span> <span data-ttu-id="96dec-127">В режиме фильтрации приложение должно обеспечить правильный уровень усиления микрофона.</span><span class="sxs-lookup"><span data-stu-id="96dec-127">In filter mode, the application must ensure that the microphone has the correct gain level.</span></span>

## <a name="requirements"></a><span data-ttu-id="96dec-128">Требования</span><span class="sxs-lookup"><span data-stu-id="96dec-128">Requirements</span></span>



| <span data-ttu-id="96dec-129">Требование</span><span class="sxs-lookup"><span data-stu-id="96dec-129">Requirement</span></span> | <span data-ttu-id="96dec-130">Значение</span><span class="sxs-lookup"><span data-stu-id="96dec-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="96dec-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="96dec-131">Minimum supported client</span></span><br/> | <span data-ttu-id="96dec-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="96dec-132">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="96dec-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="96dec-133">Minimum supported server</span></span><br/> | <span data-ttu-id="96dec-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="96dec-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="96dec-135">Header</span><span class="sxs-lookup"><span data-stu-id="96dec-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="96dec-136"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="96dec-136"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96dec-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="96dec-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96dec-138">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="96dec-138">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="96dec-139">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="96dec-139">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
