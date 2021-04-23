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
# <a name="visual-basic-method-notes-accname"></a><span data-ttu-id="20ba9-103">Примечания к методу Visual Basic: Аккнаме</span><span class="sxs-lookup"><span data-stu-id="20ba9-103">Visual Basic Method Notes: accName</span></span>

<span data-ttu-id="20ba9-104">Файл языка описания объектов (ODL) Олеакк. odl содержит сведения, которые отличаются от реализации C/C++.</span><span class="sxs-lookup"><span data-stu-id="20ba9-104">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="20ba9-105">Файл Олеакк. odl содержит следующее определение версии, которая задает свойство функции:</span><span class="sxs-lookup"><span data-stu-id="20ba9-105">The file Oleacc.odl contains the following definition for the version that sets the property of the function:</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_NAME)]
    HRESULT accName(
        [in, optional] VARIANT varChild,
        [in] BSTR szName);
```



<span data-ttu-id="20ba9-106">Хотя параметр *варчилд* указан как необязательный в ODL-файле и обозревателе объектов, его необходимо включить при вызове версии параметра свойства [**аккнаме**](https://www.bing.com/search?q=**accName**).</span><span class="sxs-lookup"><span data-stu-id="20ba9-106">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accName**](https://www.bing.com/search?q=**accName**).</span></span>

 

 




