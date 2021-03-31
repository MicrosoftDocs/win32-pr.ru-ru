---
title: Сообщение LVM_SETITEMINDEXSTATE (Коммктрл. h)
description: Задает состояние элемента представления списка. Отправьте это сообщение явным образом или с помощью \_ макроса Сетитеминдексстате ListView.
ms.assetid: 9fea6420-320a-4d2a-84b5-7923fbb14655
keywords:
- Элементы управления Windows для LVM_SETITEMINDEXSTATE сообщений
topic_type:
- apiref
api_name:
- LVM_SETITEMINDEXSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ce8f6847c733127053e2162dd785d52fb77cfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071383"
---
# <a name="lvm_setitemindexstate-message"></a><span data-ttu-id="403b5-105">\_Сообщение LVM сетитеминдексстате</span><span class="sxs-lookup"><span data-stu-id="403b5-105">LVM\_SETITEMINDEXSTATE message</span></span>

<span data-ttu-id="403b5-106">Задает состояние элемента представления списка.</span><span class="sxs-lookup"><span data-stu-id="403b5-106">Sets the state of a list-view item.</span></span> <span data-ttu-id="403b5-107">Отправьте это сообщение явным образом или с помощью макроса [**\_ сетитеминдексстате ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) .</span><span class="sxs-lookup"><span data-stu-id="403b5-107">Send this message explicitly or by using the [**ListView\_SetItemIndexState**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setitemindexstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="403b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="403b5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="403b5-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="403b5-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403b5-110">Указатель на структуру [**лвитеминдекс**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) для элемента.</span><span class="sxs-lookup"><span data-stu-id="403b5-110">A pointer to an [**LVITEMINDEX**](/windows/win32/api/commctrl/ns-commctrl-lvitemindex) structure for the item.</span></span> <span data-ttu-id="403b5-111">Вызывающий процесс отвечает за выделение этой структуры и задание элементов.</span><span class="sxs-lookup"><span data-stu-id="403b5-111">The calling process is responsible for allocating this structure and setting the members.</span></span>

</dd> <dt>

<span data-ttu-id="403b5-112">*lParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="403b5-112">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="403b5-113">Указатель на структуру [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="403b5-113">A pointer to an [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span> <span data-ttu-id="403b5-114">Вызывающий процесс отвечает за выделение памяти для структуры.</span><span class="sxs-lookup"><span data-stu-id="403b5-114">The calling process is responsible for allocating memory for the structure.</span></span> <span data-ttu-id="403b5-115">Задайте для элемента **состояния** одно или несколько (как побитовое сочетание) флагов [состояния элементов списка](list-view-item-states.md) .</span><span class="sxs-lookup"><span data-stu-id="403b5-115">Set the **state** member to one or more (as a bitwise combination) of the [List-View Item States](list-view-item-states.md) flags.</span></span> <span data-ttu-id="403b5-116">Установите элемент **статемаск** структуры, чтобы указать допустимые биты элемента **State** .</span><span class="sxs-lookup"><span data-stu-id="403b5-116">Set the **stateMask** member of the structure to indicate the valid bits of the **state** member.</span></span> <span data-ttu-id="403b5-117">Дополнительные сведения см. в описании элемента **статемаск** структуры **лвитем** .</span><span class="sxs-lookup"><span data-stu-id="403b5-117">For more information, see the **stateMask** member of the **LVITEM** structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="403b5-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="403b5-118">Return value</span></span>

<span data-ttu-id="403b5-119">Возвращает одно из следующих значений типа **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="403b5-119">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="403b5-120">Код возврата</span><span class="sxs-lookup"><span data-stu-id="403b5-120">Return code</span></span>                                                                                  | <span data-ttu-id="403b5-121">Описание</span><span class="sxs-lookup"><span data-stu-id="403b5-121">Description</span></span>                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="403b5-122"><dt>**\_Ошибка E**</dt></span><span class="sxs-lookup"><span data-stu-id="403b5-122"><dt>**E\_FAIL**</dt></span></span> </dl>       | <span data-ttu-id="403b5-123">Не удалось задать состояние.</span><span class="sxs-lookup"><span data-stu-id="403b5-123">The state could not be set.</span></span><br/>                            |
| <dl> <span data-ttu-id="403b5-124"><dt>**\_непредвиденная E**</dt></span><span class="sxs-lookup"><span data-stu-id="403b5-124"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="403b5-125">Элемент управления "представление списка" не готов к работе.</span><span class="sxs-lookup"><span data-stu-id="403b5-125">The list-view control was not ready for the operation.</span></span><br/> |
| <dl> <span data-ttu-id="403b5-126"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="403b5-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="403b5-127">Операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="403b5-127">The operation was successful.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="403b5-128">Требования</span><span class="sxs-lookup"><span data-stu-id="403b5-128">Requirements</span></span>



| <span data-ttu-id="403b5-129">Требование</span><span class="sxs-lookup"><span data-stu-id="403b5-129">Requirement</span></span> | <span data-ttu-id="403b5-130">Значение</span><span class="sxs-lookup"><span data-stu-id="403b5-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="403b5-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="403b5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="403b5-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="403b5-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="403b5-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="403b5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="403b5-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="403b5-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="403b5-135">Header</span><span class="sxs-lookup"><span data-stu-id="403b5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="403b5-136"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="403b5-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





