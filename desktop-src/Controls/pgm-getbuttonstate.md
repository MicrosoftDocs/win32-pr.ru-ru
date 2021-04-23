---
title: Сообщение PGM_GETBUTTONSTATE (Коммктрл. h)
description: Получает состояние указанной кнопки в элементе управления страничного навигатора. Это сообщение можно отправить явным образом или использовать \_ макрос Жетбуттонстате пейджера.
ms.assetid: 58f99b67-fef7-4695-86e2-0579a2f6de2f
keywords:
- Элементы управления Windows для PGM_GETBUTTONSTATE сообщений
topic_type:
- apiref
api_name:
- PGM_GETBUTTONSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d8c9eebbc0aa91651a01de1fe193544f0c8afcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988994"
---
# <a name="pgm_getbuttonstate-message"></a><span data-ttu-id="7db40-105">\_Сообщение ЖЕТБУТТОНСТАТЕ PGM</span><span class="sxs-lookup"><span data-stu-id="7db40-105">PGM\_GETBUTTONSTATE message</span></span>

<span data-ttu-id="7db40-106">Получает состояние указанной кнопки в элементе управления страничного навигатора.</span><span class="sxs-lookup"><span data-stu-id="7db40-106">Retrieves the state of the specified button in a pager control.</span></span> <span data-ttu-id="7db40-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ жетбуттонстате пейджера**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) .</span><span class="sxs-lookup"><span data-stu-id="7db40-107">You can send this message explicitly or use the [**Pager\_GetButtonState**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getbuttonstate) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="7db40-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7db40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7db40-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7db40-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7db40-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="7db40-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7db40-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7db40-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7db40-112">Указывает кнопку, для которой нужно получить состояние.</span><span class="sxs-lookup"><span data-stu-id="7db40-112">Indicates which button to retrieve the state for.</span></span> <span data-ttu-id="7db40-113">Может иметь одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="7db40-113">This can be one of the following values:</span></span>



| <span data-ttu-id="7db40-114">Значение</span><span class="sxs-lookup"><span data-stu-id="7db40-114">Value</span></span>                                                                                                                                                                     | <span data-ttu-id="7db40-115">Значение</span><span class="sxs-lookup"><span data-stu-id="7db40-115">Meaning</span></span>                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PGB_TOPORLEFT"></span><span id="pgb_toporleft"></span><dl> <span data-ttu-id="7db40-116"><dt>**ПГБ \_ топорлефт**</dt></span><span class="sxs-lookup"><span data-stu-id="7db40-116"><dt>**PGB\_TOPORLEFT**</dt></span></span> </dl>             | <span data-ttu-id="7db40-117">Указывает верхнюю кнопку в элементе управления страничного навигатора [**ПГС \_**](pager-control-styles.md) или в левой кнопке в элементе управления страничного навигатора [**ПГС \_ горизонтали**](pager-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7db40-117">Indicates the top button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the left button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/>     |
| <span id="PGB_BOTTOMORRIGHT"></span><span id="pgb_bottomorright"></span><dl> <span data-ttu-id="7db40-118"><dt>**ПГБ \_ боттоморригхт**</dt></span><span class="sxs-lookup"><span data-stu-id="7db40-118"><dt>**PGB\_BOTTOMORRIGHT**</dt></span></span> </dl> | <span data-ttu-id="7db40-119">Указывает нижнюю кнопку в элементе управления страничного навигатора [**ПГС \_**](pager-control-styles.md) или на правой кнопке в элементе управления страничного навигатора [**ПГС \_ горизонтали**](pager-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="7db40-119">Indicates the bottom button in a [**PGS\_VERT**](pager-control-styles.md) pager control or the right button in a [**PGS\_HORZ**](pager-control-styles.md) pager control.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7db40-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7db40-120">Return value</span></span>

<span data-ttu-id="7db40-121">Возвращает состояние кнопки, указанной в параметре *lParam*.</span><span class="sxs-lookup"><span data-stu-id="7db40-121">Returns the state of the button specified in *lParam*.</span></span> <span data-ttu-id="7db40-122">Это будет одно или несколько из следующих значений (если возвращается больше одного значения, они будут объединены с помощью побитового или):</span><span class="sxs-lookup"><span data-stu-id="7db40-122">This will be one or more of the following values (if more then one value is returned they will be combined using a bitwise OR):</span></span>



| <span data-ttu-id="7db40-123">Код возврата</span><span class="sxs-lookup"><span data-stu-id="7db40-123">Return code</span></span>                                                                                   | <span data-ttu-id="7db40-124">Описание</span><span class="sxs-lookup"><span data-stu-id="7db40-124">Description</span></span>                                 |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="7db40-125"><dt>**ПГФ \_ невидимый**</dt></span><span class="sxs-lookup"><span data-stu-id="7db40-125"><dt>**PGF\_INVISIBLE**</dt></span></span> </dl> | <span data-ttu-id="7db40-126">Кнопка не видна.</span><span class="sxs-lookup"><span data-stu-id="7db40-126">The button is not visible.</span></span> <br/>      |
| <dl> <span data-ttu-id="7db40-127"><dt>**ПГФ, \_ Обычная**</dt></span><span class="sxs-lookup"><span data-stu-id="7db40-127"><dt>**PGF\_NORMAL**</dt></span></span> </dl>    | <span data-ttu-id="7db40-128">Кнопка находится в нормальном состоянии.</span><span class="sxs-lookup"><span data-stu-id="7db40-128">The button is in normal state.</span></span> <br/>  |
| <dl> <span data-ttu-id="7db40-129"><dt>**ПГФ \_ серый**</dt></span><span class="sxs-lookup"><span data-stu-id="7db40-129"><dt>**PGF\_GRAYED**</dt></span></span> </dl>    | <span data-ttu-id="7db40-130">Кнопка находится в неактивном состоянии.</span><span class="sxs-lookup"><span data-stu-id="7db40-130">The button is in grayed state.</span></span> <br/>  |
| <dl> <span data-ttu-id="7db40-131"><dt>**ПГФ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="7db40-131"><dt>**PGF\_DEPRESSED**</dt></span></span> </dl> | <span data-ttu-id="7db40-132">Кнопка находится в состоянии нажатия.</span><span class="sxs-lookup"><span data-stu-id="7db40-132">The button is in pressed state.</span></span> <br/> |
| <dl> <span data-ttu-id="7db40-133"><dt>**ПГФ \_ горячий**</dt></span><span class="sxs-lookup"><span data-stu-id="7db40-133"><dt>**PGF\_HOT**</dt></span></span> </dl>       | <span data-ttu-id="7db40-134">Кнопка находится в активном состоянии.</span><span class="sxs-lookup"><span data-stu-id="7db40-134">The button is in hot state.</span></span> <br/>     |



 

## <a name="requirements"></a><span data-ttu-id="7db40-135">Требования</span><span class="sxs-lookup"><span data-stu-id="7db40-135">Requirements</span></span>



| <span data-ttu-id="7db40-136">Требование</span><span class="sxs-lookup"><span data-stu-id="7db40-136">Requirement</span></span> | <span data-ttu-id="7db40-137">Значение</span><span class="sxs-lookup"><span data-stu-id="7db40-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7db40-138">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7db40-138">Minimum supported client</span></span><br/> | <span data-ttu-id="7db40-139">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7db40-139">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="7db40-140">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7db40-140">Minimum supported server</span></span><br/> | <span data-ttu-id="7db40-141">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7db40-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7db40-142">Header</span><span class="sxs-lookup"><span data-stu-id="7db40-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="7db40-143"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="7db40-143"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





