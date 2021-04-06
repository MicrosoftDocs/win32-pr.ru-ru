---
description: Приложение отправляет \_ сообщение WM вининичанже всем окнам верхнего уровня после внесения изменений в файл WIN.INI. Функция Системпараметерсинфо отправляет это сообщение после того, как приложение использует функцию для изменения параметра в WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: Сообщение WM_WININICHANGE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991080"
---
# <a name="wm_wininichange-message"></a><span data-ttu-id="3877b-104">\_Сообщение ВИНИНИЧАНЖЕ WM</span><span class="sxs-lookup"><span data-stu-id="3877b-104">WM\_WININICHANGE message</span></span>

<span data-ttu-id="3877b-105">Приложение отправляет сообщение **WM \_ вининичанже** всем окнам верхнего уровня после внесения изменений в файл WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="3877b-105">An application sends the **WM\_WININICHANGE** message to all top-level windows after making a change to the WIN.INI file.</span></span> <span data-ttu-id="3877b-106">Функция [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) отправляет это сообщение после того, как приложение использует функцию для изменения параметра в WIN.INI.</span><span class="sxs-lookup"><span data-stu-id="3877b-106">The [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function sends this message after an application uses the function to change a setting in WIN.INI.</span></span>

> [!Note]  
> <span data-ttu-id="3877b-107">Сообщение **WM \_ вининичанже** предоставляется только для совместимости с более ранними версиями системы.</span><span class="sxs-lookup"><span data-stu-id="3877b-107">The **WM\_WININICHANGE** message is provided only for compatibility with earlier versions of the system.</span></span> <span data-ttu-id="3877b-108">Приложения должны использовать сообщение [**WM \_ сеттингчанже**](wm-settingchange.md) .</span><span class="sxs-lookup"><span data-stu-id="3877b-108">Applications should use the [**WM\_SETTINGCHANGE**](wm-settingchange.md) message.</span></span>

 

<span data-ttu-id="3877b-109">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3877b-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a><span data-ttu-id="3877b-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3877b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3877b-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3877b-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3877b-112">Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="3877b-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3877b-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3877b-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3877b-114">Указатель на строку, содержащую имя системного параметра, который был изменен.</span><span class="sxs-lookup"><span data-stu-id="3877b-114">A pointer to a string containing the name of the system parameter that was changed.</span></span> <span data-ttu-id="3877b-115">Например, эта строка может быть именем раздела реестра или именем раздела в файле Win.ini.</span><span class="sxs-lookup"><span data-stu-id="3877b-115">For example, this string can be the name of a registry key or the name of a section in the Win.ini file.</span></span> <span data-ttu-id="3877b-116">Этот параметр не особенно полезен при определении изменяемого системного параметра.</span><span class="sxs-lookup"><span data-stu-id="3877b-116">This parameter is not particularly useful in determining which system parameter changed.</span></span> <span data-ttu-id="3877b-117">Например, если строка является именем реестра, она обычно указывает только конечный узел в реестре, а не весь путь.</span><span class="sxs-lookup"><span data-stu-id="3877b-117">For example, when the string is a registry name, it typically indicates only the leaf node in the registry, not the whole path.</span></span> <span data-ttu-id="3877b-118">Кроме того, некоторые приложения отправляют это сообщение с параметром *lParam* , имеющим значение **null**.</span><span class="sxs-lookup"><span data-stu-id="3877b-118">In addition, some applications send this message with *lParam* set to **NULL**.</span></span> <span data-ttu-id="3877b-119">В общем случае при получении этого сообщения следует проверить и перезагрузить все параметры системного параметра, используемые приложением.</span><span class="sxs-lookup"><span data-stu-id="3877b-119">In general, when you receive this message, you should check and reload any system parameter settings that are used by your application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3877b-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3877b-120">Return value</span></span>

<span data-ttu-id="3877b-121">Тип: **lResult**</span><span class="sxs-lookup"><span data-stu-id="3877b-121">Type: **LRESULT**</span></span>

<span data-ttu-id="3877b-122">При обработке этого сообщения возвращается нуль.</span><span class="sxs-lookup"><span data-stu-id="3877b-122">If you process this message, return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3877b-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3877b-123">Remarks</span></span>

<span data-ttu-id="3877b-124">Чтобы отправить сообщение **WM \_ вининичанже** всем окнам верхнего уровня, используйте функцию [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) с параметром *HWND* , для которого установлено значение **HWND \_ Broadcast**.</span><span class="sxs-lookup"><span data-stu-id="3877b-124">To send the **WM\_WININICHANGE** message to all top-level windows, use the [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) function with the *hWnd* parameter set to **HWND\_BROADCAST**.</span></span>

<span data-ttu-id="3877b-125">Вместо этого вызовы функций, которые изменяют WIN.INI, могут быть сопоставлены с реестром.</span><span class="sxs-lookup"><span data-stu-id="3877b-125">Calls to functions that change WIN.INI may be mapped to the registry instead.</span></span> <span data-ttu-id="3877b-126">Это сопоставление происходит, когда WIN.INI и изменяемый раздел указываются в реестре в следующем разделе:</span><span class="sxs-lookup"><span data-stu-id="3877b-126">This mapping occurs when WIN.INI and the section being changed are specified in the registry under the following key:</span></span>

<span data-ttu-id="3877b-127">**HKEY \_ локальный \_ компьютер \\ программное обеспечение \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**</span><span class="sxs-lookup"><span data-stu-id="3877b-127">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows NT\\CurrentVersion\\IniFileMapping**</span></span>

<span data-ttu-id="3877b-128">Изменение места хранения не влияет на поведение этого сообщения.</span><span class="sxs-lookup"><span data-stu-id="3877b-128">The change in the storage location has no effect on the behavior of this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="3877b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="3877b-129">Requirements</span></span>



| <span data-ttu-id="3877b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="3877b-130">Requirement</span></span> | <span data-ttu-id="3877b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="3877b-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3877b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3877b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3877b-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3877b-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="3877b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3877b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3877b-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3877b-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3877b-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3877b-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="3877b-137"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3877b-137"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3877b-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3877b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3877b-139">**системпараметерсинфо**</span><span class="sxs-lookup"><span data-stu-id="3877b-139">**SystemParametersInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
