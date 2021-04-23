---
title: Код уведомления NM_RDBLCLK (строка состояния) (Коммктрл. h)
description: Уведомляет родительские окна элемента управления "строка состояния", что пользователь дважды щелкнул правой кнопкой мыши внутри элемента управления. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- Элементы управления Windows для кода уведомления NM_RDBLCLK (строка состояния)
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18092b03a599c75a88deb56bb256d96728b96328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493311"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a><span data-ttu-id="863bf-105">\_Код уведомления NM рдблклк (строка состояния)</span><span class="sxs-lookup"><span data-stu-id="863bf-105">NM\_RDBLCLK (status bar) notification code</span></span>

<span data-ttu-id="863bf-106">Уведомляет родительские окна элемента управления "строка состояния", что пользователь дважды щелкнул правой кнопкой мыши внутри элемента управления.</span><span class="sxs-lookup"><span data-stu-id="863bf-106">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="863bf-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="863bf-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="863bf-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="863bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="863bf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="863bf-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="863bf-110">Указатель на структуру [**нммаусе**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) , содержащую дополнительные сведения об этом уведомлении.</span><span class="sxs-lookup"><span data-stu-id="863bf-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="863bf-111">Элемент **двитемспек** содержит индекс раздела, который был выбран.</span><span class="sxs-lookup"><span data-stu-id="863bf-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="863bf-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="863bf-112">Return value</span></span>

<span data-ttu-id="863bf-113">Возвращает **значение true** , чтобы указать, что нажатие кнопки мыши было обработано, и подавить обработку по умолчанию системой.</span><span class="sxs-lookup"><span data-stu-id="863bf-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="863bf-114">Возвращает **значение false** , чтобы разрешить обработку по умолчанию щелчка.</span><span class="sxs-lookup"><span data-stu-id="863bf-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="863bf-115">Требования</span><span class="sxs-lookup"><span data-stu-id="863bf-115">Requirements</span></span>



| <span data-ttu-id="863bf-116">Требование</span><span class="sxs-lookup"><span data-stu-id="863bf-116">Requirement</span></span> | <span data-ttu-id="863bf-117">Значение</span><span class="sxs-lookup"><span data-stu-id="863bf-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="863bf-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="863bf-118">Minimum supported client</span></span><br/> | <span data-ttu-id="863bf-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="863bf-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="863bf-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="863bf-120">Minimum supported server</span></span><br/> | <span data-ttu-id="863bf-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="863bf-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="863bf-122">Header</span><span class="sxs-lookup"><span data-stu-id="863bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="863bf-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="863bf-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





