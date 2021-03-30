---
title: Сообщение TB_GETRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник для указанной кнопки панели инструментов.
ms.assetid: a93885eb-7eb7-4434-ad51-80fb30d3bfa1
keywords:
- Элементы управления Windows для TB_GETRECT сообщений
topic_type:
- apiref
api_name:
- TB_GETRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 889d067eb282e3d834ba4dc0cf6711c0561d86e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892722"
---
# <a name="tb_getrect-message"></a><span data-ttu-id="c7dcd-104">Сообщение о терабайте (ТБ) \_</span><span class="sxs-lookup"><span data-stu-id="c7dcd-104">TB\_GETRECT message</span></span>

<span data-ttu-id="c7dcd-105">Извлекает ограничивающий прямоугольник для указанной кнопки панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="c7dcd-105">Retrieves the bounding rectangle for a specified toolbar button.</span></span>

## <a name="parameters"></a><span data-ttu-id="c7dcd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c7dcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7dcd-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c7dcd-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7dcd-108">Идентификатор команды для кнопки.</span><span class="sxs-lookup"><span data-stu-id="c7dcd-108">Command identifier of the button.</span></span>

</dd> <dt>

<span data-ttu-id="c7dcd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c7dcd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c7dcd-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая будет принимать сведения об ограничивающем прямоугольнике.</span><span class="sxs-lookup"><span data-stu-id="c7dcd-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that will receive the bounding rectangle information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7dcd-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7dcd-111">Return value</span></span>

<span data-ttu-id="c7dcd-112">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c7dcd-112">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7dcd-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c7dcd-113">Remarks</span></span>

<span data-ttu-id="c7dcd-114">Это сообщение не извлекает ограничивающий прямоугольник для кнопок, состояние которых равно [**\_ скрытому**](toolbar-button-states.md) значению тбстате.</span><span class="sxs-lookup"><span data-stu-id="c7dcd-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7dcd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="c7dcd-115">Requirements</span></span>



| <span data-ttu-id="c7dcd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="c7dcd-116">Requirement</span></span> | <span data-ttu-id="c7dcd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="c7dcd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7dcd-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7dcd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c7dcd-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7dcd-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c7dcd-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7dcd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c7dcd-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c7dcd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7dcd-122">Header</span><span class="sxs-lookup"><span data-stu-id="c7dcd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7dcd-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7dcd-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

