---
title: Сообщение HDM_SETORDERARRAY (Коммктрл. h)
description: Задает порядок элементов заголовка слева направо. Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса сетордераррай.
ms.assetid: 094c424f-10bd-484d-8236-937811b703a6
keywords:
- Элементы управления Windows для HDM_SETORDERARRAY сообщений
topic_type:
- apiref
api_name:
- HDM_SETORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f07874bfc102babec18b142a087b14e330044ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490866"
---
# <a name="hdm_setorderarray-message"></a><span data-ttu-id="1e9c3-105">\_Сообщение СЕТОРДЕРАРРАЙ HDM</span><span class="sxs-lookup"><span data-stu-id="1e9c3-105">HDM\_SETORDERARRAY message</span></span>

<span data-ttu-id="1e9c3-106">Задает порядок элементов заголовка слева направо.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-106">Sets the left-to-right order of header items.</span></span> <span data-ttu-id="1e9c3-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ сетордераррай**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) .</span><span class="sxs-lookup"><span data-stu-id="1e9c3-107">You can send this message explicitly or use the [**Header\_SetOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-header_setorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="1e9c3-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e9c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e9c3-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1e9c3-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9c3-110">Размер буфера в параметре *lParam* в элементах.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-110">The size of the buffer at *lParam*, in elements.</span></span> <span data-ttu-id="1e9c3-111">Это значение должно равняться значению, возвращаемому [**HDM \_ GETITEMCOUNT**](hdm-getitemcount.md).</span><span class="sxs-lookup"><span data-stu-id="1e9c3-111">This value must equal the value returned by [**HDM\_GETITEMCOUNT**](hdm-getitemcount.md).</span></span>

</dd> <dt>

<span data-ttu-id="1e9c3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e9c3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e9c3-113">Указатель на массив, указывающий порядок отображения элементов слева направо.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-113">A pointer to an array that specifies the order in which items should be displayed, from left to right.</span></span> <span data-ttu-id="1e9c3-114">Например, если содержимое массива равно {2,0,1} , элемент управления отображает элемент 2, элемент 0 и элемент 1, слева направо.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-114">For example, if the contents of the array are {2,0,1}, the control displays item 2, item 0, and item 1, from left to right.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e9c3-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e9c3-115">Return value</span></span>

<span data-ttu-id="1e9c3-116">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="1e9c3-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e9c3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1e9c3-117">Requirements</span></span>



| <span data-ttu-id="1e9c3-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1e9c3-118">Requirement</span></span> | <span data-ttu-id="1e9c3-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1e9c3-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e9c3-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1e9c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1e9c3-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e9c3-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e9c3-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1e9c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1e9c3-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1e9c3-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e9c3-124">Header</span><span class="sxs-lookup"><span data-stu-id="1e9c3-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e9c3-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e9c3-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





