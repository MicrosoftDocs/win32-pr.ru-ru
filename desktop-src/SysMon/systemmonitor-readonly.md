---
title: Системмонитор. ReadOnly, свойство
description: Возвращает или задает значение, определяющее, может ли пользователь изменять значения свойств элемента управления.
ms.assetid: 6ecfd63a-09b1-46eb-803f-6cb05bdecc25
keywords:
- Свойство ReadOnly Сисмон
- Свойство ReadOnly Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, свойство ReadOnly
topic_type:
- apiref
api_name:
- SystemMonitor.ReadOnly
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f42481e1bb0df0966f09ee354421af6378969f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988614"
---
# <a name="systemmonitorreadonly-property"></a><span data-ttu-id="61db7-106">Системмонитор. ReadOnly, свойство</span><span class="sxs-lookup"><span data-stu-id="61db7-106">SystemMonitor.ReadOnly property</span></span>

<span data-ttu-id="61db7-107">Возвращает или задает значение, определяющее, может ли пользователь изменять значения свойств элемента управления.</span><span class="sxs-lookup"><span data-stu-id="61db7-107">Retrieves or sets a value that determines whether a user can modify the property values of the control.</span></span>

<span data-ttu-id="61db7-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="61db7-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="61db7-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="61db7-109">Syntax</span></span>


```VB
Property ReadOnly As Boolean
```



## <a name="property-value"></a><span data-ttu-id="61db7-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="61db7-110">Property value</span></span>

<span data-ttu-id="61db7-111">Значение true, если пользователь не должен изменять значения свойств элемента управления; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="61db7-111">True if you do not want the user to modify the property values of the control; otherwise, false.</span></span> <span data-ttu-id="61db7-112">Значение по умолчанию — false, означающее, что пользователи могут изменять значения свойств элемента управления.</span><span class="sxs-lookup"><span data-stu-id="61db7-112">The default value is false, meaning that users can modify the property values of the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="61db7-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61db7-113">Remarks</span></span>

<span data-ttu-id="61db7-114">Если значение этого свойства равно true, действуют следующие условия.</span><span class="sxs-lookup"><span data-stu-id="61db7-114">When the value of this property is True, the following conditions are in effect:</span></span>

-   <span data-ttu-id="61db7-115">Пользователь не может использовать контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="61db7-115">The user cannot use the context menu.</span></span>
-   <span data-ttu-id="61db7-116">Следующие кнопки панели инструментов отключены.</span><span class="sxs-lookup"><span data-stu-id="61db7-116">The following toolbar buttons are disabled:</span></span>
    -   <span data-ttu-id="61db7-117">Новый набор счетчиков</span><span class="sxs-lookup"><span data-stu-id="61db7-117">New Counter Set</span></span>
    -   <span data-ttu-id="61db7-118">Просмотр текущих действий</span><span class="sxs-lookup"><span data-stu-id="61db7-118">View Current Activity</span></span>
    -   <span data-ttu-id="61db7-119">Просмотр данных файла журнала</span><span class="sxs-lookup"><span data-stu-id="61db7-119">View Log File Data</span></span>
    -   <span data-ttu-id="61db7-120">Добавить</span><span class="sxs-lookup"><span data-stu-id="61db7-120">Add</span></span>
    -   <span data-ttu-id="61db7-121">Удалить</span><span class="sxs-lookup"><span data-stu-id="61db7-121">Delete</span></span>
    -   <span data-ttu-id="61db7-122">Вставить список счетчиков</span><span class="sxs-lookup"><span data-stu-id="61db7-122">Paste Counter List</span></span>
    -   <span data-ttu-id="61db7-123">Свойства</span><span class="sxs-lookup"><span data-stu-id="61db7-123">Properties</span></span>

<span data-ttu-id="61db7-124">Обратите внимание, что это свойство влияет только на возможность изменения значений свойств пользователем через пользовательский интерфейс, но не мешает программному изменению значений или счетчиков свойств.</span><span class="sxs-lookup"><span data-stu-id="61db7-124">Note that this property affects only the user's ability to modify property values through the user interface, it does not prevent you from programmatically modifying property values or counters.</span></span>

## <a name="requirements"></a><span data-ttu-id="61db7-125">Требования</span><span class="sxs-lookup"><span data-stu-id="61db7-125">Requirements</span></span>



| <span data-ttu-id="61db7-126">Требование</span><span class="sxs-lookup"><span data-stu-id="61db7-126">Requirement</span></span> | <span data-ttu-id="61db7-127">Значение</span><span class="sxs-lookup"><span data-stu-id="61db7-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61db7-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="61db7-128">Minimum supported client</span></span><br/> | <span data-ttu-id="61db7-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61db7-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="61db7-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="61db7-130">Minimum supported server</span></span><br/> | <span data-ttu-id="61db7-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="61db7-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="61db7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="61db7-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61db7-133"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="61db7-133"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61db7-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61db7-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61db7-135">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="61db7-135">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> </dl>

 

 





