---
title: Сообщение HDM_INSERTITEM (Коммктрл. h)
description: Вставляет новый элемент в элемент управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса InsertItem.
ms.assetid: aececf32-090d-4cd4-a239-4435a322f72e
keywords:
- Элементы управления Windows для HDM_INSERTITEM сообщений
topic_type:
- apiref
api_name:
- HDM_INSERTITEM
- HDM_INSERTITEMA
- HDM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9cabf86fea79fd437b3e9fb7e32890b3ba1a780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490710"
---
# <a name="hdm_insertitem-message"></a><span data-ttu-id="403bd-105">\_Сообщение INSERTITEM HDM</span><span class="sxs-lookup"><span data-stu-id="403bd-105">HDM\_INSERTITEM message</span></span>

<span data-ttu-id="403bd-106">Вставляет новый элемент в элемент управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="403bd-106">Inserts a new item into a header control.</span></span> <span data-ttu-id="403bd-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) .</span><span class="sxs-lookup"><span data-stu-id="403bd-107">You can send this message explicitly or use the [**Header\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_insertitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="403bd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="403bd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403bd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="403bd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="403bd-110">Индекс элемента, после которого вставляется новый элемент.</span><span class="sxs-lookup"><span data-stu-id="403bd-110">The index of the item after which the new item is to be inserted.</span></span> <span data-ttu-id="403bd-111">Новый элемент вставляется в конец элемента управления заголовка, если параметр *wParam* больше или равен числу элементов в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="403bd-111">The new item is inserted at the end of the header control if *wParam* is greater than or equal to the number of items in the control.</span></span> <span data-ttu-id="403bd-112">Если параметр *wParam* равен нулю, новый элемент вставляется в начало элемента управления заголовка.</span><span class="sxs-lookup"><span data-stu-id="403bd-112">If *wParam* is zero, the new item is inserted at the beginning of the header control.</span></span>

</dd> <dt>

<span data-ttu-id="403bd-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="403bd-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="403bd-114">Указатель на структуру [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) , содержащую сведения о новом элементе.</span><span class="sxs-lookup"><span data-stu-id="403bd-114">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains information about the new item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="403bd-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="403bd-115">Return value</span></span>

<span data-ttu-id="403bd-116">Возвращает индекс нового элемента, если он выполнен успешно, или значение-1 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="403bd-116">Returns the index of the new item if successful, or -1 otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="403bd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="403bd-117">Requirements</span></span>



| <span data-ttu-id="403bd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="403bd-118">Requirement</span></span> | <span data-ttu-id="403bd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="403bd-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="403bd-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="403bd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="403bd-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="403bd-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="403bd-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="403bd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="403bd-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="403bd-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="403bd-124">Header</span><span class="sxs-lookup"><span data-stu-id="403bd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="403bd-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="403bd-125"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="403bd-126">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="403bd-126">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="403bd-127">**Разъем HDM \_ ИНСЕРТИТЕМВ** (Юникод) и **HDM \_ инсертитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="403bd-127">**HDM\_INSERTITEMW** (Unicode) and **HDM\_INSERTITEMA** (ANSI)</span></span><br/>             |



 

 





