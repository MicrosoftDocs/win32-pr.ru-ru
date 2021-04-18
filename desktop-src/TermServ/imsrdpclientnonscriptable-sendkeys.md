---
title: Имсрдпклиентнонскриптабле SendKeys, метод
description: Отправляет в элемент управления ряд нажатий клавиш. Нажатия клавиш находятся в форме кода сканирования, которая является данными клавиатуры из фактических физических ключей.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- Метод SendKeys службы удаленных рабочих столов
- Метод SendKeys службы удаленных рабочих столов, интерфейс Имсрдпклиентнонскриптабле
- Службы удаленных рабочих столов интерфейса Имсрдпклиентнонскриптабле, метод SendKeys
- Метод SendKeys службы удаленных рабочих столов, интерфейс IMsRdpClientNonScriptable2
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable2, метод SendKeys
- Метод SendKeys службы удаленных рабочих столов, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, метод SendKeys
- Метод SendKeys службы удаленных рабочих столов, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, метод SendKeys
- Метод SendKeys службы удаленных рабочих столов, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, метод SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491658"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a><span data-ttu-id="090b0-115">Метод Имсрдпклиентнонскриптабле:: SendKeys</span><span class="sxs-lookup"><span data-stu-id="090b0-115">IMsRdpClientNonScriptable::SendKeys method</span></span>

<span data-ttu-id="090b0-116">Отправляет в элемент управления ряд нажатий клавиш.</span><span class="sxs-lookup"><span data-stu-id="090b0-116">Sends a series of keystrokes to the control.</span></span> <span data-ttu-id="090b0-117">Нажатия клавиш находятся в форме кода сканирования, которая является данными клавиатуры из фактических физических ключей.</span><span class="sxs-lookup"><span data-stu-id="090b0-117">The keystrokes are in scan code form, which is the keyboard data from the actual physical keys.</span></span>

## <a name="syntax"></a><span data-ttu-id="090b0-118">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="090b0-118">Syntax</span></span>


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="090b0-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="090b0-119">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090b0-120">*нумкэйс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="090b0-120">*numKeys* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090b0-121">Количество нажатий клавиш для отправки.</span><span class="sxs-lookup"><span data-stu-id="090b0-121">The number of keystrokes to send.</span></span> <span data-ttu-id="090b0-122">Максимальное число ключей, которые могут быть отправлены в одной операции, равно 20.</span><span class="sxs-lookup"><span data-stu-id="090b0-122">The maximum number of keys that can be sent in one operation is 20.</span></span> <span data-ttu-id="090b0-123">Метод возвращает **E \_ INVALIDARG** , если этот параметр больше 20.</span><span class="sxs-lookup"><span data-stu-id="090b0-123">The method returns **E\_INVALIDARG** if this parameter is greater than 20.</span></span> <span data-ttu-id="090b0-124">Дополнительные сведения см. в разделе "Примечания".</span><span class="sxs-lookup"><span data-stu-id="090b0-124">For more information, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="090b0-125">*пбаррайкэйуп* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="090b0-125">*pbArrayKeyUp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090b0-126">Массив, размер которого равен *нумкэйс*.</span><span class="sxs-lookup"><span data-stu-id="090b0-126">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="090b0-127">Элемент имеет **значение true** , если соответствующий ключ имеет значение up, и **false** , если соответствующий ключ не работает.</span><span class="sxs-lookup"><span data-stu-id="090b0-127">An element is **TRUE** if the corresponding key is UP and **FALSE** if the corresponding key is DOWN.</span></span>

</dd> <dt>

