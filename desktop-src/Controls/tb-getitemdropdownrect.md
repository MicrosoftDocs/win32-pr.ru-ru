---
title: Сообщение TB_GETITEMDROPDOWNRECT (Коммктрл. h)
description: Возвращает ограничивающий прямоугольник раскрывающегося окна для элемента панели инструментов с \_ раскрывающимся списком Style бтнс.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- Элементы управления Windows для TB_GETITEMDROPDOWNRECT сообщений
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071247"
---
# <a name="tb_getitemdropdownrect-message"></a><span data-ttu-id="9c5c8-104">\_Сообщение ЖЕТИТЕМДРОПДОВНРЕКТ ТБ</span><span class="sxs-lookup"><span data-stu-id="9c5c8-104">TB\_GETITEMDROPDOWNRECT message</span></span>

<span data-ttu-id="9c5c8-105">Возвращает ограничивающий прямоугольник раскрывающегося окна для элемента панели инструментов с [**\_ раскрывающимся списком Style бтнс**](toolbar-control-and-button-styles.md).</span><span class="sxs-lookup"><span data-stu-id="9c5c8-105">Gets the bounding rectangle of the dropdown window for a toolbar item with style [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md).</span></span>

## <a name="parameters"></a><span data-ttu-id="9c5c8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c5c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c5c8-107">*wParam* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9c5c8-107">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9c5c8-108">Отсчитываемый от нуля индекс элемента управления ToolBar, для которого требуется получить ограничивающий прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-108">The zero-based index of the toolbar control item for which to retrieve the bounding rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="9c5c8-109">*lParam* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9c5c8-109">*lParam* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="9c5c8-110">Указатель на структуру <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> для получения сведений о ограничивающем прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-110">A pointer to a <a href="/previous-versions//dd162897(v=vs.85)">**RECT**</a> structure to receive the bounding rectangle information.</span></span> <span data-ttu-id="9c5c8-111">Отправитель сообщения отвечает за выделение этой структуры.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-111">The message sender is responsible for allocating this structure.</span></span> <span data-ttu-id="9c5c8-112">Координаты, возвращаемые в структуре **Rect** , выражаются как клиентские координаты.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-112">The coordinates returned in the **RECT** structure are expressed as client coordinates.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c5c8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c5c8-113">Return value</span></span>

<span data-ttu-id="9c5c8-114">Всегда возвращает ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="9c5c8-114">Always returns nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c5c8-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9c5c8-115">Remarks</span></span>

<span data-ttu-id="9c5c8-116">Элемент должен иметь стиль [**\_ раскрывающегося списка бтнс**](toolbar-control-and-button-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9c5c8-116">The item must have the [**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c5c8-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9c5c8-117">Requirements</span></span>



| <span data-ttu-id="9c5c8-118">Требование</span><span class="sxs-lookup"><span data-stu-id="9c5c8-118">Requirement</span></span> | <span data-ttu-id="9c5c8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="9c5c8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c5c8-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c5c8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9c5c8-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c5c8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c5c8-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c5c8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9c5c8-123">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c5c8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c5c8-124">Header</span><span class="sxs-lookup"><span data-stu-id="9c5c8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c5c8-125"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c5c8-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

