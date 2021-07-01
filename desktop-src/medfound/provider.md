---
description: Указывает поставщика трассировки (ETW или WPP) для Мфтраце.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: элемент provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d96b3015dddbcff74c09f77a1b6245d052fe034
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118449"
---
# <a name="provider-element"></a><span data-ttu-id="d1fcf-103">элемент provider</span><span class="sxs-lookup"><span data-stu-id="d1fcf-103">provider element</span></span>

<span data-ttu-id="d1fcf-104">Указывает поставщика трассировки (ETW или WPP) для [мфтраце](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="d1fcf-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="d1fcf-105">Использование</span><span class="sxs-lookup"><span data-stu-id="d1fcf-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="d1fcf-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d1fcf-106">Attributes</span></span>



| <span data-ttu-id="d1fcf-107">attribute</span><span class="sxs-lookup"><span data-stu-id="d1fcf-107">Attribute</span></span>            | <span data-ttu-id="d1fcf-108">Тип</span><span class="sxs-lookup"><span data-stu-id="d1fcf-108">Type</span></span>             | <span data-ttu-id="d1fcf-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d1fcf-109">Required</span></span>       | <span data-ttu-id="d1fcf-110">Описание</span><span class="sxs-lookup"><span data-stu-id="d1fcf-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="d1fcf-111">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="d1fcf-111">**ID**</span></span><br/>    | <span data-ttu-id="d1fcf-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="d1fcf-112">CDATA</span></span><br/> | <span data-ttu-id="d1fcf-113">Да</span><span class="sxs-lookup"><span data-stu-id="d1fcf-113">Yes</span></span><br/> | <span data-ttu-id="d1fcf-114">Имя или идентификатор GUID поставщика.</span><span class="sxs-lookup"><span data-stu-id="d1fcf-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="d1fcf-115">**level**</span><span class="sxs-lookup"><span data-stu-id="d1fcf-115">**level**</span></span><br/> | <span data-ttu-id="d1fcf-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="d1fcf-116">CDATA</span></span><br/> | <span data-ttu-id="d1fcf-117">Да</span><span class="sxs-lookup"><span data-stu-id="d1fcf-117">Yes</span></span><br/> | <span data-ttu-id="d1fcf-118">Уровень трассировки.</span><span class="sxs-lookup"><span data-stu-id="d1fcf-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="d1fcf-119">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d1fcf-119">Child elements</span></span>



| <span data-ttu-id="d1fcf-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="d1fcf-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="d1fcf-121">**This**</span><span class="sxs-lookup"><span data-stu-id="d1fcf-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="d1fcf-122">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="d1fcf-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="d1fcf-123">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d1fcf-123">Parent elements</span></span>



| <span data-ttu-id="d1fcf-124">Элемент</span><span class="sxs-lookup"><span data-stu-id="d1fcf-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="d1fcf-125">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="d1fcf-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="d1fcf-126">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d1fcf-126">Element information</span></span>

:::row:::
    :::column:::
        <span data-ttu-id="d1fcf-127">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="d1fcf-127">Can be empty</span></span>
    :::column-end:::
    :::column span="2":::
        <span data-ttu-id="d1fcf-128">Нет</span><span class="sxs-lookup"><span data-stu-id="d1fcf-128">No</span></span>
    :::column-end:::
:::row-end:::

## <a name="see-also"></a><span data-ttu-id="d1fcf-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d1fcf-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1fcf-130">Файл конфигурации Мфтраце</span><span class="sxs-lookup"><span data-stu-id="d1fcf-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