<span data-ttu-id="090b0-128">*плкэйдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="090b0-128">*plKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="090b0-129">Массив, размер которого равен *нумкэйс*.</span><span class="sxs-lookup"><span data-stu-id="090b0-129">An array whose size is equal to *numKeys*.</span></span> <span data-ttu-id="090b0-130">Массив содержит данные о нажатии клавиш и соответствует значению параметра *lParam* сообщения [WM \_ KeyDown](../inputdev/wm-keydown.md) .</span><span class="sxs-lookup"><span data-stu-id="090b0-130">The array contains keystroke data and corresponds to the value of the *lParam* parameter of the [WM\_KEYDOWN](../inputdev/wm-keydown.md) message.</span></span> <span data-ttu-id="090b0-131">Данные указывают число повторов, код сканирования, флаг расширенного ключа, код контекста, предыдущий флаг состояния ключа и флаг состояния перехода.</span><span class="sxs-lookup"><span data-stu-id="090b0-131">The data specifies the repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span> <span data-ttu-id="090b0-132">Описание битов в этом массиве см. в разделе [WM \_ KeyDown](../inputdev/wm-keydown.md).</span><span class="sxs-lookup"><span data-stu-id="090b0-132">For a description of the bits in this array, see [WM\_KEYDOWN](../inputdev/wm-keydown.md).</span></span>

<span data-ttu-id="090b0-133">Соответствующий элемент в *пбаррайкэйуп* указывает, что ключ имеет значение up или Down.</span><span class="sxs-lookup"><span data-stu-id="090b0-133">The corresponding element in *pbArrayKeyUp* indicates if the key is UP or DOWN.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090b0-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="090b0-134">Return value</span></span>

<span data-ttu-id="090b0-135">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="090b0-135">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="090b0-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="090b0-136">Remarks</span></span>

<span data-ttu-id="090b0-137">Метод **SendKeys** не использует сочетания клавиш, сделанные локальным пользователем, с нажатиями клавиш, которые отправляет метод.</span><span class="sxs-lookup"><span data-stu-id="090b0-137">The **SendKeys** method does not mix keystrokes made by the local user with keystrokes that the method is sending.</span></span> <span data-ttu-id="090b0-138">Все нажатия клавиш, передаваемые в метод, отправляются в удаленный сеанс в одной атомарной последовательности.</span><span class="sxs-lookup"><span data-stu-id="090b0-138">All keystrokes passed to the method are sent to the remote session in a single atomic sequence.</span></span>

<span data-ttu-id="090b0-139">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="090b0-139">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="090b0-140">Требования</span><span class="sxs-lookup"><span data-stu-id="090b0-140">Requirements</span></span>



| <span data-ttu-id="090b0-141">Требование</span><span class="sxs-lookup"><span data-stu-id="090b0-141">Requirement</span></span> | <span data-ttu-id="090b0-142">Значение</span><span class="sxs-lookup"><span data-stu-id="090b0-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="090b0-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="090b0-143">Minimum supported client</span></span><br/> | <span data-ttu-id="090b0-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="090b0-144">Windows Vista</span></span><br/>                                                                     |
| <span data-ttu-id="090b0-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="090b0-145">Minimum supported server</span></span><br/> | <span data-ttu-id="090b0-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="090b0-146">Windows Server 2008</span></span><br/>                                                               |
| <span data-ttu-id="090b0-147">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="090b0-147">Type library</span></span><br/>             | <dl> <span data-ttu-id="090b0-148"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="090b0-148"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="090b0-149">DLL</span><span class="sxs-lookup"><span data-stu-id="090b0-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="090b0-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="090b0-150"><dt>MsTscAx.dll</dt></span></span> </dl>       |
| <span data-ttu-id="090b0-151">IID</span><span class="sxs-lookup"><span data-stu-id="090b0-151">IID</span></span><br/>                      | <span data-ttu-id="090b0-152">IID \_ имсрдпклиентнонскриптабле определен как 2f079c4c-87B2-4afd-97ab-20cdb43038ae</span><span class="sxs-lookup"><span data-stu-id="090b0-152">IID\_IMsRdpClientNonScriptable is defined as 2f079c4c-87b2-4afd-97ab-20cdb43038ae</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="090b0-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="090b0-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090b0-154">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="090b0-154">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="090b0-155">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="090b0-155">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="090b0-156">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="090b0-156">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="090b0-157">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="090b0-157">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="090b0-158">**имсрдпклиентнонскриптабле**</span><span class="sxs-lookup"><span data-stu-id="090b0-158">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="090b0-159">WM \_ KeyDown</span><span class="sxs-lookup"><span data-stu-id="090b0-159">WM\_KEYDOWN</span></span>](../inputdev/wm-keydown.md)
</dt> </dl>

 

