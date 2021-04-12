---
title: Сообщение EM_SELECTIONTYPE (RichEdit. h)
description: Определяет тип выбора для элемента управления Rich Edit.
ms.assetid: a4200e32-1056-47bd-be47-5fabaf99c058
keywords:
- Элементы управления Windows для EM_SELECTIONTYPE сообщений
topic_type:
- apiref
api_name:
- EM_SELECTIONTYPE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0deb62ac3bf774c72bb076f6fce9aa8c77b423f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535069"
---
# <a name="em_selectiontype-message"></a><span data-ttu-id="d081a-104">\_Сообщение СЕЛЕКТИОНТИПЕ EM</span><span class="sxs-lookup"><span data-stu-id="d081a-104">EM\_SELECTIONTYPE message</span></span>

<span data-ttu-id="d081a-105">Определяет тип выбора для элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d081a-105">Determines the selection type for a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d081a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d081a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d081a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d081a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d081a-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d081a-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d081a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d081a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d081a-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d081a-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d081a-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d081a-111">Return value</span></span>

<span data-ttu-id="d081a-112">Если выделение пустое, возвращаемое значение будет SEL \_ пустым.</span><span class="sxs-lookup"><span data-stu-id="d081a-112">If the selection is empty, the return value is SEL\_EMPTY.</span></span>

<span data-ttu-id="d081a-113">Если выделение не пустое, возвращаемое значение представляет собой набор флагов, содержащих одно или несколько из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d081a-113">If the selection is not empty, the return value is a set of flags containing one or more of the following values.</span></span>



| <span data-ttu-id="d081a-114">Код возврата</span><span class="sxs-lookup"><span data-stu-id="d081a-114">Return code</span></span>                                                                                     | <span data-ttu-id="d081a-115">Описание</span><span class="sxs-lookup"><span data-stu-id="d081a-115">Description</span></span>                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="d081a-116"><dt>**\_текст SEL**</dt></span><span class="sxs-lookup"><span data-stu-id="d081a-116"><dt>**SEL\_TEXT**</dt></span></span> </dl>        | <span data-ttu-id="d081a-117">Текст.</span><span class="sxs-lookup"><span data-stu-id="d081a-117">Text.</span></span><br/>                            |
| <dl> <span data-ttu-id="d081a-118"><dt>**\_объект SEL**</dt></span><span class="sxs-lookup"><span data-stu-id="d081a-118"><dt>**SEL\_OBJECT**</dt></span></span> </dl>      | <span data-ttu-id="d081a-119">По крайней мере один COM-объект.</span><span class="sxs-lookup"><span data-stu-id="d081a-119">At least one COM object.</span></span><br/>         |
| <dl> <span data-ttu-id="d081a-120"><dt>**SEL \_ (многосимвольный)**</dt></span><span class="sxs-lookup"><span data-stu-id="d081a-120"><dt>**SEL\_MULTICHAR**</dt></span></span> </dl>   | <span data-ttu-id="d081a-121">Более одного символа текста.</span><span class="sxs-lookup"><span data-stu-id="d081a-121">More than one character of text.</span></span><br/> |
| <dl> <span data-ttu-id="d081a-122"><dt>**\_объект SEL**</dt></span><span class="sxs-lookup"><span data-stu-id="d081a-122"><dt>**SEL\_MULTIOBJECT**</dt></span></span> </dl> | <span data-ttu-id="d081a-123">Более одного COM-объекта.</span><span class="sxs-lookup"><span data-stu-id="d081a-123">More than one COM object.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="d081a-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d081a-124">Remarks</span></span>

<span data-ttu-id="d081a-125">Это сообщение полезно при обработке [**\_ размера WM**](/windows/desktop/winmsg/wm-size) для родителя элемента управления неформатированного редактирования самого нижнего уровня.</span><span class="sxs-lookup"><span data-stu-id="d081a-125">This message is useful during [**WM\_SIZE**](/windows/desktop/winmsg/wm-size) processing for the parent of a bottomless rich edit control.</span></span>

## <a name="requirements"></a><span data-ttu-id="d081a-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d081a-126">Requirements</span></span>



| <span data-ttu-id="d081a-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d081a-127">Requirement</span></span> | <span data-ttu-id="d081a-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d081a-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d081a-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d081a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d081a-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d081a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d081a-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d081a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d081a-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d081a-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d081a-133">Header</span><span class="sxs-lookup"><span data-stu-id="d081a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="d081a-134"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d081a-134"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d081a-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d081a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d081a-136">**\_Размер WM**</span><span class="sxs-lookup"><span data-stu-id="d081a-136">**WM\_SIZE**</span></span>](/windows/desktop/winmsg/wm-size)
</dt> </dl>

 

