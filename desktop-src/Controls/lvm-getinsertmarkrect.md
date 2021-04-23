---
title: Сообщение LVM_GETINSERTMARKRECT (Коммктрл. h)
description: Извлекает прямоугольник, ограничивающий точку вставки.
ms.assetid: 7b10229c-73ab-426c-8a8a-71258a33e248
keywords:
- Элементы управления Windows для LVM_GETINSERTMARKRECT сообщений
topic_type:
- apiref
api_name:
- LVM_GETINSERTMARKRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd85bfb94f6425d2666372fd141b531fcb238643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989180"
---
# <a name="lvm_getinsertmarkrect-message"></a><span data-ttu-id="c0fc1-104">\_Сообщение LVM жетинсертмаркрект</span><span class="sxs-lookup"><span data-stu-id="c0fc1-104">LVM\_GETINSERTMARKRECT message</span></span>

<span data-ttu-id="c0fc1-105">Извлекает прямоугольник, ограничивающий точку вставки.</span><span class="sxs-lookup"><span data-stu-id="c0fc1-105">Retrieves the rectangle that bounds the insertion point.</span></span>

## <a name="parameters"></a><span data-ttu-id="c0fc1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c0fc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0fc1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c0fc1-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="c0fc1-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="c0fc1-108">Not used; must be zero.</span></span></dd> <dt>

<span data-ttu-id="c0fc1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c0fc1-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="c0fc1-110">Указатель на структуру <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> , содержащую координаты прямоугольника, ограничивающего точку вставки.</span><span class="sxs-lookup"><span data-stu-id="c0fc1-110">Pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure that contains the coordinates of a rectangle that bounds the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0fc1-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c0fc1-111">Return value</span></span>

<span data-ttu-id="c0fc1-112">Возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="c0fc1-112">Returns one of the following values.</span></span>



| <span data-ttu-id="c0fc1-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="c0fc1-113">Return code</span></span>                                                                      | <span data-ttu-id="c0fc1-114">Описание</span><span class="sxs-lookup"><span data-stu-id="c0fc1-114">Description</span></span>                          |
|----------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="c0fc1-115"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="c0fc1-115"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="c0fc1-116">Точка вставки не найдена.</span><span class="sxs-lookup"><span data-stu-id="c0fc1-116">No insertion point found.</span></span><br/> |
| <dl> <span data-ttu-id="c0fc1-117"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="c0fc1-117"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="c0fc1-118">Найдена точка вставки.</span><span class="sxs-lookup"><span data-stu-id="c0fc1-118">Insertion point found.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="c0fc1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c0fc1-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c0fc1-120">Чтобы использовать это сообщение, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="c0fc1-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c0fc1-121">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c0fc1-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c0fc1-122">Требования</span><span class="sxs-lookup"><span data-stu-id="c0fc1-122">Requirements</span></span>



| <span data-ttu-id="c0fc1-123">Требование</span><span class="sxs-lookup"><span data-stu-id="c0fc1-123">Requirement</span></span> | <span data-ttu-id="c0fc1-124">Значение</span><span class="sxs-lookup"><span data-stu-id="c0fc1-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0fc1-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c0fc1-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c0fc1-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0fc1-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0fc1-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c0fc1-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c0fc1-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c0fc1-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c0fc1-129">Header</span><span class="sxs-lookup"><span data-stu-id="c0fc1-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0fc1-130"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0fc1-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

