---
title: Перенос функций получения для ДИАФРАГМы в ГК
description: 'IRI GL \ 0034; Get \ 0034; функции принимают следующую форму:'
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Перенос GL в ГК, получение функций
- Перенос из IRI GL, получение функций
- перенос в OpenGL из IRI GL, получение функций
- Перенос по стандарту OpenGL из IRI GL, получение функций
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594b12bb1738846b98d33137dd8b623f0405ec40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105661602"
---
# <a name="porting-iris-gl-get-functions"></a><span data-ttu-id="d5277-107">Перенос функций получения для ДИАФРАГМы в ГК</span><span class="sxs-lookup"><span data-stu-id="d5277-107">Porting IRIS GL Get Functions</span></span>

<span data-ttu-id="d5277-108">Функции "Get" в форме IRI имеют следующий вид:</span><span class="sxs-lookup"><span data-stu-id="d5277-108">IRIS GL "get" functions take the following form:</span></span>

``` syntax
int getthing();
```

<span data-ttu-id="d5277-109">и</span><span class="sxs-lookup"><span data-stu-id="d5277-109">and</span></span>

``` syntax
int getthings( int *a, int *b);
```

<span data-ttu-id="d5277-110">Код в ГК для ДИАФРАГМы, вероятно, включает вызовы функций Get, которые выглядят примерно так:</span><span class="sxs-lookup"><span data-stu-id="d5277-110">Your IRIS GL code probably includes get function calls that look something like:</span></span>

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

<span data-ttu-id="d5277-111">В OpenGL используется один из следующих четырех типов функций [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) вместо эквивалентных функций IRI GL.</span><span class="sxs-lookup"><span data-stu-id="d5277-111">In OpenGL you use one of the following four types of [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) functions in place of equivalent IRIS GL get functions:</span></span>

-   <span data-ttu-id="d5277-112">**глжетбулеанв**</span><span class="sxs-lookup"><span data-stu-id="d5277-112">**glGetBooleanv**</span></span>
-   <span data-ttu-id="d5277-113">**глжетинтежерв**</span><span class="sxs-lookup"><span data-stu-id="d5277-113">**glGetIntegerv**</span></span>
-   <span data-ttu-id="d5277-114">**глжетфлоатв**</span><span class="sxs-lookup"><span data-stu-id="d5277-114">**glGetFloatv**</span></span>
-   <span data-ttu-id="d5277-115">**глжетдаублев**</span><span class="sxs-lookup"><span data-stu-id="d5277-115">**glGetDoublev**</span></span>

<span data-ttu-id="d5277-116">Функции имеют следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="d5277-116">The functions have the following syntax:</span></span>

``` syntax
glGet<Datatype>v( value, *data );
```

<span data-ttu-id="d5277-117">где *значение* имеет тип **гленум** , а данные имеют тип **глдататипе**.</span><span class="sxs-lookup"><span data-stu-id="d5277-117">where *value* is of type **GLenum** and data is of type **GLdatatype**.</span></span> <span data-ttu-id="d5277-118">При вызове **глжет** и возврате типа, отличного от ожидаемого типа, тип преобразуется соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="d5277-118">When you call **glGet** and it returns a type different from the type expected, the type is converted appropriately.</span></span> <span data-ttu-id="d5277-119">Полный список параметров **глжет** см. в разделе [**глжет**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span><span class="sxs-lookup"><span data-stu-id="d5277-119">For a complete list of **glGet** parameters, see [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).</span></span>

 

 




