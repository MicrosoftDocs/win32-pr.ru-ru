---
description: Указывает, что текущий кадр кодируется с помощью одного или нескольких фреймов LTR.
ms.assetid: 51FD6E36-9CDF-4005-942F-7A92CA706F38
title: Свойство CODECAPI_AVEncVideoUseLTRFrame (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252933180e8212c94c3c2b2442397c53d0f9c559
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808165"
---
# <a name="codecapi_avencvideouseltrframe-property"></a><span data-ttu-id="b663a-103">КОДЕКАПИ \_ авенквидеауселтрфраме, свойство</span><span class="sxs-lookup"><span data-stu-id="b663a-103">CODECAPI\_AVEncVideoUseLTRFrame property</span></span>

<span data-ttu-id="b663a-104">Указывает, что текущий кадр кодируется с помощью одного или нескольких фреймов LTR.</span><span class="sxs-lookup"><span data-stu-id="b663a-104">Specifies that the current frame is encoded using one or multiple LTR frames.</span></span>

## <a name="data-type"></a><span data-ttu-id="b663a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b663a-105">Data type</span></span>

<span data-ttu-id="b663a-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="b663a-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="b663a-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="b663a-107">Property GUID</span></span>

<span data-ttu-id="b663a-108">**КОДЕКАПИ \_ авенквидеауселтрфраме**</span><span class="sxs-lookup"><span data-stu-id="b663a-108">**CODECAPI\_AVEncVideoUseLTRFrame**</span></span>

## <a name="property-value"></a><span data-ttu-id="b663a-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b663a-109">Property value</span></span>

<span data-ttu-id="b663a-110">Значение этого элемента управления включает два поля, где каждое поле имеет 16 бит.</span><span class="sxs-lookup"><span data-stu-id="b663a-110">The value of this control includes two fields, where each field has 16 bits.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b663a-111">Значение</span><span class="sxs-lookup"><span data-stu-id="b663a-111">Value</span></span></th>
<th><span data-ttu-id="b663a-112">Значение</span><span class="sxs-lookup"><span data-stu-id="b663a-112">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <span data-ttu-id="b663a-113"><dt><strong>Первое поле</strong></dt> <dt>битов [0.. 15]</dt> </span><span class="sxs-lookup"><span data-stu-id="b663a-113"><dt><strong>The first field</strong></dt> <dt>Bits[0..15]</dt> </span></span></dl></td>
<td><span data-ttu-id="b663a-114">Указывает, какие фреймы LTR разрешено использовать для кодирования текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="b663a-114">Indicates which LTR frame(s) are allowed for encoding the current frame.</span></span> <br/> <span data-ttu-id="b663a-115"><strong>Кодировщики H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="b663a-115"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="b663a-116">Это битовая карта, указывающая, какие кадры LTR можно использовать в качестве ссылки на этот кадр.</span><span class="sxs-lookup"><span data-stu-id="b663a-116">This is a bitmap that indicates which LTR frames can be used as a reference for this frame.</span></span> <span data-ttu-id="b663a-117">Младший значащий бит соответствует индексу LTR 0, второй наименее значащий бит соответствует индексу LTR 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="b663a-117">The least significant bit corresponds to LTR index 0, the second least significant bit corresponds to LTR index 1, etc.</span></span><br/> <span data-ttu-id="b663a-118">Это значение не должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="b663a-118">This value shall not be 0.</span></span><br/> <span data-ttu-id="b663a-119">Наибольший индекс, заданный этим значением, не должен превышать максимальное число кадров LTR, указанное в свойстве <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> меньше одного.</span><span class="sxs-lookup"><span data-stu-id="b663a-119">The highest index specified by this value shall not be greater than the maximum number of LTR frames specified in the <a href="codecapi-avencvideoltrbuffercontrol.md">CODECAPI_AVEncVideoLTRBufferControl</a> property less one.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <span data-ttu-id="b663a-120"><dt><strong>Второе поле</strong></dt> <dt>битов [16.. 31]</dt> </span><span class="sxs-lookup"><span data-stu-id="b663a-120"><dt><strong>The second field</strong></dt> <dt>Bits[16..31]</dt> </span></span></dl></td>
<td><span data-ttu-id="b663a-121">Флаг, указывающий, требуются ли дополнительные ограничения для кодирования последующих кадров.</span><span class="sxs-lookup"><span data-stu-id="b663a-121">Flag that indicates whether additional limitations are required for encoding subsequent frames.</span></span> <br/> <span data-ttu-id="b663a-122"><strong>Кодировщики H. 264/AVC:</strong></span><span class="sxs-lookup"><span data-stu-id="b663a-122"><strong>H.264/AVC encoders:</strong></span></span><br/> <span data-ttu-id="b663a-123">1 является единственным допустимым значением для этого поля.</span><span class="sxs-lookup"><span data-stu-id="b663a-123">1 is on the only valid value for this field.</span></span> <span data-ttu-id="b663a-124">Все остальные значения являются недопустимыми и зарезервированы для будущего использования.</span><span class="sxs-lookup"><span data-stu-id="b663a-124">All other values are invalid and reserved for future use.</span></span><br/> <span data-ttu-id="b663a-125">Если флаг равен 1, кодировщик должен закодировать последующие кадры в порядке кодировки в соответствии со следующими ограничениями:</span><span class="sxs-lookup"><span data-stu-id="b663a-125">When the flag is 1, the encoder shall encode subsequent frames in encoding order subject to the following constraints:</span></span><br/>
<ul>
<li><span data-ttu-id="b663a-126">Он не должен использовать краткосрочные ссылочные кадры в порядке кодировки, отличном от текущего кадра, или в будущем кодировке в порядке кодировки.</span><span class="sxs-lookup"><span data-stu-id="b663a-126">It shall not use short term reference frames in encoding order older than the current frame or future encoding in encoding order.</span></span></li>
<li><span data-ttu-id="b663a-127">Он не должен использовать кадры LTR, не описанные в последнем элементе управления CODECAPI_AVEncVideoUseLTRFrame.</span><span class="sxs-lookup"><span data-stu-id="b663a-127">It shall not use LTR frames not described by the most recent CODECAPI_AVEncVideoUseLTRFrame control.</span></span></li>
<li><span data-ttu-id="b663a-128">Он может использовать фреймы LTR, обновленные после текущего кадра.</span><span class="sxs-lookup"><span data-stu-id="b663a-128">It may use LTR frames updated after the current frame.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="b663a-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b663a-129">Remarks</span></span>

<span data-ttu-id="b663a-130">**Кодировщики H. 264/AVC:**</span><span class="sxs-lookup"><span data-stu-id="b663a-130">**H.264/AVC encoders:**</span></span>

<span data-ttu-id="b663a-131">Это свойство не должно вызываться, если отложенный вызов, использующий кадр LTR, был вызван с помощью \_ Свойства кодекапи авенквидеауселтрфраме, а кодировщик еще не создал кадр, в котором использовался LTR.</span><span class="sxs-lookup"><span data-stu-id="b663a-131">This property should not be called if a pending call to use an LTR frame has been issued using the CODECAPI\_AVEncVideoUseLTRFrame property and the encoder has not yet generated a frame that has used the LTR.</span></span> <span data-ttu-id="b663a-132">Иными словами, кодировщик не должен ставить в очередь запросы КОДЕКАПИ \_ авенквидеауселтрфраме.</span><span class="sxs-lookup"><span data-stu-id="b663a-132">In other words, the encoder should not queue up CODECAPI\_AVEncVideoUseLTRFrame requests.</span></span>

<span data-ttu-id="b663a-133">Если запрос КОДЕКАПИ \_ авенквидеауселтрфраме отправляется, когда другой \_ запрос кодекапи авенквидеауселтрфраме все еще находится в состоянии ожидания, то старый запрос следует удалить.</span><span class="sxs-lookup"><span data-stu-id="b663a-133">If a CODECAPI\_AVEncVideoUseLTRFrame request is submitted while another CODECAPI\_AVEncVideoUseLTRFrame request is still pending, then the older request should be dropped.</span></span>

<span data-ttu-id="b663a-134">Вызов КОДЕКАПИ \_ авенквидеауселтрфраме в кадре небазового слоя является допустимым и применяется к кадру, не являющемуся базовым, без задержки в кадре базового слоя.</span><span class="sxs-lookup"><span data-stu-id="b663a-134">Calling CODECAPI\_AVEncVideoUseLTRFrame on a non-base layer frame is valid and shall apply to the non-base layer frame, without delay to a base layer frame.</span></span>

## <a name="requirements"></a><span data-ttu-id="b663a-135">Требования</span><span class="sxs-lookup"><span data-stu-id="b663a-135">Requirements</span></span>



| <span data-ttu-id="b663a-136">Требование</span><span class="sxs-lookup"><span data-stu-id="b663a-136">Requirement</span></span> | <span data-ttu-id="b663a-137">Значение</span><span class="sxs-lookup"><span data-stu-id="b663a-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b663a-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b663a-138">Minimum supported client</span></span><br/> | <span data-ttu-id="b663a-139">\[Приложения UWP для классических приложений Windows 8.1 \|\]</span><span class="sxs-lookup"><span data-stu-id="b663a-139">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                   |
| <span data-ttu-id="b663a-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b663a-140">Minimum supported server</span></span><br/> | <span data-ttu-id="b663a-141">\[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="b663a-141">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="b663a-142">Header</span><span class="sxs-lookup"><span data-stu-id="b663a-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="b663a-143"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="b663a-143"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b663a-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b663a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b663a-145">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b663a-145">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




