---
title: Свойство Ribbon. Куиккакцесстулбар
description: Представляет контейнер для панели быстрого доступа (QAT).
ms.assetid: 8a873a48-4f8b-439d-acad-7da2081fbf40
keywords:
- Лента Windows свойства Ribbon. Куиккакцесстулбар
topic_type:
- apiref
api_name:
- Ribbon.QuickAccessToolbar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad0e09b220bd60b60ccbb8ee05c2da9c4317ba78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414813"
---
# <a name="ribbonquickaccesstoolbar-property"></a><span data-ttu-id="33494-104">Свойство Ribbon. Куиккакцесстулбар</span><span class="sxs-lookup"><span data-stu-id="33494-104">Ribbon.QuickAccessToolbar property</span></span>

<span data-ttu-id="33494-105">Представляет контейнер для панели быстрого доступа (QAT).</span><span class="sxs-lookup"><span data-stu-id="33494-105">Represents a container for the Quick Access Toolbar (QAT).</span></span>

## <a name="usage"></a><span data-ttu-id="33494-106">Использование</span><span class="sxs-lookup"><span data-stu-id="33494-106">Usage</span></span>

``` syntax
<Ribbon.QuickAccessToolbar>
  child elements
</Ribbon.QuickAccessToolbar>
```

## <a name="attributes"></a><span data-ttu-id="33494-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="33494-107">Attributes</span></span>

<span data-ttu-id="33494-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="33494-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="33494-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="33494-109">Child elements</span></span>



| <span data-ttu-id="33494-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="33494-110">Element</span></span>                                                                           | <span data-ttu-id="33494-111">Описание</span><span class="sxs-lookup"><span data-stu-id="33494-111">Description</span></span>                                    |
|-----------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="33494-112">**куиккакцесстулбар**</span><span class="sxs-lookup"><span data-stu-id="33494-112">**QuickAccessToolbar**</span></span>](windowsribbon-element-quickaccesstoolbar.md)<br/> | <span data-ttu-id="33494-113">Должно выполняться только один раз</span><span class="sxs-lookup"><span data-stu-id="33494-113">Must occur exactly once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="33494-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="33494-114">Parent elements</span></span>



| <span data-ttu-id="33494-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="33494-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="33494-116">**Лента**</span><span class="sxs-lookup"><span data-stu-id="33494-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="33494-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="33494-117">Remarks</span></span>

<span data-ttu-id="33494-118">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="33494-118">Required.</span></span>

<span data-ttu-id="33494-119">Может происходить один или несколько раз для каждой [**ленты**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="33494-119">May occur one or more times for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="33494-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="33494-120">Examples</span></span>

<span data-ttu-id="33494-121">В следующем примере показана базовая разметка для элемента **Ribbon. куиккакцесстулбар** .</span><span class="sxs-lookup"><span data-stu-id="33494-121">The following example demonstrates the basic markup for the **Ribbon.QuickAccessToolbar** element.</span></span>


```XML
      <Ribbon.QuickAccessToolbar>
        <QuickAccessToolbar CommandName="cmdQAT"
                            CustomizeCommandName="cmdCustomizeQAT">
          <QuickAccessToolbar.ApplicationDefaults>
            <Button CommandName="cmdButton1"/>
            <ToggleButton CommandName="cmdMinimize"
                          ApplicationDefaults.IsChecked="false"/>
          </QuickAccessToolbar.ApplicationDefaults>
        </QuickAccessToolbar>
      </Ribbon.QuickAccessToolbar>
```



## <a name="requirements"></a><span data-ttu-id="33494-122">Требования</span><span class="sxs-lookup"><span data-stu-id="33494-122">Requirements</span></span>



| <span data-ttu-id="33494-123">Требование</span><span class="sxs-lookup"><span data-stu-id="33494-123">Requirement</span></span> | <span data-ttu-id="33494-124">Значение</span><span class="sxs-lookup"><span data-stu-id="33494-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="33494-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="33494-125">Minimum supported client</span></span><br/> | <span data-ttu-id="33494-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="33494-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="33494-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="33494-127">Minimum supported server</span></span><br/> | <span data-ttu-id="33494-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="33494-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





