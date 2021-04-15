---
title: IMsRdpClientNonScriptable4 Маркрдпсеттингссекуре, свойство
description: Указывает, помечены ли параметры протокол удаленного рабочего стола (RDP) как безопасные.
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Маркрдпсеттингссекуре
- Службы удаленных рабочих столов свойства Маркрдпсеттингссекуре, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Маркрдпсеттингссекуре
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534451"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a><span data-ttu-id="6fdcf-116">Свойство IMsRdpClientNonScriptable4:: Маркрдпсеттингссекуре</span><span class="sxs-lookup"><span data-stu-id="6fdcf-116">IMsRdpClientNonScriptable4::MarkRdpSettingsSecure property</span></span>

<span data-ttu-id="6fdcf-117">Указывает, помечены ли параметры [протокол удаленного рабочего стола](remote-desktop-protocol.md) (RDP) как безопасные.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-117">Specifies whether [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) settings are marked as secure.</span></span> <span data-ttu-id="6fdcf-118">Это означает, что параметры, применяемые к элементу управления, были подписаны сторонним или доверенным издателем.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-118">This indicates that the settings applied to the control have been signed by a third-party or trusted publisher.</span></span>

<span data-ttu-id="6fdcf-119">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-119">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fdcf-120">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6fdcf-120">Syntax</span></span>


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a><span data-ttu-id="6fdcf-121">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6fdcf-121">Property value</span></span>

<span data-ttu-id="6fdcf-122">Указывает, помечены ли параметры RDP как безопасные.</span><span class="sxs-lookup"><span data-stu-id="6fdcf-122">Sets whether RDP settings are marked as secure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6fdcf-123">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="6fdcf-123">Error codes</span></span>

<span data-ttu-id="6fdcf-124">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="6fdcf-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fdcf-125">Требования</span><span class="sxs-lookup"><span data-stu-id="6fdcf-125">Requirements</span></span>



| <span data-ttu-id="6fdcf-126">Требование</span><span class="sxs-lookup"><span data-stu-id="6fdcf-126">Requirement</span></span> | <span data-ttu-id="6fdcf-127">Значение</span><span class="sxs-lookup"><span data-stu-id="6fdcf-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fdcf-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fdcf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="6fdcf-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fdcf-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6fdcf-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fdcf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="6fdcf-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fdcf-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6fdcf-132">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="6fdcf-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="6fdcf-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fdcf-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="6fdcf-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6fdcf-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fdcf-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fdcf-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="6fdcf-136">IID</span><span class="sxs-lookup"><span data-stu-id="6fdcf-136">IID</span></span><br/>                      | <span data-ttu-id="6fdcf-137">IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="6fdcf-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6fdcf-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fdcf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fdcf-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="6fdcf-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="6fdcf-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





