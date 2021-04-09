---
title: Аккнаме примечания метода Visual Basic
description: Файл языка описания объектов (ODL) Олеакк. odl содержит сведения, которые отличаются от реализации C/C++.
ms.assetid: f7960acd-cb1a-4c34-a392-0243155a100f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c404c093fc3b92b4d653b0b1258c62918af8e25
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103888484"
---
# <a name="visual-basic-method-notes-accname"></a>Примечания к методу Visual Basic: Аккнаме

Файл языка описания объектов (ODL) Олеакк. odl содержит сведения, которые отличаются от реализации C/C++. Файл Олеакк. odl содержит следующее определение версии, которая задает свойство функции:


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



Хотя параметр *варчилд* указан как необязательный в ODL-файле и обозревателе объектов, его необходимо включить при вызове версии параметра свойства [**аккнаме**](https://www.bing.com/search?q=**accName**).

 

 




