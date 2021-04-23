---
title: Сообщение WM_NEXTMENU (Winuser. h)
description: Отправляется в приложение, когда для переключения между строкой меню и системным меню используется клавиша со стрелкой вправо или влево.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU меню сообщений и других ресурсов
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989405"
---
# <a name="wm_nextmenu-message"></a><span data-ttu-id="57dc0-104">\_Сообщение НЕКСТМЕНУ WM</span><span class="sxs-lookup"><span data-stu-id="57dc0-104">WM\_NEXTMENU message</span></span>

<span data-ttu-id="57dc0-105">Отправляется в приложение, когда для переключения между строкой меню и системным меню используется клавиша со стрелкой вправо или влево.</span><span class="sxs-lookup"><span data-stu-id="57dc0-105">Sent to an application when the right or left arrow key is used to switch between the menu bar and the system menu.</span></span>


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a><span data-ttu-id="57dc0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="57dc0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57dc0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="57dc0-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57dc0-108">Код виртуального ключа для ключа.</span><span class="sxs-lookup"><span data-stu-id="57dc0-108">The virtual-key code of the key.</span></span> <span data-ttu-id="57dc0-109">См. раздел [**коды виртуальных клавиш**](/windows/desktop/inputdev/virtual-key-codes).</span><span class="sxs-lookup"><span data-stu-id="57dc0-109">See [**Virtual-Key Codes**](/windows/desktop/inputdev/virtual-key-codes).</span></span>

</dd> <dt>

<span data-ttu-id="57dc0-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="57dc0-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="57dc0-111">Указатель на структуру [**мдинекстмену**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) , содержащую сведения о меню, которое должно быть активировано.</span><span class="sxs-lookup"><span data-stu-id="57dc0-111">A pointer to a [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) structure that contains information about the menu to be activated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57dc0-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="57dc0-112">Remarks</span></span>

<span data-ttu-id="57dc0-113">В ответ на это сообщение приложение может указать меню для перехода в **хменунекст** член [**мдинекстмену**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) и окно для получения сообщений уведомления меню в элементе **хвнднекст** структуры **мдинекстмену** .</span><span class="sxs-lookup"><span data-stu-id="57dc0-113">In responding to this message, the application can specify the menu to switch to in the **hmenuNext** member of [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) and the window to receive the menu notification messages in the **hwndNext** member of the **MDINEXTMENU** structure.</span></span> <span data-ttu-id="57dc0-114">Необходимо задать оба элемента, чтобы изменения вступили в силу (они изначально равны **null**).</span><span class="sxs-lookup"><span data-stu-id="57dc0-114">You must set both members for the changes to take effect (they are initially **NULL**).</span></span>

## <a name="requirements"></a><span data-ttu-id="57dc0-115">Требования</span><span class="sxs-lookup"><span data-stu-id="57dc0-115">Requirements</span></span>



| <span data-ttu-id="57dc0-116">Требование</span><span class="sxs-lookup"><span data-stu-id="57dc0-116">Requirement</span></span> | <span data-ttu-id="57dc0-117">Значение</span><span class="sxs-lookup"><span data-stu-id="57dc0-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57dc0-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57dc0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="57dc0-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57dc0-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="57dc0-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57dc0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="57dc0-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57dc0-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="57dc0-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="57dc0-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="57dc0-123"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57dc0-123"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57dc0-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="57dc0-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="57dc0-125">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="57dc0-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="57dc0-126">**мдинекстмену**</span><span class="sxs-lookup"><span data-stu-id="57dc0-126">**MDINEXTMENU**</span></span>](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

<span data-ttu-id="57dc0-127">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="57dc0-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="57dc0-128">Меню</span><span class="sxs-lookup"><span data-stu-id="57dc0-128">Menus</span></span>](menus.md)
</dt> </dl>

 

