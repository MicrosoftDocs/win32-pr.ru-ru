---
description: Объекты данных содержат фактические данные или ссылку на эти данные. Каждый объект данных имеет соответствующий шаблон, указывающий тип данных. В следующих разделах описывается форма и части объектов данных.
ms.assetid: 61dbe241-2658-4dd0-af89-3db204b56fad
title: Данные (формат файла X, кодировка текста)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1af117a0207ce804ccacd397bb990fe5f43c94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104422966"
---
# <a name="data-x-file-format-text-encoding"></a><span data-ttu-id="b0e0f-105">Данные (формат файла X, кодировка текста)</span><span class="sxs-lookup"><span data-stu-id="b0e0f-105">Data (X file format, text encoding)</span></span>

<span data-ttu-id="b0e0f-106">Объекты данных содержат фактические данные или ссылку на эти данные.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-106">Data objects contain the actual data or a reference to that data.</span></span> <span data-ttu-id="b0e0f-107">Каждый объект данных имеет соответствующий шаблон, указывающий тип данных.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-107">Each data object has a corresponding template that specifies the data type.</span></span> <span data-ttu-id="b0e0f-108">В следующих разделах описывается форма и части объектов данных.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-108">The following sections discuss the form and parts of data objects.</span></span>

## <a name="form-identifier-and-name"></a><span data-ttu-id="b0e0f-109">Форма, идентификатор и имя</span><span class="sxs-lookup"><span data-stu-id="b0e0f-109">Form, Identifier, and Name</span></span>

<span data-ttu-id="b0e0f-110">Объекты данных имеют следующую форму.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-110">Data objects have the following form.</span></span>


```
        <Identifier> [name] { [<UUID>]
    <member 1>;
...
    <member n>;
}
```



<span data-ttu-id="b0e0f-111">Идентификатор является принудительным и должен соответствовать ранее определенному типу данных или примитиву.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-111">The identifier is compulsory and must match a previously defined data type or primitive.</span></span> <span data-ttu-id="b0e0f-112">Однако имя является необязательным.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-112">However, the name is optional.</span></span>

## <a name="data-members"></a><span data-ttu-id="b0e0f-113">Элементы данных</span><span class="sxs-lookup"><span data-stu-id="b0e0f-113">Data Members</span></span>

<span data-ttu-id="b0e0f-114">Элементы данных могут иметь одно из следующих значений: объект данных, ссылка на данные, список целых чисел, список с плавающей запятой или список строк.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-114">Data members can be one of the following: data object, data reference, integer list, float list, or string list.</span></span>

<span data-ttu-id="b0e0f-115">Объект данных — это вложенный объект данных.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-115">A data object is a nested data object.</span></span> <span data-ttu-id="b0e0f-116">Это позволяет выражать иерархическую природу формата файла.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-116">This enables the hierarchical nature of the file format to be expressed.</span></span> <span data-ttu-id="b0e0f-117">Типы вложенных объектов данных, разрешенных в иерархии, могут быть ограничены.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-117">The types of nested data objects allowed in the hierarchy may be restricted.</span></span>

<span data-ttu-id="b0e0f-118">Ссылка на данные — это ссылка на ранее обнаруженный объект данных, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-118">A data reference is a reference to a previously encountered data object as shown in the following example.</span></span>


```
{
  name |
  UUID |
  name UUID
}
```



<span data-ttu-id="b0e0f-119">Целочисленный список представляет собой разделенный точками с запятой список целых чисел, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-119">An integer list is a semicolon-separated list of integers, as shown in the following example.</span></span>


```
1; 2; 3;
```



<span data-ttu-id="b0e0f-120">Список float — это разделенный точками с запятой список элементов float, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-120">A float list is a semicolon-separated list of floats, as shown in the following example.</span></span>


```
1.0; 2.0; 3.0;
```



<span data-ttu-id="b0e0f-121">Список строк представляет собой разделенный точками с запятой список строк, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="b0e0f-121">A string list is a semicolon-separated list of strings, as shown in the following example.</span></span>


```
"Moose"; "Goats"; "Sheep";
```



## <a name="related-topics"></a><span data-ttu-id="b0e0f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="b0e0f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b0e0f-123">Кодировка текста</span><span class="sxs-lookup"><span data-stu-id="b0e0f-123">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



