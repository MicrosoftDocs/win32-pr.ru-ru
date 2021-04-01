---
description: Указывает, использует ли DSP для захвата голоса режим исходного кода или режим фильтра.
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: Свойство MFPKEY_WMAAECMA_DMO_SOURCE_MODE (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5749ff1f142603cc45df475caae7bc71182bde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263529"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a><span data-ttu-id="8824e-103">МФПКЭЙ \_ вмааекма \_ DMO \_ , \_ свойство исходного режима</span><span class="sxs-lookup"><span data-stu-id="8824e-103">MFPKEY\_WMAAECMA\_DMO\_SOURCE\_MODE Property</span></span>

<span data-ttu-id="8824e-104">Указывает, использует ли DSP для захвата голоса режим исходного кода или режим фильтра.</span><span class="sxs-lookup"><span data-stu-id="8824e-104">Specifies whether the Voice Capture DSP uses source mode or filter mode.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8824e-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="8824e-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8824e-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="8824e-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8824e-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="8824e-107">Data Type</span></span>

<span data-ttu-id="8824e-108">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="8824e-108">VT\_BOOL</span></span>

## <a name="default-value"></a><span data-ttu-id="8824e-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="8824e-109">Default Value</span></span>

<span data-ttu-id="8824e-110">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="8824e-110">VARIANT\_TRUE</span></span>

## <a name="applies-to"></a><span data-ttu-id="8824e-111">Применение</span><span class="sxs-lookup"><span data-stu-id="8824e-111">Applies To</span></span>

-   [<span data-ttu-id="8824e-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="8824e-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="8824e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8824e-113">Remarks</span></span>

<span data-ttu-id="8824e-114">В режиме исходного кода приложению не требуется передавать входные данные в DSP, так как DSP автоматически извлекает данные с аудио устройств.</span><span class="sxs-lookup"><span data-stu-id="8824e-114">In source mode, the application does not need to send input data to the DSP, because the DSP automatically pulls data from the audio devices.</span></span> <span data-ttu-id="8824e-115">В режиме фильтрации приложение должно отправить входные данные в DSP.</span><span class="sxs-lookup"><span data-stu-id="8824e-115">In filter mode, the application must send the input data to the DSP.</span></span>

<span data-ttu-id="8824e-116">Это свойство может иметь следующие значения.</span><span class="sxs-lookup"><span data-stu-id="8824e-116">This property can have the following values.</span></span>



| <span data-ttu-id="8824e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="8824e-117">Value</span></span>          | <span data-ttu-id="8824e-118">Описание</span><span class="sxs-lookup"><span data-stu-id="8824e-118">Description</span></span>  |
|----------------|--------------|
| <span data-ttu-id="8824e-119">ВАРИАНТ \_ false</span><span class="sxs-lookup"><span data-stu-id="8824e-119">VARIANT\_FALSE</span></span> | <span data-ttu-id="8824e-120">Режим фильтрации.</span><span class="sxs-lookup"><span data-stu-id="8824e-120">Filter mode.</span></span> |
| <span data-ttu-id="8824e-121">ВАРИАНТ \_ true</span><span class="sxs-lookup"><span data-stu-id="8824e-121">VARIANT\_TRUE</span></span>  | <span data-ttu-id="8824e-122">Исходный режим.</span><span class="sxs-lookup"><span data-stu-id="8824e-122">Source mode.</span></span> |



 

> [!Note]  
> <span data-ttu-id="8824e-123">Когда DMO находится в режиме исходного кода, необходимо вызвать метод [**имедиаобжект:: сетаутпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) , чтобы задать формат выходного потока, и не вызывать [**Имедиаобжект:: сетинпуттипе**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) для задания форматов входного потока.</span><span class="sxs-lookup"><span data-stu-id="8824e-123">When the DMO is in source mode, you should only call [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype) to set output stream format, and do not call [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype) to set input stream formats.</span></span> <span data-ttu-id="8824e-124">В противном случае инициализация DMO завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8824e-124">Otherwise DMO initialization will fail.</span></span>

 

<span data-ttu-id="8824e-125">Если это свойство имеет значение VARIANT \_ true, то DSP не имеет входных данных.</span><span class="sxs-lookup"><span data-stu-id="8824e-125">If the value of this property is VARIANT\_TRUE, the DSP has zero inputs.</span></span> <span data-ttu-id="8824e-126">Если значение равно \_ false, то DSP имеет один или два входных параметра в зависимости от значения свойства [ \_ \_ \_ режима системы мфпкэй вмааекма](mfpkey-wmaaecma-system-modeproperty.md) , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="8824e-126">If the value is VARIANT\_FALSE, the DSP has one or two inputs, depending on the value of the [MFPKEY\_WMAAECMA\_SYSTEM\_MODE](mfpkey-wmaaecma-system-modeproperty.md) property, as shown in the following table.</span></span>



| <span data-ttu-id="8824e-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8824e-127">Value</span></span>                     | <span data-ttu-id="8824e-128">Число входов</span><span class="sxs-lookup"><span data-stu-id="8824e-128">Number of inputs</span></span> |
|---------------------------|------------------|
| <span data-ttu-id="8824e-129">\_массив оптибеам \_ и \_ контекст AEC</span><span class="sxs-lookup"><span data-stu-id="8824e-129">OPTIBEAM\_ARRAY\_AND\_AEC</span></span> | <span data-ttu-id="8824e-130">2</span><span class="sxs-lookup"><span data-stu-id="8824e-130">2</span></span>                |
| <span data-ttu-id="8824e-131">\_только массив \_ оптибеам</span><span class="sxs-lookup"><span data-stu-id="8824e-131">OPTIBEAM\_ARRAY\_ONLY</span></span>     | <span data-ttu-id="8824e-132">1</span><span class="sxs-lookup"><span data-stu-id="8824e-132">1</span></span>                |
| <span data-ttu-id="8824e-133">\_ \_ контекст AEC одного канала</span><span class="sxs-lookup"><span data-stu-id="8824e-133">SINGLE\_CHANNEL\_AEC</span></span>      | <span data-ttu-id="8824e-134">2</span><span class="sxs-lookup"><span data-stu-id="8824e-134">2</span></span>                |
| <span data-ttu-id="8824e-135">\_НСАГК одного канала \_</span><span class="sxs-lookup"><span data-stu-id="8824e-135">SINGLE\_CHANNEL\_NSAGC</span></span>    | <span data-ttu-id="8824e-136">1</span><span class="sxs-lookup"><span data-stu-id="8824e-136">1</span></span>                |



 

> [!Note]  
> <span data-ttu-id="8824e-137">Только режимы с одним входом будут работать с фильтром оболочки DMO из API DirectShow 9,0.</span><span class="sxs-lookup"><span data-stu-id="8824e-137">Only modes with a single input will work with the wrapper filter DMO from the DirectShow 9.0 API.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8824e-138">Требования</span><span class="sxs-lookup"><span data-stu-id="8824e-138">Requirements</span></span>



| <span data-ttu-id="8824e-139">Требование</span><span class="sxs-lookup"><span data-stu-id="8824e-139">Requirement</span></span> | <span data-ttu-id="8824e-140">Значение</span><span class="sxs-lookup"><span data-stu-id="8824e-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8824e-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8824e-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8824e-142">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8824e-142">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="8824e-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8824e-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8824e-144">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8824e-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8824e-145">Header</span><span class="sxs-lookup"><span data-stu-id="8824e-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8824e-146"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="8824e-146"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8824e-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8824e-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8824e-148">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8824e-148">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="8824e-149">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="8824e-149">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
