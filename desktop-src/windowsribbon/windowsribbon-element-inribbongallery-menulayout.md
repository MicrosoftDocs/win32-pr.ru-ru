---
title: Инриббонгаллери. Менулайаут, свойство
description: Представляет контейнер для макетов раскрывающихся меню коллекции In-Ribbon.
ms.assetid: 89e0eb39-2790-4571-a661-ab3ebafbb13f
keywords:
- Лента Windows для свойства Инриббонгаллери. Менулайаут
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2fc5e0eab5d8dbc35cd9cb3be96e5d5d351416
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071208"
---
# <a name="inribbongallerymenulayout-property"></a><span data-ttu-id="74c5f-104">Инриббонгаллери. Менулайаут, свойство</span><span class="sxs-lookup"><span data-stu-id="74c5f-104">InRibbonGallery.MenuLayout property</span></span>

<span data-ttu-id="74c5f-105">Представляет контейнер для макетов раскрывающихся меню [коллекции в ленте](windowsribbon-controls-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="74c5f-105">Represents a container for [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="74c5f-106">Использование</span><span class="sxs-lookup"><span data-stu-id="74c5f-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuLayout>
  child elements
</InRibbonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="74c5f-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="74c5f-107">Attributes</span></span>

<span data-ttu-id="74c5f-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="74c5f-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="74c5f-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="74c5f-109">Child elements</span></span>



| <span data-ttu-id="74c5f-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="74c5f-110">Element</span></span>                                                                           | <span data-ttu-id="74c5f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="74c5f-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="74c5f-112">**фловменулайаут**</span><span class="sxs-lookup"><span data-stu-id="74c5f-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="74c5f-113">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="74c5f-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="74c5f-114">**вертикалменулайаут**</span><span class="sxs-lookup"><span data-stu-id="74c5f-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="74c5f-115">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="74c5f-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="74c5f-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="74c5f-116">Parent elements</span></span>



| <span data-ttu-id="74c5f-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="74c5f-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="74c5f-118">**инриббонгаллери**</span><span class="sxs-lookup"><span data-stu-id="74c5f-118">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="74c5f-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="74c5f-119">Remarks</span></span>

<span data-ttu-id="74c5f-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="74c5f-120">Optional.</span></span>

<span data-ttu-id="74c5f-121">Может встречаться не более одного раза для каждого элемента [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="74c5f-121">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="74c5f-122">Допускается не более одного дочернего элемента ([**вертикалменулайаут**](windowsribbon-element-verticalmenulayout.md) или [**фловменулайаут**](windowsribbon-element-flowmenulayout.md)).</span><span class="sxs-lookup"><span data-stu-id="74c5f-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="74c5f-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="74c5f-123">Examples</span></span>

<span data-ttu-id="74c5f-124">В следующем примере показана базовая разметка для [коллекции на ленте](windowsribbon-controls-inribbongallery.md).</span><span class="sxs-lookup"><span data-stu-id="74c5f-124">The following example demonstrates the basic markup for the [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md).</span></span>

<span data-ttu-id="74c5f-125">В этом разделе кода показано объявление элемента управления **инриббонгаллери. менулайаут** .</span><span class="sxs-lookup"><span data-stu-id="74c5f-125">This section of code shows the **InRibbonGallery.MenuLayout** control declaration.</span></span>


```XML
<!-- InRibbonGallery -->
<Group CommandName="cmdInRibbonGalleryGroup" SizeDefinition="OneInRibbonGallery">
  <InRibbonGallery CommandName="cmdInRibbonGallery"
                   MaxColumns="10"
                   MaxColumnsMedium="5"
                   MinColumnsLarge="5"
                   MinColumnsMedium="3"
                   Type="Items">
    <InRibbonGallery.MenuLayout>
      <VerticalMenuLayout Rows="2"
                          Gripper="Vertical"/>
    </InRibbonGallery.MenuLayout>
    <InRibbonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </InRibbonGallery.MenuGroups>            
  </InRibbonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="74c5f-126">Требования</span><span class="sxs-lookup"><span data-stu-id="74c5f-126">Requirements</span></span>



| <span data-ttu-id="74c5f-127">Требование</span><span class="sxs-lookup"><span data-stu-id="74c5f-127">Requirement</span></span> | <span data-ttu-id="74c5f-128">Значение</span><span class="sxs-lookup"><span data-stu-id="74c5f-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="74c5f-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74c5f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="74c5f-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="74c5f-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="74c5f-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74c5f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="74c5f-132">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="74c5f-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="74c5f-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74c5f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74c5f-134">Элемент управления "Коллекция ленты"</span><span class="sxs-lookup"><span data-stu-id="74c5f-134">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="74c5f-135">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="74c5f-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





