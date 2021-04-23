---
title: Буттонтип, элемент
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования Интернет-магазинами. | Буттонтип, элемент
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- Проигрыватель Windows Media, элемент Буттонтип
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ab94794232ade6f924b87fd3f4d73d4452d544
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694561"
---
# <a name="buttontip-element"></a><span data-ttu-id="c1b6f-105">Буттонтип, элемент</span><span class="sxs-lookup"><span data-stu-id="c1b6f-105">ButtonTip Element</span></span>

> [!Note]  
> <span data-ttu-id="c1b6f-106">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="c1b6f-106">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c1b6f-107">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="c1b6f-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c1b6f-108">Элемент **буттонтип** задает текстовую строку, отображаемую при наведении пользователем на кнопку области задач.</span><span class="sxs-lookup"><span data-stu-id="c1b6f-108">The **ButtonTip** element specifies the text string that is displayed when the user points to a task pane button.</span></span>

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a><span data-ttu-id="c1b6f-109">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="c1b6f-109">Attributes</span></span>

<span data-ttu-id="c1b6f-110">Этот элемент не содержит атрибуты.</span><span class="sxs-lookup"><span data-stu-id="c1b6f-110">This element has no attributes.</span></span>

## <a name="parentchild-elements"></a><span data-ttu-id="c1b6f-111">Родительские и дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c1b6f-111">Parent/Child Elements</span></span>



| <span data-ttu-id="c1b6f-112">Иерархия</span><span class="sxs-lookup"><span data-stu-id="c1b6f-112">Hierarchy</span></span>       | <span data-ttu-id="c1b6f-113">Элемент</span><span class="sxs-lookup"><span data-stu-id="c1b6f-113">Element</span></span>                                              |
|-----------------|------------------------------------------------------|
| <span data-ttu-id="c1b6f-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="c1b6f-114">Parent elements</span></span> | <span data-ttu-id="c1b6f-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="c1b6f-115">**ServiceTask1**, **ServiceTask2**, **ServiceTask3**</span></span> |
| <span data-ttu-id="c1b6f-116">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c1b6f-116">Child elements</span></span>  | <span data-ttu-id="c1b6f-117">Нет</span><span class="sxs-lookup"><span data-stu-id="c1b6f-117">None</span></span>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="c1b6f-118">Remarks</span><span class="sxs-lookup"><span data-stu-id="c1b6f-118">Remarks</span></span>

<span data-ttu-id="c1b6f-119">Этот элемент является необязательным для каждого экземпляра **ServiceTask1**, **ServiceTask2** или **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="c1b6f-119">This element is optional for each instance of **ServiceTask1**, **ServiceTask2**, or **ServiceTask3**.</span></span> <span data-ttu-id="c1b6f-120">Если этот элемент не указан, проигрыватель Windows Media использует текст кнопки в качестве значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c1b6f-120">If this element is not supplied, Windows Media Player uses the button text as the default value.</span></span>

> [!Note]  
> <span data-ttu-id="c1b6f-121">Проигрыватель Windows Media 10 содержит три области задач, в которых Интернет-магазин может отображать свои веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="c1b6f-121">Windows Media Player 10 has three task panes where an online store can display its webpages.</span></span> <span data-ttu-id="c1b6f-122">Интернет-магазин может использовать одну, две или все три области задач.</span><span class="sxs-lookup"><span data-stu-id="c1b6f-122">The online store can choose to use one, two, or all three of the task panes.</span></span> <span data-ttu-id="c1b6f-123">Проигрыватель Windows Media 11 имеет только одну область задач, которую пользователь может просматривать, щелкнув вкладку **Интернет-магазины** . проигрыватель Windows Media 11 игнорирует элементы **ServiceTask2** и **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="c1b6f-123">Windows Media Player 11 has only one task pane, which the user can view by clicking on the **Online Stores** tab. Windows Media Player 11 ignores the **ServiceTask2** and **ServiceTask3** elements.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c1b6f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="c1b6f-124">Requirements</span></span>



| <span data-ttu-id="c1b6f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="c1b6f-125">Requirement</span></span> | <span data-ttu-id="c1b6f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="c1b6f-126">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="c1b6f-127">Версия</span><span class="sxs-lookup"><span data-stu-id="c1b6f-127">Version</span></span><br/> | <span data-ttu-id="c1b6f-128">Проигрыватель Windows Media 10 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="c1b6f-128">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1b6f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c1b6f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1b6f-130">**Пример документа ServiceInfo для Интернет-магазина типа 1**</span><span class="sxs-lookup"><span data-stu-id="c1b6f-130">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="c1b6f-131">**Пример документа ServiceInfo для Интернет-магазина типа 2**</span><span class="sxs-lookup"><span data-stu-id="c1b6f-131">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="c1b6f-132">**Документ ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="c1b6f-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 





