---
description: Некоторые свойства и поля данных содержат массивы данных.
ms.assetid: 85e3b953-be36-4d60-b04e-4f572d0b9564
title: Получение типов векторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4945b45e4e78b6c4f9f9e0fb4b3848f813549105
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540895"
---
# <a name="retrieving-vector-types"></a><span data-ttu-id="f85b1-103">Получение типов векторов</span><span class="sxs-lookup"><span data-stu-id="f85b1-103">Retrieving Vector Types</span></span>

<span data-ttu-id="f85b1-104">Некоторые свойства и поля данных содержат массивы данных.</span><span class="sxs-lookup"><span data-stu-id="f85b1-104">Some properties and data fields contain arrays of information.</span></span> <span data-ttu-id="f85b1-105">Например, \_ \_ свойство "Кривое" светлого ответа Свойства датчика \_ \_ содержит массив из 4-байтных целых чисел без знака.</span><span class="sxs-lookup"><span data-stu-id="f85b1-105">For example, the SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE property contains an array of 4-byte unsigned integers.</span></span> <span data-ttu-id="f85b1-106">Однако при получении таких массивов через API датчика они всегда представляются как тип VT \_ vector \| UI1, массив однобайтовых символов, независимо от фактического типа данных в массиве.</span><span class="sxs-lookup"><span data-stu-id="f85b1-106">However, when you receive such arrays through the Sensor API, they are always represented as type VT\_VECTOR\|UI1, an array of single-byte characters, regardless of the actual type of the data in the array.</span></span> <span data-ttu-id="f85b1-107">Для этих типов необходимо соблюдать осторожность при приведении переменных массива к правильному типу данных для свойства или поля данных.</span><span class="sxs-lookup"><span data-stu-id="f85b1-107">For these types, you must be careful to cast array variables to the correct data type for the property or data field.</span></span>

<span data-ttu-id="f85b1-108">Сведения о свойствах, полях данных и их типах см. в разделе [константы](constants.md).</span><span class="sxs-lookup"><span data-stu-id="f85b1-108">For information about properties, data fields, and their types, see [Constants](constants.md).</span></span>

<span data-ttu-id="f85b1-109">В следующем примере кода показано, как выполнить приведение данных, полученных \_ с \_ помощью кривой светлого ответа Свойства датчика, \_ \_ к правильному типу.</span><span class="sxs-lookup"><span data-stu-id="f85b1-109">The following example code shows how to cast the data retrieved in SENSOR\_PROPERTY\_LIGHT\_RESPONSE\_CURVE to the correct type.</span></span>


```C++
PROPVARIANT pvCurve;
PropVariantInit(&pvCurve);

// Retrieve the property value.
hr = pSensor->GetProperty(SENSOR_PROPERTY_LIGHT_RESPONSE_CURVE, &pvCurve);
if (SUCCEEDED(hr))
{
    if ((VT_UI1|VT_VECTOR) == V_VT(pvCurve)) // Note actual type of UI1
    {
        // Cast the array to UINT, a 4-byte unsigned integer.

        // Item count for the array.
        UINT  cElement = pvCurve.caub.cElems/sizeof(UINT);
        // Array pointer.
        UINT* pElement = (UINT*)(pvCurve.caub.pElems);

        // Use the array.
    }
}

// Remember to free the PROPVARIANT when done.
PropVariantClear(&pvCurve);
```



 

 



