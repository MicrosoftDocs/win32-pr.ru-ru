---
title: Код уведомления RBN_MINMAX (Коммктрл. h)
description: Посылается элементом управления "Главная панель" до максимизации или минимизации полосы. Этот код уведомления отправляется в виде \_ сообщения WM notify.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- RBN_MINMAX кода уведомления элементы управления Windows
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654533"
---
# <a name="rbn_minmax-notification-code"></a><span data-ttu-id="764fc-105">\_Код уведомления РБН MINMAX</span><span class="sxs-lookup"><span data-stu-id="764fc-105">RBN\_MINMAX notification code</span></span>

<span data-ttu-id="764fc-106">Посылается элементом управления "Главная панель" до максимизации или минимизации полосы.</span><span class="sxs-lookup"><span data-stu-id="764fc-106">Sent by a rebar control prior to maximizing or minimizing a band.</span></span> <span data-ttu-id="764fc-107">Этот код уведомления отправляется в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="764fc-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_MINMAX
```



## <a name="parameters"></a><span data-ttu-id="764fc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="764fc-108">Parameters</span></span>

<span data-ttu-id="764fc-109">Этот код уведомления не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="764fc-109">This notification code has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="764fc-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="764fc-110">Return value</span></span>

<span data-ttu-id="764fc-111">Возвращает ненулевое значение, чтобы не допустить выполнения операции, ноль, чтобы разрешить продолжение.</span><span class="sxs-lookup"><span data-stu-id="764fc-111">Return a nonzero value to prevent the operation from taking place, zero to allow it to continue.</span></span>

## <a name="requirements"></a><span data-ttu-id="764fc-112">Требования</span><span class="sxs-lookup"><span data-stu-id="764fc-112">Requirements</span></span>



| <span data-ttu-id="764fc-113">Требование</span><span class="sxs-lookup"><span data-stu-id="764fc-113">Requirement</span></span> | <span data-ttu-id="764fc-114">Значение</span><span class="sxs-lookup"><span data-stu-id="764fc-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="764fc-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="764fc-115">Minimum supported client</span></span><br/> | <span data-ttu-id="764fc-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="764fc-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="764fc-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="764fc-117">Minimum supported server</span></span><br/> | <span data-ttu-id="764fc-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="764fc-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="764fc-119">Header</span><span class="sxs-lookup"><span data-stu-id="764fc-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="764fc-120"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="764fc-120"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





