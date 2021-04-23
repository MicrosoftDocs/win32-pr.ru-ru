---
title: Дропдовнгаллери. Менуграупс, свойство
description: Представляет контейнер для набора элементов раскрывающегося меню в элементе управления коллекции Drop-Down.
ms.assetid: 594f6ae5-760e-456d-98cd-04ecae0bae99
keywords:
- Лента Windows для свойства Дропдовнгаллери. Менуграупс
topic_type:
- apiref
api_name:
- DropDownGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67fcaeb81020cf4c317bf065c25a770d2a77e21f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105719208"
---
# <a name="dropdowngallerymenugroups-property"></a><span data-ttu-id="17cc8-104">Дропдовнгаллери. Менуграупс, свойство</span><span class="sxs-lookup"><span data-stu-id="17cc8-104">DropDownGallery.MenuGroups property</span></span>

<span data-ttu-id="17cc8-105">Представляет контейнер для набора пунктов раскрывающегося меню в [раскрывающемся](windowsribbon-controls-dropdowngallery.md) элементе управления "Коллекция".</span><span class="sxs-lookup"><span data-stu-id="17cc8-105">Represents a container for a set of drop-down menu items in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="17cc8-106">Использование</span><span class="sxs-lookup"><span data-stu-id="17cc8-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuGroups>
  child elements
</DropDownGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="17cc8-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="17cc8-107">Attributes</span></span>

<span data-ttu-id="17cc8-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="17cc8-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="17cc8-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="17cc8-109">Child elements</span></span>



| <span data-ttu-id="17cc8-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="17cc8-110">Element</span></span>                                                         | <span data-ttu-id="17cc8-111">Описание</span><span class="sxs-lookup"><span data-stu-id="17cc8-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="17cc8-112">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="17cc8-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="17cc8-113">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="17cc8-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="17cc8-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="17cc8-114">Parent elements</span></span>



| <span data-ttu-id="17cc8-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="17cc8-115">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="17cc8-116">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="17cc8-116">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="17cc8-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17cc8-117">Remarks</span></span>

<span data-ttu-id="17cc8-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="17cc8-118">Required.</span></span>

<span data-ttu-id="17cc8-119">Должен выполняться ровно один раз для каждого элемента [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="17cc8-119">Must occur exactly once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="17cc8-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="17cc8-120">Examples</span></span>

<span data-ttu-id="17cc8-121">В следующем примере показана базовая разметка для элемента **дропдовнгаллери. менуграупс** .</span><span class="sxs-lookup"><span data-stu-id="17cc8-121">The following example demonstrates the basic markup for the **DropDownGallery.MenuGroups** element.</span></span>

<span data-ttu-id="17cc8-122">В этом разделе кода показано объявление элемента управления **дропдовнгаллери. менуграупс** в [раскрывающейся](windowsribbon-controls-dropdowngallery.md) области команд коллекции.</span><span class="sxs-lookup"><span data-stu-id="17cc8-122">This section of code shows the **DropDownGallery.MenuGroups** control declaration in a [Drop-Down Gallery](windowsribbon-controls-dropdowngallery.md) Command Space.</span></span>


```XML
<!-- DropDownGallery -->
<Group CommandName="cmdDropDownGalleryGroup">
  <DropDownGallery CommandName="cmdDropDownGallery"
                   TextPosition="Hide"
                   Type="Commands"
                   ItemHeight="32"
                   ItemWidth="32">
    <DropDownGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </DropDownGallery.MenuLayout>
    <DropDownGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
       </MenuGroup>
       <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </DropDownGallery.MenuGroups>
  </DropDownGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="17cc8-123">Требования</span><span class="sxs-lookup"><span data-stu-id="17cc8-123">Requirements</span></span>



| <span data-ttu-id="17cc8-124">Требование</span><span class="sxs-lookup"><span data-stu-id="17cc8-124">Requirement</span></span> | <span data-ttu-id="17cc8-125">Значение</span><span class="sxs-lookup"><span data-stu-id="17cc8-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="17cc8-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17cc8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="17cc8-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="17cc8-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="17cc8-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17cc8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="17cc8-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="17cc8-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17cc8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17cc8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17cc8-131">**Элемент управления "раскрывающийся список"**</span><span class="sxs-lookup"><span data-stu-id="17cc8-131">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="17cc8-132">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="17cc8-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





