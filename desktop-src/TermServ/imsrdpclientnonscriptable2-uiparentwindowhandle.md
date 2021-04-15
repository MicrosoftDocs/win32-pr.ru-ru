---
title: IMsRdpClientNonScriptable2 Уипарентвиндовхандле, свойство
description: Задает или получает маркер окна, который будет являться родительским окном для всех диалоговых окон, отображаемых элементом управления. Это позволяет корректно модальным окнам, отображаемым элементом управления, по отношению к любым окнам, отображаемым родительским приложением.
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Уипарентвиндовхандле
- Службы удаленных рабочих столов свойства Уипарентвиндовхандле, интерфейс IMsRdpClientNonScriptable2
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable2, свойство Уипарентвиндовхандле
- Службы удаленных рабочих столов свойства Уипарентвиндовхандле, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Уипарентвиндовхандле
- Службы удаленных рабочих столов свойства Уипарентвиндовхандле, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Уипарентвиндовхандле
- Службы удаленных рабочих столов свойства Уипарентвиндовхандле, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Уипарентвиндовхандле
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489117"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a><span data-ttu-id="b5108-113">Свойство IMsRdpClientNonScriptable2:: Уипарентвиндовхандле</span><span class="sxs-lookup"><span data-stu-id="b5108-113">IMsRdpClientNonScriptable2::UIParentWindowHandle property</span></span>

<span data-ttu-id="b5108-114">Задает или получает маркер окна, который будет являться родительским окном для всех диалоговых окон, отображаемых элементом управления.</span><span class="sxs-lookup"><span data-stu-id="b5108-114">Sets or retrieves the window handle to be the parent window for any dialog boxes displayed by the control.</span></span> <span data-ttu-id="b5108-115">Это позволяет корректно модальным окнам, отображаемым элементом управления, по отношению к любым окнам, отображаемым родительским приложением.</span><span class="sxs-lookup"><span data-stu-id="b5108-115">This allows any windows displayed by the control to be properly modal with respect to any windows displayed by the parent application.</span></span>

<span data-ttu-id="b5108-116">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="b5108-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5108-117">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b5108-117">Syntax</span></span>


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a><span data-ttu-id="b5108-118">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b5108-118">Property value</span></span>

<span data-ttu-id="b5108-119">Новый обработчик окна.</span><span class="sxs-lookup"><span data-stu-id="b5108-119">The new window handle.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b5108-120">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="b5108-120">Error codes</span></span>

<span data-ttu-id="b5108-121">При успешном выполнении возвращает значение **\_ ОК** .</span><span class="sxs-lookup"><span data-stu-id="b5108-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5108-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b5108-122">Remarks</span></span>

<span data-ttu-id="b5108-123">Дополнительные сведения о веб-подключение к удаленному рабочему столу см. в разделе [требования для веб-подключение к удаленному рабочему столу](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b5108-123">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b5108-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b5108-124">Requirements</span></span>



| <span data-ttu-id="b5108-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b5108-125">Requirement</span></span> | <span data-ttu-id="b5108-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b5108-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5108-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b5108-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b5108-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5108-128">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="b5108-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b5108-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b5108-130">Windows Server 2008, Windows Server 2008 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="b5108-130">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                  |
| <span data-ttu-id="b5108-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b5108-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5108-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5108-132"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="b5108-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b5108-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5108-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5108-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="b5108-135">IID</span><span class="sxs-lookup"><span data-stu-id="b5108-135">IID</span></span><br/>                      | <span data-ttu-id="b5108-136">IID \_ IMsRdpClientNonScriptable2 определен как 17a5e535-4072-4fa4-af32-c8d0d47345e9</span><span class="sxs-lookup"><span data-stu-id="b5108-136">IID\_IMsRdpClientNonScriptable2 is defined as 17a5e535-4072-4fa4-af32-c8d0d47345e9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b5108-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b5108-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5108-138">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="b5108-138">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="b5108-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="b5108-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="b5108-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="b5108-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="b5108-141">**онаусентикатионварнингдисплайед**</span><span class="sxs-lookup"><span data-stu-id="b5108-141">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="b5108-142">**онаусентикатионварнингдисмиссед**</span><span class="sxs-lookup"><span data-stu-id="b5108-142">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="b5108-143">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="b5108-143">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





