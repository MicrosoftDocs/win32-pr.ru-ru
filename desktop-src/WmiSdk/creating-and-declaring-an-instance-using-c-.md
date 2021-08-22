---
description: Экземпляр на C++ можно создать с помощью интерфейса IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Создание и объявление экземпляра с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046c8c32944c7b726e09eade2701f8d35c9edb0363635eca2a16f7e3d630799a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568804"
---
# <a name="creating-and-declaring-an-instance-using-c"></a>Создание и объявление экземпляра с помощью C++

Экземпляр на C++ можно создать с помощью интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .

В примерах кода в этом разделе \# для правильной компиляции требуется следующая инструкция include.


```C++
#include <wbemidl.h>
```



В следующей процедуре описывается создание экземпляра существующего класса.

**Создание экземпляра существующего класса**

1.  Получите определение существующего класса, вызвав методы [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .

    В следующем примере кода показано, как использовать методы [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) и [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) для получения указателя на интерфейс [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , который предоставляет доступ к определению класса.

    ```C++
    // The pSv variable is of type IWbemServices *

    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                  &pExampleClass, &pResult);
    SysFreeString(PathToClass);
    ```

    

2.  Создайте новый экземпляр, вызвав метод [**ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .

    В следующем примере кода показано, как создать новый экземпляр, а затем освободить класс.

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  Задайте значения для всех свойств, которые не наследуют значения, определенные для класса, вызвав метод [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .

    Каждый экземпляр класса наследует все свойства, определенные для класса. Однако при необходимости можно указать другие значения свойств.

    Если у существующего класса есть ключевое свойство, необходимо задать для свойства **значение NULL** или гарантированное уникальное значение. Если для ключа задано **значение NULL** , а ключ является строкой, то [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) или [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) внутренне создает и назначает идентификатор GUID для ключа. Таким образом, указание **значения NULL** для ключевого свойства позволяет создать уникальный экземпляр, который не будет перезаписывать предыдущий экземпляр.

    В следующем примере кода показано, как задать значение свойства [**index**](swbemrefreshableitem-index.md) класса экземпляра example.

    ```C++
    VARIANT v;
    VariantInit(&v);

    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);
    ```

    

4.  Задайте значения для всех соответствующих квалификаторов с помощью вызова [**ивбемклассобжект:: жеткуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).

    Метод [**жеткуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) возвращает указатель на интерфейс [**ивбемкуалифиерсет**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , который используется для доступа к квалификаторам класса или экземпляра. Можно указать разные значения квалификатора, определенного для класса, если квалификатор класса имеет значение **енаблеоверриде**. Нельзя изменить или удалить квалификатор класса с установленным флагом **DisableOverride**. Дополнительные сведения см. в разделе [Флаги квалификаторов](qualifier-flavors.md).

    В качестве параметра можно также определить дополнительные квалификаторы для класса экземпляра. Можно определить дополнительные квалификаторы для экземпляра или свойства экземпляра, которые не должны отображаться в объявлении класса.

5.  Сохраните экземпляр, вызвав метод [**IWbemServices::P утинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .

    Инструментарий WMI сохраняет экземпляр в текущем пространстве имен WMI. Таким образом, полный путь к экземпляру зависит от пространства имен, которое обычно является корневым \\ по умолчанию. В этом примере кода полное имя пути будет иметь вид \\ \\ . \\ root \\ по умолчанию: example. index = "IX100".

    В следующем примере кода показано, как сохранить экземпляр.

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

Сохранение экземпляра в WMI блокирует несколько свойств экземпляра.

В частности, вы не можете выполнять следующие операции через API инструментария WMI после того, как экземпляр существует в инфраструктуре WMI:

-   Измените родительский класс класса, которому принадлежит экземпляр.
-   Добавление или удаление свойств.
-   Измените типы свойств.
-   Добавление или удаление [**ключа**](standard-qualifiers.md) или **индексированных** квалификаторов.
-   Добавление или удаление [**одноэлементных**](standard-wmi-qualifiers.md), **динамических** или [**абстрактных**](standard-qualifiers.md) квалификаторов.

В следующем примере кода объединены примеры кода, описанные в предыдущей процедуре, чтобы продемонстрировать, как создать экземпляр с помощью API WMI.


```C++
void CreateInstance (IWbemServices *pSvc)
{
    IWbemClassObject *pNewInstance = 0;
    IWbemClassObject *pExampleClass = 0;
    IWbemContext *pCtx = 0;
    IWbemCallResult *pResult = 0;

    // Get the class definition.
    BSTR PathToClass = SysAllocString(L"Example");
    HRESULT hRes = pSvc->GetObject(PathToClass, 0, pCtx, 
                 &pExampleClass, &pResult);
    SysFreeString(PathToClass);

    if (hRes != 0)
       return;

    // Create a new instance.
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more

    VARIANT v;
    VariantInit(&v);

    // Set the Index property (the key).
    V_VT(&v) = VT_BSTR;
    V_BSTR(&v) = SysAllocString(L"IX100");

    BSTR KeyProp = SysAllocString(L"Index");
    pNewInstance->Put(KeyProp, 0, &v, 0);
    SysFreeString(KeyProp);
    VariantClear(&v);

    // Set the IntVal property.
    V_VT(&v) = VT_I4;
    V_I4(&v) = 1001;  
    
    BSTR Prop = SysAllocString(L"IntVal");
    pNewInstance->Put(Prop, 0, &v, 0);
    SysFreeString(Prop);
    VariantClear(&v);    
    
    // Other properties acquire the 'default' value specified
    // in the class definition unless otherwise modified here.

    // Write the instance to WMI. 
    hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
    pNewInstance->Release();
}
```



 

 



