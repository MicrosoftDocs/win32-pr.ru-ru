---
title: Сообщение TB_GETITEMRECT (Коммктрл. h)
description: Извлекает ограничивающий прямоугольник кнопки на панели инструментов.
ms.assetid: 42c2c86e-0002-4029-be6a-fdfdf405b78c
keywords:
- Элементы управления Windows для TB_GETITEMRECT сообщений
topic_type:
- apiref
api_name:
- TB_GETITEMRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e71a4c6540a1a7ff918b97b3a331e692f6d44529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892342"
---
# <a name="tb_getitemrect-message"></a><span data-ttu-id="3f7df-104">\_Сообщение ЖЕТИТЕМРЕКТ ТБ</span><span class="sxs-lookup"><span data-stu-id="3f7df-104">TB\_GETITEMRECT message</span></span>

<span data-ttu-id="3f7df-105">Извлекает ограничивающий прямоугольник кнопки на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="3f7df-105">Retrieves the bounding rectangle of a button in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3f7df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f7df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f7df-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3f7df-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f7df-108">Отсчитываемый от нуля индекс кнопки, для которой требуется получить сведения.</span><span class="sxs-lookup"><span data-stu-id="3f7df-108">Zero-based index of the button for which to retrieve information.</span></span>

</dd> <dt>

<span data-ttu-id="3f7df-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3f7df-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3f7df-110">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает клиентские координаты ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="3f7df-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the client coordinates of the bounding rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f7df-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f7df-111">Return value</span></span>

<span data-ttu-id="3f7df-112">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3f7df-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f7df-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f7df-113">Remarks</span></span>

<span data-ttu-id="3f7df-114">Это сообщение не извлекает ограничивающий прямоугольник для кнопок, состояние которых равно [**\_ скрытому**](toolbar-button-states.md) значению тбстате.</span><span class="sxs-lookup"><span data-stu-id="3f7df-114">This message does not retrieve the bounding rectangle for buttons whose state is set to the [**TBSTATE\_HIDDEN**](toolbar-button-states.md) value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f7df-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3f7df-115">Requirements</span></span>



| <span data-ttu-id="3f7df-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3f7df-116">Requirement</span></span> | <span data-ttu-id="3f7df-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3f7df-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7df-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f7df-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3f7df-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f7df-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3f7df-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f7df-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3f7df-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3f7df-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3f7df-122">Header</span><span class="sxs-lookup"><span data-stu-id="3f7df-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f7df-123"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f7df-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

