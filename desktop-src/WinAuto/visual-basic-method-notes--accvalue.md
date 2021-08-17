---
title: Visual Basic Заметки о методе Акквалуе
description: Файл языка описания объектов (ODL) Олеакк. odl содержит сведения, которые отличаются от реализации C/C++. Файл Олеакк. odl содержит следующее определение версии, которая задает свойство функции.
ms.assetid: 8c27d63a-ae69-4667-9b65-be743a00b49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f5a79740e71984b4d9beaba9faad23142b2c9afc78a7378e9b11be4dc521
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117744784"
---
# <a name="visual-basic-method-notes-accvalue"></a>Visual Basic Примечания к методу: Акквалуе

Файл языка описания объектов (ODL) Олеакк. odl содержит сведения, которые отличаются от реализации C/C++. Файл Олеакк. odl содержит следующее определение версии, которая задает свойство функции.


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



Хотя параметр *варчилд* указан как необязательный в ODL-файле и обозревателе объектов, его необходимо включить при вызове версии параметра свойства [**акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).

 

 




