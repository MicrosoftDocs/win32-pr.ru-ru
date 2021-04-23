---
title: Сообщение HDM_EDITFILTER (Коммктрл. h)
description: Перемещает фокус ввода в поле ввода, когда фокус находится на кнопке фильтра.
ms.assetid: 580f7872-4056-4d7d-8e69-274b4b4b5545
keywords:
- Элементы управления Windows для HDM_EDITFILTER сообщений
topic_type:
- apiref
api_name:
- HDM_EDITFILTER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 733c79bf747d3b55aa8dd38eb8fad8fdc83601e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802861"
---
# <a name="hdm_editfilter-message"></a><span data-ttu-id="738f8-104">\_Сообщение ЕДИТФИЛТЕР HDM</span><span class="sxs-lookup"><span data-stu-id="738f8-104">HDM\_EDITFILTER message</span></span>

<span data-ttu-id="738f8-105">Перемещает фокус ввода в поле ввода, когда фокус находится на кнопке фильтра.</span><span class="sxs-lookup"><span data-stu-id="738f8-105">Moves the input focus to the edit box when a filter button has the focus.</span></span>

## <a name="parameters"></a><span data-ttu-id="738f8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="738f8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="738f8-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="738f8-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="738f8-108">Значение типа, указывающее Изменяемый столбец.</span><span class="sxs-lookup"><span data-stu-id="738f8-108">A value specifying the column to edit.</span></span>

</dd> <dt>

<span data-ttu-id="738f8-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="738f8-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="738f8-110">Флаг, указывающий способ управления изменениями пользователя.</span><span class="sxs-lookup"><span data-stu-id="738f8-110">A flag that specifies how to handle the user's editing changes.</span></span> <span data-ttu-id="738f8-111">Используйте этот флаг, чтобы указать, что делать, если пользователь находится в процессе редактирования фильтра при отправке сообщения.</span><span class="sxs-lookup"><span data-stu-id="738f8-111">Use this flag to specify what to do if the user is in the process of editing the filter when the message is sent.</span></span>



| <span data-ttu-id="738f8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="738f8-112">Value</span></span>                                                                                                                                      | <span data-ttu-id="738f8-113">Значение</span><span class="sxs-lookup"><span data-stu-id="738f8-113">Meaning</span></span>                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="738f8-114"><dt></dt><dt> **Значение true**</dt></span><span class="sxs-lookup"><span data-stu-id="738f8-114"><dt></dt> <dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="738f8-115">Отмена изменений, внесенных пользователем.</span><span class="sxs-lookup"><span data-stu-id="738f8-115">Discard the changes made by the user.</span></span> <br/> |
| <dl> <span data-ttu-id="738f8-116"><dt></dt><dt> **Значение false**</dt></span><span class="sxs-lookup"><span data-stu-id="738f8-116"><dt></dt> <dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="738f8-117">Примите изменения, внесенные пользователем.</span><span class="sxs-lookup"><span data-stu-id="738f8-117">Accept the changes made by the user.</span></span> <br/>  |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="738f8-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="738f8-118">Return value</span></span>

<span data-ttu-id="738f8-119">Возвращает целое число.</span><span class="sxs-lookup"><span data-stu-id="738f8-119">Returns an integer.</span></span> <span data-ttu-id="738f8-120">**LResult** преобразуется в целое число, которое указывает **true**(1) или **false**(0).</span><span class="sxs-lookup"><span data-stu-id="738f8-120">The **LRESULT** is cast to an integer that indicates **TRUE**(1) or **FALSE**(0).</span></span>

## <a name="requirements"></a><span data-ttu-id="738f8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="738f8-121">Requirements</span></span>



| <span data-ttu-id="738f8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="738f8-122">Requirement</span></span> | <span data-ttu-id="738f8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="738f8-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="738f8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="738f8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="738f8-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="738f8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="738f8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="738f8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="738f8-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="738f8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="738f8-128">Header</span><span class="sxs-lookup"><span data-stu-id="738f8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="738f8-129"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="738f8-129"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="738f8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="738f8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="738f8-131">**\_КЛЕАРФИЛТЕР HDM**</span><span class="sxs-lookup"><span data-stu-id="738f8-131">**HDM\_CLEARFILTER**</span></span>](hdm-clearfilter.md)
</dt> </dl>

 

 





