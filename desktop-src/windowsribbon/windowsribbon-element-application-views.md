---
title: Свойство Application. views
description: Представляет контейнер для каждого представления платформы ленты, в частности Ribbon и Контекстпопуп.
ms.assetid: e7549b8b-0f95-477a-9024-1a99ee1412c2
keywords:
- Лента Windows для свойства Application. views
topic_type:
- apiref
api_name:
- Application.Views
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57e7d106d346a790ee3bd8879b2367f38341f0a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105701051"
---
# <a name="applicationviews-property"></a><span data-ttu-id="83a89-104">Свойство Application. views</span><span class="sxs-lookup"><span data-stu-id="83a89-104">Application.Views property</span></span>

<span data-ttu-id="83a89-105">Представляет контейнер для каждого представления платформы ленты, в частности [**Ribbon**](windowsribbon-element-ribbon.md) и [**контекстпопуп**](windowsribbon-element-contextpopup.md).</span><span class="sxs-lookup"><span data-stu-id="83a89-105">Represents a container for each Ribbon framework View, specifically the [**Ribbon**](windowsribbon-element-ribbon.md) and the [**ContextPopup**](windowsribbon-element-contextpopup.md).</span></span>

## <a name="usage"></a><span data-ttu-id="83a89-106">Использование</span><span class="sxs-lookup"><span data-stu-id="83a89-106">Usage</span></span>

``` syntax
<Application.Views>
  child elements
</Application.Views>
```

## <a name="attributes"></a><span data-ttu-id="83a89-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="83a89-107">Attributes</span></span>

<span data-ttu-id="83a89-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="83a89-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="83a89-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="83a89-109">Child elements</span></span>



| <span data-ttu-id="83a89-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="83a89-110">Element</span></span>                                                               | <span data-ttu-id="83a89-111">Описание</span><span class="sxs-lookup"><span data-stu-id="83a89-111">Description</span></span>                                        |
|-----------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="83a89-112">**контекстпопуп**</span><span class="sxs-lookup"><span data-stu-id="83a89-112">**ContextPopup**</span></span>](windowsribbon-element-contextpopup.md)<br/> | <span data-ttu-id="83a89-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="83a89-113">May occur one or more times</span></span><br/> <br/> |
| [<span data-ttu-id="83a89-114">**Лента**</span><span class="sxs-lookup"><span data-stu-id="83a89-114">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/>             | <span data-ttu-id="83a89-115">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="83a89-115">Must occur exactly once</span></span><br/> <br/>     |



## <a name="parent-elements"></a><span data-ttu-id="83a89-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="83a89-116">Parent elements</span></span>



| <span data-ttu-id="83a89-117">Элемент</span><span class="sxs-lookup"><span data-stu-id="83a89-117">Element</span></span>                                                             |
|---------------------------------------------------------------------|
| [<span data-ttu-id="83a89-118">**Приложение**</span><span class="sxs-lookup"><span data-stu-id="83a89-118">**Application**</span></span>](windowsribbon-element-application.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="83a89-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="83a89-119">Remarks</span></span>

<span data-ttu-id="83a89-120">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="83a89-120">Required.</span></span>

<span data-ttu-id="83a89-121">Должен выполняться ровно один раз для каждого элемента [**приложения**](windowsribbon-element-application.md) .</span><span class="sxs-lookup"><span data-stu-id="83a89-121">Must occur exactly once for each [**Application**](windowsribbon-element-application.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="83a89-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="83a89-122">Examples</span></span>

<span data-ttu-id="83a89-123">В следующем примере показан элемент **Application. views** , содержащий манифест элементов управления ленты, каждый со ссылкой на команду, объявленную в элементе [**Application. Commands**](windowsribbon-element-application-commands.md) .</span><span class="sxs-lookup"><span data-stu-id="83a89-123">The following example shows an **Application.Views** element that contains a manifest of Ribbon controls, each with a reference to a Command declared in the [**Application.Commands**](windowsribbon-element-application-commands.md) element.</span></span>


```C++
<Application.Views>
  <Ribbon Name="ScenicRibbonSampleApp">
    <Ribbon.Tabs>
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
    </Ribbon.Tabs>
  </Ribbon>
</Application.Views>
```



## <a name="requirements"></a><span data-ttu-id="83a89-124">Требования</span><span class="sxs-lookup"><span data-stu-id="83a89-124">Requirements</span></span>



| <span data-ttu-id="83a89-125">Требование</span><span class="sxs-lookup"><span data-stu-id="83a89-125">Requirement</span></span> | <span data-ttu-id="83a89-126">Значение</span><span class="sxs-lookup"><span data-stu-id="83a89-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="83a89-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83a89-127">Minimum supported client</span></span><br/> | <span data-ttu-id="83a89-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="83a89-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="83a89-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83a89-129">Minimum supported server</span></span><br/> | <span data-ttu-id="83a89-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="83a89-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83a89-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83a89-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83a89-132">**Application. Commands**</span><span class="sxs-lookup"><span data-stu-id="83a89-132">**Application.Commands**</span></span>](windowsribbon-element-application-commands.md)
</dt> </dl>

 

 





