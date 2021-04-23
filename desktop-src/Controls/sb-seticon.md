---
title: Сообщение SB_SETICON (Коммктрл. h)
description: Задает значок для части в строке состояния.
ms.assetid: d8528cd1-54d2-44ba-b0d6-29111f75616a
keywords:
- Элементы управления Windows для SB_SETICON сообщений
topic_type:
- apiref
api_name:
- SB_SETICON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f720c414238eb89cf98bf0556ebabffefceae4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892349"
---
# <a name="sb_seticon-message"></a><span data-ttu-id="ed1c2-104">\_Сообщение SB сетикон</span><span class="sxs-lookup"><span data-stu-id="ed1c2-104">SB\_SETICON message</span></span>

<span data-ttu-id="ed1c2-105">Задает значок для части в строке состояния.</span><span class="sxs-lookup"><span data-stu-id="ed1c2-105">Sets the icon for a part in a status bar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ed1c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ed1c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed1c2-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ed1c2-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed1c2-108">Отсчитываемый от нуля индекс части, которая получит значок.</span><span class="sxs-lookup"><span data-stu-id="ed1c2-108">Zero-based index of the part that will receive the icon.</span></span> <span data-ttu-id="ed1c2-109">Если этот параметр имеет значение-1, строка состояния считается простой строкой состояния.</span><span class="sxs-lookup"><span data-stu-id="ed1c2-109">If this parameter is -1, the status bar is assumed to be a simple status bar.</span></span>

</dd> <dt>

<span data-ttu-id="ed1c2-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ed1c2-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ed1c2-111">Обрабатываемый значок.</span><span class="sxs-lookup"><span data-stu-id="ed1c2-111">Handle to the icon to be set.</span></span> <span data-ttu-id="ed1c2-112">Если это значение равно **null**, значок удаляется из части.</span><span class="sxs-lookup"><span data-stu-id="ed1c2-112">If this value is **NULL**, the icon is removed from the part.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed1c2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ed1c2-113">Return value</span></span>

<span data-ttu-id="ed1c2-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ed1c2-114">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed1c2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ed1c2-115">Remarks</span></span>

<span data-ttu-id="ed1c2-116">Строка состояния не приведет к уничтожению значка.</span><span class="sxs-lookup"><span data-stu-id="ed1c2-116">The status bar will not destroy the icon.</span></span> <span data-ttu-id="ed1c2-117">Это обязанность вызывающего приложения для наблюдения и уничтожения всех значков.</span><span class="sxs-lookup"><span data-stu-id="ed1c2-117">It is the calling application's responsibility to keep track of and destroy any icons.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed1c2-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ed1c2-118">Requirements</span></span>



| <span data-ttu-id="ed1c2-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ed1c2-119">Requirement</span></span> | <span data-ttu-id="ed1c2-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ed1c2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1c2-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ed1c2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ed1c2-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed1c2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ed1c2-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ed1c2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ed1c2-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="ed1c2-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ed1c2-125">Header</span><span class="sxs-lookup"><span data-stu-id="ed1c2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed1c2-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed1c2-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





