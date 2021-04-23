---
title: Сплитбуттонгаллери. Менулайаут, свойство
description: Представляет контейнер для макетов раскрывающегося меню коллекции разделенных кнопок.
ms.assetid: 4bebdff6-16ea-4cf3-adc7-9b86ea200e81
keywords:
- Лента Windows для свойства Сплитбуттонгаллери. Менулайаут
topic_type:
- apiref
api_name:
- SplitButtonGallery.MenuLayout
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04428c14b5e47795da47e5c03970610cd08a6e8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701027"
---
# <a name="splitbuttongallerymenulayout-property"></a><span data-ttu-id="ab2c1-104">Сплитбуттонгаллери. Менулайаут, свойство</span><span class="sxs-lookup"><span data-stu-id="ab2c1-104">SplitButtonGallery.MenuLayout property</span></span>

<span data-ttu-id="ab2c1-105">Представляет контейнер для макетов раскрывающегося меню [коллекции разделенных кнопок](windowsribbon-controls-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ab2c1-105">Represents a container for [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md) drop-down menu layouts.</span></span>

## <a name="usage"></a><span data-ttu-id="ab2c1-106">Использование</span><span class="sxs-lookup"><span data-stu-id="ab2c1-106">Usage</span></span>

``` syntax
<SplitButtonGallery.MenuLayout>
  child elements
</SplitButtonGallery.MenuLayout>
```

## <a name="attributes"></a><span data-ttu-id="ab2c1-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ab2c1-107">Attributes</span></span>

<span data-ttu-id="ab2c1-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="ab2c1-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ab2c1-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ab2c1-109">Child elements</span></span>



| <span data-ttu-id="ab2c1-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="ab2c1-110">Element</span></span>                                                                           | <span data-ttu-id="ab2c1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="ab2c1-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="ab2c1-112">**фловменулайаут**</span><span class="sxs-lookup"><span data-stu-id="ab2c1-112">**FlowMenuLayout**</span></span>](windowsribbon-element-flowmenulayout.md)<br/>         | <span data-ttu-id="ab2c1-113">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="ab2c1-113">Must occur exactly once</span></span><br/> <br/> |
| [<span data-ttu-id="ab2c1-114">**вертикалменулайаут**</span><span class="sxs-lookup"><span data-stu-id="ab2c1-114">**VerticalMenuLayout**</span></span>](windowsribbon-element-verticalmenulayout.md)<br/> | <span data-ttu-id="ab2c1-115">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="ab2c1-115">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ab2c1-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ab2c1-116">Parent elements</span></span>



| <span data-ttu-id="ab2c1-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="ab2c1-117">Element</span></span>                                                                           |
|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="ab2c1-118">**сплитбуттонгаллери**</span><span class="sxs-lookup"><span data-stu-id="ab2c1-118">**SplitButtonGallery**</span></span>](windowsribbon-element-splitbuttongallery.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ab2c1-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ab2c1-119">Remarks</span></span>

<span data-ttu-id="ab2c1-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="ab2c1-120">Optional.</span></span>

<span data-ttu-id="ab2c1-121">Может встречаться не более одного раза для каждого элемента [**сплитбуттонгаллери**](windowsribbon-element-splitbuttongallery.md) .</span><span class="sxs-lookup"><span data-stu-id="ab2c1-121">May occur at most once for each [**SplitButtonGallery**](windowsribbon-element-splitbuttongallery.md) element.</span></span>

> [!Note]  
> <span data-ttu-id="ab2c1-122">Допускается не более одного дочернего элемента ([**вертикалменулайаут**](windowsribbon-element-verticalmenulayout.md) или [**фловменулайаут**](windowsribbon-element-flowmenulayout.md)).</span><span class="sxs-lookup"><span data-stu-id="ab2c1-122">A maximum of one child element ([**VerticalMenuLayout**](windowsribbon-element-verticalmenulayout.md) or [**FlowMenuLayout**](windowsribbon-element-flowmenulayout.md)) is allowed.</span></span>

 

## <a name="examples"></a><span data-ttu-id="ab2c1-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="ab2c1-123">Examples</span></span>

<span data-ttu-id="ab2c1-124">В следующем примере показана базовая разметка для [коллекции разворачивающихся кнопок](windowsribbon-controls-splitbuttongallery.md).</span><span class="sxs-lookup"><span data-stu-id="ab2c1-124">The following example demonstrates the basic markup for the [Split Button Gallery](windowsribbon-controls-splitbuttongallery.md).</span></span>

<span data-ttu-id="ab2c1-125">В этом разделе кода показано объявление элемента управления **сплитбуттонгаллери. менулайаут** .</span><span class="sxs-lookup"><span data-stu-id="ab2c1-125">This section of code shows the **SplitButtonGallery.MenuLayout** control declaration.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="ab2c1-126">Требования</span><span class="sxs-lookup"><span data-stu-id="ab2c1-126">Requirements</span></span>



| <span data-ttu-id="ab2c1-127">Требование</span><span class="sxs-lookup"><span data-stu-id="ab2c1-127">Requirement</span></span> | <span data-ttu-id="ab2c1-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ab2c1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ab2c1-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ab2c1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ab2c1-130">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ab2c1-130">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ab2c1-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ab2c1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ab2c1-132">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab2c1-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab2c1-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ab2c1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab2c1-134">Элемент управления коллекции разделенных кнопок</span><span class="sxs-lookup"><span data-stu-id="ab2c1-134">Split Button Gallery control</span></span>](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[<span data-ttu-id="ab2c1-135">Работа с коллекциями</span><span class="sxs-lookup"><span data-stu-id="ab2c1-135">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> </dl>

 

 





