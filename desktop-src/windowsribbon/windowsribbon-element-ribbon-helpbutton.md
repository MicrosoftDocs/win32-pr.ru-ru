---
title: Свойство Ribbon. Хелпбуттон
description: Представляет контейнер для кнопки "Справка".
ms.assetid: a64239b2-2440-4bcf-8fd7-079003de6d8c
keywords:
- Лента Windows свойства Ribbon. Хелпбуттон
topic_type:
- apiref
api_name:
- Ribbon.HelpButton
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49e343a5181479ede5d428937908ed4bf37764f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802872"
---
# <a name="ribbonhelpbutton-property"></a><span data-ttu-id="120d9-104">Свойство Ribbon. Хелпбуттон</span><span class="sxs-lookup"><span data-stu-id="120d9-104">Ribbon.HelpButton property</span></span>

<span data-ttu-id="120d9-105">Представляет контейнер для [кнопки "Справка"](windowsribbon-controls-helpbutton.md).</span><span class="sxs-lookup"><span data-stu-id="120d9-105">Represents a container for the [Help Button](windowsribbon-controls-helpbutton.md).</span></span>

## <a name="usage"></a><span data-ttu-id="120d9-106">Использование</span><span class="sxs-lookup"><span data-stu-id="120d9-106">Usage</span></span>

``` syntax
<Ribbon.HelpButton>
  child elements
</Ribbon.HelpButton>
```

## <a name="attributes"></a><span data-ttu-id="120d9-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="120d9-107">Attributes</span></span>

<span data-ttu-id="120d9-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="120d9-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="120d9-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="120d9-109">Child elements</span></span>



| <span data-ttu-id="120d9-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="120d9-110">Element</span></span>                                                           | <span data-ttu-id="120d9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="120d9-111">Description</span></span>                                   |
|-------------------------------------------------------------------|-----------------------------------------------|
| [<span data-ttu-id="120d9-112">**хелпбуттон**</span><span class="sxs-lookup"><span data-stu-id="120d9-112">**HelpButton**</span></span>](windowsribbon-element-helpbutton.md)<br/> | <span data-ttu-id="120d9-113">Может выполняться не более одного раза</span><span class="sxs-lookup"><span data-stu-id="120d9-113">May occur at most once</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="120d9-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="120d9-114">Parent elements</span></span>



| <span data-ttu-id="120d9-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="120d9-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="120d9-116">**Лента**</span><span class="sxs-lookup"><span data-stu-id="120d9-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="120d9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="120d9-117">Remarks</span></span>

<span data-ttu-id="120d9-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="120d9-118">Optional.</span></span>

<span data-ttu-id="120d9-119">Может встречаться не более одного раза для каждой [**ленты**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="120d9-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="120d9-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="120d9-120">Examples</span></span>

<span data-ttu-id="120d9-121">В следующем примере показана базовая разметка, необходимая для реализации кнопки справки на ленте.</span><span class="sxs-lookup"><span data-stu-id="120d9-121">The following example demonstrates the basic markup that is required to implement a Ribbon Help button.</span></span>

<span data-ttu-id="120d9-122">В этом разделе кода показано объявление команды **Ribbon. хелпбуттон** .</span><span class="sxs-lookup"><span data-stu-id="120d9-122">This section of code shows the **Ribbon.HelpButton** Command declaration.</span></span>


```XML
<Command Name="cmdHelp"
         Symbol="IDR_CMD_HELP">      
</Command>
```



<span data-ttu-id="120d9-123">В этом разделе кода показано объявление элемента управления **Ribbon. хелпбуттон** .</span><span class="sxs-lookup"><span data-stu-id="120d9-123">This section of code shows the **Ribbon.HelpButton** control declaration.</span></span>


```XML
<Ribbon.HelpButton>
  <HelpButton CommandName="cmdHelp"/>
</Ribbon.HelpButton>
```



## <a name="requirements"></a><span data-ttu-id="120d9-124">Требования</span><span class="sxs-lookup"><span data-stu-id="120d9-124">Requirements</span></span>



| <span data-ttu-id="120d9-125">Требование</span><span class="sxs-lookup"><span data-stu-id="120d9-125">Requirement</span></span> | <span data-ttu-id="120d9-126">Значение</span><span class="sxs-lookup"><span data-stu-id="120d9-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="120d9-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="120d9-127">Minimum supported client</span></span><br/> | <span data-ttu-id="120d9-128">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="120d9-128">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="120d9-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="120d9-129">Minimum supported server</span></span><br/> | <span data-ttu-id="120d9-130">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="120d9-130">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





