---
description: Функция Исвиндовредиректедфорпринт определяет, перенаправлено ли указанное окно на печать в данный момент.
ms.assetid: 49FD0D63-0F7F-48C6-81B6-25715294E7B7
title: Функция Исвиндовредиректедфорпринт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsWindowRedirectedForPrint
api_type:
- DllExport
api_location:
- user32.dll
ms.openlocfilehash: b6648e5638ec6f05a2677ce279b0c3d7b160b49b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719706"
---
# <a name="iswindowredirectedforprint-function"></a><span data-ttu-id="5ce6d-103">Функция Исвиндовредиректедфорпринт</span><span class="sxs-lookup"><span data-stu-id="5ce6d-103">IsWindowRedirectedForPrint function</span></span>

<span data-ttu-id="5ce6d-104">Функция **исвиндовредиректедфорпринт** определяет, перенаправлено ли указанное окно на печать в данный момент.</span><span class="sxs-lookup"><span data-stu-id="5ce6d-104">The **IsWindowRedirectedForPrint** function determines whether the specified window is currently redirected for printing.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce6d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ce6d-105">Syntax</span></span>


```C++
BOOL WINAPI IsWindowRedirectedForPrint(
  _In_   HWND hWnd
);
```



## <a name="parameters"></a><span data-ttu-id="5ce6d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="5ce6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ce6d-107">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5ce6d-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ce6d-108">Дескриптор окна.</span><span class="sxs-lookup"><span data-stu-id="5ce6d-108">The handle of the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ce6d-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5ce6d-109">Return value</span></span>

<span data-ttu-id="5ce6d-110">Если окно в данный момент перенаправлено для печати, функция возвращает ненулевое значение. в противном случае возвращается ноль.</span><span class="sxs-lookup"><span data-stu-id="5ce6d-110">If the window is currently redirected for printing, the function returns a nonzero value; otherwise, it returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ce6d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ce6d-111">Remarks</span></span>

<span data-ttu-id="5ce6d-112">Окно перенаправляется для печати при обработке вызова [**принтвиндов**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span><span class="sxs-lookup"><span data-stu-id="5ce6d-112">A window is redirected for printing when it processes a call to [**PrintWindow**](/windows/desktop/api/Winuser/nf-winuser-printwindow).</span></span> <span data-ttu-id="5ce6d-113">При вызове **принтвиндов** окно преобразует свое содержимое в контекст устройства без экрана.</span><span class="sxs-lookup"><span data-stu-id="5ce6d-113">In a call to **PrintWindow**, a window renders its content to an off-screen device context.</span></span>

<span data-ttu-id="5ce6d-114">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="5ce6d-114">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce6d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="5ce6d-115">Requirements</span></span>



| <span data-ttu-id="5ce6d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="5ce6d-116">Requirement</span></span> | <span data-ttu-id="5ce6d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="5ce6d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5ce6d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5ce6d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5ce6d-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5ce6d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5ce6d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5ce6d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5ce6d-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5ce6d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5ce6d-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5ce6d-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ce6d-123"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ce6d-123"><dt>User32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ce6d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5ce6d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce6d-125">**принтвиндов**</span><span class="sxs-lookup"><span data-stu-id="5ce6d-125">**PrintWindow**</span></span>](/windows/desktop/api/Winuser/nf-winuser-printwindow)
</dt> <dt>

[<span data-ttu-id="5ce6d-126">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="5ce6d-126">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="5ce6d-127">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="5ce6d-127">**LoadLibrary**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[<span data-ttu-id="5ce6d-128">**\_Печать WM**</span><span class="sxs-lookup"><span data-stu-id="5ce6d-128">**WM\_PRINT**</span></span>](/windows/desktop/gdi/wm-print)
</dt> <dt>

[<span data-ttu-id="5ce6d-129">**WM \_ принтклиент**</span><span class="sxs-lookup"><span data-stu-id="5ce6d-129">**WM\_PRINTCLIENT**</span></span>](/windows/desktop/gdi/wm-printclient)
</dt> </dl>

 

