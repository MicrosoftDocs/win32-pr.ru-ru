---
title: Доступ к атрибутам с помощью ADSI
description: Для извлечения значений именованных атрибутов используются методы IADs. Get и IADs. Жетекс.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Атрибуты, доступ с помощью ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ee6990483b45e335bb6b830cef85e482f30e00
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654352"
---
# <a name="accessing-attributes-with-adsi"></a><span data-ttu-id="ed2da-104">Доступ к атрибутам с помощью ADSI</span><span class="sxs-lookup"><span data-stu-id="ed2da-104">Accessing Attributes with ADSI</span></span>

<span data-ttu-id="ed2da-105">Для извлечения значений именованных атрибутов используются методы [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) .</span><span class="sxs-lookup"><span data-stu-id="ed2da-105">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods are used to retrieve named attribute values.</span></span> <span data-ttu-id="ed2da-106">Оба метода возвращают значение [**типа Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="ed2da-106">Both methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) value.</span></span> <span data-ttu-id="ed2da-107">Эти методы доступны только для каталогов, поддерживающих схему.</span><span class="sxs-lookup"><span data-stu-id="ed2da-107">These methods are available only for directories that support a schema.</span></span> <span data-ttu-id="ed2da-108">При доступе к объектам в каталоге без схемы для управления значениями атрибутов необходимо использовать интерфейсы [**иадспропертентри**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) и [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) .</span><span class="sxs-lookup"><span data-stu-id="ed2da-108">When accessing objects in a directory without a schema, the [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) and [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) interfaces must be used to manipulate attribute values.</span></span>

<span data-ttu-id="ed2da-109">Методы [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. Жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) возвращают [**вариант**](/windows/win32/api/oaidl/ns-oaidl-variant) , который может или не может быть массивом **вариантов** в зависимости от числа возвращаемых сервером значений.</span><span class="sxs-lookup"><span data-stu-id="ed2da-109">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods return a [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) which may, or may not, be a **VARIANT** array depending on the number of values returned by the server.</span></span> <span data-ttu-id="ed2da-110">Например, если на сервере возвращается только одно значение, независимо от того, является ли он одним или несколькими значениями, метод возвращает один **вариант**.</span><span class="sxs-lookup"><span data-stu-id="ed2da-110">For example, if only one value is returned from the server, regardless of whether it is a single or multi-valued attribute, the method returns a single **VARIANT**.</span></span> <span data-ttu-id="ed2da-111">И наоборот, если возвращается несколько значений, возвращается массив **Variant** .</span><span class="sxs-lookup"><span data-stu-id="ed2da-111">Conversely, if multiple values are returned, a **VARIANT** array is returned.</span></span> <span data-ttu-id="ed2da-112">Если возвращается массив **Variant** , элемент **VT** в структуре **Variant** содержит флаги **VT \_ Variant/вбвариант** и **VT \_ Array/VBArray** .</span><span class="sxs-lookup"><span data-stu-id="ed2da-112">If a **VARIANT** array is returned, the **vt** member of the **VARIANT** structure contains the **VT\_VARIANT/vbVariant** and **VT\_ARRAY/vbArray** flags.</span></span>

<span data-ttu-id="ed2da-113">Методы [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) также могут возвращать COM-объект с помощью интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ed2da-113">The [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods can also return a COM object using the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ed2da-114">В этом случае элемент **VT** в структуре [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) содержит флаг **\_ диспетчеризации Dispatch/вбобжект** .</span><span class="sxs-lookup"><span data-stu-id="ed2da-114">In this case, the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure contains the **VT\_DISPATCH/vbObject** flag.</span></span> <span data-ttu-id="ed2da-115">Для доступа к COM-объекту вызовите метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в интерфейсе **IDispatch** , чтобы получить нужный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ed2da-115">To access the COM object, call the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method on the **IDispatch** interface to obtain the desired interface.</span></span>

<span data-ttu-id="ed2da-116">Другим типом данных, возвращаемым методами [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) , являются двоичные данные.</span><span class="sxs-lookup"><span data-stu-id="ed2da-116">Another data type returned by the [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) methods is binary data.</span></span> <span data-ttu-id="ed2da-117">В этом случае данные передаются в виде непрерывного массива байтов, а элемент **VT** структуры [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) будет содержать флаги **VT \_ UI1/вббите** и **VT \_ Array/VBArray** .</span><span class="sxs-lookup"><span data-stu-id="ed2da-117">In this case, the data is supplied as a contiguous array of bytes and the **vt** member of the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structure will contain the **VT\_UI1/vbByte** and **VT\_ARRAY/vbArray** flags.</span></span>

> [!Note]  
> <span data-ttu-id="ed2da-118">Microsoft Visual Basic, Scripting Edition поддерживает только массивы [**типа Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) и **Variant** .</span><span class="sxs-lookup"><span data-stu-id="ed2da-118">Microsoft Visual Basic, Scripting Edition only supports [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) and **VARIANT** arrays.</span></span> <span data-ttu-id="ed2da-119">По этой причине VBScript нельзя использовать для считывания значений двоичных свойств.</span><span class="sxs-lookup"><span data-stu-id="ed2da-119">Because of this, VBScript cannot be used to read binary property values.</span></span>

 

