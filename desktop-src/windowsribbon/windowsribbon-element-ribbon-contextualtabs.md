---
title: Свойство Ribbon. Контекстуалтабс
description: Представляет контейнер для контекстных вкладок.
ms.assetid: 1f57a8d7-97ac-4007-8a36-c6aec5b85e6c
keywords:
- Лента Windows свойства Ribbon. Контекстуалтабс
topic_type:
- apiref
api_name:
- Ribbon.ContextualTabs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790a7c93df71ab5117b591367c6b80fc0f8a748d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801552"
---
# <a name="ribboncontextualtabs-property"></a><span data-ttu-id="2b4e0-104">Свойство Ribbon. Контекстуалтабс</span><span class="sxs-lookup"><span data-stu-id="2b4e0-104">Ribbon.ContextualTabs property</span></span>

<span data-ttu-id="2b4e0-105">Представляет контейнер для контекстных вкладок.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-105">Represents a container for contextual tabs.</span></span>

## <a name="usage"></a><span data-ttu-id="2b4e0-106">Использование</span><span class="sxs-lookup"><span data-stu-id="2b4e0-106">Usage</span></span>

``` syntax
<Ribbon.ContextualTabs>
  child elements
</Ribbon.ContextualTabs>
```

## <a name="attributes"></a><span data-ttu-id="2b4e0-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="2b4e0-107">Attributes</span></span>

<span data-ttu-id="2b4e0-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="2b4e0-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2b4e0-109">Child elements</span></span>



| <span data-ttu-id="2b4e0-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="2b4e0-110">Element</span></span>                                                       | <span data-ttu-id="2b4e0-111">Описание</span><span class="sxs-lookup"><span data-stu-id="2b4e0-111">Description</span></span>                                     |
|---------------------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="2b4e0-112">**Группа вкладок**</span><span class="sxs-lookup"><span data-stu-id="2b4e0-112">**TabGroup**</span></span>](windowsribbon-element-tabgroup.md)<br/> | <span data-ttu-id="2b4e0-113">Должен быть хотя бы один раз</span><span class="sxs-lookup"><span data-stu-id="2b4e0-113">Must occur at least once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="2b4e0-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="2b4e0-114">Parent elements</span></span>



| <span data-ttu-id="2b4e0-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="2b4e0-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="2b4e0-116">**Лента**</span><span class="sxs-lookup"><span data-stu-id="2b4e0-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="2b4e0-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b4e0-117">Remarks</span></span>

<span data-ttu-id="2b4e0-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-118">Optional.</span></span>

<span data-ttu-id="2b4e0-119">Может встречаться не более одного раза для каждой [**ленты**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="2b4e0-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

<span data-ttu-id="2b4e0-120">Контекстные вкладки удобно использовать для отображения функциональных возможностей, относящихся только к конкретному контексту приложения, например к вкладке Формат изображения в текстовом редакторе, который отображается только при выделении изображения.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-120">Contextual tabs are useful for displaying functionality that is relevant only to a specific application context, such as an image formatting tab in a text editor that is displayed only when an image is highlighted.</span></span> <span data-ttu-id="2b4e0-121">Как правило, контекстные вкладки невидимы до тех пор, пока не происходит конкретный контекст приложения, и приложение уведомляет платформу Ribbon.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-121">Typically, contextual tabs are not visible until a specific application context occurs, and the application notifies the Ribbon framework.</span></span>

<span data-ttu-id="2b4e0-122">При отображении контекстные вкладки имеют цветовую кодировку, чтобы отличать их от обычных вкладок.</span><span class="sxs-lookup"><span data-stu-id="2b4e0-122">When displayed, contextual tabs are color coded to differentiate them from regular tabs.</span></span>

## <a name="examples"></a><span data-ttu-id="2b4e0-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="2b4e0-123">Examples</span></span>

<span data-ttu-id="2b4e0-124">В следующем примере показана базовая разметка для элемента **Ribbon. контекстуалтабс** .</span><span class="sxs-lookup"><span data-stu-id="2b4e0-124">The following example demonstrates the basic markup for the **Ribbon.ContextualTabs** element.</span></span>

<span data-ttu-id="2b4e0-125">В этом разделе кода показано объявление команды [**табграуп**](windowsribbon-element-tabgroup.md) и два объявления команды контекстной [**вкладки**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="2b4e0-125">This section of code shows a [**TabGroup**](windowsribbon-element-tabgroup.md) Command declaration and two contextual [**Tab**](windowsribbon-element-tab.md) Command declarations.</span></span>


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



<span data-ttu-id="2b4e0-126">В этом разделе кода показано объявление элемента управления **Ribbon. контекстуалтабс** с помощью [**табграуп**](windowsribbon-element-tabgroup.md) и двух элементов управления контекстной [**вкладки**](windowsribbon-element-tab.md) .</span><span class="sxs-lookup"><span data-stu-id="2b4e0-126">This section of code shows the **Ribbon.ContextualTabs** control declaration with a [**TabGroup**](windowsribbon-element-tabgroup.md) and two contextual [**Tab**](windowsribbon-element-tab.md) controls.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2b4e0-127">Требования</span><span class="sxs-lookup"><span data-stu-id="2b4e0-127">Requirements</span></span>



| <span data-ttu-id="2b4e0-128">Требование</span><span class="sxs-lookup"><span data-stu-id="2b4e0-128">Requirement</span></span> | <span data-ttu-id="2b4e0-129">Значение</span><span class="sxs-lookup"><span data-stu-id="2b4e0-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="2b4e0-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2b4e0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="2b4e0-131">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2b4e0-131">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2b4e0-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2b4e0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="2b4e0-133">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2b4e0-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b4e0-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b4e0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b4e0-135">**Лента. вкладки**</span><span class="sxs-lookup"><span data-stu-id="2b4e0-135">**Ribbon.Tabs**</span></span>](windowsribbon-element-ribbon-tabs.md)
</dt> </dl>

 

 





