---
description: Указывает поставщика трассировки (ETW или WPP) для Мфтраце.
ms.assetid: 692cce3b-ebf5-4a49-8c37-48c8ef6caee7
title: элемент provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ca319b686101766dacd79821ac6d9caf859cf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811573"
---
# <a name="provider-element"></a><span data-ttu-id="27ef7-103">элемент provider</span><span class="sxs-lookup"><span data-stu-id="27ef7-103">provider element</span></span>

<span data-ttu-id="27ef7-104">Указывает поставщика трассировки (ETW или WPP) для [мфтраце](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="27ef7-104">Specifies a trace provider (ETW or WPP) for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="27ef7-105">Использование</span><span class="sxs-lookup"><span data-stu-id="27ef7-105">Usage</span></span>

``` syntax
<provider
  ID = "CDATA"
  level = "CDATA">
  child elements
</provider>
```

## <a name="attributes"></a><span data-ttu-id="27ef7-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="27ef7-106">Attributes</span></span>



| <span data-ttu-id="27ef7-107">attribute</span><span class="sxs-lookup"><span data-stu-id="27ef7-107">Attribute</span></span>            | <span data-ttu-id="27ef7-108">Тип</span><span class="sxs-lookup"><span data-stu-id="27ef7-108">Type</span></span>             | <span data-ttu-id="27ef7-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="27ef7-109">Required</span></span>       | <span data-ttu-id="27ef7-110">Описание</span><span class="sxs-lookup"><span data-stu-id="27ef7-110">Description</span></span>                                              |
|----------------------|------------------|----------------|----------------------------------------------------------|
| <span data-ttu-id="27ef7-111">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="27ef7-111">**ID**</span></span><br/>    | <span data-ttu-id="27ef7-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="27ef7-112">CDATA</span></span><br/> | <span data-ttu-id="27ef7-113">Да</span><span class="sxs-lookup"><span data-stu-id="27ef7-113">Yes</span></span><br/> | <span data-ttu-id="27ef7-114">Имя или идентификатор GUID поставщика.</span><span class="sxs-lookup"><span data-stu-id="27ef7-114">The name or GUID of the provider.</span></span><br/> <br/> |
| <span data-ttu-id="27ef7-115">**level**</span><span class="sxs-lookup"><span data-stu-id="27ef7-115">**level**</span></span><br/> | <span data-ttu-id="27ef7-116">CDATA</span><span class="sxs-lookup"><span data-stu-id="27ef7-116">CDATA</span></span><br/> | <span data-ttu-id="27ef7-117">Да</span><span class="sxs-lookup"><span data-stu-id="27ef7-117">Yes</span></span><br/> | <span data-ttu-id="27ef7-118">Уровень трассировки.</span><span class="sxs-lookup"><span data-stu-id="27ef7-118">The trace level.</span></span><br/> <br/>                  |



## <a name="child-elements"></a><span data-ttu-id="27ef7-119">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="27ef7-119">Child elements</span></span>



| <span data-ttu-id="27ef7-120">Элемент</span><span class="sxs-lookup"><span data-stu-id="27ef7-120">Element</span></span>                               |
|---------------------------------------|
| [<span data-ttu-id="27ef7-121">**This**</span><span class="sxs-lookup"><span data-stu-id="27ef7-121">**keyword**</span></span>](keyword.md)<br/> |



### <a name="child-element-sequence"></a><span data-ttu-id="27ef7-122">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="27ef7-122">Child element sequence</span></span>

``` syntax
keyword+
```

## <a name="parent-elements"></a><span data-ttu-id="27ef7-123">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="27ef7-123">Parent elements</span></span>



| <span data-ttu-id="27ef7-124">Элемент</span><span class="sxs-lookup"><span data-stu-id="27ef7-124">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="27ef7-125">**поставщик**</span><span class="sxs-lookup"><span data-stu-id="27ef7-125">**providers**</span></span>](providers.md)<br/> |



## <a name="element-information"></a><span data-ttu-id="27ef7-126">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="27ef7-126">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="27ef7-127">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="27ef7-127">Can be empty</span></span> | <span data-ttu-id="27ef7-128">Нет</span><span class="sxs-lookup"><span data-stu-id="27ef7-128">No</span></span>  |



## <a name="see-also"></a><span data-ttu-id="27ef7-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27ef7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27ef7-130">Файл конфигурации Мфтраце</span><span class="sxs-lookup"><span data-stu-id="27ef7-130">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




