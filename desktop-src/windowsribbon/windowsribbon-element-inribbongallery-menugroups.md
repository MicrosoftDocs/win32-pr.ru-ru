---
title: Инриббонгаллери. Менуграупс, свойство
description: Представляет контейнер для набора пунктов раскрывающегося меню элемента управления коллекции In-Ribbon.
ms.assetid: 6b9ded25-4e8e-4e30-a349-f7c091dbfe7a
keywords:
- Лента Windows для свойства Инриббонгаллери. Менуграупс
topic_type:
- apiref
api_name:
- InRibbonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd447b66dada74b1a9b909b3030e080198143b12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071684"
---
# <a name="inribbongallerymenugroups-property"></a><span data-ttu-id="12e4f-104">Инриббонгаллери. Менуграупс, свойство</span><span class="sxs-lookup"><span data-stu-id="12e4f-104">InRibbonGallery.MenuGroups property</span></span>

<span data-ttu-id="12e4f-105">Представляет контейнер для набора пунктов раскрывающегося меню элемента управления [коллекции в ленте](windowsribbon-controls-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="12e4f-105">Represents a container for the set of drop-down menu items of an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="12e4f-106">Использование</span><span class="sxs-lookup"><span data-stu-id="12e4f-106">Usage</span></span>

``` syntax
<InRibbonGallery.MenuGroups>
  child elements
</InRibbonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="12e4f-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="12e4f-107">Attributes</span></span>

<span data-ttu-id="12e4f-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="12e4f-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="12e4f-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="12e4f-109">Child elements</span></span>



| <span data-ttu-id="12e4f-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="12e4f-110">Element</span></span>                                                         | <span data-ttu-id="12e4f-111">Описание</span><span class="sxs-lookup"><span data-stu-id="12e4f-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="12e4f-112">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="12e4f-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="12e4f-113">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="12e4f-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="12e4f-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="12e4f-114">Parent elements</span></span>



| <span data-ttu-id="12e4f-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="12e4f-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="12e4f-116">**инриббонгаллери**</span><span class="sxs-lookup"><span data-stu-id="12e4f-116">**InRibbonGallery**</span></span>](windowsribbon-element-inribbongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="12e4f-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12e4f-117">Remarks</span></span>

<span data-ttu-id="12e4f-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="12e4f-118">Optional.</span></span>

<span data-ttu-id="12e4f-119">Может встречаться не более одного раза для каждого элемента [**инриббонгаллери**](windowsribbon-element-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="12e4f-119">May occur at most once for each [**InRibbonGallery**](windowsribbon-element-inribbongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="12e4f-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="12e4f-120">Examples</span></span>

<span data-ttu-id="12e4f-121">В следующем примере показана базовая разметка для элемента управления [коллекции в ленте](windowsribbon-controls-inribbongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="12e4f-121">The following example demonstrates the basic markup for an [In-Ribbon Gallery](windowsribbon-controls-inribbongallery.md) control.</span></span>

<span data-ttu-id="12e4f-122">В этом разделе кода показано объявление элемента управления **инриббонгаллери. менуграупс** .</span><span class="sxs-lookup"><span data-stu-id="12e4f-122">This section of code shows the **InRibbonGallery.MenuGroups** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="12e4f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="12e4f-123">Requirements</span></span>



| <span data-ttu-id="12e4f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="12e4f-124">Requirement</span></span> | <span data-ttu-id="12e4f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="12e4f-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="12e4f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="12e4f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="12e4f-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="12e4f-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="12e4f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="12e4f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="12e4f-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="12e4f-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="12e4f-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="12e4f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e4f-131">Элемент управления "Коллекция ленты"</span><span class="sxs-lookup"><span data-stu-id="12e4f-131">In-Ribbon Gallery control</span></span>](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="12e4f-132">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="12e4f-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="12e4f-133">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="12e4f-133">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





