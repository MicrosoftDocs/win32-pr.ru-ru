---
title: IMsRdpClientNonScriptable3 Неготиатесекуритилайер, свойство
description: Указывает или получает значение, указывающее, включен ли уровень безопасности согласования для соединения.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Неготиатесекуритилайер
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672667"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a><span data-ttu-id="7df99-120">Свойство IMsRdpClientNonScriptable3:: Неготиатесекуритилайер</span><span class="sxs-lookup"><span data-stu-id="7df99-120">IMsRdpClientNonScriptable3::NegotiateSecurityLayer property</span></span>

<span data-ttu-id="7df99-121">Указывает или получает значение, указывающее, включен ли уровень безопасности согласования для соединения.</span><span class="sxs-lookup"><span data-stu-id="7df99-121">Specifies or retrieves whether the negotiation security layer is enabled for the connection.</span></span>

<span data-ttu-id="7df99-122">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="7df99-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df99-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7df99-123">Syntax</span></span>


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a><span data-ttu-id="7df99-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="7df99-124">Property value</span></span>

<span data-ttu-id="7df99-125">Указывает, следует ли включить согласование уровня безопасности.</span><span class="sxs-lookup"><span data-stu-id="7df99-125">Specifies whether to enable negotiation of the security layer.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df99-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7df99-126">Remarks</span></span>

<span data-ttu-id="7df99-127">Если это свойство имеет значение **Variant \_ FALSE** и проверка подлинности на уровне сети (NLA) включено в клиентской операционной системе, клиент не будет согласовывать уровень безопасности и вместо этого будет использовать NLA для защиты RDP-подключения.</span><span class="sxs-lookup"><span data-stu-id="7df99-127">If this property is set to **VARIANT\_FALSE** and Network Level Authentication (NLA) is enabled on the client operating system, the client will not negotiate the security layer and instead, it will use NLA to secure the RDP connection.</span></span> <span data-ttu-id="7df99-128">Если для этого свойства задано **значение \_ true**, клиент будет согласовываться между NLA и базовой безопасностью RDP.</span><span class="sxs-lookup"><span data-stu-id="7df99-128">If this property is set to **VARIANT\_TRUE**, then the client will negotiate between NLA and basic RDP security.</span></span>

> [!Note]  
> <span data-ttu-id="7df99-129">Отключение согласования уровня безопасности возможно только при подключении к серверу узла сеансов удаленный рабочий стол (к узлу сеансов удаленных рабочих столов) под управлением Windows Vista или более поздних операционных систем.</span><span class="sxs-lookup"><span data-stu-id="7df99-129">Disabling security layer negotiation is only possible when connecting to a Remote Desktop Session Host (RD Session Host) server running Windows Vista or later operating systems.</span></span> <span data-ttu-id="7df99-130">Если это свойство включено и клиент пытается подключиться к серверу узла сеансов удаленных рабочих столов под управлением более ранней операционной системы, произойдет сбой подключения.</span><span class="sxs-lookup"><span data-stu-id="7df99-130">If this property is enabled and the client attempts to connect to an RD Session Host server running an earlier operating system, the connection will fail.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7df99-131">Требования</span><span class="sxs-lookup"><span data-stu-id="7df99-131">Requirements</span></span>



| <span data-ttu-id="7df99-132">Требование</span><span class="sxs-lookup"><span data-stu-id="7df99-132">Requirement</span></span> | <span data-ttu-id="7df99-133">Значение</span><span class="sxs-lookup"><span data-stu-id="7df99-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df99-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7df99-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7df99-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7df99-135">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="7df99-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7df99-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7df99-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7df99-137">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="7df99-138">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="7df99-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="7df99-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7df99-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7df99-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7df99-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7df99-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7df99-141"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="7df99-142">IID</span><span class="sxs-lookup"><span data-stu-id="7df99-142">IID</span></span><br/>                      | <span data-ttu-id="7df99-143">IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="7df99-143">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7df99-144">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7df99-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df99-145">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="7df99-145">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="7df99-146">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="7df99-146">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="7df99-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="7df99-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





