---
title: Атрибут length_is
description: Атрибут \ size = \_ \ позволяет указать максимальный размер массива.
ms.assetid: 577a1efd-2d16-40d6-99bb-998d81ee2f8c
keywords:
- length_is
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 436559961d815adb417d83de5ffa8c06d8497fa0899644411d252c84d6e34ea0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924263"
---
# <a name="the-length_is-attribute"></a>\[Длина \_ \] атрибута

Атрибут \[ [**size \_ имеет**](/windows/desktop/Midl/size-is) значение, \] позволяя указать максимальный размер массива. Если это единственный атрибут, передаются все элементы массива. Вместо отправки всех элементов массива можно указать передаваемые элементы с помощью \[ атрибута [**length \_ —**](/windows/desktop/Midl/length-is) \] , как показано ниже.

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

Размер описывает выделение, а длина описывает передачу. Число передаваемых элементов должно всегда быть меньше или равно количеству выделенных элементов. Значение, связанное **с \_ length** , всегда меньше или равно **размеру \_**.

 

 