---
title: Сообщение EM_GETTYPOGRAPHYOPTIONS (RichEdit. h)
description: Возвращает текущее состояние типографских параметров элемента управления Rich Edit.
ms.assetid: 6ff5980e-3201-4b0f-9a03-3de78730ce33
keywords:
- Элементы управления Windows для EM_GETTYPOGRAPHYOPTIONS сообщений
topic_type:
- apiref
api_name:
- EM_GETTYPOGRAPHYOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d692639ba6c8cea758abe694faed3a46e3f65be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136850"
---
# <a name="em_gettypographyoptions-message"></a><span data-ttu-id="d7051-104">\_Сообщение ЖЕТТИПОГРАФЙОПТИОНС EM</span><span class="sxs-lookup"><span data-stu-id="d7051-104">EM\_GETTYPOGRAPHYOPTIONS message</span></span>

<span data-ttu-id="d7051-105">Возвращает текущее состояние типографских параметров элемента управления Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="d7051-105">Returns the current state of the typography options of a rich edit control.</span></span>

## <a name="parameters"></a><span data-ttu-id="d7051-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7051-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7051-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d7051-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7051-108">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d7051-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d7051-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d7051-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d7051-110">Не используется; должно быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="d7051-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7051-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7051-111">Return value</span></span>

<span data-ttu-id="d7051-112">Возвращает текущие параметры оформления.</span><span class="sxs-lookup"><span data-stu-id="d7051-112">Returns the current typography options.</span></span> <span data-ttu-id="d7051-113">Список параметров см. в разделе [**EM \_ сеттипографйоптионс**](em-settypographyoptions.md).</span><span class="sxs-lookup"><span data-stu-id="d7051-113">For a list of options, see [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d7051-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d7051-114">Remarks</span></span>

<span data-ttu-id="d7051-115">Вы можете включить дополнительные разрывы строк, отправив сообщение [**EM \_ сеттипографйоптионс**](em-settypographyoptions.md) .</span><span class="sxs-lookup"><span data-stu-id="d7051-115">You can turn on advanced line breaking by sending the [**EM\_SETTYPOGRAPHYOPTIONS**](em-settypographyoptions.md) message.</span></span> <span data-ttu-id="d7051-116">Расширенные и нормальные разрывы строк также можно включить автоматически с помощью элемента управления Rich Edit, если это необходимо для определенных языков.</span><span class="sxs-lookup"><span data-stu-id="d7051-116">Advanced and normal line breaking may also be turned on automatically by the rich edit control if it is needed for certain languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7051-117">Требования</span><span class="sxs-lookup"><span data-stu-id="d7051-117">Requirements</span></span>



| <span data-ttu-id="d7051-118">Требование</span><span class="sxs-lookup"><span data-stu-id="d7051-118">Requirement</span></span> | <span data-ttu-id="d7051-119">Значение</span><span class="sxs-lookup"><span data-stu-id="d7051-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7051-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d7051-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d7051-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d7051-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d7051-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d7051-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d7051-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d7051-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d7051-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="d7051-124">Redistributable</span></span><br/>          | <span data-ttu-id="d7051-125">Расширенное редактирование 3,0</span><span class="sxs-lookup"><span data-stu-id="d7051-125">Rich Edit 3.0</span></span><br/>                                                              |
| <span data-ttu-id="d7051-126">Header</span><span class="sxs-lookup"><span data-stu-id="d7051-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7051-127"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7051-127"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7051-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d7051-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="d7051-129">**Ссылки**</span><span class="sxs-lookup"><span data-stu-id="d7051-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d7051-130">**EM \_ сеттипографйоптионс**</span><span class="sxs-lookup"><span data-stu-id="d7051-130">**EM\_SETTYPOGRAPHYOPTIONS**</span></span>](em-settypographyoptions.md)
</dt> <dt>

<span data-ttu-id="d7051-131">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="d7051-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d7051-132">Общие сведения об элементах управления "поле ввода"</span><span class="sxs-lookup"><span data-stu-id="d7051-132">About Rich Edit Controls</span></span>](about-rich-edit-controls.md)
</dt> </dl>

 

 





