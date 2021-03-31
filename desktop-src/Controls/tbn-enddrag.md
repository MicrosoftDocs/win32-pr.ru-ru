---
title: Код уведомления TBN_ENDDRAG (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь остановил перетаскивание кнопки на панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 846ba42e-6e0d-45bb-88ce-7b4d2cb17e13
keywords:
- TBN_ENDDRAG кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd493ac338e11716ea381e83102b200334a1eec4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136799"
---
# <a name="tbn_enddrag-notification-code"></a><span data-ttu-id="bfa72-105">\_Код уведомления ТБН енддраг</span><span class="sxs-lookup"><span data-stu-id="bfa72-105">TBN\_ENDDRAG notification code</span></span>

<span data-ttu-id="bfa72-106">Сообщает родительскому окну панели инструментов, что пользователь остановил перетаскивание кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="bfa72-106">Notifies the toolbar's parent window that the user has stopped dragging a button in a toolbar.</span></span> <span data-ttu-id="bfa72-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bfa72-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDDRAG 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="bfa72-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfa72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bfa72-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bfa72-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bfa72-110">Указатель на структуру [**нмтулбар**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) .</span><span class="sxs-lookup"><span data-stu-id="bfa72-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure.</span></span> <span data-ttu-id="bfa72-111">Элемент **Член iItem** содержит идентификатор команды для перетаскивания кнопки.</span><span class="sxs-lookup"><span data-stu-id="bfa72-111">The **iItem** member contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bfa72-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bfa72-112">Return value</span></span>

<span data-ttu-id="bfa72-113">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="bfa72-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfa72-114">Требования</span><span class="sxs-lookup"><span data-stu-id="bfa72-114">Requirements</span></span>



| <span data-ttu-id="bfa72-115">Требование</span><span class="sxs-lookup"><span data-stu-id="bfa72-115">Requirement</span></span> | <span data-ttu-id="bfa72-116">Значение</span><span class="sxs-lookup"><span data-stu-id="bfa72-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bfa72-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bfa72-117">Minimum supported client</span></span><br/> | <span data-ttu-id="bfa72-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bfa72-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bfa72-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bfa72-119">Minimum supported server</span></span><br/> | <span data-ttu-id="bfa72-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bfa72-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bfa72-121">Header</span><span class="sxs-lookup"><span data-stu-id="bfa72-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="bfa72-122"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfa72-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





