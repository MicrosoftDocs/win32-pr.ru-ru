---
title: Сообщение WM_GETTITLEBARINFOEX (Winuser. h)
description: Отправлено на запрос расширенных сведений в строке заголовка. Окно получает это сообщение через функцию WindowProc.
ms.assetid: 0760dbf1-5b20-471c-bfd9-b8d28b52074b
keywords:
- WM_GETTITLEBARINFOEX меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_GETTITLEBARINFOEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea31326faf5953df0facf34b58b06d7766c2e7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415013"
---
# <a name="wm_gettitlebarinfoex-message"></a><span data-ttu-id="348d0-105">\_Сообщение ЖЕТТИТЛЕБАРИНФОЕКС WM</span><span class="sxs-lookup"><span data-stu-id="348d0-105">WM\_GETTITLEBARINFOEX message</span></span>

<span data-ttu-id="348d0-106">Отправлено на запрос расширенных сведений в строке заголовка.</span><span class="sxs-lookup"><span data-stu-id="348d0-106">Sent to request extended title bar information.</span></span> <span data-ttu-id="348d0-107">Окно получает это сообщение через функцию [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="348d0-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETTITLEBARINFOEX            0x033F
```



## <a name="parameters"></a><span data-ttu-id="348d0-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="348d0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="348d0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="348d0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="348d0-110">Этот параметр не используется и должен быть равен 0.</span><span class="sxs-lookup"><span data-stu-id="348d0-110">This parameter is not used and must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="348d0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="348d0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="348d0-112">Указатель на структуру [**титлебаринфоекс**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="348d0-112">A pointer to a [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span> <span data-ttu-id="348d0-113">Отправитель сообщения отвечает за выделение памяти для этой структуры.</span><span class="sxs-lookup"><span data-stu-id="348d0-113">The message sender is responsible for allocating memory for this structure.</span></span> <span data-ttu-id="348d0-114">Задайте для элемента **кбсизе** этой структуры значение `sizeof(TITLEBARINFOEX)` перед передачей этой структуры вместе с сообщением.</span><span class="sxs-lookup"><span data-stu-id="348d0-114">Set the **cbSize** member of this structure to `sizeof(TITLEBARINFOEX)` before passing this structure with the message.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="348d0-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="348d0-115">Remarks</span></span>

<span data-ttu-id="348d0-116">В следующем примере показано, как получатель сообщения приводит значение **lParam** для получения структуры [**титлебаринфоекс**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="348d0-116">The following example shows how the message receiver casts an **LPARAM** value to retrieve the [**TITLEBARINFOEX**](/windows/win32/api/winuser/ns-winuser-titlebarinfoex) structure.</span></span>

`TITLEBARINFOEX *ptinfo = (TITLEBARINFOEX *)lParam;`

## <a name="requirements"></a><span data-ttu-id="348d0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="348d0-117">Requirements</span></span>



| <span data-ttu-id="348d0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="348d0-118">Requirement</span></span> | <span data-ttu-id="348d0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="348d0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="348d0-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="348d0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="348d0-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="348d0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="348d0-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="348d0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="348d0-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="348d0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="348d0-124">Header</span><span class="sxs-lookup"><span data-stu-id="348d0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="348d0-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="348d0-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="348d0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="348d0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="348d0-127">Общие сведения о меню</span><span class="sxs-lookup"><span data-stu-id="348d0-127">Menus Overview</span></span>](menus.md)
</dt> </dl>

 

