---
title: Код уведомления EN_ALIGN_RTL_EC (Winuser. h)
description: Посылается, когда пользователь изменяет направление элемента управления Edit на "справа налево". Родительское окно элемента управления "поле ввода" получает этот код уведомления через \_ командное сообщение WM.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca94073b86ea44b192360e593f4b76d4227cf82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891710"
---
# <a name="en_align_rtl_ec-notification-code"></a><span data-ttu-id="83313-105">EN — \_ выровняйте \_ \_ код уведомления EC справа налево</span><span class="sxs-lookup"><span data-stu-id="83313-105">EN\_ALIGN\_RTL\_EC notification code</span></span>

<span data-ttu-id="83313-106">Посылается, когда пользователь изменяет направление элемента управления Edit на "справа налево".</span><span class="sxs-lookup"><span data-stu-id="83313-106">Sent when the user has changed the edit control direction to right-to-left.</span></span> <span data-ttu-id="83313-107">Родительское окно элемента управления "поле ввода" получает этот код уведомления [**через \_ командное сообщение WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="83313-107">The parent window of the edit control receives this notification code through a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message.</span></span>


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="83313-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="83313-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83313-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="83313-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83313-110">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) содержит идентификатор элемента управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="83313-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contains the identifier of the edit control.</span></span> <span data-ttu-id="83313-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) указывает код уведомления.</span><span class="sxs-lookup"><span data-stu-id="83313-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the notification code.</span></span>

</dd> <dt>

<span data-ttu-id="83313-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="83313-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="83313-113">Маркер элемента управления редактирования, отправляющего код уведомления.</span><span class="sxs-lookup"><span data-stu-id="83313-113">A handle to the edit control sending the notification code.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="83313-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83313-114">Remarks</span></span>

<span data-ttu-id="83313-115">Если в системе установлен двунаправленный язык, например арабский или иврит, можно изменить направление элемента управления редактирования с помощью клавиш CTRL + ЛШИФТ (слева направо) и CTRL + РШИФТ (справа налево).</span><span class="sxs-lookup"><span data-stu-id="83313-115">If there is a bidirectional language installed on your system, for example, Arabic or Hebrew, you can change the edit control direction using CTRL+LSHIFT (for left to right) and CTRL+RSHIFT (for right to left).</span></span>

<span data-ttu-id="83313-116">**Расширенное редактирование:** Этот код уведомления не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="83313-116">**Rich Edit:** This notification code is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="83313-117">Требования</span><span class="sxs-lookup"><span data-stu-id="83313-117">Requirements</span></span>



| <span data-ttu-id="83313-118">Требование</span><span class="sxs-lookup"><span data-stu-id="83313-118">Requirement</span></span> | <span data-ttu-id="83313-119">Значение</span><span class="sxs-lookup"><span data-stu-id="83313-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83313-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83313-120">Minimum supported client</span></span><br/> | <span data-ttu-id="83313-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="83313-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="83313-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83313-122">Minimum supported server</span></span><br/> | <span data-ttu-id="83313-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83313-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="83313-124">Header</span><span class="sxs-lookup"><span data-stu-id="83313-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="83313-125"><dt>Winuser. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83313-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83313-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83313-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83313-127">**\_команда WM**</span><span class="sxs-lookup"><span data-stu-id="83313-127">**WM\_COMMAND**</span></span>](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

