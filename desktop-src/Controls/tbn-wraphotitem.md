---
title: Код уведомления TBN_WRAPHOTITEM (Коммктрл. h)
description: Уведомляет приложение с двумя или более панелями инструментов, которые должны быть изменены в активном элементе. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490191"
---
# <a name="tbn_wraphotitem-notification-code"></a><span data-ttu-id="97deb-105">\_Код уведомления ТБН врафотитем</span><span class="sxs-lookup"><span data-stu-id="97deb-105">TBN\_WRAPHOTITEM notification code</span></span>

<span data-ttu-id="97deb-106">Уведомляет приложение с двумя или более панелями инструментов, которые должны быть изменены в активном элементе.</span><span class="sxs-lookup"><span data-stu-id="97deb-106">Notifies an application with two or more toolbars that the hot item is about to change.</span></span> <span data-ttu-id="97deb-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="97deb-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="97deb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="97deb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97deb-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="97deb-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="97deb-110">Указатель на структуру, которая содержит старый элемент Hot (**истарт**) и указывает, находится ли новый горячий элемент перед ним (**идир** =-1) или после него (**идир** = 1), а также по причине изменения горячего элемента.</span><span class="sxs-lookup"><span data-stu-id="97deb-110">A pointer to a structure that contains the old hot item (**iStart**) and whether the new hot item is before it (**iDir** = -1) or after it (**iDir** = 1), as well as a reason why the hot item is changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97deb-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="97deb-111">Return value</span></span>

<span data-ttu-id="97deb-112">**Значение true** , если приложение обрабатывает горячее изменение элемента; в противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="97deb-112">**TRUE** if the application is handling the hot item change itself; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97deb-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="97deb-113">Remarks</span></span>

<span data-ttu-id="97deb-114">Структура **нмтбврафотитем** должна быть определена приложением следующим образом:</span><span class="sxs-lookup"><span data-stu-id="97deb-114">The **NMTBWRAPHOTITEM** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a><span data-ttu-id="97deb-115">Требования</span><span class="sxs-lookup"><span data-stu-id="97deb-115">Requirements</span></span>



| <span data-ttu-id="97deb-116">Требование</span><span class="sxs-lookup"><span data-stu-id="97deb-116">Requirement</span></span> | <span data-ttu-id="97deb-117">Значение</span><span class="sxs-lookup"><span data-stu-id="97deb-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="97deb-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97deb-118">Minimum supported client</span></span><br/> | <span data-ttu-id="97deb-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97deb-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="97deb-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97deb-120">Minimum supported server</span></span><br/> | <span data-ttu-id="97deb-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97deb-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="97deb-122">Header</span><span class="sxs-lookup"><span data-stu-id="97deb-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="97deb-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="97deb-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





