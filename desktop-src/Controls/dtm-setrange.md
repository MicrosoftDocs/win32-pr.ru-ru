---
title: Сообщение DTM_SETRANGE (Коммктрл. h)
description: Задает минимальное и максимальное допустимое системное время для элемента управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или воспользоваться \_ макросом DateTime SetRange.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- Элементы управления Windows для DTM_SETRANGE сообщений
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70578e7d468c6a0e54d1373af2d46e680afbbe5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803070"
---
# <a name="dtm_setrange-message"></a><span data-ttu-id="36039-105">\_Сообщение SETRANGE DTM</span><span class="sxs-lookup"><span data-stu-id="36039-105">DTM\_SETRANGE message</span></span>

<span data-ttu-id="36039-106">Задает минимальное и максимальное допустимое системное время для элемента управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="36039-106">Sets the minimum and maximum allowable system times for a date and time picker (DTP) control.</span></span> <span data-ttu-id="36039-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) .</span><span class="sxs-lookup"><span data-stu-id="36039-107">You can send this message explicitly or use the [**DateTime\_SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="36039-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="36039-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36039-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="36039-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36039-110">Значение типа, указывающее допустимые значения диапазона.</span><span class="sxs-lookup"><span data-stu-id="36039-110">A value specifying which range values are valid.</span></span> <span data-ttu-id="36039-111">Этот параметр может быть сочетанием следующих значений:</span><span class="sxs-lookup"><span data-stu-id="36039-111">This parameter can be a combination of the following values:</span></span>



| <span data-ttu-id="36039-112">Значение</span><span class="sxs-lookup"><span data-stu-id="36039-112">Value</span></span>                                                                                                                                          | <span data-ttu-id="36039-113">Значение</span><span class="sxs-lookup"><span data-stu-id="36039-113">Meaning</span></span>                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <span data-ttu-id="36039-114"><dt>**ГДТР \_ мин**</dt></span><span class="sxs-lookup"><span data-stu-id="36039-114"><dt>**GDTR\_MIN**</dt></span></span> </dl> | <span data-ttu-id="36039-115">Первый элемент в массиве структуры [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) является допустимым и будет использоваться для установки минимального допустимого системного времени.</span><span class="sxs-lookup"><span data-stu-id="36039-115">The first element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the minimum allowable system time.</span></span><br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <span data-ttu-id="36039-116"><dt>**ГДТР \_ Max**</dt></span><span class="sxs-lookup"><span data-stu-id="36039-116"><dt>**GDTR\_MAX**</dt></span></span> </dl> | <span data-ttu-id="36039-117">Второй элемент в массиве структуры [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) является допустимым и будет использоваться для установки максимально допустимого системного времени.</span><span class="sxs-lookup"><span data-stu-id="36039-117">The second element in the [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure array is valid and will be used to set the maximum allowable system time.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="36039-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="36039-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="36039-119">Указатель на массив структур [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) с двумя элементами.</span><span class="sxs-lookup"><span data-stu-id="36039-119">A pointer to a two-element array of [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structures.</span></span> <span data-ttu-id="36039-120">Первый элемент массива **SYSTEMTIME** содержит минимальное допустимое время.</span><span class="sxs-lookup"><span data-stu-id="36039-120">The first element of the **SYSTEMTIME** array contains the minimum allowable time.</span></span> <span data-ttu-id="36039-121">Второй элемент массива **SYSTEMTIME** содержит максимально допустимое время.</span><span class="sxs-lookup"><span data-stu-id="36039-121">The second element of the **SYSTEMTIME** array contains the maximum allowable time.</span></span> <span data-ttu-id="36039-122">Нет необходимости заполнять элемент массива, не указанный в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="36039-122">It is not necessary to fill an array element that is not specified in the *wParam* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36039-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="36039-123">Return value</span></span>

<span data-ttu-id="36039-124">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="36039-124">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="36039-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36039-125">Remarks</span></span>

<span data-ttu-id="36039-126">Средство выбора даты и времени отображает только даты и время, которые находятся в пределах указанного диапазона, запрещая пользователю выбирать дату и время, находящиеся за пределами диапазона.</span><span class="sxs-lookup"><span data-stu-id="36039-126">The date and time picker displays only dates/times that fall within the specified range, preventing the user from selecting a date and time that falls outside the range.</span></span> <span data-ttu-id="36039-127">Если сообщение [**DTM \_ сетсистемтиме**](dtm-setsystemtime.md) указывает дату и время, которые выходят за пределы диапазона, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="36039-127">If the [**DTM\_SETSYSTEMTIME**](dtm-setsystemtime.md) message specifies a date and time that falls outside the range, it will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="36039-128">Требования</span><span class="sxs-lookup"><span data-stu-id="36039-128">Requirements</span></span>



| <span data-ttu-id="36039-129">Требование</span><span class="sxs-lookup"><span data-stu-id="36039-129">Requirement</span></span> | <span data-ttu-id="36039-130">Значение</span><span class="sxs-lookup"><span data-stu-id="36039-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="36039-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="36039-131">Minimum supported client</span></span><br/> | <span data-ttu-id="36039-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36039-132">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="36039-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="36039-133">Minimum supported server</span></span><br/> | <span data-ttu-id="36039-134">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="36039-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="36039-135">Header</span><span class="sxs-lookup"><span data-stu-id="36039-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="36039-136"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="36039-136"><dt>Commctrl.h</dt></span></span> </dl> |



 

