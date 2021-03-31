---
description: Сообщение, которое отправляется всем окнам верхнего уровня, когда функция Системпараметерсинфо изменяет параметр на уровне системы или при изменении параметров политики.
ms.assetid: 77174e06-a25b-440a-9e9c-4fd5979c433c
title: Сообщение WM_SETTINGCHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c3d1360b5e4cc5de2dbd23b09b8f2ad034948f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272475"
---
# <a name="wm_settingchange-message"></a><span data-ttu-id="41713-103">\_Сообщение СЕТТИНГЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="41713-103">WM\_SETTINGCHANGE message</span></span>

<span data-ttu-id="41713-104">Сообщение, которое отправляется всем окнам верхнего уровня, когда функция [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) изменяет параметр на уровне системы или при изменении параметров политики.</span><span class="sxs-lookup"><span data-stu-id="41713-104">A message that is sent to all top-level windows when the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function changes a system-wide setting or when policy settings have changed.</span></span>

<span data-ttu-id="41713-105">Приложения должны отсылать **WM \_ сеттингчанже** всем окнам верхнего уровня при внесении изменений в системные параметры.</span><span class="sxs-lookup"><span data-stu-id="41713-105">Applications should send **WM\_SETTINGCHANGE** to all top-level windows when they make changes to system parameters.</span></span> <span data-ttu-id="41713-106">(Это сообщение не может быть отправлено непосредственно в окно.) Чтобы отправить сообщение **WM \_ сеттингчанже** всем окнам верхнего уровня, используйте функцию [**функции sendmessagetimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) с параметром *HWND* , имеющим значение **HWND \_ Broadcast**.</span><span class="sxs-lookup"><span data-stu-id="41713-106">(This message cannot be sent directly to a window.) To send the **WM\_SETTINGCHANGE** message to all top-level windows, use the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function with the *hwnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="41713-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="41713-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
#define WM_SETTINGCHANGE                WM_WININICHANGE
```



## <a name="parameters"></a><span data-ttu-id="41713-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="41713-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41713-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41713-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41713-110">Когда система отправляет это сообщение в результате вызова [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , параметр *wParam* является значением параметра *Уиактион* , передаваемого функции **системпараметерсинфо** .</span><span class="sxs-lookup"><span data-stu-id="41713-110">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, the *wParam* parameter is the value of the *uiAction* parameter passed to the **SystemParametersInfo** function.</span></span> <span data-ttu-id="41713-111">Список значений см. в разделе **системпараметерсинфо**.</span><span class="sxs-lookup"><span data-stu-id="41713-111">For a list of values, see **SystemParametersInfo**.</span></span>

<span data-ttu-id="41713-112">Когда система отправляет это сообщение в результате изменения параметров политики, этот параметр указывает тип примененной политики.</span><span class="sxs-lookup"><span data-stu-id="41713-112">When the system sends this message as a result of a change in policy settings, this parameter indicates the type of policy that was applied.</span></span> <span data-ttu-id="41713-113">Это значение равно 1, если политика компьютера была применена, или нуль, если применена политика пользователя.</span><span class="sxs-lookup"><span data-stu-id="41713-113">This value is 1 if computer policy was applied or zero if user policy was applied.</span></span>

<span data-ttu-id="41713-114">Если система отправляет это сообщение в результате изменения параметров языкового стандарта, этот параметр равен нулю.</span><span class="sxs-lookup"><span data-stu-id="41713-114">When the system sends this message as a result of a change in locale settings, this parameter is zero.</span></span>

<span data-ttu-id="41713-115">Когда приложение отправляет это сообщение, этот параметр должен иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="41713-115">When an application sends this message, this parameter must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="41713-116">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41713-116">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41713-117">Когда система отправляет это сообщение в результате вызова [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) , *lParam* — это указатель на строку, которая указывает на область, содержащую измененный системный параметр.</span><span class="sxs-lookup"><span data-stu-id="41713-117">When the system sends this message as a result of a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) call, *lParam* is a pointer to a string that indicates the area containing the system parameter that was changed.</span></span> <span data-ttu-id="41713-118">Этот параметр обычно не указывает, какой именно системный параметр изменился.</span><span class="sxs-lookup"><span data-stu-id="41713-118">This parameter does not usually indicate which specific system parameter changed.</span></span> <span data-ttu-id="41713-119">(Обратите внимание, что некоторые приложения отправляют это сообщение с параметром *lParam* , имеющим значение **null**.) В общем случае при получении этого сообщения следует проверить и перезагрузить все параметры системного параметра, используемые приложением.</span><span class="sxs-lookup"><span data-stu-id="41713-119">(Note that some applications send this message with *lParam* set to **NULL**.) In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

<span data-ttu-id="41713-120">Эта строка может быть именем раздела реестра или именем раздела в файле Win.ini.</span><span class="sxs-lookup"><span data-stu-id="41713-120">This string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="41713-121">Если строка является именем реестра, она обычно указывает только конечный узел в реестре, а не полный путь.</span><span class="sxs-lookup"><span data-stu-id="41713-121">When the string is a registry name, it typically indicates only the leaf node in the registry, not the full path.</span></span>

<span data-ttu-id="41713-122">Когда система отправляет это сообщение в результате изменения параметров политики, этот параметр указывает на строку "Policy".</span><span class="sxs-lookup"><span data-stu-id="41713-122">When the system sends this message as a result of a change in policy settings, this parameter points to the string "Policy".</span></span>

<span data-ttu-id="41713-123">Когда система отправляет это сообщение в результате изменения параметров языкового стандарта, этот параметр указывает на строку "Intl".</span><span class="sxs-lookup"><span data-stu-id="41713-123">When the system sends this message as a result of a change in locale settings, this parameter points to the string "intl".</span></span>

<span data-ttu-id="41713-124">Чтобы изменить переменные среды для системы или пользователя, передайте это сообщение с параметром *lParam* в строку "среда".</span><span class="sxs-lookup"><span data-stu-id="41713-124">To effect a change in the environment variables for the system or the user, broadcast this message with *lParam* set to the string "Environment".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41713-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="41713-125">Return value</span></span>

<span data-ttu-id="41713-126">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="41713-126">Type: **LRESULT**</span></span>

<span data-ttu-id="41713-127">При обработке этого сообщения возвращается нуль.</span><span class="sxs-lookup"><span data-stu-id="41713-127">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="41713-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41713-128">Remarks</span></span>

<span data-ttu-id="41713-129">Параметр *lParam* указывает, какая Метрика системы изменилась, например "конвертиблеслатемоде", если индикатор конвертиблеслатемоде был переключен, или "системдоккмоде", если был переключен закрепленный индикатор.</span><span class="sxs-lookup"><span data-stu-id="41713-129">The *lParam* parameter indicates which system metric has changed, for example, "ConvertibleSlateMode" if the CONVERTIBLESLATEMODE indicator was toggled or "SystemDockMode" if the DOCKED indicator was toggled.</span></span>

## <a name="requirements"></a><span data-ttu-id="41713-130">Требования</span><span class="sxs-lookup"><span data-stu-id="41713-130">Requirements</span></span>



| <span data-ttu-id="41713-131">Требование</span><span class="sxs-lookup"><span data-stu-id="41713-131">Requirement</span></span> | <span data-ttu-id="41713-132">Значение</span><span class="sxs-lookup"><span data-stu-id="41713-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41713-133">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="41713-133">Minimum supported client</span></span><br/> | <span data-ttu-id="41713-134">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41713-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="41713-135">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="41713-135">Minimum supported server</span></span><br/> | <span data-ttu-id="41713-136">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="41713-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41713-137">Заголовок</span><span class="sxs-lookup"><span data-stu-id="41713-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="41713-138"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="41713-138"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41713-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41713-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41713-140">События политики</span><span class="sxs-lookup"><span data-stu-id="41713-140">Policy Events</span></span>](/previous-versions/windows/desktop/Policy/policy-events)
</dt> <dt>

[<span data-ttu-id="41713-141">**Функции sendmessagetimeout**</span><span class="sxs-lookup"><span data-stu-id="41713-141">**SendMessageTimeout**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)
</dt> <dt>

[<span data-ttu-id="41713-142">**системпараметерсинфо**</span><span class="sxs-lookup"><span data-stu-id="41713-142">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
