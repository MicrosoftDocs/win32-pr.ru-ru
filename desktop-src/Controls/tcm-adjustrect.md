---
title: Сообщение TCM_ADJUSTRECT (Коммктрл. h)
description: Вычисляет область просмотра элемента управления вкладки по заданному прямоугольнику окна или вычисляет прямоугольник окна, который соответствует заданной отображаемой области. Это сообщение можно отправить явным образом или с помощью \_ макроса табктрл аджустрект.
ms.assetid: 2f14201a-e4a3-4ae5-b9cf-4a674c52f24a
keywords:
- Элементы управления Windows для TCM_ADJUSTRECT сообщений
topic_type:
- apiref
api_name:
- TCM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9c1612a4f6c2fc436f858807fca59112c376a35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654673"
---
# <a name="tcm_adjustrect-message"></a><span data-ttu-id="29dbe-105">\_Сообщение АДЖУСТРЕКТ TCM</span><span class="sxs-lookup"><span data-stu-id="29dbe-105">TCM\_ADJUSTRECT message</span></span>

<span data-ttu-id="29dbe-106">Вычисляет область просмотра элемента управления вкладки по заданному прямоугольнику окна или вычисляет прямоугольник окна, который соответствует заданной отображаемой области.</span><span class="sxs-lookup"><span data-stu-id="29dbe-106">Calculates a tab control's display area given a window rectangle, or calculates the window rectangle that would correspond to a specified display area.</span></span> <span data-ttu-id="29dbe-107">Это сообщение можно отправить явным образом или с помощью макроса [**табктрл \_ аджустрект**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) .</span><span class="sxs-lookup"><span data-stu-id="29dbe-107">You can send this message explicitly or by using the [**TabCtrl\_AdjustRect**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_adjustrect) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="29dbe-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="29dbe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29dbe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="29dbe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29dbe-110">Выполняемая операция.</span><span class="sxs-lookup"><span data-stu-id="29dbe-110">Operation to perform.</span></span> <span data-ttu-id="29dbe-111">Если этот параметр имеет **значение true**, *lParam* задает отображаемый прямоугольник и получает соответствующий прямоугольник окна.</span><span class="sxs-lookup"><span data-stu-id="29dbe-111">If this parameter is **TRUE**, *lParam* specifies a display rectangle and receives the corresponding window rectangle.</span></span> <span data-ttu-id="29dbe-112">Если этот параметр имеет **значение false**, *lParam* задает прямоугольник окна и получает соответствующую область экрана.</span><span class="sxs-lookup"><span data-stu-id="29dbe-112">If this parameter is **FALSE**, *lParam* specifies a window rectangle and receives the corresponding display area.</span></span>

</dd> <dt>

<span data-ttu-id="29dbe-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="29dbe-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="29dbe-114">Указатель на структуру [**Rect**](/previous-versions//dd162897(v=vs.85)) , которая указывает заданный прямоугольник и получает вычисляемый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="29dbe-114">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the given rectangle and receives the calculated rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29dbe-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="29dbe-115">Return value</span></span>

<span data-ttu-id="29dbe-116">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="29dbe-116">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29dbe-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="29dbe-117">Remarks</span></span>

<span data-ttu-id="29dbe-118">Это сообщение относится только к элементам управления "Вкладка", расположенным вверху.</span><span class="sxs-lookup"><span data-stu-id="29dbe-118">This message applies only to tab controls that are at the top.</span></span> <span data-ttu-id="29dbe-119">Он не применяется к элементам управления "Вкладка", находящиеся на сторонах или внизу.</span><span class="sxs-lookup"><span data-stu-id="29dbe-119">It does not apply to tab controls that are on the sides or bottom.</span></span>

## <a name="requirements"></a><span data-ttu-id="29dbe-120">Требования</span><span class="sxs-lookup"><span data-stu-id="29dbe-120">Requirements</span></span>



| <span data-ttu-id="29dbe-121">Требование</span><span class="sxs-lookup"><span data-stu-id="29dbe-121">Requirement</span></span> | <span data-ttu-id="29dbe-122">Значение</span><span class="sxs-lookup"><span data-stu-id="29dbe-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="29dbe-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="29dbe-123">Minimum supported client</span></span><br/> | <span data-ttu-id="29dbe-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29dbe-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="29dbe-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="29dbe-125">Minimum supported server</span></span><br/> | <span data-ttu-id="29dbe-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="29dbe-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="29dbe-127">Header</span><span class="sxs-lookup"><span data-stu-id="29dbe-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="29dbe-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="29dbe-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

