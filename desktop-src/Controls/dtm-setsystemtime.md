---
title: Сообщение DTM_SETSYSTEMTIME (Коммктрл. h)
description: Задает время в элементе управления "Выбор даты и времени" (DTP). Это сообщение можно отправить явным образом или использовать \_ макрос Сетсистемтиме DateTime.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- Элементы управления Windows для DTM_SETSYSTEMTIME сообщений
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b2a3c625ad4ff02bed138a8086ca0da984de35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989127"
---
# <a name="dtm_setsystemtime-message"></a><span data-ttu-id="6fa57-105">\_Сообщение DTM сетсистемтиме</span><span class="sxs-lookup"><span data-stu-id="6fa57-105">DTM\_SETSYSTEMTIME message</span></span>

<span data-ttu-id="6fa57-106">Задает время в элементе управления "Выбор даты и времени" (DTP).</span><span class="sxs-lookup"><span data-stu-id="6fa57-106">Sets the time in a date and time picker (DTP) control.</span></span> <span data-ttu-id="6fa57-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетсистемтиме DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="6fa57-107">You can send this message explicitly or use the [**DateTime\_SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6fa57-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6fa57-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fa57-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6fa57-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fa57-110">Значение типа, указывающее действие, которое должно быть выполнено.</span><span class="sxs-lookup"><span data-stu-id="6fa57-110">A value specifying the action that should be performed.</span></span> <span data-ttu-id="6fa57-111">Для этого значения необходимо задать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="6fa57-111">This value must be set to one of the following:</span></span>



| <span data-ttu-id="6fa57-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6fa57-112">Value</span></span>                                                                                                                                             | <span data-ttu-id="6fa57-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6fa57-113">Meaning</span></span>                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <span data-ttu-id="6fa57-114"><dt>**ГДТ \_ допустимое**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa57-114"><dt>**GDT\_VALID**</dt></span></span> </dl> | <span data-ttu-id="6fa57-115">Установите элемент управления DTP в соответствии с данными в структуре, на которую указывает *lParam* .</span><span class="sxs-lookup"><span data-stu-id="6fa57-115">Set the DTP control according to the data within the structure that *lParam* points to.</span></span> <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <span data-ttu-id="6fa57-116"><dt>**ГДТ \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="6fa57-116"><dt>**GDT\_NONE**</dt></span></span> </dl>    | <span data-ttu-id="6fa57-117">Установите для элемента управления DTP значение "без даты" и снимите его флажок.</span><span class="sxs-lookup"><span data-stu-id="6fa57-117">Set the DTP control to "no date" and clear its check box.</span></span> <span data-ttu-id="6fa57-118">Если этот флаг указан, параметр *lParam* игнорируется.</span><span class="sxs-lookup"><span data-stu-id="6fa57-118">When this flag is specified, *lParam* is ignored.</span></span> <span data-ttu-id="6fa57-119">Этот флаг применяется только к элементам управления DTP, для которых задан [**стиль \_ Шовноне служб DTS**](date-and-time-picker-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6fa57-119">This flag applies only to DTP controls that are set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="6fa57-120">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6fa57-120">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6fa57-121">Указатель на структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) , содержащую системное время, используемое для задания элемента управления DTP.</span><span class="sxs-lookup"><span data-stu-id="6fa57-121">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure containing the system time used to set the DTP control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fa57-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fa57-122">Return value</span></span>

<span data-ttu-id="6fa57-123">Возвращает ненулевое значение в случае успеха или ноль в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6fa57-123">Returns nonzero if successful, or zero otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fa57-124">Требования</span><span class="sxs-lookup"><span data-stu-id="6fa57-124">Requirements</span></span>



| <span data-ttu-id="6fa57-125">Требование</span><span class="sxs-lookup"><span data-stu-id="6fa57-125">Requirement</span></span> | <span data-ttu-id="6fa57-126">Значение</span><span class="sxs-lookup"><span data-stu-id="6fa57-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa57-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fa57-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6fa57-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fa57-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6fa57-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fa57-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6fa57-130">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6fa57-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6fa57-131">Header</span><span class="sxs-lookup"><span data-stu-id="6fa57-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fa57-132"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fa57-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

