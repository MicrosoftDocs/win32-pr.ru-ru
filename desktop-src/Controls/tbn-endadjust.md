---
title: Код уведомления TBN_ENDADJUST (Коммктрл. h)
description: Сообщает родительскому окну панели инструментов, что пользователь остановил настройку панели инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 9a7496ec-787d-4571-8eca-50d60383519b
keywords:
- TBN_ENDADJUST кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_ENDADJUST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec420c535a207f02d12e17901efab1c18a11bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071514"
---
# <a name="tbn_endadjust-notification-code"></a><span data-ttu-id="a1074-105">\_Код уведомления ТБН ендаджуст</span><span class="sxs-lookup"><span data-stu-id="a1074-105">TBN\_ENDADJUST notification code</span></span>

<span data-ttu-id="a1074-106">Сообщает родительскому окну панели инструментов, что пользователь остановил настройку панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="a1074-106">Notifies a toolbar's parent window that the user has stopped customizing a toolbar.</span></span> <span data-ttu-id="a1074-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="a1074-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_ENDADJUST 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a1074-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1074-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1074-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a1074-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a1074-110">Указатель на структуру [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) , содержащую сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="a1074-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1074-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a1074-111">Return value</span></span>

<span data-ttu-id="a1074-112">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="a1074-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1074-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a1074-113">Requirements</span></span>



| <span data-ttu-id="a1074-114">Требование</span><span class="sxs-lookup"><span data-stu-id="a1074-114">Requirement</span></span> | <span data-ttu-id="a1074-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a1074-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1074-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a1074-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1074-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1074-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a1074-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a1074-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1074-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a1074-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1074-120">Header</span><span class="sxs-lookup"><span data-stu-id="a1074-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1074-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1074-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





