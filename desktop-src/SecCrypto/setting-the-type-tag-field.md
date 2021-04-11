---
description: Переменные типа VARIANT имеют поле тега типа VT, которое указывает тип данных.
ms.assetid: 3436faf6-2e66-46a1-b1e8-84f513282c16
title: Установка поля тега типа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e443fae33b14bd4270e63188ff96a042a91c8e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104262850"
---
# <a name="setting-the-type-tag-field"></a><span data-ttu-id="ba7d7-103">Установка поля тега типа</span><span class="sxs-lookup"><span data-stu-id="ba7d7-103">Setting the Type Tag Field</span></span>

<span data-ttu-id="ba7d7-104">Переменные типа **Variant** имеют поле тега типа **VT** , которое указывает тип данных.</span><span class="sxs-lookup"><span data-stu-id="ba7d7-104">**VARIANT** type variables have a type tag field **vt** that indicates the data type of the data.</span></span> <span data-ttu-id="ba7d7-105">Возвращаемые значения типа **Variant** возвращаются методам с полем тега типа, для которого задан тип данных возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="ba7d7-105">**VARIANT** type return values are returned by methods with the type tag field set to the data type of the return value.</span></span> <span data-ttu-id="ba7d7-106">Входные параметры типа **Variant** в вызове метода должны иметь поле тега типа, установленное приложением, на одно из поддерживаемых значений.</span><span class="sxs-lookup"><span data-stu-id="ba7d7-106">**VARIANT** type input parameters in a method call must have the type tag field set by the application to one of the supported values.</span></span> <span data-ttu-id="ba7d7-107">Соответствие типов параметров типам данных выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="ba7d7-107">The correspondence of parameter types to data types is as follows.</span></span>



| <span data-ttu-id="ba7d7-108">Тип параметра</span><span class="sxs-lookup"><span data-stu-id="ba7d7-108">Parameter type</span></span>              | <span data-ttu-id="ba7d7-109">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ba7d7-109">Data type</span></span>                                      |
|-----------------------------|------------------------------------------------|
| <span data-ttu-id="ba7d7-110">ПРОПТИПЕ \_ Long</span><span class="sxs-lookup"><span data-stu-id="ba7d7-110">PROPTYPE\_LONG</span></span><br/>   | <span data-ttu-id="ba7d7-111">VT \_ I2 или VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ba7d7-111">VT\_I2 or VT\_I4</span></span><br/>                    |
| <span data-ttu-id="ba7d7-112">\_Дата проптипе</span><span class="sxs-lookup"><span data-stu-id="ba7d7-112">PROPTYPE\_DATE</span></span><br/>   | <span data-ttu-id="ba7d7-113">\_Дата VT</span><span class="sxs-lookup"><span data-stu-id="ba7d7-113">VT\_DATE</span></span><br/>                            |
| <span data-ttu-id="ba7d7-114">\_двоичный файл проптипе</span><span class="sxs-lookup"><span data-stu-id="ba7d7-114">PROPTYPE\_BINARY</span></span><br/> | <span data-ttu-id="ba7d7-115">VT \_ BSTR или (VT \_ BSTR \| VT \_ ByRef)</span><span class="sxs-lookup"><span data-stu-id="ba7d7-115">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |
| <span data-ttu-id="ba7d7-116">\_строка проптипе</span><span class="sxs-lookup"><span data-stu-id="ba7d7-116">PROPTYPE\_STRING</span></span><br/> | <span data-ttu-id="ba7d7-117">VT \_ BSTR или (VT \_ BSTR \| VT \_ ByRef)</span><span class="sxs-lookup"><span data-stu-id="ba7d7-117">VT\_BSTR or (VT\_BSTR \| VT\_BYREF)</span></span><br/> |



 

<span data-ttu-id="ba7d7-118">В следующем примере показано, как инициализировать типы данных Variant, перечисленные выше.</span><span class="sxs-lookup"><span data-stu-id="ba7d7-118">The following example shows how to initialize the variant data types listed above.</span></span>


```C++
HRESULT hr;
VARIANT vEMail;
VARIANT vNotBefore;
VARIANT vCount;
VARIANT vByRef;
BSTR bstr = NULL;
SYSTEMTIME st;

//Set the BSTR variant data type.
VariantInit(&vEMail);
vEMail.vt = VT_BSTR;   
vEMail.bstrVal = SysAllocString(L"someone@example.com");
if (NULL == vEMail.bstrVal)
{
    hr = E_OUTOFMEMORY;
    //Handle error.   
}
//Use the variant.
VariantClear(&vEMail);  //when done


//Set the BSTR|BYREF variant data type.
VariantInit(&vByRef);
vByRef.vt = VT_BSTR | VT_BYREF;   
vByRef.pbstrVal = &bstr;
//Use the variant.
VariantClear(&vByRef);  //when done
SysFreeString(bstr);


//Set the DATE variant data type.
memset(&st, 0, sizeof(SYSTEMTIME));
st.wYear = 2000;
st.wMonth = 1;
st.wDay = 1;
st.wHour = 12;

VariantInit(&vNotBefore);
vNotBefore.vt = VT_DATE;
if (!SystemTimeToVariantTime(&st, &vNotBefore.date))
{
    hr = E_FAIL;
    //Handle error.
}
//Use the variant.
VariantClear(&vNotBefore);  //when done


//Set the LONG variant data type.
VariantInit(&vCount);
vCount.vt = VT_I4;
vCount.long = 123456;
//Use the variant.
VariantClear(&vCount);  //when done
```



 

 




