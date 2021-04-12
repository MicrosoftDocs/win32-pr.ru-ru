---
title: Сообщение LVM_SETHOVERTIME (Коммктрл. h)
description: Задает период времени, в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран. Это сообщение можно отправить явным образом или использовать \_ макрос Сесовертиме ListView.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- Элементы управления Windows для LVM_SETHOVERTIME сообщений
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135119"
---
# <a name="lvm_sethovertime-message"></a><span data-ttu-id="114e5-105">\_Сообщение LVM сесовертиме</span><span class="sxs-lookup"><span data-stu-id="114e5-105">LVM\_SETHOVERTIME message</span></span>

<span data-ttu-id="114e5-106">Задает период времени, в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран.</span><span class="sxs-lookup"><span data-stu-id="114e5-106">Sets the amount of time which the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="114e5-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сесовертиме ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .</span><span class="sxs-lookup"><span data-stu-id="114e5-107">You can send this message explicitly or use the [**ListView\_SetHoverTime**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="114e5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="114e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="114e5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="114e5-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="114e5-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="114e5-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="114e5-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="114e5-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="114e5-112">Новое время (в миллисекундах), в течение которого курсор мыши должен навести указатель на элемент, прежде чем он будет выбран.</span><span class="sxs-lookup"><span data-stu-id="114e5-112">The new amount of time, in milliseconds, that the mouse cursor must hover over an item before it is selected.</span></span> <span data-ttu-id="114e5-113">Если это значение равно (**DWORD**)-1, то во время наведения по умолчанию устанавливается значение времени наведения.</span><span class="sxs-lookup"><span data-stu-id="114e5-113">If this value is (**DWORD**)-1, then the hover time is set to the default hover time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="114e5-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="114e5-114">Return value</span></span>

<span data-ttu-id="114e5-115">Возвращает предыдущее время наведения.</span><span class="sxs-lookup"><span data-stu-id="114e5-115">Returns the previous hover time.</span></span>

## <a name="remarks"></a><span data-ttu-id="114e5-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="114e5-116">Remarks</span></span>

<span data-ttu-id="114e5-117">Время наведения на себя влияет только на элементы управления "представление списка", которые имеют расширенный стиль представления списка [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md), [**LVS \_ ex \_ онекликкактивате**](extended-list-view-styles.md)или [**LVS \_ ex \_ твокликкактивате**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="114e5-117">The hover time only affects list-view controls that have the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md), [**LVS\_EX\_ONECLICKACTIVATE**](extended-list-view-styles.md), or [**LVS\_EX\_TWOCLICKACTIVATE**](extended-list-view-styles.md) extended list-view style.</span></span>

## <a name="requirements"></a><span data-ttu-id="114e5-118">Требования</span><span class="sxs-lookup"><span data-stu-id="114e5-118">Requirements</span></span>



| <span data-ttu-id="114e5-119">Требование</span><span class="sxs-lookup"><span data-stu-id="114e5-119">Requirement</span></span> | <span data-ttu-id="114e5-120">Значение</span><span class="sxs-lookup"><span data-stu-id="114e5-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="114e5-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="114e5-121">Minimum supported client</span></span><br/> | <span data-ttu-id="114e5-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="114e5-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="114e5-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="114e5-123">Minimum supported server</span></span><br/> | <span data-ttu-id="114e5-124">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="114e5-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="114e5-125">Header</span><span class="sxs-lookup"><span data-stu-id="114e5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="114e5-126"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="114e5-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





