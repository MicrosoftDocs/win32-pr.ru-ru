---
title: Имстскакс Циферстренгс, свойство
description: Возвращает максимальную стойкость шифрования текущего элемента управления.
ms.assetid: 94efe3e5-4074-4187-b58a-b812f37f3622
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс Имстскакс
- Службы удаленных рабочих столов интерфейса Имстскакс, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс Имсрдпклиент
- Службы удаленных рабочих столов интерфейса Имсрдпклиент, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient2
- Службы удаленных рабочих столов интерфейса IMsRdpClient2, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient3
- Службы удаленных рабочих столов интерфейса IMsRdpClient3, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient4
- Службы удаленных рабочих столов интерфейса IMsRdpClient4, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient5
- Службы удаленных рабочих столов интерфейса IMsRdpClient5, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient6
- Службы удаленных рабочих столов интерфейса IMsRdpClient6, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient7
- Службы удаленных рабочих столов интерфейса IMsRdpClient7, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient8
- Службы удаленных рабочих столов интерфейса IMsRdpClient8, свойство Циферстренгс
- Службы удаленных рабочих столов свойства Циферстренгс, интерфейс IMsRdpClient9
- Службы удаленных рабочих столов интерфейса IMsRdpClient9, свойство Циферстренгс
topic_type:
- apiref
api_name:
- IMsTscAx.CipherStrength
- IMsTscAx.get_CipherStrength
- IMsRdpClient.CipherStrength
- IMsRdpClient.get_CipherStrength
- IMsRdpClient2.CipherStrength
- IMsRdpClient2.get_CipherStrength
- IMsRdpClient3.CipherStrength
- IMsRdpClient3.get_CipherStrength
- IMsRdpClient4.CipherStrength
- IMsRdpClient4.get_CipherStrength
- IMsRdpClient5.CipherStrength
- IMsRdpClient5.get_CipherStrength
- IMsRdpClient6.CipherStrength
- IMsRdpClient6.get_CipherStrength
- IMsRdpClient7.CipherStrength
- IMsRdpClient7.get_CipherStrength
- IMsRdpClient8.CipherStrength
- IMsRdpClient8.get_CipherStrength
- IMsRdpClient9.CipherStrength
- IMsRdpClient9.get_CipherStrength
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401cf3796d349aaa6764eae46a371a9d485f763c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414908"
---
# <a name="imstscaxcipherstrength-property"></a><span data-ttu-id="07b0a-124">Свойство Имстскакс:: Циферстренгс</span><span class="sxs-lookup"><span data-stu-id="07b0a-124">IMsTscAx::CipherStrength property</span></span>

<span data-ttu-id="07b0a-125">Возвращает максимальную стойкость шифрования текущего элемента управления.</span><span class="sxs-lookup"><span data-stu-id="07b0a-125">Retrieves the maximum encryption strength of the current control.</span></span>

<span data-ttu-id="07b0a-126">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="07b0a-126">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07b0a-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="07b0a-127">Syntax</span></span>


```C++
HRESULT get_CipherStrength(
  [out] LONG *pCipherStrength
);
```



## <a name="property-value"></a><span data-ttu-id="07b0a-128">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="07b0a-128">Property value</span></span>

<span data-ttu-id="07b0a-129">Стойкость шифрования.</span><span class="sxs-lookup"><span data-stu-id="07b0a-129">The encryption strength.</span></span>

## <a name="error-codes"></a><span data-ttu-id="07b0a-130">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="07b0a-130">Error codes</span></span>

<span data-ttu-id="07b0a-131">В случае успеха возвратите значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="07b0a-131">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="07b0a-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="07b0a-132">Remarks</span></span>

<span data-ttu-id="07b0a-133">Для веб-подключение к удаленному рабочему столу стойкость шифра всегда 128, так как элемент управления ActiveX удаленный рабочий стол поддерживает шифрование до 128 бит.</span><span class="sxs-lookup"><span data-stu-id="07b0a-133">For Remote Desktop Web Connection, the cipher strength is always 128 because the Remote Desktop ActiveX control supports encryption up to and including 128 bits.</span></span> <span data-ttu-id="07b0a-134">128-разрядный элемент управления по-прежнему может подключаться к 56 разрядного шифрования удаленный рабочий стол серверов узла сеансов удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="07b0a-134">The 128-bit control can still connect to 56 bit encryption Remote Desktop Session Host (RD Session Host) servers.</span></span>

<span data-ttu-id="07b0a-135">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="07b0a-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="07b0a-136">Требования</span><span class="sxs-lookup"><span data-stu-id="07b0a-136">Requirements</span></span>



| <span data-ttu-id="07b0a-137">Требование</span><span class="sxs-lookup"><span data-stu-id="07b0a-137">Requirement</span></span> | <span data-ttu-id="07b0a-138">Значение</span><span class="sxs-lookup"><span data-stu-id="07b0a-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="07b0a-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="07b0a-139">Minimum supported client</span></span><br/> | <span data-ttu-id="07b0a-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07b0a-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="07b0a-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="07b0a-141">Minimum supported server</span></span><br/> | <span data-ttu-id="07b0a-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07b0a-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="07b0a-143">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="07b0a-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="07b0a-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07b0a-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07b0a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="07b0a-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07b0a-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07b0a-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="07b0a-147">IID</span><span class="sxs-lookup"><span data-stu-id="07b0a-147">IID</span></span><br/>                      | <span data-ttu-id="07b0a-148">IID \_ имстскакс определен как 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span><span class="sxs-lookup"><span data-stu-id="07b0a-148">IID\_IMsTscAx is defined as 8C11EFAE-92C3-11D1-BC1E-00C04FA31489</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="07b0a-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="07b0a-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07b0a-150">**имсрдпклиент**</span><span class="sxs-lookup"><span data-stu-id="07b0a-150">**IMsRdpClient**</span></span>](imsrdpclient-interface.md)
</dt> <dt>

[<span data-ttu-id="07b0a-151">**IMsRdpClient2**</span><span class="sxs-lookup"><span data-stu-id="07b0a-151">**IMsRdpClient2**</span></span>](imsrdpclient2.md)
</dt> <dt>

[<span data-ttu-id="07b0a-152">**IMsRdpClient3**</span><span class="sxs-lookup"><span data-stu-id="07b0a-152">**IMsRdpClient3**</span></span>](imsrdpclient3.md)
</dt> <dt>

[<span data-ttu-id="07b0a-153">**IMsRdpClient4**</span><span class="sxs-lookup"><span data-stu-id="07b0a-153">**IMsRdpClient4**</span></span>](imsrdpclient4.md)
</dt> <dt>

[<span data-ttu-id="07b0a-154">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="07b0a-154">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="07b0a-155">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="07b0a-155">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="07b0a-156">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="07b0a-156">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="07b0a-157">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="07b0a-157">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="07b0a-158">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="07b0a-158">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="07b0a-159">**имстскакс**</span><span class="sxs-lookup"><span data-stu-id="07b0a-159">**IMsTscAx**</span></span>](imstscax-interface.md)
</dt> </dl>

 

 





