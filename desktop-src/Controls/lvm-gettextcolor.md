---
title: Сообщение LVM_GETTEXTCOLOR (Коммктрл. h)
description: Извлекает цвет текста элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Жеттекстколор ListView.
ms.assetid: 51685e61-dd0a-4c21-8c66-31cf72c2b3e4
keywords:
- Элементы управления Windows для LVM_GETTEXTCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_GETTEXTCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7686e8f06f49dbfc14899f47ba52017daaf23c07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654650"
---
# <a name="lvm_gettextcolor-message"></a><span data-ttu-id="cb30f-105">\_Сообщение LVM жеттекстколор</span><span class="sxs-lookup"><span data-stu-id="cb30f-105">LVM\_GETTEXTCOLOR message</span></span>

<span data-ttu-id="cb30f-106">Извлекает цвет текста элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="cb30f-106">Retrieves the text color of a list-view control.</span></span> <span data-ttu-id="cb30f-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жеттекстколор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) .</span><span class="sxs-lookup"><span data-stu-id="cb30f-107">You can send this message explicitly or by using the [**ListView\_GetTextColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="cb30f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb30f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb30f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb30f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cb30f-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cb30f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cb30f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb30f-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cb30f-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="cb30f-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb30f-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb30f-113">Return value</span></span>

<span data-ttu-id="cb30f-114">Возвращает цвет текста.</span><span class="sxs-lookup"><span data-stu-id="cb30f-114">Returns the text color.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb30f-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cb30f-115">Requirements</span></span>



| <span data-ttu-id="cb30f-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cb30f-116">Requirement</span></span> | <span data-ttu-id="cb30f-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cb30f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cb30f-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cb30f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cb30f-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb30f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cb30f-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cb30f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cb30f-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cb30f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cb30f-122">Header</span><span class="sxs-lookup"><span data-stu-id="cb30f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb30f-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb30f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





