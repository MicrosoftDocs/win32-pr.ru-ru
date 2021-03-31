---
description: Содержит список поставщиков трассировки для Мфтраце.
ms.assetid: ee483f0a-5a90-4150-ada4-0b63ae312523
title: Providers, элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04e5aaedcd14d840cfdc0d85559f6a7981943593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263495"
---
# <a name="providers-element"></a><span data-ttu-id="acf43-103">Providers, элемент</span><span class="sxs-lookup"><span data-stu-id="acf43-103">providers element</span></span>

<span data-ttu-id="acf43-104">Содержит список поставщиков трассировки для [мфтраце](mftrace.md).</span><span class="sxs-lookup"><span data-stu-id="acf43-104">Contains a list of trace providers for [MFTrace](mftrace.md).</span></span>

## <a name="usage"></a><span data-ttu-id="acf43-105">Использование</span><span class="sxs-lookup"><span data-stu-id="acf43-105">Usage</span></span>

``` syntax
<providers>
  child elements
</providers>
```

## <a name="attributes"></a><span data-ttu-id="acf43-106">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="acf43-106">Attributes</span></span>

<span data-ttu-id="acf43-107">Атрибуты отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="acf43-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="acf43-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="acf43-108">Child elements</span></span>



| <span data-ttu-id="acf43-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="acf43-109">Element</span></span>                                   | <span data-ttu-id="acf43-110">Описание</span><span class="sxs-lookup"><span data-stu-id="acf43-110">Description</span></span>                                                                                                      |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="acf43-111">**мфдетаурс**</span><span class="sxs-lookup"><span data-stu-id="acf43-111">**mfdetours**</span></span>](mfdetours.md)<br/> | <span data-ttu-id="acf43-112">Указывает поставщик Media Foundation для обзора, который отслеживает вызовы API Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="acf43-112">Specifies the Media Foundation Detours provider, which traces Media Foundation API calls.</span></span><br/> <br/> |
| [<span data-ttu-id="acf43-113">**поставщики**</span><span class="sxs-lookup"><span data-stu-id="acf43-113">**provider**</span></span>](provider.md)<br/>   | <span data-ttu-id="acf43-114">Указывает поставщика трассировки (ETW или WPP).</span><span class="sxs-lookup"><span data-stu-id="acf43-114">Specifies a trace provider (ETW or WPP).</span></span><br/> <br/>                                                  |



### <a name="child-element-sequence"></a><span data-ttu-id="acf43-115">Последовательность дочерних элементов</span><span class="sxs-lookup"><span data-stu-id="acf43-115">Child element sequence</span></span>

``` syntax
(
  mfdetours?, 
  provider*
)
```

## <a name="parent-elements"></a><span data-ttu-id="acf43-116">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="acf43-116">Parent elements</span></span>

<span data-ttu-id="acf43-117">Нет родительских элементов.</span><span class="sxs-lookup"><span data-stu-id="acf43-117">There are no parent elements.</span></span>

## <a name="element-information"></a><span data-ttu-id="acf43-118">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="acf43-118">Element information</span></span>



|              |     |
|--------------|-----|
| <span data-ttu-id="acf43-119">Может быть пустым</span><span class="sxs-lookup"><span data-stu-id="acf43-119">Can be empty</span></span> | <span data-ttu-id="acf43-120">Да</span><span class="sxs-lookup"><span data-stu-id="acf43-120">Yes</span></span> |



## <a name="see-also"></a><span data-ttu-id="acf43-121">См. также</span><span class="sxs-lookup"><span data-stu-id="acf43-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf43-122">Файл конфигурации Мфтраце</span><span class="sxs-lookup"><span data-stu-id="acf43-122">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)
</dt> </dl>

 

 




