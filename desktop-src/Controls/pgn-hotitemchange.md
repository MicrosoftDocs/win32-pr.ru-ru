---
title: Сообщение PGN_HOTITEMCHANGE (Коммктрл. h)
description: Сообщает родительскому окну элемента управления страничного навигатора, что элемент "горячий" (выделенный) изменился. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- Элементы управления Windows для PGN_HOTITEMCHANGE сообщений
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 573f3dd93a6e4b0b3db6682d36804416d6f6f1e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071517"
---
# <a name="pgn_hotitemchange-message"></a><span data-ttu-id="58452-105">\_Сообщение ПГН хотитемчанже</span><span class="sxs-lookup"><span data-stu-id="58452-105">PGN\_HOTITEMCHANGE message</span></span>

<span data-ttu-id="58452-106">Сообщает родительскому окну элемента управления страничного навигатора, что элемент "горячий" (выделенный) изменился.</span><span class="sxs-lookup"><span data-stu-id="58452-106">Notifies a pager control's parent window that the hot (highlighted) item has change.</span></span> <span data-ttu-id="58452-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="58452-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="58452-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="58452-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58452-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="58452-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="58452-110">Указатель на структуру [**нмпгхотитем**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) , содержащую сведения об этом коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="58452-110">Pointer to a [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58452-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="58452-111">Return value</span></span>

<span data-ttu-id="58452-112">Возвращает ноль для выделения элемента или ненулевого значения, чтобы предотвратить выделение.</span><span class="sxs-lookup"><span data-stu-id="58452-112">Return zero to highlight the item or nonzero to prevent highlighting.</span></span>

## <a name="remarks"></a><span data-ttu-id="58452-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="58452-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58452-114">Чтобы использовать этот код уведомления, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="58452-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="58452-115">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="58452-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58452-116">Требования</span><span class="sxs-lookup"><span data-stu-id="58452-116">Requirements</span></span>



| <span data-ttu-id="58452-117">Требование</span><span class="sxs-lookup"><span data-stu-id="58452-117">Requirement</span></span> | <span data-ttu-id="58452-118">Значение</span><span class="sxs-lookup"><span data-stu-id="58452-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58452-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="58452-119">Minimum supported client</span></span><br/> | <span data-ttu-id="58452-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="58452-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="58452-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="58452-121">Minimum supported server</span></span><br/> | <span data-ttu-id="58452-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="58452-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="58452-123">Header</span><span class="sxs-lookup"><span data-stu-id="58452-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="58452-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="58452-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





