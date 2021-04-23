---
title: Инкапсулированные объединения
description: Объединение, содержащее его discriminant в структуре в, является инкапсулированным объединением.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- типы данных MIDL, инкапсулированные объединения
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105681514"
---
# <a name="encapsulated-unions"></a><span data-ttu-id="8c129-104">Инкапсулированные объединения</span><span class="sxs-lookup"><span data-stu-id="8c129-104">Encapsulated Unions</span></span>

<span data-ttu-id="8c129-105">Объединение, содержащее его discriminant в структуре в, является инкапсулированным объединением.</span><span class="sxs-lookup"><span data-stu-id="8c129-105">A union that is contained with its discriminant in a structure within is an encapsulated union.</span></span> <span data-ttu-id="8c129-106">Инкапсулированное объединение обозначается наличием ключевого слова [**switch**](switch.md) .</span><span class="sxs-lookup"><span data-stu-id="8c129-106">The encapsulated union is indicated by the presence of the [**switch**](switch.md) keyword.</span></span> <span data-ttu-id="8c129-107">Этот тип объединения имеет имя, так как компилятор MIDL автоматически инкапсулирует объединение и его discriminant в структуре для передачи во время удаленного вызова процедуры.</span><span class="sxs-lookup"><span data-stu-id="8c129-107">This type of union is so named because the MIDL compiler automatically encapsulates the union and its discriminant in a structure for transmission during a remote procedure call.</span></span>

<span data-ttu-id="8c129-108">Если отсутствует тег Union (тип U1 в приведенном \_ выше примере), компилятор создаст структуру с полем Union с именем *\_ Union с тегами*.</span><span class="sxs-lookup"><span data-stu-id="8c129-108">If the union tag is missing (U1\_TYPE in the example above), the compiler will generate the structure with the union field named *tagged\_union*.</span></span>

<span data-ttu-id="8c129-109">Для обеспечения взаимодействия между платформами все объединения должны быть одинаковыми для разных платформ.</span><span class="sxs-lookup"><span data-stu-id="8c129-109">The shape of unions must be the same across platforms to ensure interconnectivity.</span></span>

<span data-ttu-id="8c129-110">Описание формы инкапсулированного объединения см. в разделе [**Union**](union.md).</span><span class="sxs-lookup"><span data-stu-id="8c129-110">For a description of the form of an encapsulated union, see [**union**](union.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8c129-111">Примеры</span><span class="sxs-lookup"><span data-stu-id="8c129-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

<span data-ttu-id="8c129-112">Дополнительные сведения см. в разделе [базовые типы MIDL](midl-base-types.md), [**char**](char-idl.md), **\[** [**\_ маркер контекста**](context-handle.md) **\]** , [**перечисление**](enum.md), **\[** [**первый \_ —**](first-is.md) **\]** , **\[** [**Handle**](handle.md) **\]** , **\[** [**Ignore**](ignore.md) **\]** , [**int**](int.md), **\[** [**игнорировать**](ignore.md) **\]** , **\[** [**Last \_ —**](last-is.md) **\]** , **\[** [**length \_ —**](length-is.md) **\]** , **\[** [**Max \_ —**](max-is.md) **\]** , **\[** [**MS \_ Union**](ms-union-attrib.md) **\]** , [неинкапсулированные объединения](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md) **\]** , **\[** [**ref**](ref.md) **\]** , **\[** [**размер \_ —**](size-is.md) **\]** , **\[** [**строка**](string.md) **\]** , [**Структура**](struct.md), [**переключатель**](switch.md), **\[** [**параметр \_ —**](switch-is.md) **\]** , **\[** [**\_ тип коммутатора**](switch-type.md), " **\]** **\[** [**передать \_ как**](transmit-as.md) **\]** [](union.md) **\[** [](unique.md) ", "объединить" и "уникальный"**\]**</span><span class="sxs-lookup"><span data-stu-id="8c129-112">For related information, see [MIDL Base Types](midl-base-types.md), [**char**](char-idl.md), **\[**[**context\_handle**](context-handle.md)**\]**, [**enum**](enum.md), **\[**[**first\_is**](first-is.md)**\]**, **\[**[**handle**](handle.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, [**int**](int.md), **\[**[**ignore**](ignore.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**ms\_union**](ms-union-attrib.md)**\]**, [Nonencapsulated Unions](nonencapsulated-unions.md), **\[**[**ptr**](ptr.md)**\]**, **\[**[**ref**](ref.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, **\[**[**string**](string.md)**\]**, [**struct**](struct.md), [**switch**](switch.md), **\[**[**switch\_is**](switch-is.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**, [**union**](union.md), and **\[**[**unique**](unique.md)**\]**</span></span>

 

 