<span data-ttu-id="ed2da-120">Многие интерфейсы ADSI определяют свойства, зависящие от интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ed2da-120">Many ADSI interfaces define interface-specific properties.</span></span> <span data-ttu-id="ed2da-121">Например, интерфейс [**иадскомпутер**](/windows/desktop/api/Iads/nn-iads-iadscomputer) определяет свойство [**Location**](iadscomputer-property-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="ed2da-121">For example, the [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer) interface defines the [**Location**](iadscomputer-property-methods.md) property.</span></span> <span data-ttu-id="ed2da-122">Эти определяемые интерфейсом свойства могут содержать данные, идентичные одному из именованных атрибутов, но свойства относятся к типу объекта, на который ссылается интерфейс.</span><span class="sxs-lookup"><span data-stu-id="ed2da-122">These interface-defined properties may contain data that is identical to one of the named attributes, but the properties are specific to the type of object the interface refers to.</span></span> <span data-ttu-id="ed2da-123">В языках, поддерживающих автоматизацию, доступ к этим определенным интерфейсам свойств можно получить с помощью точечной нотации, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="ed2da-123">In languages that support automation, these interface-defined properties can be accessed using the dot notation as shown in the following code example.</span></span>

## <a name="examples"></a><span data-ttu-id="ed2da-124">Примеры</span><span class="sxs-lookup"><span data-stu-id="ed2da-124">Examples</span></span>

<span data-ttu-id="ed2da-125">В следующем примере кода показано, как получить доступ к свойству ADsPath в интерфейсе IADs.</span><span class="sxs-lookup"><span data-stu-id="ed2da-125">The following code example shows how to access the ADsPath property on the IADs interface.</span></span>


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



<span data-ttu-id="ed2da-126">В языках, не относящихся к автоматизации, для доступа к свойствам, определяемым интерфейсом, необходимо использовать методы доступа к свойствам.</span><span class="sxs-lookup"><span data-stu-id="ed2da-126">In non-automation languages, the property access methods must be used to access the interface-defined properties.</span></span> <span data-ttu-id="ed2da-127">Например, метод [**иадскомпутер:: Get \_ Location**](iadscomputer-property-methods.md) используется для получения свойства **иадскомпутер. Location** .</span><span class="sxs-lookup"><span data-stu-id="ed2da-127">For example, the [**IADsComputer::get\_Location**](iadscomputer-property-methods.md) method is used to retrieve the **IADsComputer.Location** property.</span></span>

<span data-ttu-id="ed2da-128">В следующем примере кода C++ показано, как использовать метод доступа к свойству в C++ для получения значения ADsPath пользователя.</span><span class="sxs-lookup"><span data-stu-id="ed2da-128">The following C++ code example demonstrates how to use the property access method in C++ to retrieve the ADsPath of a user.</span></span>


```C++
HRESULT hr;
IADs *pUser; 
 
// Bind to user object.
hr = ADsGetObject(
     L"LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com", 
     IID_IADs, 
     (void**)&pUser);
if(SUCCEEDED(hr)) 
{
    BSTR bstrName;

    // Get property.
    hr = pUser->get_Name(&bstrName);
    if(SUCCEEDED(hr)) 
    {
        wprintf(bstrName);
 
        SysFreeString(bstrName);
    }

    pUser->Release();
}
```



<span data-ttu-id="ed2da-129">Дополнительные сведения о доступе к атрибутам с помощью ADSI см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="ed2da-129">For more information about accessing attributes with ADSI, see:</span></span>

-   [<span data-ttu-id="ed2da-130">Метод Get</span><span class="sxs-lookup"><span data-stu-id="ed2da-130">The Get Method</span></span>](the-get-method.md)
-   [<span data-ttu-id="ed2da-131">Метод Жетекс</span><span class="sxs-lookup"><span data-stu-id="ed2da-131">The GetEx Method</span></span>](the-getex-method.md)
-   [<span data-ttu-id="ed2da-132">Метод info</span><span class="sxs-lookup"><span data-stu-id="ed2da-132">The GetInfo Method</span></span>](the-getinfo-method.md)
-   [<span data-ttu-id="ed2da-133">Оптимизация с помощью Жетинфоекс</span><span class="sxs-lookup"><span data-stu-id="ed2da-133">Optimization Using GetInfoEx</span></span>](optimization-using-getinfoex.md)
-   [<span data-ttu-id="ed2da-134">Доступ к атрибутам с помощью интерфейса Идиректорйобжект</span><span class="sxs-lookup"><span data-stu-id="ed2da-134">Accessing Attributes with the IDirectoryObject Interface</span></span>](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [<span data-ttu-id="ed2da-135">Пример кода для чтения атрибутов</span><span class="sxs-lookup"><span data-stu-id="ed2da-135">Example Code for Reading Attributes</span></span>](example-code-for-reading-attributes.md)

 

 