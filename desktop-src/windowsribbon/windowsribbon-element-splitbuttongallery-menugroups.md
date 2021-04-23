---
title: Сплитбуттонгаллери. Менуграупс, свойство
description: Представляет контейнер для набора элементов раскрывающегося меню в элементе управления Сплитбуттонгаллери.
ms.assetid: e30fcf9a-488b-423a-8bc4-fccbc78f74de
keywords:
- Лента Windows для свойства Сплитбуттонгаллери. Менуграупс
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuGroups
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72176e7d7e79b076c3a7cf4d1fd847aa4f4e0561
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135874"
---
# <a name="splitbuttongallerymenugroups-property"></a><span data-ttu-id="a2ed0-104">Сплитбуттонгаллери. Менуграупс, свойство</span><span class="sxs-lookup"><span data-stu-id="a2ed0-104">SplitButtonGallery.MenuGroups property</span></span>

<span data-ttu-id="a2ed0-105">Представляет контейнер для набора элементов раскрывающегося меню в элементе управления [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ed0-105">Represents a container for a set of drop-down menu items in a [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) control.</span></span>

## <a name="usage"></a><span data-ttu-id="a2ed0-106">Использование</span><span class="sxs-lookup"><span data-stu-id="a2ed0-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuGroups>
  child elements
</SplitButtonGallery.MenuGroups>
```

## <a name="attributes"></a><span data-ttu-id="a2ed0-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a2ed0-107">Attributes</span></span>

<span data-ttu-id="a2ed0-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a2ed0-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a2ed0-109">Child elements</span></span>



| <span data-ttu-id="a2ed0-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="a2ed0-110">Element</span></span>                                                         | <span data-ttu-id="a2ed0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a2ed0-111">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="a2ed0-112">**менуграуп**</span><span class="sxs-lookup"><span data-stu-id="a2ed0-112">**MenuGroup**</span></span>](windowsribbon-element-menugroup.md)<br/> | <span data-ttu-id="a2ed0-113">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="a2ed0-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="a2ed0-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="a2ed0-114">Parent elements</span></span>



| <span data-ttu-id="a2ed0-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="a2ed0-115">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="a2ed0-116">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="a2ed0-116">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="a2ed0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a2ed0-117">Remarks</span></span>

<span data-ttu-id="a2ed0-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="a2ed0-118">Required.</span></span>

<span data-ttu-id="a2ed0-119">Должен выполняться ровно один раз для каждого элемента [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="a2ed0-119">Must occur exactly once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="a2ed0-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="a2ed0-120">Examples</span></span>

<span data-ttu-id="a2ed0-121">В следующем примере показана базовая разметка для элемента **сплитбуттонгаллери. менуграупс** .</span><span class="sxs-lookup"><span data-stu-id="a2ed0-121">The following example demonstrates the basic markup for the **SplitButtonGallery.MenuGroups** element.</span></span>

<span data-ttu-id="a2ed0-122">В этом разделе кода показано объявление элемента управления **сплитбуттонгаллери. менуграупс** .</span><span class="sxs-lookup"><span data-stu-id="a2ed0-122">This section of code shows the **SplitButtonGallery.MenuGroups** control declaration.</span></span>


```XML
<!-- SplitButtonGallery -->
<Group CommandName="cmdSplitButtonGalleryGroup">
  <SplitButtonGallery CommandName="cmdSplitButtonGallery">
    <SplitButtonGallery.MenuLayout>
      <FlowMenuLayout Rows="2"
                      Columns="3"
                      Gripper="None"/>
    </SplitButtonGallery.MenuLayout>
    <SplitButtonGallery.MenuGroups>
      <MenuGroup>
        <Button CommandName="cmdButton1"></Button>
        <Button CommandName="cmdButton2"></Button>
      </MenuGroup>
      <MenuGroup>
        <Button CommandName="cmdButton3"></Button>
      </MenuGroup>
    </SplitButtonGallery.MenuGroups>
  </SplitButtonGallery>
</Group>
```



## <a name="requirements"></a><span data-ttu-id="a2ed0-123">Требования</span><span class="sxs-lookup"><span data-stu-id="a2ed0-123">Requirements</span></span>



| <span data-ttu-id="a2ed0-124">Требование</span><span class="sxs-lookup"><span data-stu-id="a2ed0-124">Requirement</span></span> | <span data-ttu-id="a2ed0-125">Значение</span><span class="sxs-lookup"><span data-stu-id="a2ed0-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="a2ed0-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a2ed0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ed0-127">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a2ed0-127">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="a2ed0-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a2ed0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ed0-129">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="a2ed0-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2ed0-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a2ed0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2ed0-131">Элемент управления коллекции разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="a2ed0-131">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="a2ed0-132">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="a2ed0-132">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





