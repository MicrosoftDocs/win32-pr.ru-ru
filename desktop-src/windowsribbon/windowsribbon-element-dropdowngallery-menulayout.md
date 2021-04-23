---
title: Дропдовнгаллери. Менулайаут, свойство
description: Представляет контейнер для раскрывающихся раскрывающихся меню Дропдовнгаллери.
ms.assetid: 7251e889-377d-4d7f-b049-bd81a202774d
keywords:
- Лента Windows для свойства Дропдовнгаллери. Менулайаут
topic_type:
- apiref
api_name:
- DropDownGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1b6ad3f07f369dfef90b1e6c52c34793e60520
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710525"
---
# <a name="dropdowngallerymenulayout-property"></a><span data-ttu-id="6c4a7-104">Дропдовнгаллери. Менулайаут, свойство</span><span class="sxs-lookup"><span data-stu-id="6c4a7-104">DropDownGallery.MenuLayout property</span></span>

<span data-ttu-id="6c4a7-105">Представляет контейнер для раскрывающихся раскрывающихся меню [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="6c4a7-105">Represents a container for [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="6c4a7-106">Использование</span><span class="sxs-lookup"><span data-stu-id="6c4a7-106">Usage</span></span>

``` syntax
<DropDownGallery.MenuLayout>
  child elements
</DropDownGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="6c4a7-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6c4a7-107">Attributes</span></span>

<span data-ttu-id="6c4a7-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="6c4a7-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6c4a7-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6c4a7-109">Child elements</span></span>



| <span data-ttu-id="6c4a7-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="6c4a7-110">Element</span></span>                                                                           | <span data-ttu-id="6c4a7-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6c4a7-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="6c4a7-112">**фловменулайаут**</span><span class="sxs-lookup"><span data-stu-id="6c4a7-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="6c4a7-113">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="6c4a7-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="6c4a7-114">**вертикалменулайаут**</span><span class="sxs-lookup"><span data-stu-id="6c4a7-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="6c4a7-115">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="6c4a7-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="6c4a7-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6c4a7-116">Parent elements</span></span>



| <span data-ttu-id="6c4a7-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="6c4a7-117">Element</span></span>                                                                     |
|-----------------------------------------------------------------------------|
| [<span data-ttu-id="6c4a7-118">**дропдовнгаллери**</span><span class="sxs-lookup"><span data-stu-id="6c4a7-118">**DropDownGallery**</span></span>](windowsribbon-element-dropdowngallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="6c4a7-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c4a7-119">Remarks</span></span>

<span data-ttu-id="6c4a7-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="6c4a7-120">Optional.</span></span>

<span data-ttu-id="6c4a7-121">Может встречаться не более одного раза для каждого элемента [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md) .</span><span class="sxs-lookup"><span data-stu-id="6c4a7-121">May occur at most once for each [**DropDownGallery**](windowsribbon-element-dropdowngallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="6c4a7-122">Допускается не более одного дочернего элемента ([**вертикалменулайаут**](windowsribbon-element-verticalmenulayout.md) или [**фловменулайаут**](windowsribbon-element-flowmenulayout.md)).</span><span class="sxs-lookup"><span data-stu-id="6c4a7-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="6c4a7-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="6c4a7-123">Examples</span></span>

<span data-ttu-id="6c4a7-124">В следующем примере показана базовая разметка для [**дропдовнгаллери**](windowsribbon-element-dropdowngallery.md).</span><span class="sxs-lookup"><span data-stu-id="6c4a7-124">The following example demonstrates the basic markup for the [**DropDownGallery**](windowsribbon-element-dropdowngallery.md).</span></span>

<span data-ttu-id="6c4a7-125">В этом разделе кода показано объявление элемента управления **дропдовнгаллери. менулайаут** .</span><span class="sxs-lookup"><span data-stu-id="6c4a7-125">This section of code shows the **DropDownGallery.MenuLayout** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="6c4a7-126">Требования</span><span class="sxs-lookup"><span data-stu-id="6c4a7-126">Requirements</span></span>



| <span data-ttu-id="6c4a7-127">Требование</span><span class="sxs-lookup"><span data-stu-id="6c4a7-127">Requirement</span></span> | <span data-ttu-id="6c4a7-128">Значение</span><span class="sxs-lookup"><span data-stu-id="6c4a7-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6c4a7-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c4a7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6c4a7-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="6c4a7-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6c4a7-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c4a7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6c4a7-132">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6c4a7-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c4a7-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c4a7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c4a7-134">**Элемент управления "раскрывающийся список"**</span><span class="sxs-lookup"><span data-stu-id="6c4a7-134">**Drop-Down Gallery control**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="6c4a7-135">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="6c4a7-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





