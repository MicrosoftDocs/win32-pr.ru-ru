---
description: Посылается, когда пользователь удаляет файл в окне приложения, которое зарегистрировалось как получатель удаленных файлов.
ms.assetid: 07dc2df7-4699-4e9c-b1a5-4ce877116268
title: Сообщение WM_DROPFILES (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb8362bfa746eaab519cdfc34d2cdf7757105fb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985393"
---
# <a name="wm_dropfiles-message"></a><span data-ttu-id="cd651-103">\_Сообщение ДРОПФИЛЕС WM</span><span class="sxs-lookup"><span data-stu-id="cd651-103">WM\_DROPFILES message</span></span>

<span data-ttu-id="cd651-104">Посылается, когда пользователь удаляет файл в окне приложения, которое зарегистрировалось как получатель удаленных файлов.</span><span class="sxs-lookup"><span data-stu-id="cd651-104">Sent when the user drops a file on the window of an application that has registered itself as a recipient of dropped files.</span></span>


```C++
PostMessage(
    (HWND) hWndControl,   // handle to destination control
    (UINT) WM_DROPFILES,  // message ID
    (WPARAM) wParam,      // = (WPARAM) (HDROP) hDrop;
    (LPARAM) lParam       // = 0; not used, must be zero 
);          
```



## <a name="parameters"></a><span data-ttu-id="cd651-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd651-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd651-106">*hDrop*</span><span class="sxs-lookup"><span data-stu-id="cd651-106">*hDrop*</span></span> 
</dt> <dd>

<span data-ttu-id="cd651-107">Маркер внутренней структуры, описывающей удаленные файлы.</span><span class="sxs-lookup"><span data-stu-id="cd651-107">A handle to an internal structure describing the dropped files.</span></span> <span data-ttu-id="cd651-108">Передайте этот обработчик [**драгфиниш**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**драгкуерифиле**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea)или [**драгкуерипоинт**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) , чтобы получить сведения об удаленных файлах.</span><span class="sxs-lookup"><span data-stu-id="cd651-108">Pass this handle [**DragFinish**](/windows/desktop/api/Shellapi/nf-shellapi-dragfinish), [**DragQueryFile**](/windows/desktop/api/Shellapi/nf-shellapi-dragqueryfilea), or [**DragQueryPoint**](/windows/desktop/api/Shellapi/nf-shellapi-dragquerypoint) to retrieve information about the dropped files.</span></span>

</dd> <dt>

<span data-ttu-id="cd651-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd651-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd651-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cd651-110">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd651-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cd651-111">Return value</span></span>

<span data-ttu-id="cd651-112">Приложение должно вернуть нуль, если оно обрабатывает это сообщение.</span><span class="sxs-lookup"><span data-stu-id="cd651-112">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd651-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="cd651-113">Remarks</span></span>

<span data-ttu-id="cd651-114">Маркер HDROP объявляется в Шеллапи. h.</span><span class="sxs-lookup"><span data-stu-id="cd651-114">The HDROP handle is declared in Shellapi.h.</span></span> <span data-ttu-id="cd651-115">Этот заголовок необходимо включить в сборку для использования **WM \_ дропфилес**.</span><span class="sxs-lookup"><span data-stu-id="cd651-115">You must include this header in your build to use **WM\_DROPFILES**.</span></span> <span data-ttu-id="cd651-116">Более подробное обсуждение того, как использовать перетаскивание для передачи данных оболочки, см. в разделе [Передача данных оболочки с помощью перетаскивания или буфера обмена](dragdrop.md).</span><span class="sxs-lookup"><span data-stu-id="cd651-116">For further discussion of how to use drag-and-drop to transfer Shell data, see [Transferring Shell Data Using Drag-and-Drop or the Clipboard](dragdrop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cd651-117">Требования</span><span class="sxs-lookup"><span data-stu-id="cd651-117">Requirements</span></span>



| <span data-ttu-id="cd651-118">Требование</span><span class="sxs-lookup"><span data-stu-id="cd651-118">Requirement</span></span> | <span data-ttu-id="cd651-119">Значение</span><span class="sxs-lookup"><span data-stu-id="cd651-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd651-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd651-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cd651-121">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cd651-121">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="cd651-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd651-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cd651-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="cd651-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cd651-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="cd651-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd651-125"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd651-125"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd651-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd651-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd651-127">**PostMessage**</span><span class="sxs-lookup"><span data-stu-id="cd651-127">**PostMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[<span data-ttu-id="cd651-128">**DragAcceptFiles**</span><span class="sxs-lookup"><span data-stu-id="cd651-128">**DragAcceptFiles**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-dragacceptfiles)
</dt> </dl>

 

 
