---
title: Код уведомления CBEN_ENDEDIT (Коммктрл. h)
description: Посылается, когда пользователь завершает операцию в поле ввода или выбрал элемент из раскрывающегося списка элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: b6b50951-7304-4499-b57b-a5b592de2190
keywords:
- CBEN_ENDEDIT кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- CBEN_ENDEDIT
- CBEN_ENDEDITA
- CBEN_ENDEDITW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 679b9f878dbd8f7f374b461ee548f9ce2c62e281
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414809"
---
# <a name="cben_endedit-notification-code"></a><span data-ttu-id="f0850-105">\_Код уведомления кбен ENDEDIT</span><span class="sxs-lookup"><span data-stu-id="f0850-105">CBEN\_ENDEDIT notification code</span></span>

<span data-ttu-id="f0850-106">Посылается, когда пользователь завершает операцию в поле ввода или выбрал элемент из раскрывающегося списка элемента управления.</span><span class="sxs-lookup"><span data-stu-id="f0850-106">Sent when the user has concluded an operation within the edit box or has selected an item from the control's drop-down list.</span></span> <span data-ttu-id="f0850-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f0850-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
CBEN_ENDEDIT

    pnmEditInfo = (PNMCBEENDEDIT) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f0850-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0850-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0850-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0850-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0850-110">Указатель на структуру [**нмкбиндедит**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) , которая содержит сведения о том, как пользователь завершил операцию изменения.</span><span class="sxs-lookup"><span data-stu-id="f0850-110">A pointer to an [**NMCBEENDEDIT**](/windows/desktop/api/Commctrl/ns-commctrl-nmcbeendedita) structure that contains information about how the user concluded the edit operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0850-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0850-111">Return value</span></span>

<span data-ttu-id="f0850-112">**Значение false** , чтобы принять код уведомления и разрешить элементу управления отображать выбранный элемент; в противном случае — **значение true**.</span><span class="sxs-lookup"><span data-stu-id="f0850-112">**FALSE** to accept the notification code and allow the control to display the selected item; otherwise, **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0850-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f0850-113">Requirements</span></span>



| <span data-ttu-id="f0850-114">Требование</span><span class="sxs-lookup"><span data-stu-id="f0850-114">Requirement</span></span> | <span data-ttu-id="f0850-115">Значение</span><span class="sxs-lookup"><span data-stu-id="f0850-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0850-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0850-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f0850-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0850-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0850-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0850-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f0850-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0850-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0850-120">Header</span><span class="sxs-lookup"><span data-stu-id="f0850-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0850-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0850-121"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f0850-122">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f0850-122">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f0850-123">**Кбен \_ ЕНДЕДИТВ** (Юникод) и **кбен \_ ендедита** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f0850-123">**CBEN\_ENDEDITW** (Unicode) and **CBEN\_ENDEDITA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f0850-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f0850-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0850-125">Сведения об элементах управления ComboBoxEx</span><span class="sxs-lookup"><span data-stu-id="f0850-125">About ComboBoxEx Controls</span></span>](comboboxex-controls.md)
</dt> </dl>

 

 





