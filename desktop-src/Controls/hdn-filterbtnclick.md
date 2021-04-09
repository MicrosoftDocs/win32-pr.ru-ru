---
title: Код уведомления HDN_FILTERBTNCLICK (Коммктрл. h)
description: Уведомляет родительское окно элемента управления заголовка при нажатии кнопки фильтра или в ответ на \_ сообщение СЕТИТЕМ HDM. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3dbbdab8adf0bee400d591f3d8b4cec6fa1ea81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891502"
---
# <a name="hdn_filterbtnclick-notification-code"></a><span data-ttu-id="ca944-105">\_Код уведомления ХДН филтербтнкликк</span><span class="sxs-lookup"><span data-stu-id="ca944-105">HDN\_FILTERBTNCLICK notification code</span></span>

<span data-ttu-id="ca944-106">Уведомляет родительское окно элемента управления заголовка при нажатии кнопки фильтра или в ответ на сообщение [**\_ сетитем HDM**](hdm-setitem.md) .</span><span class="sxs-lookup"><span data-stu-id="ca944-106">Notifies the header control's parent window when the filter button is clicked or in response to an [**HDM\_SETITEM**](hdm-setitem.md) message.</span></span> <span data-ttu-id="ca944-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="ca944-107">This notification code sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a><span data-ttu-id="ca944-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="ca944-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca944-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ca944-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ca944-110">Указатель на структуру [**нмхдфилтербтнкликк**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) , содержащую сведения о элементе управления "заголовок" и кнопку фильтра заголовка.</span><span class="sxs-lookup"><span data-stu-id="ca944-110">A pointer to an [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) structure that contains information about the header control and the header filter button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca944-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ca944-111">Return value</span></span>

<span data-ttu-id="ca944-112">Если вы возвращаете **значение true**, код уведомления [ХДН \_ филтерчанже](hdn-filterchange.md) будет отправлен в родительское окно элемента управления заголовка.</span><span class="sxs-lookup"><span data-stu-id="ca944-112">If you return **TRUE**, an [HDN\_FILTERCHANGE](hdn-filterchange.md) notification code will be sent to the header control's parent window.</span></span> <span data-ttu-id="ca944-113">Этот код уведомления дает родительскому окну возможность синхронизировать свои элементы пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ca944-113">This notification code gives the parent window an opportunity to synchronize its user interface elements.</span></span> <span data-ttu-id="ca944-114">Возвращает **значение false** , если не нужно отправлять уведомление.</span><span class="sxs-lookup"><span data-stu-id="ca944-114">Return **FALSE** if you do not want the notification sent.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca944-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ca944-115">Requirements</span></span>



| <span data-ttu-id="ca944-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ca944-116">Requirement</span></span> | <span data-ttu-id="ca944-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ca944-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca944-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca944-118">Minimum supported client</span></span><br/> | <span data-ttu-id="ca944-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ca944-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ca944-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca944-120">Minimum supported server</span></span><br/> | <span data-ttu-id="ca944-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ca944-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ca944-122">Header</span><span class="sxs-lookup"><span data-stu-id="ca944-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca944-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca944-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca944-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca944-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca944-125">**нмхдфилтербтнкликк**</span><span class="sxs-lookup"><span data-stu-id="ca944-125">**NMHDFILTERBTNCLICK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





