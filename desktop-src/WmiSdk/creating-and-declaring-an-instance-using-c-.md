---
description: Экземпляр на C++ можно создать с помощью интерфейса IWbemServices.
ms.assetid: ee54c1ef-bc91-4771-8c11-9ee3aacd8112
ms.tgt_platform: multiple
title: Создание и объявление экземпляра с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd316975c68625383a9d2a2d1fe2fc389d30494a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702838"
---
# <a name="creating-and-declaring-an-instance-using-c"></a><span data-ttu-id="07475-103">Создание и объявление экземпляра с помощью C++</span><span class="sxs-lookup"><span data-stu-id="07475-103">Creating and Declaring an Instance Using C++</span></span>

<span data-ttu-id="07475-104">Экземпляр на C++ можно создать с помощью интерфейса [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="07475-104">You can create an instance in C++ through the [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) interface.</span></span>

<span data-ttu-id="07475-105">В примерах кода в этом разделе \# для правильной компиляции требуется следующая инструкция include.</span><span class="sxs-lookup"><span data-stu-id="07475-105">The code examples in this topic require the following \#include statement to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="07475-106">В следующей процедуре описывается создание экземпляра существующего класса.</span><span class="sxs-lookup"><span data-stu-id="07475-106">The following procedure describes how to create an instance of an existing class.</span></span>

<span data-ttu-id="07475-107">**Создание экземпляра существующего класса**</span><span class="sxs-lookup"><span data-stu-id="07475-107">**To create an instance of an existing class**</span></span>

1.  <span data-ttu-id="07475-108">Получите определение существующего класса, вызвав методы [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) .</span><span class="sxs-lookup"><span data-stu-id="07475-108">Retrieve the definition of the existing class by calling the [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods.</span></span>

    <span data-ttu-id="07475-109">В следующем примере кода показано, как использовать методы [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) и [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) для получения указателя на интерфейс [**ивбемклассобжект**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) , который предоставляет доступ к определению класса.</span><span class="sxs-lookup"><span data-stu-id="07475-109">The following code example shows how to use the [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) and [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) methods to get a pointer to the [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) interface that provides access to the class definition.</span></span>

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

    

2.  <span data-ttu-id="07475-110">Создайте новый экземпляр, вызвав метод [**ивбемклассобжект:: спавнинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) .</span><span class="sxs-lookup"><span data-stu-id="07475-110">Create the new instance by calling the [**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance) method.</span></span>

    <span data-ttu-id="07475-111">В следующем примере кода показано, как создать новый экземпляр, а затем освободить класс.</span><span class="sxs-lookup"><span data-stu-id="07475-111">The following code example shows how to create a new instance and then release the class.</span></span>

    ```C++
    pExampleClass->SpawnInstance(0, &pNewInstance);
    pExampleClass->Release();  // Don't need the class any more
    ```

    

3.  <span data-ttu-id="07475-112">Задайте значения для всех свойств, которые не наследуют значения, определенные для класса, вызвав метод [**ивбемклассобжект::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) .</span><span class="sxs-lookup"><span data-stu-id="07475-112">Set values for any properties that do not inherit the values defined for the class by calling the [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put) method.</span></span>

    <span data-ttu-id="07475-113">Каждый экземпляр класса наследует все свойства, определенные для класса.</span><span class="sxs-lookup"><span data-stu-id="07475-113">Each instance of a class inherits all of the properties that are defined for the class.</span></span> <span data-ttu-id="07475-114">Однако при необходимости можно указать другие значения свойств.</span><span class="sxs-lookup"><span data-stu-id="07475-114">However, you can specify different property values if you choose.</span></span>

    <span data-ttu-id="07475-115">Если у существующего класса есть ключевое свойство, необходимо задать для свойства **значение NULL** или гарантированное уникальное значение.</span><span class="sxs-lookup"><span data-stu-id="07475-115">If the existing class has a key property, you should set the property either to **NULL** or a guaranteed unique value.</span></span> <span data-ttu-id="07475-116">Если для ключа задано **значение NULL** , а ключ является строкой, то [**путинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) или [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) внутренне создает и назначает идентификатор GUID для ключа.</span><span class="sxs-lookup"><span data-stu-id="07475-116">If you set the key to **NULL** and the key is a string, then [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) or [**PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) internally generates and assigns a GUID to the key.</span></span> <span data-ttu-id="07475-117">Таким образом, указание **значения NULL** для ключевого свойства позволяет создать уникальный экземпляр, который не будет перезаписывать предыдущий экземпляр.</span><span class="sxs-lookup"><span data-stu-id="07475-117">This way, specifying **NULL** for a key property lets you create a unique instance that will not overwrite any previous instance.</span></span>

    <span data-ttu-id="07475-118">В следующем примере кода показано, как задать значение свойства [**index**](swbemrefreshableitem-index.md) класса экземпляра example.</span><span class="sxs-lookup"><span data-stu-id="07475-118">The following code example shows how to set the [**Index**](swbemrefreshableitem-index.md) property value of the example instance class.</span></span>

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

    

4.  <span data-ttu-id="07475-119">Задайте значения для всех соответствующих квалификаторов с помощью вызова [**ивбемклассобжект:: жеткуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span><span class="sxs-lookup"><span data-stu-id="07475-119">Set the values for any relevant qualifiers through a call to [**IWbemClassObject::GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset).</span></span>

    <span data-ttu-id="07475-120">Метод [**жеткуалифиерсет**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) возвращает указатель на интерфейс [**ивбемкуалифиерсет**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) , который используется для доступа к квалификаторам класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="07475-120">The [**GetQualifierSet**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getqualifierset) method returns a pointer to an [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) interface, which use to access the qualifiers for a class or instance.</span></span> <span data-ttu-id="07475-121">Можно указать разные значения квалификатора, определенного для класса, если квалификатор класса имеет значение **енаблеоверриде**.</span><span class="sxs-lookup"><span data-stu-id="07475-121">You can specify different values for a qualifier defined for the class if the class qualifier flavor is **EnableOverride**.</span></span> <span data-ttu-id="07475-122">Нельзя изменить или удалить квалификатор класса с установленным флагом **DisableOverride**.</span><span class="sxs-lookup"><span data-stu-id="07475-122">You cannot modify or delete a class qualifier with the flavor set to **DisableOverride**.</span></span> <span data-ttu-id="07475-123">Дополнительные сведения см. в разделе [Флаги квалификаторов](qualifier-flavors.md).</span><span class="sxs-lookup"><span data-stu-id="07475-123">For more information, see [Qualifier Flavors](qualifier-flavors.md).</span></span>

    <span data-ttu-id="07475-124">В качестве параметра можно также определить дополнительные квалификаторы для класса экземпляра.</span><span class="sxs-lookup"><span data-stu-id="07475-124">As an option, you can also define additional qualifiers for your instance class.</span></span> <span data-ttu-id="07475-125">Можно определить дополнительные квалификаторы для экземпляра или свойства экземпляра, которые не должны отображаться в объявлении класса.</span><span class="sxs-lookup"><span data-stu-id="07475-125">You can define additional qualifiers for the instance or instance property which do not need to appear in the class declaration.</span></span>

5.  <span data-ttu-id="07475-126">Сохраните экземпляр, вызвав метод [**IWbemServices::P утинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) или [**IWbemServices::P утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="07475-126">Save the instance by calling the [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) method.</span></span>

    <span data-ttu-id="07475-127">Инструментарий WMI сохраняет экземпляр в текущем пространстве имен WMI.</span><span class="sxs-lookup"><span data-stu-id="07475-127">WMI saves the instance in the current WMI namespace.</span></span> <span data-ttu-id="07475-128">Таким образом, полный путь к экземпляру зависит от пространства имен, которое обычно является корневым \\ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07475-128">As such, the full path of the instance is dependent on the namespace, which is typically root\\default.</span></span> <span data-ttu-id="07475-129">В этом примере кода полное имя пути будет иметь вид \\ \\ . \\ root \\ по умолчанию: example. index = "IX100".</span><span class="sxs-lookup"><span data-stu-id="07475-129">For this code example, the full path name would be \\\\.\\root\\default:Example.Index="IX100".</span></span>

    <span data-ttu-id="07475-130">В следующем примере кода показано, как сохранить экземпляр.</span><span class="sxs-lookup"><span data-stu-id="07475-130">The following code example shows how to save an instance.</span></span>

    ```C++
        hRes = pSvc->PutInstance(pNewInstance, 0, pCtx, &pResult);
        pNewInstance->Release();
    ```

    

<span data-ttu-id="07475-131">Сохранение экземпляра в WMI блокирует несколько свойств экземпляра.</span><span class="sxs-lookup"><span data-stu-id="07475-131">Saving the instance to WMI locks down several of the properties of the instance.</span></span>

<span data-ttu-id="07475-132">В частности, вы не можете выполнять следующие операции через API инструментария WMI после того, как экземпляр существует в инфраструктуре WMI:</span><span class="sxs-lookup"><span data-stu-id="07475-132">Specifically, you cannot perform any of the following operations through the WMI API after an instance exists within the WMI infrastructure:</span></span>

-   <span data-ttu-id="07475-133">Измените родительский класс класса, которому принадлежит экземпляр.</span><span class="sxs-lookup"><span data-stu-id="07475-133">Change the parent class of the class to which the instance belongs.</span></span>
-   <span data-ttu-id="07475-134">Добавление или удаление свойств.</span><span class="sxs-lookup"><span data-stu-id="07475-134">Add or remove properties.</span></span>
-   <span data-ttu-id="07475-135">Измените типы свойств.</span><span class="sxs-lookup"><span data-stu-id="07475-135">Change property types.</span></span>
-   <span data-ttu-id="07475-136">Добавление или удаление [**ключа**](standard-qualifiers.md) или **индексированных** квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="07475-136">Add or remove [**Key**](standard-qualifiers.md) or **Indexed** qualifiers.</span></span>
-   <span data-ttu-id="07475-137">Добавление или удаление [**одноэлементных**](standard-wmi-qualifiers.md), **динамических** или [**абстрактных**](standard-qualifiers.md) квалификаторов.</span><span class="sxs-lookup"><span data-stu-id="07475-137">Add or remove [**Singleton**](standard-wmi-qualifiers.md), **Dynamic**, or [**Abstract**](standard-qualifiers.md) qualifiers.</span></span>

<span data-ttu-id="07475-138">В следующем примере кода объединены примеры кода, описанные в предыдущей процедуре, чтобы продемонстрировать, как создать экземпляр с помощью API WMI.</span><span class="sxs-lookup"><span data-stu-id="07475-138">The following code example combines the code examples discussed in the previous procedure to show how to create an instance using the WMI API.</span></span>


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



 

 



