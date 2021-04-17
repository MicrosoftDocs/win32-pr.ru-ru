---
description: Задает ключевое слово для поставщика Мфтраце.
ms.assetid: 1ce4a5ee-c053-4d31-a984-dc11acebbf2a
title: элемент Keyword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11632a257e7d51378ddb816124e51548746a178
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702921"
---
# <a name="keyword-element"></a><span data-ttu-id="ffbf1-103">элемент Keyword</span><span class="sxs-lookup"><span data-stu-id="ffbf1-103">keyword element</span></span>

<span data-ttu-id="ffbf1-104">Задает ключевое слово для поставщика [мфтраце](mftrace.md) .</span><span class="sxs-lookup"><span data-stu-id="ffbf1-104">Specifies a key word for an [MFTrace](mftrace.md) provider.</span></span>

## <a name="usage"></a><span data-ttu-id="ffbf1-105">Использование</span><span class="sxs-lookup"><span data-stu-id="ffbf1-105">Usage</span></span>

``` syntax
<keyword
  ID = "CDATA"/>
```

## <a name="attributes"></a><span data-ttu-id="ffbf1-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ffbf1-106">Attributes</span></span>



| <span data-ttu-id="ffbf1-107">attribute</span><span class="sxs-lookup"><span data-stu-id="ffbf1-107">Attribute</span></span>         | <span data-ttu-id="ffbf1-108">Тип</span><span class="sxs-lookup"><span data-stu-id="ffbf1-108">Type</span></span>             | <span data-ttu-id="ffbf1-109">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ffbf1-109">Required</span></span>       | <span data-ttu-id="ffbf1-110">Описание</span><span class="sxs-lookup"><span data-stu-id="ffbf1-110">Description</span></span>                                             |
|-------------------|------------------|----------------|---------------------------------------------------------|
| <span data-ttu-id="ffbf1-111">**Идентификатор**</span><span class="sxs-lookup"><span data-stu-id="ffbf1-111">**ID**</span></span><br/> | <span data-ttu-id="ffbf1-112">CDATA</span><span class="sxs-lookup"><span data-stu-id="ffbf1-112">CDATA</span></span><br/> | <span data-ttu-id="ffbf1-113">Да</span><span class="sxs-lookup"><span data-stu-id="ffbf1-113">Yes</span></span><br/> | <span data-ttu-id="ffbf1-114">Имя или маска ключевого слова</span><span class="sxs-lookup"><span data-stu-id="ffbf1-114">The name or mask of the key word</span></span><br/> <br/> |



## <a name="child-elements"></a><span data-ttu-id="ffbf1-115">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ffbf1-115">Child elements</span></span>

<span data-ttu-id="ffbf1-116">Нет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="ffbf1-116">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="ffbf1-117">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ffbf1-117">Parent elements</span></span>



| <span data-ttu-id="ffbf1-118">Элемент</span><span class="sxs-lookup"><span data-stu-id="ffbf1-118">Element</span></span>                                   |
|-------------------------------------------|
| [<span data-ttu-id="ffbf1-119">**мфдетаурс**</span><span class="sxs-lookup"><span data-stu-id="ffbf1-119">**mfdetours**</span></span>](mfdetours.md)<br/> |
| [<span data-ttu-id="ffbf1-120">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="ffbf1-120">**provider**</span></span>](provider.md)<br/>   |



## <a name="remarks"></a><span data-ttu-id="ffbf1-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ffbf1-121">Remarks</span></span>

<span data-ttu-id="ffbf1-122">Для элемента [**мфдетаурс**](mfdetours.md) допустимые ключевые слова перечислены в разделе [Ключевые слова мфтраце](mftrace-keywords.md).</span><span class="sxs-lookup"><span data-stu-id="ffbf1-122">For the [**mfdetours**](mfdetours.md) element, the valid key words are listed in the topic [MFTrace Keywords](mftrace-keywords.md).</span></span>

<span data-ttu-id="ffbf1-123">Для элемента [**provider**](provider.md) ключевые слова зависят от поставщика событий.</span><span class="sxs-lookup"><span data-stu-id="ffbf1-123">For the [**provider**](provider.md) element, the key words depend on the event provider.</span></span> <span data-ttu-id="ffbf1-124">Для перечисления ключевых слов конкретного поставщика можно использовать служебную программу Wevtutil.exe.</span><span class="sxs-lookup"><span data-stu-id="ffbf1-124">You can use the Wevtutil.exe utility to list the key words for a given provider.</span></span>

## <a name="element-information"></a><span data-ttu-id="ffbf1-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ffbf1-125">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="ffbf1-126">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="ffbf1-126">Can be empty</span></span> | <span data-ttu-id="ffbf1-127">Да</span><span class="sxs-lookup"><span data-stu-id="ffbf1-127">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="ffbf1-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ffbf1-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbf1-129">Файл конфигурации Мфтраце</span><span class="sxs-lookup"><span data-stu-id="ffbf1-129">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> <dt>

[<span data-ttu-id="ffbf1-130">Ключевые слова Мфтраце</span><span class="sxs-lookup"><span data-stu-id="ffbf1-130">MFTrace Keywords</span></span>](mftrace-keywords.md)
</dt> </dl>

 

 




