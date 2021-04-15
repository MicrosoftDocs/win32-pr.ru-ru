---
title: Код уведомления TBN_INITCUSTOMIZE (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что настройка запущена. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: f4b9a1b0-94f7-4b2b-81b3-772da09134d2
keywords:
- TBN_INITCUSTOMIZE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_INITCUSTOMIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d5e855374699a100bf78019f1ca3d89857bc7c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654417"
---
# <a name="tbn_initcustomize-notification-code"></a><span data-ttu-id="9f615-105">\_Код уведомления ТБН иниткустомизе</span><span class="sxs-lookup"><span data-stu-id="9f615-105">TBN\_INITCUSTOMIZE notification code</span></span>

<span data-ttu-id="9f615-106">Сообщает родительскому окну панели инструментов, что настройка запущена.</span><span class="sxs-lookup"><span data-stu-id="9f615-106">Notifies a toolbar's parent window that customizing has started.</span></span> <span data-ttu-id="9f615-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="9f615-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_INITCUSTOMIZE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9f615-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f615-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f615-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f615-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f615-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="9f615-110">Pointer to the toolbar's [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f615-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f615-111">Return value</span></span>

<span data-ttu-id="9f615-112">Возвращает ТБНРФ \_ хидехелп, чтобы отключить кнопку "Справка".</span><span class="sxs-lookup"><span data-stu-id="9f615-112">Returns TBNRF\_HIDEHELP to suppress the Help button.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f615-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9f615-113">Requirements</span></span>



| <span data-ttu-id="9f615-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9f615-114">Requirement</span></span> | <span data-ttu-id="9f615-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9f615-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f615-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f615-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9f615-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f615-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f615-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f615-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9f615-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f615-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f615-120">Header</span><span class="sxs-lookup"><span data-stu-id="9f615-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f615-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f615-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





