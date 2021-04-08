---
title: Системмонитор. выделение, свойство
description: Возвращает или задает значение, указывающее, выделяются ли значения выбранных счетчиков в графе.
ms.assetid: 5342b81f-71bb-4564-b520-1e91d3002c5b
keywords:
- Выделить свойство Сисмон
- Выделение свойства Сисмон, класс Системмонитор
- Класс Системмонитор Сисмон, выделение свойства
topic_type:
- apiref
api_name:
- SystemMonitor.Highlight
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3009501123673175c64d88acd838f94aa7e332aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891969"
---
# <a name="systemmonitorhighlight-property"></a><span data-ttu-id="be1b8-106">Системмонитор. выделение, свойство</span><span class="sxs-lookup"><span data-stu-id="be1b8-106">SystemMonitor.Highlight property</span></span>

<span data-ttu-id="be1b8-107">Возвращает или задает значение, указывающее, выделяются ли значения выбранных счетчиков в графе.</span><span class="sxs-lookup"><span data-stu-id="be1b8-107">Retrieves or sets a value indicating whether the values of the selected counters are highlighted in the graph.</span></span>

<span data-ttu-id="be1b8-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="be1b8-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="be1b8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be1b8-109">Syntax</span></span>


```VB
Property Highlight As Boolean
```



## <a name="property-value"></a><span data-ttu-id="be1b8-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="be1b8-110">Property value</span></span>

<span data-ttu-id="be1b8-111">Значение true указывает, что значения выбранных счетчиков выделены на диаграмме; в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="be1b8-111">True indicates that the values of the selected counters are highlighted in the graph; otherwise, False.</span></span> <span data-ttu-id="be1b8-112">Значение по умолчанию равно False.</span><span class="sxs-lookup"><span data-stu-id="be1b8-112">The default value is False.</span></span>

## <a name="remarks"></a><span data-ttu-id="be1b8-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be1b8-113">Remarks</span></span>

<span data-ttu-id="be1b8-114">Чтобы выбрать один или несколько счетчиков, можно задать для [**каунтеритем. Selected**](counteritem-selected.md) значение true или выбрать счетчики из списка счетчиков, показанных в условных обозначениях.</span><span class="sxs-lookup"><span data-stu-id="be1b8-114">To select one or more counters, you can set [**CounterItem.Selected**](counteritem-selected.md) to True, or the user can select the counters from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="be1b8-115">**До Windows Vista:** Вы не можете программно выбирать счетчики, и пользователь может выбрать только один счетчик из списка счетчиков, показанных в условных обозначениях.</span><span class="sxs-lookup"><span data-stu-id="be1b8-115">**Prior to Windows Vista:** You cannot programmatically select counters and the user can select only one counter from the list of counters shown in the Legend.</span></span>

<span data-ttu-id="be1b8-116">Выделение может быть черным или белым в зависимости от значения свойства [**BackColor**](systemmonitor-backcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="be1b8-116">Highlighting can be black or white, depending on the value of the [**BackColor**](systemmonitor-backcolor.md) property.</span></span> <span data-ttu-id="be1b8-117">Для выделения автоматически устанавливается цвет, обеспечивающий достаточную контрастность между цветом выделения и цветом фона.</span><span class="sxs-lookup"><span data-stu-id="be1b8-117">The highlighting is automatically set to the color that will provide sufficient contrast between highlight color and the background color.</span></span>

## <a name="requirements"></a><span data-ttu-id="be1b8-118">Требования</span><span class="sxs-lookup"><span data-stu-id="be1b8-118">Requirements</span></span>



| <span data-ttu-id="be1b8-119">Требование</span><span class="sxs-lookup"><span data-stu-id="be1b8-119">Requirement</span></span> | <span data-ttu-id="be1b8-120">Значение</span><span class="sxs-lookup"><span data-stu-id="be1b8-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="be1b8-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="be1b8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="be1b8-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be1b8-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="be1b8-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="be1b8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="be1b8-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="be1b8-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="be1b8-125">DLL</span><span class="sxs-lookup"><span data-stu-id="be1b8-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be1b8-126"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="be1b8-126"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be1b8-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="be1b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be1b8-128">**системмонитор**</span><span class="sxs-lookup"><span data-stu-id="be1b8-128">**SystemMonitor**</span></span>](systemmonitor.md)
</dt> <dt>

[<span data-ttu-id="be1b8-129">**Каунтеритем. выбрано**</span><span class="sxs-lookup"><span data-stu-id="be1b8-129">**CounterItem.Selected**</span></span>](counteritem-selected.md)
</dt> </dl>

 

 





