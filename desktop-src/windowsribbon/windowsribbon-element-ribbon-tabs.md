---
title: Свойство Ribbon. табуляции
description: Представляет контейнер для всех основных вкладок на ленте.
ms.assetid: b43d0544-c110-4785-85d7-935842b8f03e
keywords:
- Лента окна свойств ленты. табуляции
topic_type:
- apiref
api_name:
- Ribbon.Tabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4300a2385b6ada64e05e16671802460930cc2a7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489309"
---
# <a name="ribbontabs-property"></a><span data-ttu-id="17dc9-104">Свойство Ribbon. табуляции</span><span class="sxs-lookup"><span data-stu-id="17dc9-104">Ribbon.Tabs property</span></span>

<span data-ttu-id="17dc9-105">Представляет контейнер для всех основных вкладок на ленте.</span><span class="sxs-lookup"><span data-stu-id="17dc9-105">Represents a container for all core tabs in a Ribbon.</span></span>

## <a name="usage"></a><span data-ttu-id="17dc9-106">Использование</span><span class="sxs-lookup"><span data-stu-id="17dc9-106">Usage</span></span>

``` syntax
<Ribbon.Tabs>
  child elements
</Ribbon.Tabs>
```

## <a name="attributes"></a><span data-ttu-id="17dc9-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="17dc9-107">Attributes</span></span>

<span data-ttu-id="17dc9-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="17dc9-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="17dc9-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="17dc9-109">Child elements</span></span>



| <span data-ttu-id="17dc9-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="17dc9-110">Element</span></span>                                             | <span data-ttu-id="17dc9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="17dc9-111">Description</span></span>                                     |
|-----------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="17dc9-112">**TAB**</span><span class="sxs-lookup"><span data-stu-id="17dc9-112">**Tab**</span></span>](windowsribbon-element-tab.md)<br/> | <span data-ttu-id="17dc9-113">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="17dc9-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="17dc9-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="17dc9-114">Parent elements</span></span>



| <span data-ttu-id="17dc9-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="17dc9-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="17dc9-116">**Лента**</span><span class="sxs-lookup"><span data-stu-id="17dc9-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="17dc9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="17dc9-117">Remarks</span></span>

<span data-ttu-id="17dc9-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="17dc9-118">Required.</span></span>

<span data-ttu-id="17dc9-119">Может происходить один или несколько раз для каждой [**ленты**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="17dc9-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="17dc9-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="17dc9-120">Examples</span></span>

<span data-ttu-id="17dc9-121">В следующем примере показана базовая разметка для элемента **Ribbon. Табуляторы** с объявлением **домашней** [**вкладки**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="17dc9-121">The following example demonstrates the basic markup for a **Ribbon.Tabs** element with a **Home** [**Tab**](windowsribbon-element-tab.md) declaration.</span></span>


```C++
<Ribbon Name="ScenicRibbonSampleApp">
  <Ribbon.QuickAccessToolbar>
  ...
  </Ribbon.QuickAccessToolbar>
  <Ribbon.ApplicationMenu>
  ...
  </Ribbon.ApplicationMenu>
  <Ribbon.SizeDefinitions>
  ...
  </Ribbon.SizeDefinitions>
  <Ribbon.Tabs>
  ...
```




```C++
<Tab CommandName="cmdHomeTab">
  <Group CommandName="cmdClipboardGroup" 
         SizeDefinition="ThreeButtons">
    <Button CommandName="cmdCopy"/>
    <Button CommandName="cmdPaste"/>
    <ToggleButton CommandName="cmdMinimize"/>
  </Group>
</Tab>
```




```C++
  ...
  </Ribbon.Tabs>
  <Ribbon.ContextualTabs>
  ...
  </Ribbon.ContextualTabs>
  <Ribbon.HelpButton>
  ...
  </Ribbon.HelpButton>
</Ribbon>
```



## <a name="requirements"></a><span data-ttu-id="17dc9-122">Требования</span><span class="sxs-lookup"><span data-stu-id="17dc9-122">Requirements</span></span>



| <span data-ttu-id="17dc9-123">Требование</span><span class="sxs-lookup"><span data-stu-id="17dc9-123">Requirement</span></span> | <span data-ttu-id="17dc9-124">Значение</span><span class="sxs-lookup"><span data-stu-id="17dc9-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="17dc9-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="17dc9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="17dc9-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="17dc9-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="17dc9-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="17dc9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="17dc9-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="17dc9-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="17dc9-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="17dc9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17dc9-130">**Лента. Контекстуалтабс**</span><span class="sxs-lookup"><span data-stu-id="17dc9-130">**Ribbon.ContextualTabs**</span></span>](windowsribbon-element-ribbon-contextualtabs.md)
</dt> </dl>

 

 





