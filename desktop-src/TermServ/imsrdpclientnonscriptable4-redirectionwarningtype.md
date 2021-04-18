---
title: IMsRdpClientNonScriptable4 Редиректионварнингтипе, свойство
description: Управляет присутствием и внешним видом диалогового окна, которое уведомляет пользователя о перенаправлении.
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Редиректионварнингтипе
- Службы удаленных рабочих столов свойства Редиректионварнингтипе, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Редиректионварнингтипе
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681934"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a><span data-ttu-id="dd958-116">Свойство IMsRdpClientNonScriptable4:: Редиректионварнингтипе</span><span class="sxs-lookup"><span data-stu-id="dd958-116">IMsRdpClientNonScriptable4::RedirectionWarningType property</span></span>

<span data-ttu-id="dd958-117">Управляет присутствием и внешним видом диалогового окна, которое уведомляет пользователя о перенаправлении.</span><span class="sxs-lookup"><span data-stu-id="dd958-117">Controls the presence and appearance of the dialog box that notifies the user about redirection.</span></span>

<span data-ttu-id="dd958-118">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="dd958-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd958-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dd958-119">Syntax</span></span>


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a><span data-ttu-id="dd958-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dd958-120">Property value</span></span>

<span data-ttu-id="dd958-121">Задает тип диалогового окна, которое уведомляет пользователя о перенаправлении.</span><span class="sxs-lookup"><span data-stu-id="dd958-121">Sets the type of the dialog box that notifies the user of redirection.</span></span>

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span data-ttu-id="dd958-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**Редиректионварнингтипедефаулт** (символ 0x0000)</span><span class="sxs-lookup"><span data-stu-id="dd958-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="dd958-123">Диалоговое окно не зависит от издателя.</span><span class="sxs-lookup"><span data-stu-id="dd958-123">The dialog box is not publisher specific.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span data-ttu-id="dd958-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**Редиректионварнингтипеунсигнед** (0x0001)</span><span class="sxs-lookup"><span data-stu-id="dd958-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="dd958-125">Диалоговое окно предназначено для неподписанных файлов.</span><span class="sxs-lookup"><span data-stu-id="dd958-125">The dialog box is for unsigned files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span data-ttu-id="dd958-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**Редиректионварнингтипеункновн** (0x0002)</span><span class="sxs-lookup"><span data-stu-id="dd958-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="dd958-127">Диалоговое окно предназначено для неизвестного издателя.</span><span class="sxs-lookup"><span data-stu-id="dd958-127">The dialog box is for an unknown publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span data-ttu-id="dd958-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**Редиректионварнингтипеусер** (0x0003)</span><span class="sxs-lookup"><span data-stu-id="dd958-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span></span>


</dt> <dd>

<span data-ttu-id="dd958-129">Диалоговое окно предназначено для файлов пользователя.</span><span class="sxs-lookup"><span data-stu-id="dd958-129">The dialog box is for the user's files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span data-ttu-id="dd958-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**Редиректионварнингтипесирдпартисигнед** (0x0004)</span><span class="sxs-lookup"><span data-stu-id="dd958-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span></span>


</dt> <dd>

<span data-ttu-id="dd958-131">Диалоговое окно отображается для файлов, сертифицированных сторонними компаниями и подписанных.</span><span class="sxs-lookup"><span data-stu-id="dd958-131">The dialog box is displayed for third-party-certified, signed files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span data-ttu-id="dd958-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**Редиректионварнингтипетрустед** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="dd958-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="dd958-133">Диалоговое окно не отображается, так как приложение публикуется доверенным издателем.</span><span class="sxs-lookup"><span data-stu-id="dd958-133">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span data-ttu-id="dd958-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**Редиректионварнингтипемакс** (0x0005)</span><span class="sxs-lookup"><span data-stu-id="dd958-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="dd958-135">Диалоговое окно не отображается, так как приложение публикуется доверенным издателем.</span><span class="sxs-lookup"><span data-stu-id="dd958-135">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="dd958-136">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="dd958-136">Error codes</span></span>

<span data-ttu-id="dd958-137">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="dd958-137">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd958-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd958-138">Remarks</span></span>

<span data-ttu-id="dd958-139">Значение **редиректионварнингтипедефаулт**, которое является значением этого свойства по умолчанию, не оказывает никакого контроля над диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="dd958-139">The value **RedirectionWarningTypeDefault**, which is the default value of this property, exerts no control over the dialog box.</span></span> <span data-ttu-id="dd958-140">Свойство управления в данном случае — [**шовредиректионварнингдиалог**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) в [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span><span class="sxs-lookup"><span data-stu-id="dd958-140">The controlling property in this case is [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dd958-141">Требования</span><span class="sxs-lookup"><span data-stu-id="dd958-141">Requirements</span></span>



| <span data-ttu-id="dd958-142">Требование</span><span class="sxs-lookup"><span data-stu-id="dd958-142">Requirement</span></span> | <span data-ttu-id="dd958-143">Значение</span><span class="sxs-lookup"><span data-stu-id="dd958-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd958-144">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd958-144">Minimum supported client</span></span><br/> | <span data-ttu-id="dd958-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dd958-145">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="dd958-146">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd958-146">Minimum supported server</span></span><br/> | <span data-ttu-id="dd958-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dd958-147">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="dd958-148">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="dd958-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="dd958-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd958-149"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="dd958-150">DLL</span><span class="sxs-lookup"><span data-stu-id="dd958-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd958-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd958-151"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="dd958-152">IID</span><span class="sxs-lookup"><span data-stu-id="dd958-152">IID</span></span><br/>                      | <span data-ttu-id="dd958-153">IMsRdpClientNonScriptable4 определяется как f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="dd958-153">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd958-154">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd958-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd958-155">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="dd958-155">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="dd958-156">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="dd958-156">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





