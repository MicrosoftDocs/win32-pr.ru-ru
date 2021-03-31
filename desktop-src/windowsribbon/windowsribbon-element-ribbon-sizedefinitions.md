---
title: Свойство Ribbon. Сизедефинитионс
description: Представляет контейнер для пользовательских шаблонов макета элементов управления ленты.
ms.assetid: 1f5fcffc-7f2e-4763-b0a7-4e8f46534da8
keywords:
- Лента Windows свойства Ribbon. Сизедефинитионс
topic_type:
- apiref
api_name:
- Ribbon.SizeDefinitions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b8ffe5a3339b0f32e493a1f7ddc33789526695e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071206"
---
# <a name="ribbonsizedefinitions-property"></a><span data-ttu-id="0c165-104">Свойство Ribbon. Сизедефинитионс</span><span class="sxs-lookup"><span data-stu-id="0c165-104">Ribbon.SizeDefinitions property</span></span>

<span data-ttu-id="0c165-105">Представляет контейнер для пользовательских шаблонов макета элементов управления ленты.</span><span class="sxs-lookup"><span data-stu-id="0c165-105">Represents a container for custom layout templates of Ribbon controls.</span></span>

## <a name="usage"></a><span data-ttu-id="0c165-106">Использование</span><span class="sxs-lookup"><span data-stu-id="0c165-106">Usage</span></span>

``` syntax
<Ribbon.SizeDefinitions>
  child elements
</Ribbon.SizeDefinitions>
```

## <a name="attributes"></a><span data-ttu-id="0c165-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0c165-107">Attributes</span></span>

<span data-ttu-id="0c165-108">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="0c165-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="0c165-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0c165-109">Child elements</span></span>



| <span data-ttu-id="0c165-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="0c165-110">Element</span></span>                                                                   | <span data-ttu-id="0c165-111">Описание</span><span class="sxs-lookup"><span data-stu-id="0c165-111">Description</span></span>                                        |
|---------------------------------------------------------------------------|----------------------------------------------------|
| [<span data-ttu-id="0c165-112">**сизедефинитион**</span><span class="sxs-lookup"><span data-stu-id="0c165-112">**SizeDefinition**</span></span>](windowsribbon-element-sizedefinition.md)<br/> | <span data-ttu-id="0c165-113">Может происходить один или несколько раз</span><span class="sxs-lookup"><span data-stu-id="0c165-113">May occur one or more times</span></span><br/> <br/> |



## <a name="parent-elements"></a><span data-ttu-id="0c165-114">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="0c165-114">Parent elements</span></span>



| <span data-ttu-id="0c165-115">Элемент</span><span class="sxs-lookup"><span data-stu-id="0c165-115">Element</span></span>                                                   |
|-----------------------------------------------------------|
| [<span data-ttu-id="0c165-116">**Лента**</span><span class="sxs-lookup"><span data-stu-id="0c165-116">**Ribbon**</span></span>](windowsribbon-element-ribbon.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="0c165-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c165-117">Remarks</span></span>

<span data-ttu-id="0c165-118">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="0c165-118">Optional.</span></span>

<span data-ttu-id="0c165-119">Может встречаться не более одного раза для каждой [**ленты**](windowsribbon-element-ribbon.md).</span><span class="sxs-lookup"><span data-stu-id="0c165-119">May occur at most once for each [**Ribbon**](windowsribbon-element-ribbon.md).</span></span>

## <a name="examples"></a><span data-ttu-id="0c165-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="0c165-120">Examples</span></span>

<span data-ttu-id="0c165-121">В следующем примере кода показан базовый пользовательский шаблон.</span><span class="sxs-lookup"><span data-stu-id="0c165-121">The following code example illustrates a basic custom template.</span></span>


```
<Ribbon.SizeDefinitions>
  <SizeDefinition Name="CustomTemplate">
    <GroupSizeDefinition Size="Large">
      <ControlSizeDefinition ImageSize="Large" IsLabelVisible="true" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Medium">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
    <GroupSizeDefinition Size="Small">
      <ControlSizeDefinition ImageSize="Small" IsLabelVisible="false" />
    </GroupSizeDefinition>
  </SizeDefinition>
</Ribbon.SizeDefinitions>
```



## <a name="requirements"></a><span data-ttu-id="0c165-122">Требования</span><span class="sxs-lookup"><span data-stu-id="0c165-122">Requirements</span></span>



| <span data-ttu-id="0c165-123">Требование</span><span class="sxs-lookup"><span data-stu-id="0c165-123">Requirement</span></span> | <span data-ttu-id="0c165-124">Значение</span><span class="sxs-lookup"><span data-stu-id="0c165-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0c165-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c165-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0c165-126">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="0c165-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0c165-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c165-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0c165-128">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c165-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0c165-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c165-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c165-130">Настройка ленты с помощью определений размеров и политик масштабирования</span><span class="sxs-lookup"><span data-stu-id="0c165-130">Customizing a Ribbon Through Size Definitions and Scaling Policies</span></span>](windowsribbon-templates.md)
</dt> </dl>

 

 





