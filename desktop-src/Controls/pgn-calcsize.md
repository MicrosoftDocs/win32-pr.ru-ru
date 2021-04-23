---
title: Код уведомления PGN_CALCSIZE (Коммктрл. h)
description: Посылается элементом управления страничного навигатора для получения прокручиваемых измерений автономного окна.
ms.assetid: a15f4191-2f26-4139-bdaf-bab219449b78
keywords:
- PGN_CALCSIZE кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- PGN_CALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee6de1c45402f8bdc154f9f10be00140d7c766c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802063"
---
# <a name="pgn_calcsize-notification-code"></a><span data-ttu-id="bf6e1-104">\_Код уведомления ПГН калксизе</span><span class="sxs-lookup"><span data-stu-id="bf6e1-104">PGN\_CALCSIZE notification code</span></span>

<span data-ttu-id="bf6e1-105">Посылается элементом управления страничного навигатора для получения прокручиваемых измерений автономного окна.</span><span class="sxs-lookup"><span data-stu-id="bf6e1-105">Sent by a pager control to obtain the scrollable dimensions of the contained window.</span></span> <span data-ttu-id="bf6e1-106">Эти измерения используются элементом управления страничного навигатора для определения размера прокрутки автономного окна.</span><span class="sxs-lookup"><span data-stu-id="bf6e1-106">These dimensions are used by the pager control to determine the scrollable size of the contained window.</span></span> <span data-ttu-id="bf6e1-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="bf6e1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PGN_CALCSIZE

    lpnmcs = (LPNMPGCALCSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="bf6e1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf6e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf6e1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bf6e1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bf6e1-110">Указатель на структуру [**нмпгкалксизе**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) , которая содержит и получает сведения о коде уведомления.</span><span class="sxs-lookup"><span data-stu-id="bf6e1-110">Pointer to an [**NMPGCALCSIZE**](/windows/desktop/api/Commctrl/ns-commctrl-nmpgcalcsize) structure that contains and receives information about the notification code.</span></span> <span data-ttu-id="bf6e1-111">Элемент **dwFlag** этой структуры указывает, какое измерение вычисляется.</span><span class="sxs-lookup"><span data-stu-id="bf6e1-111">The **dwFlag** member of this structure indicates which dimension is being calculated.</span></span> <span data-ttu-id="bf6e1-112">В зависимости от значения **dwFlag** следует поместить нужное измерение в элемент **ивидс** или **ихеигхт** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="bf6e1-112">Depending on the value of **dwFlag**, you should place the desired dimension in the **iWidth** or **iHeight** member of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf6e1-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf6e1-113">Return value</span></span>

<span data-ttu-id="bf6e1-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="bf6e1-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf6e1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="bf6e1-115">Requirements</span></span>



| <span data-ttu-id="bf6e1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="bf6e1-116">Requirement</span></span> | <span data-ttu-id="bf6e1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bf6e1-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bf6e1-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf6e1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf6e1-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf6e1-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bf6e1-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf6e1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf6e1-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="bf6e1-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bf6e1-122">Header</span><span class="sxs-lookup"><span data-stu-id="bf6e1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf6e1-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf6e1-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





