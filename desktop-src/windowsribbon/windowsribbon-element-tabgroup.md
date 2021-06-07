---
title: Табграуп, элемент
description: Представляет контекстный набор элементов управления "Вкладка".
ms.assetid: f131efe1-b8c4-416e-997a-5e2d3bcc03ea
keywords:
- Лента Windows для элемента Табграуп
topic_type:
- apiref
api_name:
- TabGroup
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4c18db72d6b0161842bfde9d5a836d14189c6a
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444065"
---
# <a name="tabgroup-element"></a><span data-ttu-id="40aaf-104">Табграуп, элемент</span><span class="sxs-lookup"><span data-stu-id="40aaf-104">TabGroup element</span></span>

<span data-ttu-id="40aaf-105">Представляет контекстный набор элементов управления ["Вкладка"](windowsribbon-controls-tabgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="40aaf-105">Represents a contextual set of [Tab](windowsribbon-controls-tabgroup.md) controls.</span></span>

## <a name="usage"></a><span data-ttu-id="40aaf-106">Использование</span><span class="sxs-lookup"><span data-stu-id="40aaf-106">Usage</span></span>

``` syntax
<TabGroup
  CommandName = "xs:positiveInteger or xs:string">
  child elements
</TabGroup>
```

## <a name="attributes"></a><span data-ttu-id="40aaf-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="40aaf-107">Attributes</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="40aaf-108">attribute</span><span class="sxs-lookup"><span data-stu-id="40aaf-108">Attribute</span></span></th>
<th><span data-ttu-id="40aaf-109">Тип</span><span class="sxs-lookup"><span data-stu-id="40aaf-109">Type</span></span></th>
<th><span data-ttu-id="40aaf-110">Обязательно</span><span class="sxs-lookup"><span data-stu-id="40aaf-110">Required</span></span></th>
<th><span data-ttu-id="40aaf-111">Описание</span><span class="sxs-lookup"><span data-stu-id="40aaf-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="40aaf-112"><strong>CommandName</strong></span><span class="sxs-lookup"><span data-stu-id="40aaf-112"><strong>CommandName</strong></span></span><br/></td>
<td><span data-ttu-id="40aaf-113">xs: Поситивеинтежер или xs: String</span><span class="sxs-lookup"><span data-stu-id="40aaf-113">xs:positiveInteger or xs:string</span></span><br/></td>
<td><span data-ttu-id="40aaf-114">Нет</span><span class="sxs-lookup"><span data-stu-id="40aaf-114">No</span></span><br/></td>
<td><span data-ttu-id="40aaf-115">Связывает элемент с <a href="windowsribbon-element-command.md"><strong>командой</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="40aaf-115">Associates the element with a <a href="windowsribbon-element-command.md"><strong>Command</strong></a>.</span></span><br/> <br/><span data-ttu-id="40aaf-116">
<dt><span></span><span></span><strong></strong> (xs: Поситивеинтежер или xs: String)</span><span class="sxs-lookup"><span data-stu-id="40aaf-116">
<dt><span></span><span></span><strong></strong> (xs:positiveInteger or xs:string)</span></span><br/> </dt> <dd> <span data-ttu-id="40aaf-117">Строка, целочисленное значение в диапазоне от 2 до 59999 включительно или шестнадцатеричное значение между 0x2 и 0xea5f включительно.</span><span class="sxs-lookup"><span data-stu-id="40aaf-117">A string, an integer value between 2 and 59999, inclusive, or a hexadecimal value between 0x2 and 0xea5f, inclusive.</span></span> <br/> <span data-ttu-id="40aaf-118">Значение должно быть уникальным в XML-документе ленты.</span><span class="sxs-lookup"><span data-stu-id="40aaf-118">The value must be unique within the Ribbon XML document.</span></span> <br/> <span data-ttu-id="40aaf-119">Максимальная длина: 100 символов.</span><span class="sxs-lookup"><span data-stu-id="40aaf-119">Maximum length: 100 characters.</span></span> <br/> </dd> </dl></td>
</tr>
</tbody>
</table>



## <a name="child-elements"></a><span data-ttu-id="40aaf-120">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="40aaf-120">Child elements</span></span>



| <span data-ttu-id="40aaf-121">Элемент</span><span class="sxs-lookup"><span data-stu-id="40aaf-121">Element</span></span>                                             | <span data-ttu-id="40aaf-122">Описание</span><span class="sxs-lookup"><span data-stu-id="40aaf-122">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="40aaf-123">**Вкладка**</span><span class="sxs-lookup"><span data-stu-id="40aaf-123">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="40aaf-124">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="40aaf-124">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="40aaf-125">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="40aaf-125">Parent elements</span></span>



| <span data-ttu-id="40aaf-126">Элемент</span><span class="sxs-lookup"><span data-stu-id="40aaf-126">Element</span></span>                                                                                 |
|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="40aaf-127">**Лента. Контекстуалтабс**</span><span class="sxs-lookup"><span data-stu-id="40aaf-127">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="40aaf-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="40aaf-128">Remarks</span></span>

<span data-ttu-id="40aaf-129">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="40aaf-129">Required.</span></span>

<span data-ttu-id="40aaf-130">Должен быть хотя бы один раз для каждого элемента [**Ribbon. контекстуалтабс**](windowsribbon-element-ribbon-contextualtabs.md) .</span><span class="sxs-lookup"><span data-stu-id="40aaf-130">Must occur at least once for each [**Ribbon.ContextualTabs**](windowsribbon-element-ribbon-contextualtabs.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="40aaf-131">Примеры</span><span class="sxs-lookup"><span data-stu-id="40aaf-131">Examples</span></span>

<span data-ttu-id="40aaf-132">В следующем примере показана базовая разметка для элемента **табграуп** .</span><span class="sxs-lookup"><span data-stu-id="40aaf-132">The following example demonstrates the basic markup for the **TabGroup** element.</span></span>

<span data-ttu-id="40aaf-133">В этом разделе кода показано объявление команды **табграуп** с двумя контекстными вкладками.</span><span class="sxs-lookup"><span data-stu-id="40aaf-133">This section of code shows a **TabGroup** Command declaration with two contextual tabs.</span></span>


```XML
<!-- Contextual Tabs -->
<Command Name='cmdContextualTab1'
         LabelTitle='Contextual Tab 1'
         Symbol='ID_CONTEXTUALTAB1'/>
<Command Name='cmdContextualTab2'
         LabelTitle='Contextual Tab 2'
         Symbol='ID_CONTEXTUALTAB2'/>
<Command Name='cmdContextualTabGroup'
         LabelTitle='Contextual Tabs'
         Symbol='ID_CONTEXTUALTAB_GROUP'/>
```



<span data-ttu-id="40aaf-134">В этом разделе кода показаны соответствующие объявления элементов управления **табграуп** .</span><span class="sxs-lookup"><span data-stu-id="40aaf-134">This section of code shows corresponding **TabGroup** control declarations.</span></span>


```XML
      <Ribbon.ContextualTabs>
        <TabGroup CommandName='cmdContextualTabGroup'>
          <Tab CommandName='cmdContextualTab1'>
            <!--InRibbonGallery Group-->
            <Group CommandName='cmdInRibbonGalleryGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdTextSizeGallery3'
                               HasLargeItems='true'
                               ItemHeight='32'
                               ItemWidth='32'
                               MaxColumns='3' >
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
            <!--Command Galleries Group-->
            <Group CommandName='cmdCommandGalleriesGroup'
                   SizeDefinition='OneInRibbonGallery'>
              <InRibbonGallery CommandName='cmdCommandGallery1'
                               Type='Commands'
                               MaxRows='3'
                               MaxColumns='3'>
                <InRibbonGallery.MenuLayout>
                  <FlowMenuLayout Columns='3'
                                  Gripper ='Corner'/>
                </InRibbonGallery.MenuLayout>
              </InRibbonGallery>
            </Group>
          </Tab>
          <Tab CommandName='cmdContextualTab2'></Tab>
        </TabGroup>
      </Ribbon.ContextualTabs> 
```



## <a name="element-information"></a><span data-ttu-id="40aaf-135">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="40aaf-135">Element information</span></span>

- <span data-ttu-id="40aaf-136">**Минимальная поддерживаемая система**: Windows 7</span><span class="sxs-lookup"><span data-stu-id="40aaf-136">**Minimum supported system**: Windows 7</span></span> 
- <span data-ttu-id="40aaf-137">**Может быть пустым**: нет</span><span class="sxs-lookup"><span data-stu-id="40aaf-137">**Can be empty**: No</span></span>



## <a name="see-also"></a><span data-ttu-id="40aaf-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40aaf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40aaf-139">Элемент управления группы вкладок</span><span class="sxs-lookup"><span data-stu-id="40aaf-139">Tab Group control</span></span>](windowsribbon-controls-tabgroup.md)
</dt> <dt>

[<span data-ttu-id="40aaf-140">Элемент управления табуляции</span><span class="sxs-lookup"><span data-stu-id="40aaf-140">Tab control</span></span>](windowsribbon-controls-tab.md)
</dt> </dl>

 

 





