---
title: Просмотр. изменяемый размер
description: Атрибут с изменяемым размером извлекает значение, указывающее, можно ли изменить размер представления.
ms.assetid: 4f0e4f31-cf16-498f-823f-da43566043b1
keywords:
- Просмотр. изменение размера проигрывателя Windows Media
topic_type:
- apiref
api_name:
- VIEW.resizable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4d61973e34891d336ea5729ea40478c6c32808
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105714087"
---
# <a name="viewresizable"></a><span data-ttu-id="e1292-104">Просмотр. изменяемый размер</span><span class="sxs-lookup"><span data-stu-id="e1292-104">VIEW.resizable</span></span>

<span data-ttu-id="e1292-105">Атрибут с **изменяемым размером** извлекает значение, указывающее, можно ли изменить размер **представления** .</span><span class="sxs-lookup"><span data-stu-id="e1292-105">The **resizable** attribute retrieves a value indicating whether the **VIEW** can be resized.</span></span>

``` syntax
        elementID.resizable
```

## <a name="possible-values"></a><span data-ttu-id="e1292-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="e1292-106">Possible Values</span></span>

<span data-ttu-id="e1292-107">Этот атрибут является **логическим** , доступным только для чтения, со значением по умолчанию, равным атрибуту **заголовка** окна.</span><span class="sxs-lookup"><span data-stu-id="e1292-107">This attribute is a read-only **Boolean** with a default value equal to the **titlebar** attribute.</span></span>



| <span data-ttu-id="e1292-108">Значения</span><span class="sxs-lookup"><span data-stu-id="e1292-108">Values</span></span> | <span data-ttu-id="e1292-109">Описание</span><span class="sxs-lookup"><span data-stu-id="e1292-109">Description</span></span>             |
|--------|-------------------------|
| <span data-ttu-id="e1292-110">true</span><span class="sxs-lookup"><span data-stu-id="e1292-110">true</span></span>   | <span data-ttu-id="e1292-111">Можно изменить размер представления.</span><span class="sxs-lookup"><span data-stu-id="e1292-111">View can be resized.</span></span>    |
| <span data-ttu-id="e1292-112">false</span><span class="sxs-lookup"><span data-stu-id="e1292-112">false</span></span>  | <span data-ttu-id="e1292-113">Невозможно изменить размер представления.</span><span class="sxs-lookup"><span data-stu-id="e1292-113">View cannot be resized.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e1292-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1292-114">Remarks</span></span>

<span data-ttu-id="e1292-115">Если **строка заголовка** отсутствует, и, следовательно, нет окна или границы, необходимо использовать метод **size** для изменения размера элемента **View** .</span><span class="sxs-lookup"><span data-stu-id="e1292-115">If there is no **titlebar**, and therefore no window or border, you must use the **size** method to resize the **VIEW** element.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1292-116">Требования</span><span class="sxs-lookup"><span data-stu-id="e1292-116">Requirements</span></span>



| <span data-ttu-id="e1292-117">Требование</span><span class="sxs-lookup"><span data-stu-id="e1292-117">Requirement</span></span> | <span data-ttu-id="e1292-118">Значение</span><span class="sxs-lookup"><span data-stu-id="e1292-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e1292-119">Версия</span><span class="sxs-lookup"><span data-stu-id="e1292-119">Version</span></span><br/> | <span data-ttu-id="e1292-120">Проигрыватель Windows Media версии 7,0 или более поздней</span><span class="sxs-lookup"><span data-stu-id="e1292-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e1292-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1292-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1292-122">**VIEW, элемент**</span><span class="sxs-lookup"><span data-stu-id="e1292-122">**VIEW Element**</span></span>](view-element.md)
</dt> </dl>

 

 





