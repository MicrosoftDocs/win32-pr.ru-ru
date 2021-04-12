---
title: Сообщение HDM_GETITEMRECT (Коммктрл. h)
description: Возвращает ограничивающий прямоугольник для заданного элемента в элементе управления "заголовок". Это сообщение можно отправить явным образом или воспользоваться заголовком \_ макроса жетитемрект.
ms.assetid: b483ef97-3700-425b-8160-81c673850f68
keywords:
- Элементы управления Windows для HDM_GETITEMRECT сообщений
topic_type:
- apiref
api_name:
- HDM_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4baec72bd914a9d2dad72556a5444c0059452cf3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491475"
---
# <a name="hdm_getitemrect-message"></a><span data-ttu-id="25dda-105">\_Сообщение ЖЕТИТЕМРЕКТ HDM</span><span class="sxs-lookup"><span data-stu-id="25dda-105">HDM\_GETITEMRECT message</span></span>

<span data-ttu-id="25dda-106">Возвращает ограничивающий прямоугольник для заданного элемента в элементе управления "заголовок".</span><span class="sxs-lookup"><span data-stu-id="25dda-106">Gets the bounding rectangle for a given item in a header control.</span></span> <span data-ttu-id="25dda-107">Это сообщение можно отправить явным образом или воспользоваться [**заголовком макроса \_ жетитемрект**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) .</span><span class="sxs-lookup"><span data-stu-id="25dda-107">You can send this message explicitly or use the [**Header\_GetItemRect**](/windows/desktop/api/Commctrl/nf-commctrl-header_getitemrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="25dda-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="25dda-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25dda-109">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="25dda-109">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25dda-110">Отсчитываемый от нуля индекс элемента управления заголовка, для которого требуется получить ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="25dda-110">The zero-based index of the header control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="25dda-111">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="25dda-111">*lParam* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="25dda-112">Указатель на структуру [**Rect**](/windows/win32/api/windef/ns-windef-rect) , которая получает сведения об ограничивающем прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="25dda-112">A pointer to a [**RECT**](/windows/win32/api/windef/ns-windef-rect) structure that receives the bounding rectangle information.</span></span> <span data-ttu-id="25dda-113">Отправитель сообщения отвечает за выделение этой структуры.</span><span class="sxs-lookup"><span data-stu-id="25dda-113">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="25dda-114">Координаты, возвращаемые в структуре RECT, выражаются относительно родительского элемента управления заголовка.</span><span class="sxs-lookup"><span data-stu-id="25dda-114">The coordinates returned in the RECT structure are expressed relative to the header control parent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25dda-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="25dda-115">Return value</span></span>

<span data-ttu-id="25dda-116">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="25dda-116">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="25dda-117">Требования</span><span class="sxs-lookup"><span data-stu-id="25dda-117">Requirements</span></span>



| <span data-ttu-id="25dda-118">Требование</span><span class="sxs-lookup"><span data-stu-id="25dda-118">Requirement</span></span> | <span data-ttu-id="25dda-119">Значение</span><span class="sxs-lookup"><span data-stu-id="25dda-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="25dda-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="25dda-120">Minimum supported client</span></span><br/> | <span data-ttu-id="25dda-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25dda-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="25dda-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="25dda-122">Minimum supported server</span></span><br/> | <span data-ttu-id="25dda-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="25dda-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="25dda-124">Header</span><span class="sxs-lookup"><span data-stu-id="25dda-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="25dda-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="25dda-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





