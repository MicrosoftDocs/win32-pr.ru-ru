---
title: IMsRdpClientNonScriptable4 Публишерцертификатечаин, свойство
description: Управляет цепочкой сертификатов издателя. Цепочка хранится в варианте типа VT \_ ByRef, который содержит указатель на \_ структуру контекста цепочки сертификатов \_ . Сведения о \_ структурах VT ByRef см. в разделе Variant и VARIANTARG.
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Публишерцертификатечаин
- Службы удаленных рабочих столов свойства Публишерцертификатечаин, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Публишерцертификатечаин
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892205"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a><span data-ttu-id="aa911-118">IMsRdpClientNonScriptable4: свойство Ублишерцертификатечаин:P</span><span class="sxs-lookup"><span data-stu-id="aa911-118">IMsRdpClientNonScriptable4::PublisherCertificateChain property</span></span>

<span data-ttu-id="aa911-119">Управляет цепочкой сертификатов издателя.</span><span class="sxs-lookup"><span data-stu-id="aa911-119">Controls the publisher certificate chain.</span></span> <span data-ttu-id="aa911-120">Цепочка хранится в варианте типа **VT \_ ByRef** , который содержит указатель на структуру [**\_ \_ контекста цепочки сертификатов**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="aa911-120">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span> <span data-ttu-id="aa911-121">Сведения о структурах **VT \_ ByRef** см. в разделе [Variant и VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="aa911-121">For information about **VT\_BYREF** structures, see [VARIANT and VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="aa911-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="aa911-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa911-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aa911-123">Syntax</span></span>


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a><span data-ttu-id="aa911-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="aa911-124">Property value</span></span>

<span data-ttu-id="aa911-125">Задает цепочку сертификатов издателя.</span><span class="sxs-lookup"><span data-stu-id="aa911-125">Sets the publisher certificate chain.</span></span> <span data-ttu-id="aa911-126">Цепочка хранится в варианте типа **VT \_ ByRef** , который содержит указатель на структуру [**\_ \_ контекста цепочки сертификатов**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) .</span><span class="sxs-lookup"><span data-stu-id="aa911-126">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="aa911-127">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="aa911-127">Error codes</span></span>

<span data-ttu-id="aa911-128">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="aa911-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa911-129">Требования</span><span class="sxs-lookup"><span data-stu-id="aa911-129">Requirements</span></span>



| <span data-ttu-id="aa911-130">Требование</span><span class="sxs-lookup"><span data-stu-id="aa911-130">Requirement</span></span> | <span data-ttu-id="aa911-131">Значение</span><span class="sxs-lookup"><span data-stu-id="aa911-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa911-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aa911-132">Minimum supported client</span></span><br/> | <span data-ttu-id="aa911-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa911-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="aa911-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aa911-134">Minimum supported server</span></span><br/> | <span data-ttu-id="aa911-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa911-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="aa911-136">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="aa911-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="aa911-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa911-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="aa911-138">DLL</span><span class="sxs-lookup"><span data-stu-id="aa911-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa911-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa911-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="aa911-140">IID</span><span class="sxs-lookup"><span data-stu-id="aa911-140">IID</span></span><br/>                      | <span data-ttu-id="aa911-141">IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="aa911-141">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa911-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aa911-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa911-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="aa911-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="aa911-144">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="aa911-144">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

