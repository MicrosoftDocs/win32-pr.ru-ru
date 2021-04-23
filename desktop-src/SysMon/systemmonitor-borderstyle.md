---
title: Системмонитор. BorderStyle, свойство
description: Возвращает или задает стиль границы элемента управления.
ms.assetid: 9151a3f6-71fb-43ea-b7f6-cc35048145cb
keywords:
- Свойство BorderStyle Сисмон
- Свойство BorderStyle Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство BorderStyle
topic_type:
- apiref
api_name:
- SystemMonitor.BorderStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5dd0cec7e4d0d6d3223da4486d4569f8bc611e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891825"
---
# <a name="systemmonitorborderstyle-property"></a><span data-ttu-id="9b977-106">Системмонитор. BorderStyle, свойство</span><span class="sxs-lookup"><span data-stu-id="9b977-106">SystemMonitor.BorderStyle property</span></span>

<span data-ttu-id="9b977-107">Возвращает или задает стиль границы элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9b977-107">Retrieves or sets the border style of the control.</span></span>

<span data-ttu-id="9b977-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9b977-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b977-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9b977-109">Syntax</span></span>


```VB
Property BorderStyle As Long
```



## <a name="property-value"></a><span data-ttu-id="9b977-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9b977-110">Property value</span></span>

<span data-ttu-id="9b977-111">Стиль границы элемента управления.</span><span class="sxs-lookup"><span data-stu-id="9b977-111">Border style of the control.</span></span>

<span data-ttu-id="9b977-112">Для этого свойства можно задать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="9b977-112">You can set this property to one of the following values.</span></span>



| <span data-ttu-id="9b977-113">Значение</span><span class="sxs-lookup"><span data-stu-id="9b977-113">Value</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="9b977-114">Значение</span><span class="sxs-lookup"><span data-stu-id="9b977-114">Meaning</span></span>                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="System.Windows.Forms.FormBorderStyle.VbBSNone"></span><span id="system.windows.forms.formborderstyle.vbbsnone"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBBSNONE"></span><dl> <span data-ttu-id="9b977-115"><dt>**System. Windows. Forms. FormBorderStyle. вббсноне**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="9b977-115"><dt>**System.Windows.Forms.FormBorderStyle.VbBSNone**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="9b977-116">Нет границы.</span><span class="sxs-lookup"><span data-stu-id="9b977-116">No border.</span></span> <span data-ttu-id="9b977-117">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b977-117">This is the default value.</span></span><br/> |
| <span id="System.Windows.Forms.FormBorderStyle.VbFixedSingle"></span><span id="system.windows.forms.formborderstyle.vbfixedsingle"></span><span id="SYSTEM.WINDOWS.FORMS.FORMBORDERSTYLE.VBFIXEDSINGLE"></span><dl> <span data-ttu-id="9b977-118"><dt>**System. Windows. Forms. FormBorderStyle. вбфикседсингле**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9b977-118"><dt>**System.Windows.Forms.FormBorderStyle.VbFixedSingle**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="9b977-119">Фиксированная одинарная граница.</span><span class="sxs-lookup"><span data-stu-id="9b977-119">Fixed, single border.</span></span><br/>                 |



 

## <a name="exceptions"></a><span data-ttu-id="9b977-120">Исключения</span><span class="sxs-lookup"><span data-stu-id="9b977-120">Exceptions</span></span>



| <span data-ttu-id="9b977-121">Тип исключения</span><span class="sxs-lookup"><span data-stu-id="9b977-121">Exception type</span></span>               | <span data-ttu-id="9b977-122">Условие</span><span class="sxs-lookup"><span data-stu-id="9b977-122">Condition</span></span>                                |
|------------------------------|------------------------------------------|
| <span data-ttu-id="9b977-123">**System. ArgumentException**</span><span class="sxs-lookup"><span data-stu-id="9b977-123">**System.ArgumentException**</span></span> | <span data-ttu-id="9b977-124">Указан недопустимый стиль границы.</span><span class="sxs-lookup"><span data-stu-id="9b977-124">The specified border style is not valid.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9b977-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9b977-125">Requirements</span></span>



| <span data-ttu-id="9b977-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9b977-126">Requirement</span></span> | <span data-ttu-id="9b977-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9b977-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9b977-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b977-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9b977-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9b977-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9b977-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b977-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9b977-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9b977-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9b977-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9b977-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b977-133"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="9b977-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b977-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b977-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b977-135">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="9b977-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





