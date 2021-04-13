---
title: Сообщение TVM_SORTCHILDRENCB (Коммктрл. h)
description: Сортирует элементы древовидного представления с помощью определяемой приложением функции обратного вызова, которая сравнивает элементы. Это сообщение можно отправить явно или с помощью \_ макроса Сортчилдренкб TreeView.
ms.assetid: 1669e576-5e57-49f6-8097-7d6547306014
keywords:
- Элементы управления Windows для TVM_SORTCHILDRENCB сообщений
topic_type:
- apiref
api_name:
- TVM_SORTCHILDRENCB
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1dab4abbbc019a81d7a066c81dbb3537a0d80d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492837"
---
# <a name="tvm_sortchildrencb-message"></a><span data-ttu-id="9e5ea-105">\_Сообщение TVM сортчилдренкб</span><span class="sxs-lookup"><span data-stu-id="9e5ea-105">TVM\_SORTCHILDRENCB message</span></span>

<span data-ttu-id="9e5ea-106">Сортирует элементы древовидного представления с помощью определяемой приложением функции обратного вызова, которая сравнивает элементы.</span><span class="sxs-lookup"><span data-stu-id="9e5ea-106">Sorts tree-view items using an application-defined callback function that compares the items.</span></span> <span data-ttu-id="9e5ea-107">Это сообщение можно отправить явно или с помощью макроса [**\_ сортчилдренкб TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) .</span><span class="sxs-lookup"><span data-stu-id="9e5ea-107">You can send this message explicitly or by using the [**TreeView\_SortChildrenCB**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_sortchildrencb) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e5ea-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e5ea-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5ea-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e5ea-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e5ea-110">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="9e5ea-110">Reserved.</span></span> <span data-ttu-id="9e5ea-111">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9e5ea-111">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e5ea-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e5ea-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e5ea-113">Указатель на структуру [**твсорткб**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) .</span><span class="sxs-lookup"><span data-stu-id="9e5ea-113">Pointer to a [**TVSORTCB**](/windows/win32/api/commctrl/ns-commctrl-tvsortcb) structure.</span></span> <span data-ttu-id="9e5ea-114">Элемент **лпфнкомпаре** является адресом определяемой приложением функции обратного вызова, которая вызывается во время операции сортировки каждый раз, когда необходимо сравнивать относительный порядок двух элементов списка.</span><span class="sxs-lookup"><span data-stu-id="9e5ea-114">The **lpfnCompare** member is the address of the application-defined callback function, which is called during the sort operation each time the relative order of two list items needs to be compared.</span></span> <span data-ttu-id="9e5ea-115">Дополнительные сведения о функции обратного вызова см. в описании **твсорткб**.</span><span class="sxs-lookup"><span data-stu-id="9e5ea-115">For more information about the callback function, see the description of **TVSORTCB**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5ea-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e5ea-116">Return value</span></span>

<span data-ttu-id="9e5ea-117">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9e5ea-117">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e5ea-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9e5ea-118">Requirements</span></span>



| <span data-ttu-id="9e5ea-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9e5ea-119">Requirement</span></span> | <span data-ttu-id="9e5ea-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9e5ea-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5ea-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9e5ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5ea-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e5ea-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e5ea-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9e5ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5ea-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9e5ea-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e5ea-125">Header</span><span class="sxs-lookup"><span data-stu-id="9e5ea-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e5ea-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e5ea-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





