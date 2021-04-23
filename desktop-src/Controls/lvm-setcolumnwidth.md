---
title: Сообщение LVM_SETCOLUMNWIDTH (Коммктрл. h)
description: Изменяет ширину столбца в режиме представления отчета или ширину всех столбцов в режиме просмотра списка. Это сообщение можно отправить явным образом или использовать \_ макрос Сетколумнвидс ListView.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- Элементы управления Windows для LVM_SETCOLUMNWIDTH сообщений
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135126"
---
# <a name="lvm_setcolumnwidth-message"></a><span data-ttu-id="475b1-105">\_Сообщение LVM сетколумнвидс</span><span class="sxs-lookup"><span data-stu-id="475b1-105">LVM\_SETCOLUMNWIDTH message</span></span>

<span data-ttu-id="475b1-106">Изменяет ширину столбца в режиме представления отчета или ширину всех столбцов в режиме просмотра списка.</span><span class="sxs-lookup"><span data-stu-id="475b1-106">Changes the width of a column in report-view mode or the width of all columns in list-view mode.</span></span> <span data-ttu-id="475b1-107">Это сообщение можно отправить явным образом или использовать макрос [**\_ сетколумнвидс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) .</span><span class="sxs-lookup"><span data-stu-id="475b1-107">You can send this message explicitly or use the [**ListView\_SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="475b1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="475b1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="475b1-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="475b1-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="475b1-110">Отсчитываемый от нуля индекс допустимого столбца.</span><span class="sxs-lookup"><span data-stu-id="475b1-110">Zero-based index of a valid column.</span></span> <span data-ttu-id="475b1-111">Для режима просмотра списка этот параметр должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="475b1-111">For list-view mode, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="475b1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="475b1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="475b1-113">Новая ширина столбца в пикселях.</span><span class="sxs-lookup"><span data-stu-id="475b1-113">New width of the column, in pixels.</span></span> <span data-ttu-id="475b1-114">Для режима представления отчета поддерживаются следующие специальные значения:</span><span class="sxs-lookup"><span data-stu-id="475b1-114">For report-view mode, the following special values are supported:</span></span>



| <span data-ttu-id="475b1-115">Значение</span><span class="sxs-lookup"><span data-stu-id="475b1-115">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="475b1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="475b1-116">Meaning</span></span>                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <span data-ttu-id="475b1-117"><dt>**ЛВСКВ \_ AUTOSIZE**</dt></span><span class="sxs-lookup"><span data-stu-id="475b1-117"><dt>**LVSCW\_AUTOSIZE**</dt></span></span> </dl>                                | <span data-ttu-id="475b1-118">Автоматически изменяет размер столбца.</span><span class="sxs-lookup"><span data-stu-id="475b1-118">Automatically sizes the column.</span></span><br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <span data-ttu-id="475b1-119"><dt>**ЛВСКВ \_ AUTOSIZE \_ усехеадер**</dt></span><span class="sxs-lookup"><span data-stu-id="475b1-119"><dt>**LVSCW\_AUTOSIZE\_USEHEADER**</dt></span></span> </dl> | <span data-ttu-id="475b1-120">Автоматически изменяет размер столбца в соответствии с текстом заголовка.</span><span class="sxs-lookup"><span data-stu-id="475b1-120">Automatically sizes the column to fit the header text.</span></span> <span data-ttu-id="475b1-121">Если это значение используется с последним столбцом, его ширина задается для заполнения оставшейся ширины элемента управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="475b1-121">If you use this value with the last column, its width is set to fill the remaining width of the list-view control.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="475b1-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="475b1-122">Return value</span></span>

<span data-ttu-id="475b1-123">Возвращает **значение true** , если успешно, или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="475b1-123">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="475b1-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="475b1-124">Remarks</span></span>

<span data-ttu-id="475b1-125">Предположим, что у вас есть представление списка из двух столбцов с шириной 500 пикселей.</span><span class="sxs-lookup"><span data-stu-id="475b1-125">Assume that you have a 2-column list-view control with a width of 500 pixels.</span></span> <span data-ttu-id="475b1-126">Если ширина столбца равна 200 пикселов и сообщение отправляется с параметром *wParam* = 1 и *lParam* = лвскв \_ AUTOSIZE \_ усехеадер, то второй (и последний) столбец будет равен 300 пикселей в ширину.</span><span class="sxs-lookup"><span data-stu-id="475b1-126">If the width of column zero is set to 200 pixels, and you send this message with *wParam* = 1 and *lParam* = LVSCW\_AUTOSIZE\_USEHEADER, the second (and last) column will be 300 pixels wide.</span></span>

## <a name="requirements"></a><span data-ttu-id="475b1-127">Требования</span><span class="sxs-lookup"><span data-stu-id="475b1-127">Requirements</span></span>



| <span data-ttu-id="475b1-128">Требование</span><span class="sxs-lookup"><span data-stu-id="475b1-128">Requirement</span></span> | <span data-ttu-id="475b1-129">Значение</span><span class="sxs-lookup"><span data-stu-id="475b1-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="475b1-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="475b1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="475b1-131">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="475b1-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="475b1-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="475b1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="475b1-133">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="475b1-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="475b1-134">Header</span><span class="sxs-lookup"><span data-stu-id="475b1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="475b1-135"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="475b1-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





