---
title: Сообщение DTM_GETSYSTEMTIME (Коммктрл. h)
description: Получает выбранное в данный момент время из элемента управления "Выбор даты и времени" (DTP) и помещает его в указанную структуру SYSTEMTIME. Это сообщение можно отправить явным образом или использовать \_ макрос GetSystemtime типа DateTime.
ms.assetid: 81c95187-109c-4b36-98ea-a2e77ce42d9a
keywords:
- Элементы управления Windows для DTM_GETSYSTEMTIME сообщений
topic_type:
- apiref
api_name:
- DTM_GETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e14d8c998720cc987a03877e1918e97304bf769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136674"
---
# <a name="dtm_getsystemtime-message"></a><span data-ttu-id="e6272-105">\_Сообщение DTM GETSYSTEMTIME</span><span class="sxs-lookup"><span data-stu-id="e6272-105">DTM\_GETSYSTEMTIME message</span></span>

<span data-ttu-id="e6272-106">Получает выбранное в данный момент время из элемента управления "Выбор даты и времени" (DTP) и помещает его в указанную структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="e6272-106">Gets the currently selected time from a date and time picker (DTP) control and places it in a specified [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="e6272-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ GetSystemtime типа DateTime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) .</span><span class="sxs-lookup"><span data-stu-id="e6272-107">You can send this message explicitly or use the [**DateTime\_GetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getsystemtime) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="e6272-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6272-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6272-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e6272-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="e6272-110">Должен равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="e6272-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="e6272-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e6272-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e6272-112">Указатель на структуру [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .</span><span class="sxs-lookup"><span data-stu-id="e6272-112">A pointer to a [**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) structure.</span></span> <span data-ttu-id="e6272-113">Если **DTM \_ GETSYSTEMTIME** возвращает ГДТ \_ допустимое значение, эта структура будет содержать текущее выбранное время.</span><span class="sxs-lookup"><span data-stu-id="e6272-113">If **DTM\_GETSYSTEMTIME** returns GDT\_VALID, this structure will contain the currently selected time.</span></span> <span data-ttu-id="e6272-114">В противном случае он не будет содержать действительные сведения.</span><span class="sxs-lookup"><span data-stu-id="e6272-114">Otherwise, it will not contain valid information.</span></span> <span data-ttu-id="e6272-115">Этот параметр должен быть допустимым указателем; Он не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="e6272-115">This parameter must be a valid pointer; it cannot be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6272-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6272-116">Return value</span></span>

<span data-ttu-id="e6272-117">Возвращает ГДТ \_ , допустимое, если сведения о времени были успешно помещены в *lParam*.</span><span class="sxs-lookup"><span data-stu-id="e6272-117">Returns GDT\_VALID if the time information was successfully placed in *lParam*.</span></span> <span data-ttu-id="e6272-118">Возвращает \_ значение ГДТ None, если элементу управления задан стиль [**DTS \_ шовноне**](date-and-time-picker-control-styles.md) , а флажок Control (элемент управления) не установлен.</span><span class="sxs-lookup"><span data-stu-id="e6272-118">Returns GDT\_NONE if the control was set to the [**DTS\_SHOWNONE**](date-and-time-picker-control-styles.md) style and the control check box was not selected.</span></span> <span data-ttu-id="e6272-119">Возвращает \_ ошибку ГДТ при возникновении ошибки.</span><span class="sxs-lookup"><span data-stu-id="e6272-119">Returns GDT\_ERROR if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6272-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e6272-120">Requirements</span></span>



| <span data-ttu-id="e6272-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e6272-121">Requirement</span></span> | <span data-ttu-id="e6272-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e6272-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e6272-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6272-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6272-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6272-124">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e6272-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6272-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6272-126">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e6272-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e6272-127">Header</span><span class="sxs-lookup"><span data-stu-id="e6272-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6272-128"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6272-128"><dt>Commctrl.h</dt></span></span> </dl> |



 

