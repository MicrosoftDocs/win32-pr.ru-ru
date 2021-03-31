---
title: Сообщение LVM_GETCOLUMNORDERARRAY (Коммктрл. h)
description: Возвращает текущий порядок столбцов слева направо в элементе управления "представление списка". Это сообщение можно отправить явным образом или использовать \_ макрос Жетколумнордераррай ListView.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- Элементы управления Windows для LVM_GETCOLUMNORDERARRAY сообщений
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071123"
---
# <a name="lvm_getcolumnorderarray-message"></a><span data-ttu-id="46fd1-105">\_Сообщение LVM жетколумнордераррай</span><span class="sxs-lookup"><span data-stu-id="46fd1-105">LVM\_GETCOLUMNORDERARRAY message</span></span>

<span data-ttu-id="46fd1-106">Возвращает текущий порядок столбцов слева направо в элементе управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="46fd1-106">Gets the current left-to-right order of columns in a list-view control.</span></span> <span data-ttu-id="46fd1-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетколумнордераррай ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .</span><span class="sxs-lookup"><span data-stu-id="46fd1-107">You can send this message explicitly or use the [**ListView\_GetColumnOrderArray**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="46fd1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="46fd1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46fd1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="46fd1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46fd1-110">Число столбцов в элементе управления "список".</span><span class="sxs-lookup"><span data-stu-id="46fd1-110">The number of columns in the list-view control.</span></span>

</dd> <dt>

<span data-ttu-id="46fd1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="46fd1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="46fd1-112">Указатель на массив целых чисел, который получает значения индекса столбцов в элементе управления List-View.</span><span class="sxs-lookup"><span data-stu-id="46fd1-112">A pointer to an array of integers that receives the index values of the columns in the list-view control.</span></span> <span data-ttu-id="46fd1-113">Массив должен быть достаточно большим, чтобы вместить элементы *wParam* .</span><span class="sxs-lookup"><span data-stu-id="46fd1-113">The array must be large enough to hold *wParam* elements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46fd1-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46fd1-114">Return value</span></span>

<span data-ttu-id="46fd1-115">В случае успеха возвращает ненулевое значение, и буфер в *lParam* получает индекс столбца для каждого столбца в элементе управления в том порядке, в котором они отображаются слева направо.</span><span class="sxs-lookup"><span data-stu-id="46fd1-115">If successful, returns nonzero, and the buffer at *lParam* receives the column index of each column in the control in the order they appear from left to right.</span></span> <span data-ttu-id="46fd1-116">В противном случае возвращаемое значение равно нулю.</span><span class="sxs-lookup"><span data-stu-id="46fd1-116">Otherwise, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="46fd1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="46fd1-117">Requirements</span></span>



| <span data-ttu-id="46fd1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="46fd1-118">Requirement</span></span> | <span data-ttu-id="46fd1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="46fd1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46fd1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46fd1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="46fd1-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="46fd1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="46fd1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46fd1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="46fd1-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="46fd1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46fd1-124">Header</span><span class="sxs-lookup"><span data-stu-id="46fd1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="46fd1-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="46fd1-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





