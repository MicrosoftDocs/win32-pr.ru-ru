---
title: Сообщение LVM_GETTEXTBKCOLOR (Коммктрл. h)
description: Извлекает цвет фона текста для элемента управления "представление списка". Это сообщение можно отправить явно или с помощью \_ макроса Жеттекстбкколор ListView.
ms.assetid: 3d2c8be8-d7f9-4aa7-b358-f7effc6dbb25
keywords:
- Элементы управления Windows для LVM_GETTEXTBKCOLOR сообщений
topic_type:
- apiref
api_name:
- LVM_GETTEXTBKCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bf5b6700904c5af47ef47e749dfa753c5ff8cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989172"
---
# <a name="lvm_gettextbkcolor-message"></a><span data-ttu-id="963e7-105">\_Сообщение LVM жеттекстбкколор</span><span class="sxs-lookup"><span data-stu-id="963e7-105">LVM\_GETTEXTBKCOLOR message</span></span>

<span data-ttu-id="963e7-106">Извлекает цвет фона текста для элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="963e7-106">Retrieves the text background color of a list-view control.</span></span> <span data-ttu-id="963e7-107">Это сообщение можно отправить явно или с помощью макроса [**\_ жеттекстбкколор ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) .</span><span class="sxs-lookup"><span data-stu-id="963e7-107">You can send this message explicitly or by using the [**ListView\_GetTextBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gettextbkcolor) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="963e7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="963e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="963e7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="963e7-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="963e7-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="963e7-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="963e7-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="963e7-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="963e7-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="963e7-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="963e7-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="963e7-113">Return value</span></span>

<span data-ttu-id="963e7-114">Возвращает цвет фона текста.</span><span class="sxs-lookup"><span data-stu-id="963e7-114">Returns the background color of the text.</span></span>

## <a name="requirements"></a><span data-ttu-id="963e7-115">Требования</span><span class="sxs-lookup"><span data-stu-id="963e7-115">Requirements</span></span>



| <span data-ttu-id="963e7-116">Требование</span><span class="sxs-lookup"><span data-stu-id="963e7-116">Requirement</span></span> | <span data-ttu-id="963e7-117">Значение</span><span class="sxs-lookup"><span data-stu-id="963e7-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="963e7-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="963e7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="963e7-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="963e7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="963e7-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="963e7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="963e7-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="963e7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="963e7-122">Header</span><span class="sxs-lookup"><span data-stu-id="963e7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="963e7-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="963e7-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





