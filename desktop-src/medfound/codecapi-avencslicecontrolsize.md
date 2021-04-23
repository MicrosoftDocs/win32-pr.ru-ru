---
description: Задает размер среза в мегабайтах (МБ), битах или MB.
ms.assetid: 42E7DB19-9FB9-4226-B0B5-97AD6B9C0E12
title: Свойство CODECAPI_AVEncSliceControlSize (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e4c3e58fa34922941ea564d42e449cefd798ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143243"
---
# <a name="codecapi_avencslicecontrolsize-property"></a><span data-ttu-id="2965e-103">КОДЕКАПИ \_ авенкслицеконтролсизе, свойство</span><span class="sxs-lookup"><span data-stu-id="2965e-103">CODECAPI\_AVEncSliceControlSize property</span></span>

<span data-ttu-id="2965e-104">Задает размер среза в мегабайтах (МБ), битах или MB.</span><span class="sxs-lookup"><span data-stu-id="2965e-104">Specifies the size of the slice in units of megabyte (MB), bits, or MB row.</span></span>

## <a name="data-type"></a><span data-ttu-id="2965e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2965e-105">Data type</span></span>

<span data-ttu-id="2965e-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="2965e-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="2965e-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="2965e-107">Property GUID</span></span>

<span data-ttu-id="2965e-108">**КОДЕКАПИ \_ авенкслицеконтролсизе**</span><span class="sxs-lookup"><span data-stu-id="2965e-108">**CODECAPI\_AVEncSliceControlSize**</span></span>

## <a name="remarks"></a><span data-ttu-id="2965e-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2965e-109">Remarks</span></span>

<span data-ttu-id="2965e-110">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="2965e-110">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="2965e-111">Значение параметра КОДЕКАПИ \_ авенкслицеконтролсизе управляется свойством [кодекапи \_ авенкслицеконтролмоде](codecapi-avencslicecontrolmode.md) .</span><span class="sxs-lookup"><span data-stu-id="2965e-111">The meaning of the value of CODECAPI\_AVEncSliceControlSize is controlled by the [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md) property.</span></span> <span data-ttu-id="2965e-112">В следующей таблице показано, как \_ Свойства кодекапи авенкслицеконтролсизе и кодекапи \_ авенкслицеконтролмоде управляют размером и количеством срезов в кадре.</span><span class="sxs-lookup"><span data-stu-id="2965e-112">The following table illustrates how the CODECAPI\_AVEncSliceControlSize and CODECAPI\_AVEncSliceControlMode properties control the size and number of slices in a frame.</span></span>



| <span data-ttu-id="2965e-113">\_Параметр АВЕНКСЛИЦЕКОНТРОЛМОДЕ кодекапи</span><span class="sxs-lookup"><span data-stu-id="2965e-113">CODECAPI\_AVEncSliceControlMode setting</span></span> | <span data-ttu-id="2965e-114">Смысл значения</span><span class="sxs-lookup"><span data-stu-id="2965e-114">Meaning of value</span></span>                                                                                                                                                                                                                                                                                                                                                                                           |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2965e-115">0</span><span class="sxs-lookup"><span data-stu-id="2965e-115">0</span></span>                                       | <span data-ttu-id="2965e-116">Это целое число, указывающее размер каждого среза в кадре в единицах макроблоккс.</span><span class="sxs-lookup"><span data-stu-id="2965e-116">This is an integer that indicates the size of each slice in the frame in units of macroblocks.</span></span> <br/> <span data-ttu-id="2965e-117">Кодировщик должен отклонить параметр, если значение больше числа макроблоккс в кадре.</span><span class="sxs-lookup"><span data-stu-id="2965e-117">The encoder should reject the setting when the value is greater than the number of macroblocks in the frame.</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="2965e-118">1</span><span class="sxs-lookup"><span data-stu-id="2965e-118">1</span></span>                                       | <span data-ttu-id="2965e-119">Это целое число, которое указывает размер каждого среза в кадре в единицах битов.</span><span class="sxs-lookup"><span data-stu-id="2965e-119">This is an integer that indicates the size of each slice in the frame in units of bits.</span></span> <br/> <span data-ttu-id="2965e-120">Кодировщик должен запустить новый срез на макроблокк, который приводит к превышению этого значения числом битов в срезе (поэтому размер каждого среза всегда будет меньше или равен этому значению).</span><span class="sxs-lookup"><span data-stu-id="2965e-120">The encoder should start a new slice at the macroblock that causes the number of bits in the slice to exceed this value (so the size of each slice will always be less than or equal than this value).</span></span> <span data-ttu-id="2965e-121">Это означает, что размер последнего среза может быть значительно меньше этого значения.</span><span class="sxs-lookup"><span data-stu-id="2965e-121">This means that the last slice size could be significantly smaller than this value.</span></span> <br/> |
| <span data-ttu-id="2965e-122">2</span><span class="sxs-lookup"><span data-stu-id="2965e-122">2</span></span>                                       | <span data-ttu-id="2965e-123">Это целое число, указывающее размер каждого среза в кадре в единицах макроблокк строк.</span><span class="sxs-lookup"><span data-stu-id="2965e-123">This is an integer that indicates the size of each slice in the frame in units of macroblock rows.</span></span> <br/> <span data-ttu-id="2965e-124">Кодировщик должен отклонить параметр, если значение больше числа строк макроблокк в кадре.</span><span class="sxs-lookup"><span data-stu-id="2965e-124">The encoder should reject the setting when the value is greater than the number of macroblock rows in the frame.</span></span><br/>                                                                                                                                                                 |



 

<span data-ttu-id="2965e-125">Если приложение не устанавливает значение для [кодекапи \_ авенкслицеконтролмоде](codecapi-avencslicecontrolmode.md), кодировщик должен вернуть ошибку.</span><span class="sxs-lookup"><span data-stu-id="2965e-125">If the application does not set a value for [CODECAPI\_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md), the encoder should return an error.</span></span>

<span data-ttu-id="2965e-126">Рекомендуемое значение по умолчанию — наличие одного среза для всего фрейма.</span><span class="sxs-lookup"><span data-stu-id="2965e-126">The recommended default is to have a single slice for whole frame.</span></span>

<span data-ttu-id="2965e-127">Некоторые Кодировщики могут параллельно кодировать срезы, и производительность может зависеть от параметров элемента управления "срез".</span><span class="sxs-lookup"><span data-stu-id="2965e-127">Some encoders might encode slices in parallel and so performance could be affected depending on the slice control settings.</span></span> <span data-ttu-id="2965e-128">Например, кодирование кадра в виде одного среза может быть медленнее, чем при кодировании кадра как нескольких срезов.</span><span class="sxs-lookup"><span data-stu-id="2965e-128">For example, encoding a frame as a single slice might be slower than if the frame was encoded as multiple slices.</span></span>

<span data-ttu-id="2965e-129">Параметры элемента управления среза являются динамическими и могут быть изменены во время сеанса кодирования.</span><span class="sxs-lookup"><span data-stu-id="2965e-129">The slice control settings are dynamic and can be changed during the encoding session.</span></span>

## <a name="requirements"></a><span data-ttu-id="2965e-130">Требования</span><span class="sxs-lookup"><span data-stu-id="2965e-130">Requirements</span></span>



| <span data-ttu-id="2965e-131">Требование</span><span class="sxs-lookup"><span data-stu-id="2965e-131">Requirement</span></span> | <span data-ttu-id="2965e-132">Значение</span><span class="sxs-lookup"><span data-stu-id="2965e-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2965e-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2965e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2965e-134">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="2965e-134">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="2965e-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2965e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2965e-136">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="2965e-136">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2965e-137">Header</span><span class="sxs-lookup"><span data-stu-id="2965e-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2965e-138"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="2965e-138"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2965e-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2965e-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2965e-140">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2965e-140">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




