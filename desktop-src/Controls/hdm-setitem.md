---
title: Сообщение HDM_SETITEM (Коммктрл. h)
description: Задает атрибуты указанного элемента в элементе управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса сетитем.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- Элементы управления Windows для HDM_SETITEM сообщений
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b03a05b909cf8c7887edd2031f5346c419f1cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492159"
---
# <a name="hdm_setitem-message"></a><span data-ttu-id="f0b7b-105">\_Сообщение СЕТИТЕМ HDM</span><span class="sxs-lookup"><span data-stu-id="f0b7b-105">HDM\_SETITEM message</span></span>

<span data-ttu-id="f0b7b-106">Задает атрибуты указанного элемента в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="f0b7b-106">Sets the attributes of the specified item in a header control.</span></span> <span data-ttu-id="f0b7b-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ сетитем**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) .</span><span class="sxs-lookup"><span data-stu-id="f0b7b-107">You can send this message explicitly or use the [**Header\_SetItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="f0b7b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f0b7b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0b7b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f0b7b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0b7b-110">Текущий индекс элемента, атрибуты которого необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="f0b7b-110">The current index of the item whose attributes are to be changed.</span></span>

</dd> <dt>

<span data-ttu-id="f0b7b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f0b7b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f0b7b-112">Указатель на структуру [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) , содержащую сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="f0b7b-112">A pointer to an [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that contains item information.</span></span> <span data-ttu-id="f0b7b-113">При отправке этого сообщения элемент **маски** структуры должен быть установлен, чтобы указать, какие атрибуты задаются.</span><span class="sxs-lookup"><span data-stu-id="f0b7b-113">When this message is sent, the **mask** member of the structure must be set to indicate which attributes are being set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0b7b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f0b7b-114">Return value</span></span>

<span data-ttu-id="f0b7b-115">Возвращает ненулевое значение при успешном выполнении или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f0b7b-115">Returns nonzero upon success, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0b7b-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f0b7b-116">Remarks</span></span>

<span data-ttu-id="f0b7b-117">Структура [**хдитем**](/windows/win32/api/commctrl/ns-commctrl-hditema) , поддерживающая это сообщение, поддерживает порядок элементов и сведения о списке изображений.</span><span class="sxs-lookup"><span data-stu-id="f0b7b-117">The [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure that supports this message supports item order and image list information.</span></span> <span data-ttu-id="f0b7b-118">С помощью этих членов можно управлять порядком отображения элементов и указывать изображения, отображаемые с элементами.</span><span class="sxs-lookup"><span data-stu-id="f0b7b-118">By using these members, you can control the order in which items are displayed and specify images to appear with items.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0b7b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f0b7b-119">Requirements</span></span>



| <span data-ttu-id="f0b7b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f0b7b-120">Requirement</span></span> | <span data-ttu-id="f0b7b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f0b7b-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f0b7b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f0b7b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f0b7b-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f0b7b-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f0b7b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f0b7b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f0b7b-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f0b7b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f0b7b-126">Header</span><span class="sxs-lookup"><span data-stu-id="f0b7b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0b7b-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0b7b-127"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="f0b7b-128">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f0b7b-128">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f0b7b-129">**Разъем HDM \_ СЕТИТЕМВ** (Юникод) и **HDM \_ сетитема** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f0b7b-129">**HDM\_SETITEMW** (Unicode) and **HDM\_SETITEMA** (ANSI)</span></span><br/>                   |



 

 





