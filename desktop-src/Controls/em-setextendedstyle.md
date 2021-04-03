---
title: Сообщение EM_SETEXTENDEDSTYLE (Коммктрл. h)
description: Информирует элемент управления "поле ввода" о необходимости установки расширенных стилей. Отправьте это сообщение или используйте макрос Edit \_ сетекстендедстиле.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- Элементы управления Windows для EM_SETEXTENDEDSTYLE сообщений
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137159"
---
# <a name="em_setextendedstyle-message"></a><span data-ttu-id="596fd-105">\_Сообщение СЕТЕКСТЕНДЕДСТИЛЕ EM</span><span class="sxs-lookup"><span data-stu-id="596fd-105">EM\_SETEXTENDEDSTYLE message</span></span>

<span data-ttu-id="596fd-106">Информирует элемент управления "поле ввода" о необходимости установки расширенных стилей.</span><span class="sxs-lookup"><span data-stu-id="596fd-106">Informs the edit control to set extended styles.</span></span> <span data-ttu-id="596fd-107">Отправьте это сообщение или используйте макрос [**Edit \_ сетекстендедстиле**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span><span class="sxs-lookup"><span data-stu-id="596fd-107">Send this message or use the macro [**Edit\_SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).</span></span>

## <a name="parameters"></a><span data-ttu-id="596fd-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="596fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="596fd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="596fd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="596fd-110">Маска, используемая для выбора устанавливаемых стилей.</span><span class="sxs-lookup"><span data-stu-id="596fd-110">Mask used to select the styles to be set.</span></span>

</dd> <dt>

<span data-ttu-id="596fd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="596fd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="596fd-112">Значение, указывающее расширенный стиль.</span><span class="sxs-lookup"><span data-stu-id="596fd-112">Value that indicates the extended style.</span></span> <span data-ttu-id="596fd-113">Дополнительные сведения о стилях см. в разделе [Правка Управление расширенными стилями](edit-control-window-extended-styles.md).</span><span class="sxs-lookup"><span data-stu-id="596fd-113">For more information on styles, see [Edit Control Extended Styles](edit-control-window-extended-styles.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="596fd-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="596fd-114">Return value</span></span>

<span data-ttu-id="596fd-115">Если это сообщение завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="596fd-115">If this message succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="596fd-116">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="596fd-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="596fd-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="596fd-117">Remarks</span></span>

<span data-ttu-id="596fd-118">Расширенные стили для элемента управления "поле ввода" не имеют никаких действий с расширенными стилями, используемыми с функцией [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) или функцией [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span><span class="sxs-lookup"><span data-stu-id="596fd-118">The extended styles for an edit control have nothing to do with the extended styles used with function [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) or function [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).</span></span>

## <a name="requirements"></a><span data-ttu-id="596fd-119">Требования</span><span class="sxs-lookup"><span data-stu-id="596fd-119">Requirements</span></span>



| <span data-ttu-id="596fd-120">Требование</span><span class="sxs-lookup"><span data-stu-id="596fd-120">Requirement</span></span> | <span data-ttu-id="596fd-121">Значение</span><span class="sxs-lookup"><span data-stu-id="596fd-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="596fd-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="596fd-122">Minimum supported client</span></span><br/> | <span data-ttu-id="596fd-123">\[Только для настольных приложений Windows 10 версии 1809\]</span><span class="sxs-lookup"><span data-stu-id="596fd-123">Windows 10, version 1809 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="596fd-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="596fd-124">Minimum supported server</span></span><br/> | <span data-ttu-id="596fd-125">\[Только для настольных приложений Windows Server 2019\]</span><span class="sxs-lookup"><span data-stu-id="596fd-125">Windows Server 2019 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="596fd-126">Header</span><span class="sxs-lookup"><span data-stu-id="596fd-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="596fd-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="596fd-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

