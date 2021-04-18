---
title: Объединение атрибутов массива
description: Атрибуты полей можно указывать в различных сочетаниях, если заглушка может использовать эти сведения для определения размера массива и числа байтов для передачи на сервер.
ms.assetid: ff4f971f-9e46-4454-9d57-d8ebdf70b261
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffc60777caeb3950e37fe167fe09ecc181d88b8f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "105672364"
---
# <a name="combining-array-attributes"></a><span data-ttu-id="fc215-103">Объединение атрибутов массива</span><span class="sxs-lookup"><span data-stu-id="fc215-103">Combining Array Attributes</span></span>

<span data-ttu-id="fc215-104">Атрибуты полей можно указывать в различных сочетаниях, если заглушка может использовать эти сведения для определения размера массива и числа байтов для передачи на сервер.</span><span class="sxs-lookup"><span data-stu-id="fc215-104">Field attributes can be supplied in various combinations as long as the stub can use the information to determine the size of the array and the number of bytes to transmit to the server.</span></span> <span data-ttu-id="fc215-105">Связи между атрибутами определяются с помощью следующих формул:</span><span class="sxs-lookup"><span data-stu-id="fc215-105">The relationships between the attributes are defined using the following formulas:</span></span>

``` syntax
size_is = max_is + 1;
length_is = last_is - first_is + 1;
```

<span data-ttu-id="fc215-106">Значения, связанные с атрибутами, должны соблюдать несколько общих правил, основанных на этих формулах.</span><span class="sxs-lookup"><span data-stu-id="fc215-106">The values associated with the attributes must obey several common-sense rules based on those formulas.</span></span> <span data-ttu-id="fc215-107">В эти правила входит следующее:</span><span class="sxs-lookup"><span data-stu-id="fc215-107">These rules are:</span></span>

-   <span data-ttu-id="fc215-108">Не указывайте первый параметр \[ [**\_ —**](/windows/desktop/Midl/first-is) \] значение индекса меньше нуля, а \[ [**Последнее \_ —**](/windows/desktop/Midl/last-is) \] значение больше \[ [**максимального \_**](/windows/desktop/Midl/max-is) \] .</span><span class="sxs-lookup"><span data-stu-id="fc215-108">Do not specify a \[[**first\_is**](/windows/desktop/Midl/first-is)\] index value smaller than zero or a \[[**last\_is**](/windows/desktop/Midl/last-is)\] value greater than \[[**max\_is**](/windows/desktop/Midl/max-is)\].</span></span>
-   <span data-ttu-id="fc215-109">Не указывайте отрицательный размер для массива.</span><span class="sxs-lookup"><span data-stu-id="fc215-109">Do not specify a negative size for an array.</span></span> <span data-ttu-id="fc215-110">Определите первый и последний элементы таким образом, чтобы они выводили нулевое или большее значение длины.</span><span class="sxs-lookup"><span data-stu-id="fc215-110">Define the first and last elements so that they result in a length value of zero or greater.</span></span> <span data-ttu-id="fc215-111">Определите \[ [**Максимальное \_**](/windows/desktop/Midl/max-is) \] значение, чтобы размер был нулевым или большим.</span><span class="sxs-lookup"><span data-stu-id="fc215-111">Define the \[[**max\_is**](/windows/desktop/Midl/max-is)\] value so that the size is zero or greater.</span></span> <span data-ttu-id="fc215-112">Если MIDL вызывался с параметром CHECK [**/Error**](/windows/desktop/Midl/-error) boundss \_ , то заглушка вызывает исключение, если размер меньше нуля, или передаваемая длина меньше нуля.</span><span class="sxs-lookup"><span data-stu-id="fc215-112">If MIDL was invoked with the [**/error**](/windows/desktop/Midl/-error) bounds\_check option, then the stub raises an exception when the size is less than zero, or the transmitted length is less than zero.</span></span>
-   <span data-ttu-id="fc215-113">Не используйте \[ атрибуты [**length \_**](/windows/desktop/Midl/length-is) \] и \[ [**Last \_ —**](/windows/desktop/Midl/last-is) \] одновременно, а \[ атрибуты **size \_** \] и \[ **Last \_ —** \] одновременно.</span><span class="sxs-lookup"><span data-stu-id="fc215-113">Do not use the \[[**length\_is**](/windows/desktop/Midl/length-is)\] and \[[**last\_is**](/windows/desktop/Midl/last-is)\] attributes at the same time, nor the \[**size\_is**\] and \[**last\_is**\] attributes at the same time.</span></span>

<span data-ttu-id="fc215-114">Из-за замкнутой связи в C между массивами и указателями MIDL также позволяет объявлять массивы в списках параметров с помощью нотации указателя.</span><span class="sxs-lookup"><span data-stu-id="fc215-114">Because of the close relationship in C between arrays and pointers, MIDL also lets you declare arrays in parameter lists using pointer notation.</span></span> <span data-ttu-id="fc215-115">MIDL обрабатывает параметр, который является указателем на тип, в виде массива этого типа, если параметр имеет какие-либо атрибуты, обычно связанные с массивами.</span><span class="sxs-lookup"><span data-stu-id="fc215-115">MIDL treats a parameter that is a pointer to a type as an array of that type if the parameter has any of the attributes commonly associated with arrays.</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45)
  version(6.0) 
]
interface arraytest
{
  void fArray6([in] short sSize, 
               [in, out, size_is(sSize)] char * p1);
  void fArray7([in] short sSize, 
               [in, out, size_is(sSize)] char achArray[]);
}
```

<span data-ttu-id="fc215-116">В предыдущем примере параметры массива и указателя в функциях fArray6 и fArray7 эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="fc215-116">In the preceding example, the array and pointer parameters in the functions fArray6 and fArray7 are equivalent.</span></span>

 

 