---
description: 'Задает режим элемента управления "срез". Допустимые значения: 0, 1, и 2.'
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: Свойство CODECAPI_AVEncSliceControlMode (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990842"
---
# <a name="codecapi_avencslicecontrolmode-property"></a><span data-ttu-id="3ae31-104">КОДЕКАПИ \_ авенкслицеконтролмоде, свойство</span><span class="sxs-lookup"><span data-stu-id="3ae31-104">CODECAPI\_AVEncSliceControlMode property</span></span>

<span data-ttu-id="3ae31-105">Задает режим элемента управления "срез".</span><span class="sxs-lookup"><span data-stu-id="3ae31-105">Specifies the slice control mode.</span></span> <span data-ttu-id="3ae31-106">Допустимые значения: 0, 1, и 2.</span><span class="sxs-lookup"><span data-stu-id="3ae31-106">Valid values are 0, 1, and 2.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ae31-107">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3ae31-107">Data type</span></span>

<span data-ttu-id="3ae31-108">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="3ae31-108">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="3ae31-109">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="3ae31-109">Property GUID</span></span>

<span data-ttu-id="3ae31-110">**КОДЕКАПИ \_ авенкслицеконтролмоде**</span><span class="sxs-lookup"><span data-stu-id="3ae31-110">**CODECAPI\_AVEncSliceControlMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="3ae31-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3ae31-111">Property value</span></span>

<span data-ttu-id="3ae31-112">Значения режима элемента управления среза:</span><span class="sxs-lookup"><span data-stu-id="3ae31-112">Slice control mode values:</span></span>



| <span data-ttu-id="3ae31-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3ae31-113">Value</span></span>                                                                        | <span data-ttu-id="3ae31-114">Значение</span><span class="sxs-lookup"><span data-stu-id="3ae31-114">Meaning</span></span>                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ae31-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3ae31-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="3ae31-116">Установка этого значения равным 0 означает, что свойство [кодекапи \_ авенкслицеконтролсизе](codecapi-avencslicecontrolsize.md) будет указывать размер среза в единицах макроблоккс на срез.</span><span class="sxs-lookup"><span data-stu-id="3ae31-116">Setting this value to 0 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblocks per slice.</span></span><br/>     |
| <dl> <span data-ttu-id="3ae31-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3ae31-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="3ae31-118">Установка этого значения равным 1 означает, что свойство [кодекапи \_ авенкслицеконтролсизе](codecapi-avencslicecontrolsize.md) будет указывать размер среза в единицах на срез.</span><span class="sxs-lookup"><span data-stu-id="3ae31-118">Setting this value to 1 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of bits per slice.</span></span><br/>            |
| <dl> <span data-ttu-id="3ae31-119"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3ae31-119"><dt>2</dt></span></span> </dl> | <span data-ttu-id="3ae31-120">Установка этого значения равным 2 означает, что свойство [кодекапи \_ авенкслицеконтролсизе](codecapi-avencslicecontrolsize.md) будет указывать размер среза в единицах макроблокк строк на срез.</span><span class="sxs-lookup"><span data-stu-id="3ae31-120">Setting this value to 2 indicates that the [CODECAPI\_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) property will specify the slice size in units of macroblock rows per slice.</span></span><br/> |



 

<span data-ttu-id="3ae31-121">Кодировщик Возвращает поддерживаемые им значения.</span><span class="sxs-lookup"><span data-stu-id="3ae31-121">The encoder returns the values that it supports.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ae31-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ae31-122">Remarks</span></span>

<span data-ttu-id="3ae31-123">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="3ae31-123">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="3ae31-124">Рекомендуется, чтобы кодировщик поддерживал [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)и [**жетпараметерранже**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="3ae31-124">It is recommended that the encoder supports [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue), [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue), and [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

<span data-ttu-id="3ae31-125">Если [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) не вызывается для кодекапи \_ Авенкслицеконтролмоде, метод [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) for Кодекапи \_ авенкслицеконтролмоде может возвращать **VFW \_ E \_ кодекапи \_ No \_ Current \_ value**.</span><span class="sxs-lookup"><span data-stu-id="3ae31-125">If [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) is not called for CODECAPI\_AVEncSliceControlMode, [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) for CODECAPI\_AVEncSliceControlMode can return **VFW\_E\_CODECAPI\_NO\_CURRENT\_VALUE**.</span></span> <span data-ttu-id="3ae31-126">Параметр [**noreturn может**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) возвращать **VFW \_ E \_ кодекапи \_ No \_ по умолчанию** для кодекапи \_ авенкслицеконтролмоде.</span><span class="sxs-lookup"><span data-stu-id="3ae31-126">[**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) may return **VFW\_E\_CODECAPI\_NO\_DEFAULT** for CODECAPI\_AVEncSliceControlMode.</span></span>

<span data-ttu-id="3ae31-127">Рекомендуемое значение по умолчанию — 2 (размер в МБ на одну строку на срез).</span><span class="sxs-lookup"><span data-stu-id="3ae31-127">Recommended default value is 2 (size in MB row per slice).</span></span>

<span data-ttu-id="3ae31-128">Это статический интерфейс API, что означает, что приложение будет изменяться при выполнении кодировщика.</span><span class="sxs-lookup"><span data-stu-id="3ae31-128">This is a static API, which means the application won t change this while the encoder is running.</span></span>

## <a name="examples"></a><span data-ttu-id="3ae31-129">Примеры</span><span class="sxs-lookup"><span data-stu-id="3ae31-129">Examples</span></span>


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a><span data-ttu-id="3ae31-130">Требования</span><span class="sxs-lookup"><span data-stu-id="3ae31-130">Requirements</span></span>



| <span data-ttu-id="3ae31-131">Требование</span><span class="sxs-lookup"><span data-stu-id="3ae31-131">Requirement</span></span> | <span data-ttu-id="3ae31-132">Значение</span><span class="sxs-lookup"><span data-stu-id="3ae31-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae31-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ae31-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae31-134">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="3ae31-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="3ae31-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ae31-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae31-136">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="3ae31-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="3ae31-137">Header</span><span class="sxs-lookup"><span data-stu-id="3ae31-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ae31-138"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ae31-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ae31-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ae31-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ae31-140">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ae31-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

