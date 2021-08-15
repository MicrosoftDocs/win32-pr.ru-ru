---
title: Доступ к атрибутам с помощью ADSI
description: Для извлечения значений именованных атрибутов используются методы IADs. Get и IADs. Жетекс.
ms.assetid: 8aa139e1-6b20-4745-92f1-d2f352071f33
ms.tgt_platform: multiple
keywords:
- Атрибуты, доступ с помощью ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e37c63b61986a56e7b22f114b5956d9e047f1ae45b5dc2e653074ea35440f10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024132"
---
# <a name="accessing-attributes-with-adsi"></a>Доступ к атрибутам с помощью ADSI

Для извлечения значений именованных атрибутов используются методы [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) . Оба метода возвращают значение [**типа Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . Эти методы доступны только для каталогов, поддерживающих схему. При доступе к объектам в каталоге без схемы для управления значениями атрибутов необходимо использовать интерфейсы [**иадспропертентри**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) и [**иадспропертивалуе**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) .

Методы [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. Жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) возвращают [**вариант**](/windows/win32/api/oaidl/ns-oaidl-variant) , который может или не может быть массивом **вариантов** в зависимости от числа возвращаемых сервером значений. Например, если на сервере возвращается только одно значение, независимо от того, является ли он одним или несколькими значениями, метод возвращает один **вариант**. И наоборот, если возвращается несколько значений, возвращается массив **Variant** . Если возвращается массив **Variant** , элемент **VT** в структуре **Variant** содержит флаги **VT \_ Variant/вбвариант** и **VT \_ Array/VBArray** .

Методы [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) также могут возвращать COM-объект с помощью интерфейса [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . В этом случае элемент **VT** в структуре [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) содержит флаг **\_ диспетчеризации Dispatch/вбобжект** . Для доступа к COM-объекту вызовите метод [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) в интерфейсе **IDispatch** , чтобы получить нужный интерфейс.

Другим типом данных, возвращаемым методами [**iAds. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) и [**iAds. жетекс**](/windows/desktop/api/Iads/nf-iads-iads-getex) , являются двоичные данные. В этом случае данные передаются в виде непрерывного массива байтов, а элемент **VT** структуры [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) будет содержать флаги **VT \_ UI1/вббите** и **VT \_ Array/VBArray** .

> [!Note]  
> Microsoft Visual Basic, scripting Edition поддерживает только массивы [**типа variant**](/windows/win32/api/oaidl/ns-oaidl-variant) и **variant** . По этой причине VBScript нельзя использовать для считывания значений двоичных свойств.

 

Многие интерфейсы ADSI определяют свойства, зависящие от интерфейса. Например, интерфейс [**иадскомпутер**](/windows/desktop/api/Iads/nn-iads-iadscomputer) определяет свойство [**Location**](iadscomputer-property-methods.md) . Эти определяемые интерфейсом свойства могут содержать данные, идентичные одному из именованных атрибутов, но свойства относятся к типу объекта, на который ссылается интерфейс. В языках, поддерживающих автоматизацию, доступ к этим определенным интерфейсам свойств можно получить с помощью точечной нотации, как показано в следующем примере кода.

## <a name="examples"></a>Примеры

В следующем примере кода показано, как получить доступ к свойству ADsPath в интерфейсе IADs.


```VB
Dim oUser as IADs
Dim Path as String
 
' Bind to a specific user object.
set oUser = GetObject(
            "LDAP://CN=Jeff Smith,CN=Users,DC=fabrikam,DC=com")
 
' Get property.
Path = MyUser.ADsPath
```



В языках, не относящихся к автоматизации, для доступа к свойствам, определяемым интерфейсом, необходимо использовать методы доступа к свойствам. Например, метод [**иадскомпутер:: Get \_ Location**](iadscomputer-property-methods.md) используется для получения свойства **иадскомпутер. Location** .

В следующем примере кода C++ показано, как использовать метод доступа к свойству в C++ для получения значения ADsPath пользователя.


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



Дополнительные сведения о доступе к атрибутам с помощью ADSI см. в следующих статьях:

-   [Метод Get](the-get-method.md)
-   [Метод Жетекс](the-getex-method.md)
-   [Метод info](the-getinfo-method.md)
-   [Оптимизация с помощью Жетинфоекс](optimization-using-getinfoex.md)
-   [Доступ к атрибутам с помощью интерфейса Идиректорйобжект](accessing-attributes-with-the-idirectoryobject-interface.md)
-   [Пример кода для чтения атрибутов](example-code-for-reading-attributes.md)

 

 