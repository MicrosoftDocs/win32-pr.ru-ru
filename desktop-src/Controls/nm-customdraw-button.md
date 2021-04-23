---
title: Код уведомления NM_CUSTOMDRAW (кнопка) (Коммктрл. h)
description: Сообщает родительскому окну элемента управления "Кнопка" о пользовательских операциях рисования на кнопке. Элемент управления "Кнопка" отправляет этот код уведомления в виде сообщения WM \_ Notify.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- Элементы управления Windows для кода уведомления NM_CUSTOMDRAW (кнопка)
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493317"
---
# <a name="nm_customdraw-button-notification-code"></a><span data-ttu-id="15fc6-105">\_Код уведомления NM кустомдрав (кнопка)</span><span class="sxs-lookup"><span data-stu-id="15fc6-105">NM\_CUSTOMDRAW (button) notification code</span></span>

<span data-ttu-id="15fc6-106">Сообщает родительскому окну элемента управления "Кнопка" о пользовательских операциях рисования на кнопке.</span><span class="sxs-lookup"><span data-stu-id="15fc6-106">Notifies the parent window of a button control about custom draw operations on the button.</span></span>

<span data-ttu-id="15fc6-107">Элемент управления "Кнопка" отправляет этот код уведомления в виде сообщения [**WM \_ Notify**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="15fc6-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="15fc6-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="15fc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15fc6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="15fc6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="15fc6-110">Указатель на структуру [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) , содержащую сведения об операции рисования.</span><span class="sxs-lookup"><span data-stu-id="15fc6-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="15fc6-111">Элемент **двитемспек** этой структуры содержит индекс рисуемого элемента, а элемент **литемлпарам** этой структуры содержит *lParam* элемента.</span><span class="sxs-lookup"><span data-stu-id="15fc6-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15fc6-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="15fc6-112">Return value</span></span>

<span data-ttu-id="15fc6-113">Значение, которое может возвращать приложение, зависит от текущей стадии рисования.</span><span class="sxs-lookup"><span data-stu-id="15fc6-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="15fc6-114">Элемент **двдравстаже** связанной структуры [**нмкустомдрав**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) содержит значение, указывающее стадию рисования.</span><span class="sxs-lookup"><span data-stu-id="15fc6-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="15fc6-115">Необходимо вернуть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="15fc6-115">You must return one of the following values.</span></span>



| <span data-ttu-id="15fc6-116">Код возврата</span><span class="sxs-lookup"><span data-stu-id="15fc6-116">Return code</span></span>                                                                                          | <span data-ttu-id="15fc6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="15fc6-117">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="15fc6-118"><dt>**КДРФ \_ нотифипостерасе**</dt></span><span class="sxs-lookup"><span data-stu-id="15fc6-118"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl> | <span data-ttu-id="15fc6-119">Элемент управления будет уведомлять родительский элемент после стирания элемента.</span><span class="sxs-lookup"><span data-stu-id="15fc6-119">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="15fc6-120">Его можно использовать, только если **двдравстаже** равняется кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="15fc6-120">This can be used only if **dwDrawStage** equals CDDS\_PREERASE.</span></span><br/>                                  |
| <dl> <span data-ttu-id="15fc6-121"><dt>**КДРФ \_ нотифипостпаинт**</dt></span><span class="sxs-lookup"><span data-stu-id="15fc6-121"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl> | <span data-ttu-id="15fc6-122">Элемент управления будет уведомлять родительский элемент после рисования элемента.</span><span class="sxs-lookup"><span data-stu-id="15fc6-122">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="15fc6-123">Его можно использовать, только если **двдравстаже** равняется кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="15fc6-123">This can be used only if **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                 |
| <dl> <span data-ttu-id="15fc6-124"><dt>**КДРФ \_ скипдефаулт**</dt></span><span class="sxs-lookup"><span data-stu-id="15fc6-124"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>     | <span data-ttu-id="15fc6-125">Приложение назначит элемент вручную.</span><span class="sxs-lookup"><span data-stu-id="15fc6-125">The application drew the item manually.</span></span> <span data-ttu-id="15fc6-126">Элемент управления не будет рисовать элемент.</span><span class="sxs-lookup"><span data-stu-id="15fc6-126">The control will not draw the item.</span></span> <span data-ttu-id="15fc6-127">Это можно использовать, когда **двдравстаже** равно КДДС \_ reerase или кддс \_ .</span><span class="sxs-lookup"><span data-stu-id="15fc6-127">This can be used when **dwDrawStage** equals CDDS\_PREERASE or CDDS\_PREPAINT.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="15fc6-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="15fc6-128">Remarks</span></span>

<span data-ttu-id="15fc6-129">Если элемент управления "Кнопка" помечен как овнердрав (BS \_ овнердрав), то \_ код уведомления NM кустомдрав не отправляется.</span><span class="sxs-lookup"><span data-stu-id="15fc6-129">If the button control is marked ownerdraw (BS\_OWNERDRAW), the NM\_CUSTOMDRAW notification code is not sent.</span></span>

<span data-ttu-id="15fc6-130">Дополнительные сведения см. [в статье Использование пользовательского рисования](custom-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="15fc6-130">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

> [!Note]  
> <span data-ttu-id="15fc6-131">Чтобы использовать этот код уведомления, необходимо указать манифест, указывающий Comclt32.dll версии 6,0.</span><span class="sxs-lookup"><span data-stu-id="15fc6-131">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="15fc6-132">Дополнительные сведения о манифестах см. в разделе [Включение визуальных стилей](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="15fc6-132">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="15fc6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="15fc6-133">Requirements</span></span>



| <span data-ttu-id="15fc6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="15fc6-134">Requirement</span></span> | <span data-ttu-id="15fc6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="15fc6-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15fc6-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="15fc6-136">Minimum supported client</span></span><br/> | <span data-ttu-id="15fc6-137">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15fc6-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="15fc6-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="15fc6-138">Minimum supported server</span></span><br/> | <span data-ttu-id="15fc6-139">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="15fc6-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15fc6-140">Header</span><span class="sxs-lookup"><span data-stu-id="15fc6-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="15fc6-141"><dt>Коммктрл. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15fc6-141"><dt>Commctrl.h (include Windows.h)</dt></span></span> </dl> |



 

 





