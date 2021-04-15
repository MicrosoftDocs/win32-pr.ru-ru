---
description: Указывает тип обнаружения действия голоса, выполняемого DSP.
ms.assetid: 59c8e348-8c08-4cf8-9c72-8d0f4fabc473
title: Свойство MFPKEY_WMAAECMA_FEATR_VAD (Вмкодекдсп. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e41b8ad80d909a0285b266587d02c09c08d794
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701812"
---
# <a name="mfpkey_wmaaecma_featr_vad-property"></a><span data-ttu-id="56ce5-103">МФПКЭЙ \_ вмааекма \_ феатр \_ Вад, свойство</span><span class="sxs-lookup"><span data-stu-id="56ce5-103">MFPKEY\_WMAAECMA\_FEATR\_VAD Property</span></span>

<span data-ttu-id="56ce5-104">Указывает тип обнаружения действия голоса, выполняемого DSP.</span><span class="sxs-lookup"><span data-stu-id="56ce5-104">Specifies the type of voice activity detection that the Voice Capture DSP performs.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="56ce5-105">Константа для Ипропертибаг</span><span class="sxs-lookup"><span data-stu-id="56ce5-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="56ce5-106">Доступно только с помощью [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="56ce5-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="56ce5-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="56ce5-107">Data Type</span></span>

<span data-ttu-id="56ce5-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="56ce5-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="56ce5-109">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="56ce5-109">Default Value</span></span>

<span data-ttu-id="56ce5-110">0</span><span class="sxs-lookup"><span data-stu-id="56ce5-110">0</span></span>

## <a name="applies-to"></a><span data-ttu-id="56ce5-111">Применение</span><span class="sxs-lookup"><span data-stu-id="56ce5-111">Applies To</span></span>

-   [<span data-ttu-id="56ce5-112">DSP для записи речи</span><span class="sxs-lookup"><span data-stu-id="56ce5-112">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="56ce5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56ce5-113">Remarks</span></span>

<span data-ttu-id="56ce5-114">Значение этого свойства является членом перечисления [ \_ Вад \_ режима AEC](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) .</span><span class="sxs-lookup"><span data-stu-id="56ce5-114">The value of this property is a member of the [AEC\_VAD\_MODE](/windows/desktop/api/wmcodecdsp/ne-wmcodecdsp-aec_vad_mode) enumeration.</span></span> <span data-ttu-id="56ce5-115">Выходными данными при обнаружении голосовой активности является число от 0 до 3, вычисляемое для каждого звукового кадра.</span><span class="sxs-lookup"><span data-stu-id="56ce5-115">The output from voice activity detection is a number from 0 to 3, calculated for each audio frame.</span></span> <span data-ttu-id="56ce5-116">DSP кодирует результат в наименьшем бите первых двух звуковых образцов в каждом звуковом кадре.</span><span class="sxs-lookup"><span data-stu-id="56ce5-116">The DSP encodes the result in the lowest bit of the first two audio samples in each audio frame.</span></span> <span data-ttu-id="56ce5-117">Значение этого параметра зависит от указанного режима.</span><span class="sxs-lookup"><span data-stu-id="56ce5-117">The meaning of the value depends on the specified mode.</span></span>

<span data-ttu-id="56ce5-118">В следующем коде показано, как извлечь результаты из звуковых данных.</span><span class="sxs-lookup"><span data-stu-id="56ce5-118">The following code shows how to extract the results from the audio data.</span></span> <span data-ttu-id="56ce5-119">В этом примере *паутпут* является указателем на начало звукового кадра в выходных данных.</span><span class="sxs-lookup"><span data-stu-id="56ce5-119">In this example, *pOutput* is a pointer to the start of an audio frame in the output data.</span></span>


```
int AecDecodeVAD(short *pOutput)
{
    int iVAD = (*pOutput) & 0x01;
    pOutput++;
    iVAD |= (*pOutput << 1) & 0x02;
    return iVAD;
}
```



<span data-ttu-id="56ce5-120">Значение этого свойства по умолчанию равно 0 (отключено).</span><span class="sxs-lookup"><span data-stu-id="56ce5-120">The default value of this property is 0 (disabled).</span></span> <span data-ttu-id="56ce5-121">Перед установкой этого свойства необходимо присвоить свойству [ \_ \_ \_ режима компонента мфпкэй вмааекма](mfpkey-wmaaecma-feature-modeproperty.md) значение Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="56ce5-121">Before setting this property, you must set the [MFPKEY\_WMAAECMA\_FEATURE\_MODE](mfpkey-wmaaecma-feature-modeproperty.md) property to VARIANT\_TRUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="56ce5-122">Требования</span><span class="sxs-lookup"><span data-stu-id="56ce5-122">Requirements</span></span>



| <span data-ttu-id="56ce5-123">Требование</span><span class="sxs-lookup"><span data-stu-id="56ce5-123">Requirement</span></span> | <span data-ttu-id="56ce5-124">Значение</span><span class="sxs-lookup"><span data-stu-id="56ce5-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56ce5-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56ce5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="56ce5-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="56ce5-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="56ce5-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56ce5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="56ce5-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="56ce5-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="56ce5-129">Header</span><span class="sxs-lookup"><span data-stu-id="56ce5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="56ce5-130"><dt>Вмкодекдсп. h</dt></span><span class="sxs-lookup"><span data-stu-id="56ce5-130"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56ce5-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56ce5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56ce5-132">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="56ce5-132">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
