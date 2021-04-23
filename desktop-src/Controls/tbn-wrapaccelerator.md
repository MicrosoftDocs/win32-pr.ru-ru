---
title: Код уведомления TBN_WRAPACCELERATOR (Коммктрл. h)
description: Запрашивает индекс кнопки на одной или нескольких панелях инструментов, соответствующих указанному символу ускорителя. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: fc2443fd-e1b3-4085-b65d-96c08f544944
keywords:
- TBN_WRAPACCELERATOR кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_WRAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5e6063f8ac32b317b8f7ce37682b151c56a4a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654440"
---
# <a name="tbn_wrapaccelerator-notification-code"></a><span data-ttu-id="170f3-105">\_Код уведомления ТБН врапакцелератор</span><span class="sxs-lookup"><span data-stu-id="170f3-105">TBN\_WRAPACCELERATOR notification code</span></span>

<span data-ttu-id="170f3-106">Запрашивает индекс кнопки на одной или нескольких панелях инструментов, соответствующих указанному символу ускорителя.</span><span class="sxs-lookup"><span data-stu-id="170f3-106">Requests the index of the button in one or more toolbars corresponding to the specified accelerator character.</span></span> <span data-ttu-id="170f3-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="170f3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPACCELERATOR

    lpnmtb = (NMTBWRAPACCELERATOR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="170f3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="170f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="170f3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="170f3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="170f3-110">Указатель на структуру, содержащую символ клавиши быстрого вызова и получающий индекс соответствующей кнопки.</span><span class="sxs-lookup"><span data-stu-id="170f3-110">A pointer to a structure that contains the accelerator key character, and that receives the index of the corresponding button.</span></span> <span data-ttu-id="170f3-111">Индекс имеет значение-1, если ускоритель не соответствует команде.</span><span class="sxs-lookup"><span data-stu-id="170f3-111">The index is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="170f3-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="170f3-112">Return value</span></span>

<span data-ttu-id="170f3-113">**Значение true** , если возвращается индекс; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="170f3-113">**TRUE** if an index is returned, otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="170f3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="170f3-114">Remarks</span></span>

<span data-ttu-id="170f3-115">Приложения с одной или несколькими панелями инструментов могут получить этот код уведомления.</span><span class="sxs-lookup"><span data-stu-id="170f3-115">Applications with one or more toolbars may receive this notification code.</span></span>

<span data-ttu-id="170f3-116">Структура **нмтбврапакцелератор** должна быть определена приложением следующим образом:</span><span class="sxs-lookup"><span data-stu-id="170f3-116">The **NMTBWRAPACCELERATOR** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPACCELERATOR {
    NMHDR hdr;
    UINT ch;
    int iButton;
} NMTBWRAPACCELERATOR, *LPNMTBWRAPACCELERATOR;
```

## <a name="requirements"></a><span data-ttu-id="170f3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="170f3-117">Requirements</span></span>



| <span data-ttu-id="170f3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="170f3-118">Requirement</span></span> | <span data-ttu-id="170f3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="170f3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="170f3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="170f3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="170f3-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="170f3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="170f3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="170f3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="170f3-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="170f3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="170f3-124">Header</span><span class="sxs-lookup"><span data-stu-id="170f3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="170f3-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="170f3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





