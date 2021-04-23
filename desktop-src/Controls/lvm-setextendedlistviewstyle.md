---
title: Сообщение LVM_SETEXTENDEDLISTVIEWSTYLE (Коммктрл. h)
description: Задает расширенные стили в элементах управления "представление списка". Это сообщение можно отправить явным образом или воспользоваться \_ макросом ListView сетекстендедлиствиевстиле или ListView \_ сетекстендедлиствиевстиликс.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- Элементы управления Windows для LVM_SETEXTENDEDLISTVIEWSTYLE сообщений
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988200"
---
# <a name="lvm_setextendedlistviewstyle-message"></a><span data-ttu-id="c1da6-105">\_Сообщение LVM сетекстендедлиствиевстиле</span><span class="sxs-lookup"><span data-stu-id="c1da6-105">LVM\_SETEXTENDEDLISTVIEWSTYLE message</span></span>

<span data-ttu-id="c1da6-106">Задает расширенные стили в элементах управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="c1da6-106">Sets extended styles in list-view controls.</span></span> <span data-ttu-id="c1da6-107">Это сообщение можно отправить явным образом или воспользоваться макросом [**ListView \_ Сетекстендедлиствиевстиле**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) или [**ListView \_ сетекстендедлиствиевстиликс**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .</span><span class="sxs-lookup"><span data-stu-id="c1da6-107">You can send this message explicitly or use the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) or [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c1da6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1da6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1da6-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c1da6-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1da6-110">Значение **типа DWORD** , указывающее, какие стили в *lParam* должны быть затронуты.</span><span class="sxs-lookup"><span data-stu-id="c1da6-110">**DWORD** value that specifies which styles in *lParam* are to be affected.</span></span> <span data-ttu-id="c1da6-111">Этот параметр может быть сочетанием [**расширенных стилей List-View**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="c1da6-111">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="c1da6-112">Будут изменены только расширенные стили в параметре *wParam* .</span><span class="sxs-lookup"><span data-stu-id="c1da6-112">Only the extended styles in *wParam* will be changed.</span></span> <span data-ttu-id="c1da6-113">Все остальные стили будут поддерживаться по мере их возникновения.</span><span class="sxs-lookup"><span data-stu-id="c1da6-113">All other styles will be maintained as they are.</span></span> <span data-ttu-id="c1da6-114">Если этот параметр равен нулю, будут затронуты все стили в *lParam* .</span><span class="sxs-lookup"><span data-stu-id="c1da6-114">If this parameter is zero, all of the styles in *lParam* will be affected.</span></span>

</dd> <dt>

<span data-ttu-id="c1da6-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c1da6-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c1da6-116">Значение **типа DWORD** , указывающее набор расширенных стилей элементов управления "представление списка".</span><span class="sxs-lookup"><span data-stu-id="c1da6-116">**DWORD** value that specifies the extended list-view control styles to set.</span></span> <span data-ttu-id="c1da6-117">Этот параметр может быть сочетанием [**расширенных стилей List-View**](extended-list-view-styles.md).</span><span class="sxs-lookup"><span data-stu-id="c1da6-117">This parameter can be a combination of [**Extended List-View Styles**](extended-list-view-styles.md).</span></span> <span data-ttu-id="c1da6-118">Стили, которые не заданы, но указаны в параметре *wParam*, удаляются.</span><span class="sxs-lookup"><span data-stu-id="c1da6-118">Styles that are not set, but that are specified in *wParam*, are removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1da6-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c1da6-119">Return value</span></span>

<span data-ttu-id="c1da6-120">Возвращает значение **типа DWORD** , содержащее предыдущие стили элемента управления "список" расширенного представления списка.</span><span class="sxs-lookup"><span data-stu-id="c1da6-120">Returns a **DWORD** value that contains the previous extended list-view control styles.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1da6-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c1da6-121">Remarks</span></span>

<span data-ttu-id="c1da6-122">Параметр *wParam* позволяет изменять один или несколько расширенных стилей без предварительного получения существующих стилей.</span><span class="sxs-lookup"><span data-stu-id="c1da6-122">The *wParam* parameter allows you to modify one or more extended styles without having to retrieve the existing styles first.</span></span> <span data-ttu-id="c1da6-123">Например, если передать [**LVS \_ ex \_ фуллровселект**](extended-list-view-styles.md) для *wParam* и 0 для *lParam*, то стиль **LVS \_ ex \_ фуллровселект** будет сброшен, но все остальные стили останутся прежними.</span><span class="sxs-lookup"><span data-stu-id="c1da6-123">For example, if you pass [**LVS\_EX\_FULLROWSELECT**](extended-list-view-styles.md) for *wParam* and 0 for *lParam*, the **LVS\_EX\_FULLROWSELECT** style will be cleared but all other styles will remain the same.</span></span>

<span data-ttu-id="c1da6-124">В целях обратной совместимости макрос [**\_ сетекстендедлиствиевстиле ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) не был обновлен для использования *wParam*.</span><span class="sxs-lookup"><span data-stu-id="c1da6-124">For backward compatibility reasons, the [**ListView\_SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) macro has not been updated to use *wParam*.</span></span> <span data-ttu-id="c1da6-125">Чтобы использовать значение *wParam* , используйте макрос [**\_ сетекстендедлиствиевстиликс ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .</span><span class="sxs-lookup"><span data-stu-id="c1da6-125">To use the *wParam* value, use the [**ListView\_SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) macro.</span></span>

<span data-ttu-id="c1da6-126">Если это сообщение используется для установки [**\_ \_ флажка LVS ex**](extended-list-view-styles.md) , все ранее установленные индексы изображений состояния будут удалены.</span><span class="sxs-lookup"><span data-stu-id="c1da6-126">When you use this message to set the [**LVS\_EX\_CHECKBOXES**](extended-list-view-styles.md) style, any previously set state image index will be discarded.</span></span> <span data-ttu-id="c1da6-127">Все флажки будут инициализированы с непроверенным состоянием.</span><span class="sxs-lookup"><span data-stu-id="c1da6-127">All check boxes will be initialized to the unchecked state.</span></span> <span data-ttu-id="c1da6-128">Индекс изображения состояния содержится в битах 12 – 15 элемента **State** структуры [**лвитем**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .</span><span class="sxs-lookup"><span data-stu-id="c1da6-128">The state image index is contained in bits 12 through 15 of the **state** member of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1da6-129">Требования</span><span class="sxs-lookup"><span data-stu-id="c1da6-129">Requirements</span></span>



| <span data-ttu-id="c1da6-130">Требование</span><span class="sxs-lookup"><span data-stu-id="c1da6-130">Requirement</span></span> | <span data-ttu-id="c1da6-131">Значение</span><span class="sxs-lookup"><span data-stu-id="c1da6-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c1da6-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c1da6-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c1da6-133">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c1da6-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c1da6-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c1da6-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c1da6-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c1da6-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c1da6-136">Header</span><span class="sxs-lookup"><span data-stu-id="c1da6-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1da6-137"><dt>Коммктрл. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1da6-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





