---
title: Код уведомления LVN_INCREMENTALSEARCH (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "представление списка", что началось добавочный поиск. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- LVN_INCREMENTALSEARCH кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654734"
---
# <a name="lvn_incrementalsearch-notification-code"></a><span data-ttu-id="f3494-105">\_Код уведомления ЛВН INCREMENTALSEARCH</span><span class="sxs-lookup"><span data-stu-id="f3494-105">LVN\_INCREMENTALSEARCH notification code</span></span>

<span data-ttu-id="f3494-106">Сообщает родительскому окну элемента управления "представление списка", что началось добавочный поиск.</span><span class="sxs-lookup"><span data-stu-id="f3494-106">Notifies a list-view control's parent window that an incremental search has started.</span></span> <span data-ttu-id="f3494-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="f3494-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f3494-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3494-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3494-109">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f3494-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3494-110">Указатель на структуру [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) , описывающую код уведомления.</span><span class="sxs-lookup"><span data-stu-id="f3494-110">Pointer to a [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that describes the notification code.</span></span> <span data-ttu-id="f3494-111">Вызывающий объект отвечает за выделение этой структуры, включая содержащиеся в ней структуры [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) и [**лвфиндинфо**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) .</span><span class="sxs-lookup"><span data-stu-id="f3494-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) and [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structures.</span></span> <span data-ttu-id="f3494-112">Задайте элементы структуры **NMHDR** .</span><span class="sxs-lookup"><span data-stu-id="f3494-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="f3494-113">Элемент **Code** должен иметь значение ЛВН \_ INCREMENTALSEARCH.</span><span class="sxs-lookup"><span data-stu-id="f3494-113">The **code** member must be set to LVN\_INCREMENTALSEARCH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3494-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f3494-114">Return value</span></span>

<span data-ttu-id="f3494-115">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="f3494-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3494-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f3494-116">Remarks</span></span>

<span data-ttu-id="f3494-117">Получатель уведомлений выполняет приведение *lParam* для получения структуры [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .</span><span class="sxs-lookup"><span data-stu-id="f3494-117">The notification receiver casts *lParam* to retrieve the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span> <span data-ttu-id="f3494-118">Параметр *wParam* содержит идентификатор элемента управления, который отправляет этот код уведомления.</span><span class="sxs-lookup"><span data-stu-id="f3494-118">The *wParam* parameter contains the ID of the control that sends this notification code.</span></span>

<span data-ttu-id="f3494-119">Этот код уведомления дает приложению (или получателю уведомления) возможность настроить добавочный поиск.</span><span class="sxs-lookup"><span data-stu-id="f3494-119">This notification code gives an application (or the notification receiver) the opportunity to customize an incremental search.</span></span> <span data-ttu-id="f3494-120">Например, если элементы поиска являются числовыми, приложение может выполнить числовой Поиск вместо поиска строки.</span><span class="sxs-lookup"><span data-stu-id="f3494-120">For example, if the search items are numeric, the application can perform a numerical search instead of a string search.</span></span>

<span data-ttu-id="f3494-121">Приложение устанавливает член **lParam** структуры [**лвфиндинфо**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , содержащейся в структуре [**нмлвфиндитем**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) , в результат поиска или в другое определенное приложением значение, чтобы завершить поиск неудачей и указать элементу управления, как это делается.</span><span class="sxs-lookup"><span data-stu-id="f3494-121">The application sets the **lParam** member of the [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure contained in [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure  to the result of the search, or to another application defined value to fail the search and indicate to the control how to proceed.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3494-122">Требования</span><span class="sxs-lookup"><span data-stu-id="f3494-122">Requirements</span></span>



| <span data-ttu-id="f3494-123">Требование</span><span class="sxs-lookup"><span data-stu-id="f3494-123">Requirement</span></span> | <span data-ttu-id="f3494-124">Значение</span><span class="sxs-lookup"><span data-stu-id="f3494-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3494-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f3494-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f3494-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f3494-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f3494-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f3494-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f3494-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f3494-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f3494-129">Header</span><span class="sxs-lookup"><span data-stu-id="f3494-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3494-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f3494-130"><dt>Commctrl.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3494-131">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f3494-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f3494-132">**ЛВН \_ ИНКРЕМЕНТАЛСЕАРЧВ** (Юникод) и **ЛВН \_ инкременталсеарча** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f3494-132">**LVN\_INCREMENTALSEARCHW** (Unicode) and **LVN\_INCREMENTALSEARCHA** (ANSI)</span></span><br/> |



 

 





