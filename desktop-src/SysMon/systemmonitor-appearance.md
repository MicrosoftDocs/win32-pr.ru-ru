---
title: Системмонитор. Appearance, свойство
description: Извлекает или задает внешний вид элемента управления для включения или исключения трехмерных эффектов отображения.
ms.assetid: cbc1f17f-991a-4b35-9c64-7750a17b42c8
keywords:
- Свойство Appearance Сисмон
- Свойство Appearance Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство Appearance
topic_type:
- apiref
api_name:
- SystemMonitor.Appearance
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9200c66f83a47f15421480967e8ea1ae9509b13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661831"
---
# <a name="systemmonitorappearance-property"></a><span data-ttu-id="e182f-106">Системмонитор. Appearance, свойство</span><span class="sxs-lookup"><span data-stu-id="e182f-106">SystemMonitor.Appearance property</span></span>

<span data-ttu-id="e182f-107">Извлекает или задает внешний вид элемента управления для включения или исключения трехмерных эффектов отображения.</span><span class="sxs-lookup"><span data-stu-id="e182f-107">Retrieves or sets the control's appearance to include or omit three-dimensional display effects.</span></span>

<span data-ttu-id="e182f-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e182f-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e182f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e182f-109">Syntax</span></span>


```VB
Property Appearance As Long
```



## <a name="property-value"></a><span data-ttu-id="e182f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e182f-110">Property value</span></span>

<span data-ttu-id="e182f-111">Значение вида, определяющее, закрашивается ли элемент управления трехмерными эффектами.</span><span class="sxs-lookup"><span data-stu-id="e182f-111">Appearance value that determines if the control is painted with three-dimensional effects.</span></span>

<span data-ttu-id="e182f-112">Для этого свойства можно задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e182f-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="e182f-113">Значение</span><span class="sxs-lookup"><span data-stu-id="e182f-113">Value</span></span>                                                                        | <span data-ttu-id="e182f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e182f-114">Meaning</span></span>                                                                                  |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e182f-115"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e182f-115"><dt>0</dt></span></span> </dl> | <span data-ttu-id="e182f-116">Закрашивает элемент управления без визуальных эффектов.</span><span class="sxs-lookup"><span data-stu-id="e182f-116">Paints the control without visual effects.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e182f-117"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="e182f-117"><dt>1</dt></span></span> </dl> | <span data-ttu-id="e182f-118">Закрашивает элемент управления с помощью трехмерных эффектов.</span><span class="sxs-lookup"><span data-stu-id="e182f-118">Paints the control with three-dimensional effects.</span></span> <span data-ttu-id="e182f-119">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e182f-119">This is the default value.</span></span><br/> |



 

## <a name="exceptions"></a><span data-ttu-id="e182f-120">Исключения</span><span class="sxs-lookup"><span data-stu-id="e182f-120">Exceptions</span></span>



| <span data-ttu-id="e182f-121">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="e182f-121">Exception type</span></span>               | <span data-ttu-id="e182f-122">Условие</span><span class="sxs-lookup"><span data-stu-id="e182f-122">Condition</span></span>                                    |
|------------------------------|----------------------------------------------|
| <span data-ttu-id="e182f-123">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="e182f-123">**System.ArgumentException**</span></span> | <span data-ttu-id="e182f-124">Указано недопустимое значение внешнего вида.</span><span class="sxs-lookup"><span data-stu-id="e182f-124">The specified appearance value is not valid.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e182f-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e182f-125">Remarks</span></span>

<span data-ttu-id="e182f-126">Это внешнее свойство.</span><span class="sxs-lookup"><span data-stu-id="e182f-126">This is an ambient property.</span></span> <span data-ttu-id="e182f-127">Значение этого свойства определяется контейнером.</span><span class="sxs-lookup"><span data-stu-id="e182f-127">The value of this property is determined by the container.</span></span> <span data-ttu-id="e182f-128">Установка значения этого свойства может повлиять на иллюзию элемента управления и контейнера на одно приложение.</span><span class="sxs-lookup"><span data-stu-id="e182f-128">Setting the value of this property could affect the illusion of the control and container being a single application.</span></span>

## <a name="requirements"></a><span data-ttu-id="e182f-129">Требования</span><span class="sxs-lookup"><span data-stu-id="e182f-129">Requirements</span></span>



| <span data-ttu-id="e182f-130">Требование</span><span class="sxs-lookup"><span data-stu-id="e182f-130">Requirement</span></span> | <span data-ttu-id="e182f-131">Значение</span><span class="sxs-lookup"><span data-stu-id="e182f-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e182f-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e182f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e182f-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e182f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e182f-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e182f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e182f-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e182f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e182f-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e182f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e182f-137"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="e182f-137"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e182f-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e182f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e182f-139">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="e182f-139">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





