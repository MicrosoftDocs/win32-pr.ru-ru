---
title: Атрибут length_is
description: Атрибут \ size = \_ \ позволяет указать максимальный размер массива.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f49ad63b2546d39dcc00d251f39143b7eec354c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793494"
---
# <a name="the-length_is-attribute"></a><span data-ttu-id="00abf-104">\[Длина \_ \] атрибута</span><span class="sxs-lookup"><span data-stu-id="00abf-104">The \[length\_is\] Attribute</span></span>

<span data-ttu-id="00abf-105">Атрибут \[ [**size \_ имеет**](/windows/desktop/Midl/size-is) значение, \] позволяя указать максимальный размер массива.</span><span class="sxs-lookup"><span data-stu-id="00abf-105">The \[[**size\_is**](/windows/desktop/Midl/size-is)\] attribute lets you specify the maximum size of the array.</span></span> <span data-ttu-id="00abf-106">Если это единственный атрибут, передаются все элементы массива.</span><span class="sxs-lookup"><span data-stu-id="00abf-106">When this is the only attribute, all elements of the array are transmitted.</span></span> <span data-ttu-id="00abf-107">Вместо отправки всех элементов массива можно указать передаваемые элементы с помощью \[ атрибута [**length \_ —**](/windows/desktop/Midl/length-is) \] , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="00abf-107">Instead of sending all elements of the array, you can specify the transmitted elements using the \[[**length\_is**](/windows/desktop/Midl/length-is)\] attribute, as follows:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(3.0)
]
interface arraytest
{
  void fArray3([in] short sSize,
               [in] short sLength
               [in, out, size_is(sSize), 
                 length_is(sLength)] char achArray[*]);
}
```

<span data-ttu-id="00abf-108">Размер описывает выделение, а длина описывает передачу.</span><span class="sxs-lookup"><span data-stu-id="00abf-108">Size describes allocation while length describes transmission.</span></span> <span data-ttu-id="00abf-109">Число передаваемых элементов должно всегда быть меньше или равно количеству выделенных элементов.</span><span class="sxs-lookup"><span data-stu-id="00abf-109">The number of elements transmitted must always be less than or equal to the number of elements allocated.</span></span> <span data-ttu-id="00abf-110">Значение, связанное **с \_ length** , всегда меньше или равно **размеру \_**.</span><span class="sxs-lookup"><span data-stu-id="00abf-110">The value associated with **length\_is** is always less than or equal to **size\_is**.</span></span>

 

 