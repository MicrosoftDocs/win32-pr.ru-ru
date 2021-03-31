---
title: Сообщение MCM_SETMAXSELCOUNT (Коммктрл. h)
description: Задает максимальное число дней, которое может быть выбрано в элементе управления ' календарь на месяц '. Это сообщение можно отправить явным образом или с помощью \_ макроса монскал сетмаксселкаунт.
ms.assetid: 190453ab-e53b-4db7-82c1-f9d50188ad39
keywords:
- Элементы управления Windows для MCM_SETMAXSELCOUNT сообщений
topic_type:
- apiref
api_name:
- MCM_SETMAXSELCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c67bcb7191bb20b9688c2fe1ffc2b458ecb7b8a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103892622"
---
# <a name="mcm_setmaxselcount-message"></a><span data-ttu-id="9c302-105">\_Сообщение MCM сетмаксселкаунт</span><span class="sxs-lookup"><span data-stu-id="9c302-105">MCM\_SETMAXSELCOUNT message</span></span>

<span data-ttu-id="9c302-106">Задает максимальное число дней, которое может быть выбрано в элементе управления ' календарь на месяц '.</span><span class="sxs-lookup"><span data-stu-id="9c302-106">Sets the maximum number of days that can be selected in a month calendar control.</span></span> <span data-ttu-id="9c302-107">Это сообщение можно отправить явным образом или с помощью макроса [**монскал \_ сетмаксселкаунт**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) .</span><span class="sxs-lookup"><span data-stu-id="9c302-107">You can send this message explicitly or by using the [**MonthCal\_SetMaxSelCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setmaxselcount) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9c302-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c302-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c302-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9c302-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9c302-110">Значение типа **int** , которое будет иметь значение, представляющее максимальное число дней, которое может быть выбрано.</span><span class="sxs-lookup"><span data-stu-id="9c302-110">Value of type **int** that will be set to represent the maximum number of days that can be selected.</span></span>

</dd> <dt>

<span data-ttu-id="9c302-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9c302-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9c302-112">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="9c302-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c302-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c302-113">Return value</span></span>

<span data-ttu-id="9c302-114">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9c302-114">Returns nonzero if successful, or zero otherwise.</span></span> <span data-ttu-id="9c302-115">Это сообщение не будет выполнено, если применяется к элементу управления "месячный календарь", который не использует многоэлементный стиль [**MCS \_**](month-calendar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="9c302-115">This message will fail if applied to a month calendar control that does not use the [**MCS\_MULTISELECT**](month-calendar-control-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c302-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9c302-116">Requirements</span></span>



| <span data-ttu-id="9c302-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9c302-117">Requirement</span></span> | <span data-ttu-id="9c302-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9c302-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9c302-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c302-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9c302-120">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9c302-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9c302-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c302-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9c302-122">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="9c302-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9c302-123">Header</span><span class="sxs-lookup"><span data-stu-id="9c302-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c302-124"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9c302-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





