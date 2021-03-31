---
title: Сообщение LVM_SETCOLUMNORDERARRAY (Коммктрл. h)
description: Устанавливает порядок столбцов слева направо в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Сетколумнордераррай ListView.
ms.assetid: 9b491832-42cc-4262-8f6c-23cbc2c889bf
keywords:
- Элементы управления Windows для LVM_SETCOLUMNORDERARRAY сообщений
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94fdeb27074a3f6762e7fb3788fd7ccc0a2dcc5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071115"
---
# <a name="lvm_setcolumnorderarray-message"></a><span data-ttu-id="2933c-105">\_Сообщение LVM сетколумнордераррай</span><span class="sxs-lookup"><span data-stu-id="2933c-105">LVM\_SETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="2933c-106">Устанавливает порядок столбцов слева направо в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="2933c-106">Sets the left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="2933c-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетколумнордераррай ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="2933c-107">You can send this message explicitly or use the [**ListView\_SetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="2933c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="2933c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2933c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2933c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2933c-110">Размер (в элементах) буфера в параметре *lParam*.</span><span class="sxs-lookup"><span data-stu-id="2933c-110">Size, in elements, of the buffer at *lParam*.</span></span>

</dd> <dt>

<span data-ttu-id="2933c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2933c-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2933c-112">Указатель на массив, указывающий порядок отображения столбцов слева направо.</span><span class="sxs-lookup"><span data-stu-id="2933c-112">Pointer to an array that specifies the order in which columns should be displayed, from left to right.</span></span> <span data-ttu-id="2933c-113">Например, если содержимое массива равно {2,0,1} , то элемент управления отображает столбец 2, столбец 0 и столбец 1 в этом порядке.</span><span class="sxs-lookup"><span data-stu-id="2933c-113">For example, if the contents of the array are {2,0,1}, the control displays column 2, column 0, and column 1 in that order.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2933c-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2933c-114">Return value</span></span>

<span data-ttu-id="2933c-115">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2933c-115">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2933c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="2933c-116">Requirements</span></span>



| <span data-ttu-id="2933c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="2933c-117">Requirement</span></span> | <span data-ttu-id="2933c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="2933c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2933c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2933c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2933c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2933c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2933c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2933c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2933c-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="2933c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2933c-123">Header</span><span class="sxs-lookup"><span data-stu-id="2933c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2933c-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2933c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





