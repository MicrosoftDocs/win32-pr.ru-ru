---
title: Сообщение SB_GETRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник части в окне состояния.
ms.assetid: 76b8d470-07ae-440b-9bf5-7875b80b0168
keywords:
- Элементы управления Windows для SB_GETRECT сообщений
topic_type:
- apiref
api_name:
- SB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b48808b7bdf9c97fa6b9da53112e505e8cb8e66e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491994"
---
# <a name="sb_getrect-message"></a><span data-ttu-id="77765-104">\_Сообщение SB</span><span class="sxs-lookup"><span data-stu-id="77765-104">SB\_GETRECT message</span></span>

<span data-ttu-id="77765-105">Извлекает ограничивающий прямоугольник части в окне состояния.</span><span class="sxs-lookup"><span data-stu-id="77765-105">Retrieves the bounding rectangle of a part in a status window.</span></span>

## <a name="parameters"></a><span data-ttu-id="77765-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77765-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77765-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77765-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77765-108">Отсчитываемый от нуля индекс части, для которой необходимо извлечь ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="77765-108">Zero-based index of the part whose bounding rectangle is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="77765-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77765-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77765-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="77765-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77765-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="77765-111">Return value</span></span>

<span data-ttu-id="77765-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="77765-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="77765-113">Требования</span><span class="sxs-lookup"><span data-stu-id="77765-113">Requirements</span></span>



| <span data-ttu-id="77765-114">Требование</span><span class="sxs-lookup"><span data-stu-id="77765-114">Requirement</span></span> | <span data-ttu-id="77765-115">Значение</span><span class="sxs-lookup"><span data-stu-id="77765-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77765-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="77765-116">Minimum supported client</span></span><br/> | <span data-ttu-id="77765-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="77765-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77765-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="77765-118">Minimum supported server</span></span><br/> | <span data-ttu-id="77765-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="77765-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77765-120">Header</span><span class="sxs-lookup"><span data-stu-id="77765-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="77765-121"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="77765-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

