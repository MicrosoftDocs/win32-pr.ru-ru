---
title: Сообщение TB_GETIMAGELIST (Коммктрл. h)
description: Извлекает список изображений, используемый элементом управления Toolbar для отображения кнопок в состоянии по умолчанию. Элемент управления ToolBar использует этот список изображений для вывода кнопок, если они не являются неактивными или отключенными.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- Элементы управления Windows для TB_GETIMAGELIST сообщений
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801355"
---
# <a name="tb_getimagelist-message"></a><span data-ttu-id="9f46e-105">\_Сообщение ТБ</span><span class="sxs-lookup"><span data-stu-id="9f46e-105">TB\_GETIMAGELIST message</span></span>

<span data-ttu-id="9f46e-106">Извлекает список изображений, используемый элементом управления Toolbar для отображения кнопок в состоянии по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9f46e-106">Retrieves the image list that a toolbar control uses to display buttons in their default state.</span></span> <span data-ttu-id="9f46e-107">Элемент управления ToolBar использует этот список изображений для вывода кнопок, если они не являются неактивными или отключенными.</span><span class="sxs-lookup"><span data-stu-id="9f46e-107">A toolbar control uses this image list to display buttons when they are not hot or disabled.</span></span>

## <a name="parameters"></a><span data-ttu-id="9f46e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9f46e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f46e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9f46e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f46e-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9f46e-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="9f46e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9f46e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9f46e-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9f46e-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f46e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9f46e-113">Return value</span></span>

<span data-ttu-id="9f46e-114">Возвращает маркер в список изображений или **значение NULL** , если список изображений не задан.</span><span class="sxs-lookup"><span data-stu-id="9f46e-114">Returns the handle to the image list, or **NULL** if no image list is set.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f46e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9f46e-115">Requirements</span></span>



| <span data-ttu-id="9f46e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9f46e-116">Requirement</span></span> | <span data-ttu-id="9f46e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9f46e-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9f46e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9f46e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9f46e-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9f46e-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9f46e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9f46e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9f46e-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9f46e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9f46e-122">Header</span><span class="sxs-lookup"><span data-stu-id="9f46e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9f46e-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f46e-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





