---
title: Сообщение LVM_SETHOTCURSOR (Коммктрл. h)
description: Задает значение ХКУРСОР, которое используется элементом управления "представление списка" при наведении указателя мыши на элемент, пока включено отслеживание.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- Элементы управления Windows для LVM_SETHOTCURSOR сообщений
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801109"
---
# <a name="lvm_sethotcursor-message"></a><span data-ttu-id="8e04b-104">\_Сообщение LVM сесоткурсор</span><span class="sxs-lookup"><span data-stu-id="8e04b-104">LVM\_SETHOTCURSOR message</span></span>

<span data-ttu-id="8e04b-105">Задает значение ХКУРСОР, которое используется элементом управления "представление списка" при наведении указателя мыши на элемент, пока включено отслеживание.</span><span class="sxs-lookup"><span data-stu-id="8e04b-105">Sets the HCURSOR value that the list-view control uses when the pointer is over an item while hot tracking is enabled.</span></span> <span data-ttu-id="8e04b-106">Это сообщение можно отправить явным образом или использовать макрос [**\_ сесоткурсор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) .</span><span class="sxs-lookup"><span data-stu-id="8e04b-106">You can send this message explicitly or use the [**ListView\_SetHotCursor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) macro.</span></span> <span data-ttu-id="8e04b-107">Чтобы проверить, включено ли оперативное отслеживание, вызовите [**системпараметерсинфо**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span><span class="sxs-lookup"><span data-stu-id="8e04b-107">To check whether hot tracking is enabled, call [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).</span></span>

## <a name="parameters"></a><span data-ttu-id="8e04b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8e04b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e04b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8e04b-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8e04b-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="8e04b-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8e04b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8e04b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8e04b-112">Указатель на заданный курсор.</span><span class="sxs-lookup"><span data-stu-id="8e04b-112">Handle to the cursor to be set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e04b-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8e04b-113">Return value</span></span>

<span data-ttu-id="8e04b-114">Возвращает значение ХКУРСОР, которое является предыдущим активным курсором.</span><span class="sxs-lookup"><span data-stu-id="8e04b-114">Returns an HCURSOR value that is the previous hot cursor.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e04b-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8e04b-115">Remarks</span></span>

<span data-ttu-id="8e04b-116">Элемент управления "представление списка" использует функцию отслеживания и выбора при наведении указателя, если установлен стиль [**LVS \_ ex \_ траккселект**](extended-list-view-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="8e04b-116">A list-view control uses hot tracking and hover selection when the [**LVS\_EX\_TRACKSELECT**](extended-list-view-styles.md) style is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e04b-117">Требования</span><span class="sxs-lookup"><span data-stu-id="8e04b-117">Requirements</span></span>



| <span data-ttu-id="8e04b-118">Требование</span><span class="sxs-lookup"><span data-stu-id="8e04b-118">Requirement</span></span> | <span data-ttu-id="8e04b-119">Значение</span><span class="sxs-lookup"><span data-stu-id="8e04b-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e04b-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8e04b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8e04b-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e04b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8e04b-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8e04b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8e04b-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="8e04b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8e04b-124">Header</span><span class="sxs-lookup"><span data-stu-id="8e04b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e04b-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e04b-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

