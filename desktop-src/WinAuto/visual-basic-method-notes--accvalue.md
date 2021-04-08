---
title: Акквалуе примечания метода Visual Basic
description: Файл языка описания объектов (ODL) Олеакк. odl содержит сведения, которые отличаются от реализации C/C++. Файл Олеакк. odl содержит следующее определение версии, которая задает свойство функции.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce93bc5d4ff2a2e01da55e30630fda42c573b7f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067823"
---
# <a name="visual-basic-method-notes-accvalue"></a>Примечания к методу Visual Basic: Акквалуе

Файл языка описания объектов (ODL) Олеакк. odl содержит сведения, которые отличаются от реализации C/C++. Файл Олеакк. odl содержит следующее определение версии, которая задает свойство функции.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Хотя параметр *варчилд* указан как необязательный в ODL-файле и обозревателе объектов, его необходимо включить при вызове версии параметра свойства [**акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




