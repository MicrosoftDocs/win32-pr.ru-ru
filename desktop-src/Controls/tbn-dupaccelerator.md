---
title: Код уведомления TBN_DUPACCELERATOR (Коммктрл. h)
description: Определяет, можно ли использовать сочетание клавиш на двух или более активных панелях инструментов. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 98068d1a-1460-4be3-8575-9294b82ce903
keywords:
- TBN_DUPACCELERATOR кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_DUPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e530fa2101f8145148b7ede7d74f53a1828fa58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071853"
---
# <a name="tbn_dupaccelerator-notification-code"></a><span data-ttu-id="11b7d-105">\_Код уведомления ТБН дупакцелератор</span><span class="sxs-lookup"><span data-stu-id="11b7d-105">TBN\_DUPACCELERATOR notification code</span></span>

<span data-ttu-id="11b7d-106">Определяет, можно ли использовать сочетание клавиш на двух или более активных панелях инструментов.</span><span class="sxs-lookup"><span data-stu-id="11b7d-106">Ascertains whether an accelerator key can be used on two or more active toolbars.</span></span> <span data-ttu-id="11b7d-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="11b7d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DUPACCELERATOR

    lpnmtb = (NMTBDUPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="11b7d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="11b7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11b7d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="11b7d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="11b7d-110">Указатель на структуру, которая предоставляет ускоритель и получает значение, указывающее, реагируют ли несколько панелей инструментов на один и тот же символ.</span><span class="sxs-lookup"><span data-stu-id="11b7d-110">A pointer to a structure that provides an accelerator and that receives a value specifying whether multiple toolbars respond to the same character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11b7d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="11b7d-111">Return value</span></span>

<span data-ttu-id="11b7d-112">Возвращает **значение true** в случае успеха, в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="11b7d-112">Returns **TRUE** if successful, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="11b7d-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11b7d-113">Remarks</span></span>

<span data-ttu-id="11b7d-114">Приложение должно объявить структуру **нмтбдупакцелератор** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="11b7d-114">The application must declare the **NMTBDUPACCELERATOR** structure as follows:</span></span>

``` syntax
typedef struct tagNMTBDUPACCELERATOR
{
    NMHDR hdr;
    UINT ch;   // The accelerator.
    BOOL fDup; // TRUE if multiple toolbars respond to the accelerator.
} NMTBDUPACCELERATOR, *LPNMTBDUPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="11b7d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="11b7d-115">Requirements</span></span>



| <span data-ttu-id="11b7d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="11b7d-116">Requirement</span></span> | <span data-ttu-id="11b7d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="11b7d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11b7d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="11b7d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="11b7d-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="11b7d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="11b7d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="11b7d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="11b7d-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="11b7d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="11b7d-122">Header</span><span class="sxs-lookup"><span data-stu-id="11b7d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="11b7d-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="11b7d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





