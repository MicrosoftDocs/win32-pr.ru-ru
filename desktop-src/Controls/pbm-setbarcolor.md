---
title: Сообщение PBM_SETBARCOLOR (Коммктрл. h)
description: Задает цвет индикатора хода выполнения в элементе управления "индикатор выполнения".
ms.assetid: 4b512420-04ec-4884-ab13-4c58304b95f6
keywords:
- Элементы управления Windows для PBM_SETBARCOLOR сообщений
topic_type:
- apiref
api_name:
- PBM_SETBARCOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1387e69622e84990a197dc5a374d1c3449393408
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534673"
---
# <a name="pbm_setbarcolor-message"></a><span data-ttu-id="3117c-104">\_Сообщение СЕТБАРКОЛОР PBM</span><span class="sxs-lookup"><span data-stu-id="3117c-104">PBM\_SETBARCOLOR message</span></span>

<span data-ttu-id="3117c-105">Задает цвет индикатора хода выполнения в элементе управления "индикатор выполнения".</span><span class="sxs-lookup"><span data-stu-id="3117c-105">Sets the color of the progress indicator bar in the progress bar control.</span></span>

## <a name="parameters"></a><span data-ttu-id="3117c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3117c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3117c-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3117c-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3117c-108">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="3117c-108">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3117c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3117c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3117c-110">Значение **COLORREF** , указывающее новый цвет панели индикаторов хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="3117c-110">The **COLORREF** value that specifies the new progress indicator bar color.</span></span> <span data-ttu-id="3117c-111">Указание \_ значения по умолчанию для CLR приводит к тому, что индикатор выполнения будет использовать цвет панели индикаторов хода выполнения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3117c-111">Specifying the CLR\_DEFAULT value causes the progress bar to use its default progress indicator bar color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3117c-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3117c-112">Return value</span></span>

<span data-ttu-id="3117c-113">Возвращает цвет диаграммы предыдущего индикатора хода выполнения или \_ значение по умолчанию CLR, если цвет панели индикаторов выполнения является цветом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3117c-113">Returns the previous progress indicator bar color, or CLR\_DEFAULT if the progress indicator bar color is the default color.</span></span>

## <a name="remarks"></a><span data-ttu-id="3117c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3117c-114">Remarks</span></span>

<span data-ttu-id="3117c-115">Если стили оформления включены, это сообщение не действует.</span><span class="sxs-lookup"><span data-stu-id="3117c-115">When visual styles are enabled, this message has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="3117c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="3117c-116">Requirements</span></span>



| <span data-ttu-id="3117c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="3117c-117">Requirement</span></span> | <span data-ttu-id="3117c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="3117c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3117c-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3117c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3117c-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3117c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3117c-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3117c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3117c-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3117c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3117c-123">Header</span><span class="sxs-lookup"><span data-stu-id="3117c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3117c-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3117c-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





