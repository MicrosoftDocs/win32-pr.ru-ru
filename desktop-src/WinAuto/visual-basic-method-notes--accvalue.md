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
# <a name="visual-basic-method-notes-accvalue"></a><span data-ttu-id="05010-104">Примечания к методу Visual Basic: Акквалуе</span><span class="sxs-lookup"><span data-stu-id="05010-104">Visual Basic Method Notes: accValue</span></span>

<span data-ttu-id="05010-105">Файл языка описания объектов (ODL) Олеакк. odl содержит сведения, которые отличаются от реализации C/C++.</span><span class="sxs-lookup"><span data-stu-id="05010-105">The Object Description Language (ODL) file, Oleacc.odl, contains information that differs from the C/C++ implementation.</span></span> <span data-ttu-id="05010-106">Файл Олеакк. odl содержит следующее определение версии, которая задает свойство функции.</span><span class="sxs-lookup"><span data-stu-id="05010-106">The file Oleacc.odl contains the following definition for the version that sets the property of the function.</span></span>


```C++
    [hidden, propput, id(DISPID_ACC_VALUE)]
    HRESULT accValue(
        [in, optional] VARIANT varChild,
        [in] BSTR szValue);
```



<span data-ttu-id="05010-107">Хотя параметр *варчилд* указан как необязательный в ODL-файле и обозревателе объектов, его необходимо включить при вызове версии параметра свойства [**акквалуе**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span><span class="sxs-lookup"><span data-stu-id="05010-107">Although the *varChild* parameter is listed as optional in the ODL file and the object browser, you must include it when calling the property-setting version of [**accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-put_accvalue).</span></span>

 

 




