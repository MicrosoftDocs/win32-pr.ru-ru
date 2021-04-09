---
title: Сообщение TB_SETROWS (Коммктрл. h)
description: Задает количество строк кнопок на панели инструментов.
ms.assetid: d8ea7b80-d23e-4593-8eb1-d23808173fc9
keywords:
- Элементы управления Windows для TB_SETROWS сообщений
topic_type:
- apiref
api_name:
- TB_SETROWS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d0065a3f5f6a277713e368177886ebd064ea132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072028"
---
# <a name="tb_setrows-message"></a><span data-ttu-id="0d74e-104">\_Сообщение СЕТРОВС ТБ</span><span class="sxs-lookup"><span data-stu-id="0d74e-104">TB\_SETROWS message</span></span>

<span data-ttu-id="0d74e-105">Задает количество строк кнопок на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="0d74e-105">Sets the number of rows of buttons in a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="0d74e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d74e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d74e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0d74e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d74e-108">[**Ловорд**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) указывает количество запрошенных строк.</span><span class="sxs-lookup"><span data-stu-id="0d74e-108">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the number of rows requested.</span></span> <span data-ttu-id="0d74e-109">Минимальное число строк равно единице, а максимальное число строк равно числу кнопок на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="0d74e-109">The minimum number of rows is one, and the maximum number of rows is equal to the number of buttons in the toolbar.</span></span>

<span data-ttu-id="0d74e-110">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) — это **логическое** значение, указывающее, следует ли создавать больше строк, чем было запрошено, если система не может создать число строк, заданное параметром *wParam*.</span><span class="sxs-lookup"><span data-stu-id="0d74e-110">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) is a **BOOL** that indicates whether to create more rows than requested when the system cannot create the number of rows specified by *wParam*.</span></span> <span data-ttu-id="0d74e-111">Если **значение равно true**, система создает больше строк.</span><span class="sxs-lookup"><span data-stu-id="0d74e-111">If **TRUE**, the system creates more rows.</span></span> <span data-ttu-id="0d74e-112">Если **значение равно false**, система создает меньше строк.</span><span class="sxs-lookup"><span data-stu-id="0d74e-112">If **FALSE**, the system creates fewer rows.</span></span>

</dd> <dt>

<span data-ttu-id="0d74e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0d74e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0d74e-114">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая получает ограничивающий прямоугольник панели инструментов после задания строк.</span><span class="sxs-lookup"><span data-stu-id="0d74e-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that receives the bounding rectangle of the toolbar after the rows are set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d74e-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d74e-115">Return value</span></span>

<span data-ttu-id="0d74e-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="0d74e-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d74e-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d74e-117">Remarks</span></span>

<span data-ttu-id="0d74e-118">Поскольку система не разбивает группы кнопок при задании числа строк, результирующее число строк может отличаться от запрошенного числа.</span><span class="sxs-lookup"><span data-stu-id="0d74e-118">Because the system does not break up button groups when setting the number of rows, the resulting number of rows might differ from the number requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d74e-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0d74e-119">Requirements</span></span>



| <span data-ttu-id="0d74e-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0d74e-120">Requirement</span></span> | <span data-ttu-id="0d74e-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0d74e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d74e-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d74e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0d74e-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d74e-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0d74e-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d74e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0d74e-125">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0d74e-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0d74e-126">Header</span><span class="sxs-lookup"><span data-stu-id="0d74e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d74e-127"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d74e-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

