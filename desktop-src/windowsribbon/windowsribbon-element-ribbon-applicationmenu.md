---
title: Свойство Ribbon. Аппликатионмену
description: Представляет меню приложения. | Свойство Ribbon. Аппликатионмену
ms.assetid: 6945e976-8ac8-40fa-8e71-31812871b496
keywords:
- Лента Windows свойства Ribbon. Аппликатионмену
topic_type:
- apiref
api_name:
- Ribbon.ApplicationMenu
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71263a19057d3f66747b1a40aaa2d0a46528e9b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105713437"
---
# <a name="ribbonapplicationmenu-property"></a><span data-ttu-id="ef522-105">Свойство Ribbon. Аппликатионмену</span><span class="sxs-lookup"><span data-stu-id="ef522-105">Ribbon.ApplicationMenu property</span></span>

<span data-ttu-id="ef522-106">Представляет меню приложения.</span><span class="sxs-lookup"><span data-stu-id="ef522-106">Represents the Application Menu.</span></span>

## <a name="usage"></a><span data-ttu-id="ef522-107">Использование</span><span class="sxs-lookup"><span data-stu-id="ef522-107">Usage</span></span>

``` syntax
<Ribbon.ApplicationMenu>
  child elements
</Ribbon.ApplicationMenu>
```

## <a name="attributes"></a><span data-ttu-id="ef522-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ef522-108">Attributes</span></span>

<span data-ttu-id="ef522-109">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="ef522-109">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="ef522-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ef522-110">Child elements</span></span>



| <span data-ttu-id="ef522-111">Элемент</span><span class="sxs-lookup"><span data-stu-id="ef522-111">Element</span></span>                                                                     | <span data-ttu-id="ef522-112">Описание</span><span class="sxs-lookup"><span data-stu-id="ef522-112">Description</span></span>                                    |
|-----------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="ef522-113">**аппликатионмену**</span><span class="sxs-lookup"><span data-stu-id="ef522-113">**ApplicationMenu**</span></span>](windowsribbon-element-applicationmenu.md)<br/> | <span data-ttu-id="ef522-114">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="ef522-114">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="ef522-115">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ef522-115">Parent elements</span></span>



| <span data-ttu-id="ef522-116">Элемент</span><span class="sxs-lookup"><span data-stu-id="ef522-116">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="ef522-117">**Лента**</span><span class="sxs-lookup"><span data-stu-id="ef522-117">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="ef522-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ef522-118">Remarks</span></span>

<span data-ttu-id="ef522-119">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="ef522-119">Required.</span></span>

<span data-ttu-id="ef522-120">Может встречаться не более одного раза для каждой [**ленты**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="ef522-120">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="ef522-121">Примеры</span><span class="sxs-lookup"><span data-stu-id="ef522-121">Examples</span></span>

<span data-ttu-id="ef522-122">В следующем примере показана базовая разметка для элемента **Ribbon. аппликатионмену** .</span><span class="sxs-lookup"><span data-stu-id="ef522-122">The following example demonstrates the basic markup for the **Ribbon.ApplicationMenu** element.</span></span>

<span data-ttu-id="ef522-123">В этом разделе кода показано объявление элемента управления **Ribbon. аппликатионмену** .</span><span class="sxs-lookup"><span data-stu-id="ef522-123">This section of code shows the **Ribbon.ApplicationMenu** control declaration.</span></span>


```XML
<!-- Control declarations for Application Menu items. -->
<Ribbon.ApplicationMenu>
  <ApplicationMenu CommandName="cmdFileMenu">
    <!-- Most recently used items collection. -->
    <ApplicationMenu.RecentItems>
      <RecentItems CommandName="cmdMRUItems"/>
    </ApplicationMenu.RecentItems>
    <!-- Menu items collection. -->
    <MenuGroup>
      <Button CommandName="cmdNew" />
      <Button CommandName="cmdOpen" />
      <Button CommandName="cmdSave" />
    </MenuGroup>
    <MenuGroup>
      <Button CommandName="cmdPrint" />
      <Button CommandName="cmdExit" />
    </MenuGroup>
  </ApplicationMenu>
</Ribbon.ApplicationMenu>
```



## <a name="requirements"></a><span data-ttu-id="ef522-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ef522-124">Requirements</span></span>



| <span data-ttu-id="ef522-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ef522-125">Requirement</span></span> | <span data-ttu-id="ef522-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ef522-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="ef522-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ef522-127">Minimum supported client</span></span><br/> | <span data-ttu-id="ef522-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ef522-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="ef522-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ef522-129">Minimum supported server</span></span><br/> | <span data-ttu-id="ef522-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef522-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





