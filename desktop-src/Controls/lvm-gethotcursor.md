---
title: Сообщение LVM_GETHOTCURSOR (Коммктрл. h)
description: Получает значение ХКУРСОР, используемое, когда указатель находится над элементом, а активирована Оперативное отслеживание. Это сообщение можно отправить явным образом или использовать \_ макрос Жесоткурсор ListView.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- Элементы управления Windows для LVM_GETHOTCURSOR сообщений
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803406"
---
# <a name="lvm_gethotcursor-message"></a><span data-ttu-id="90725-105">\_Сообщение LVM жесоткурсор</span><span class="sxs-lookup"><span data-stu-id="90725-105">LVM\_GETHOTCURSOR message</span></span>

<span data-ttu-id="90725-106">Получает значение ХКУРСОР, используемое, когда указатель находится над элементом, а активирована Оперативное отслеживание.</span><span class="sxs-lookup"><span data-stu-id="90725-106">Retrieves the HCURSOR value used when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="90725-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жесоткурсор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="90725-107">You can send this message explicitly or use the [**ListView\_GetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="90725-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="90725-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90725-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="90725-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="90725-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="90725-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="90725-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="90725-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="90725-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="90725-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90725-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="90725-113">Return value</span></span>

<span data-ttu-id="90725-114">Возвращает значение ХКУРСОР, которое является маркером для курсора, который используется элементом управления "список" при включенном режиме отслеживания.</span><span class="sxs-lookup"><span data-stu-id="90725-114">Returns an HCURSOR value that is the handle to the cursor that the list-view control uses when hot tracking is enabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="90725-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90725-115">Remarks</span></span>

<span data-ttu-id="90725-116">Элемент управления "представление списка" использует функцию отслеживания и выбора при наведении указателя, если установлен стиль [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="90725-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="90725-117">Требования</span><span class="sxs-lookup"><span data-stu-id="90725-117">Requirements</span></span>



| <span data-ttu-id="90725-118">Требование</span><span class="sxs-lookup"><span data-stu-id="90725-118">Requirement</span></span> | <span data-ttu-id="90725-119">Значение</span><span class="sxs-lookup"><span data-stu-id="90725-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="90725-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="90725-120">Minimum supported client</span></span><br/> | <span data-ttu-id="90725-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="90725-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="90725-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="90725-122">Minimum supported server</span></span><br/> | <span data-ttu-id="90725-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="90725-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="90725-124">Header</span><span class="sxs-lookup"><span data-stu-id="90725-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="90725-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="90725-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





