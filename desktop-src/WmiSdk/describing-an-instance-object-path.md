---
description: Путь к объекту экземпляра описывает расположение экземпляра данного класса в определенном пространстве имен.
ms.assetid: 78a194f0-cd21-4622-9242-be7e430b96c0
ms.tgt_platform: multiple
title: Описание пути к объекту экземпляра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f977359ea9c3c4346052f1edd076c0cce5544441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347045"
---
# <a name="describing-an-instance-object-path"></a><span data-ttu-id="274ed-103">Описание пути к объекту экземпляра</span><span class="sxs-lookup"><span data-stu-id="274ed-103">Describing an Instance Object Path</span></span>

<span data-ttu-id="274ed-104">Путь к объекту экземпляра описывает расположение экземпляра данного класса в определенном пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="274ed-104">An instance object path describes the location of an instance of a given class within a specific namespace.</span></span>

<span data-ttu-id="274ed-105">Можно использовать несколько различных типов путей объектов экземпляров.</span><span class="sxs-lookup"><span data-stu-id="274ed-105">You can have several different kinds of instance object paths:</span></span>

-   <span data-ttu-id="274ed-106">Полное</span><span class="sxs-lookup"><span data-stu-id="274ed-106">Full</span></span>

    <span data-ttu-id="274ed-107">Путь к объекту полного экземпляра добавляет имя и значение ключевого свойства класса в полный путь к объекту класса.</span><span class="sxs-lookup"><span data-stu-id="274ed-107">A full instance object path appends the name and value of the key property for the class to a full class object path.</span></span>

    <span data-ttu-id="274ed-108">В следующем примере показано определение пути к объекту полного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="274ed-108">The following example shows the definition of the full instance object path.</span></span>

    ``` syntax
    \\Server\Namespace:Class.KeyName="KeyValue"
    ```

-   <span data-ttu-id="274ed-109">Относительное значение</span><span class="sxs-lookup"><span data-stu-id="274ed-109">Relative</span></span>

    <span data-ttu-id="274ed-110">Относительный путь к объекту ссылается на экземпляр, расположенный в текущем пространстве имен на текущем сервере.</span><span class="sxs-lookup"><span data-stu-id="274ed-110">A relative object path refers to an instance located in the current namespace on the current server.</span></span> <span data-ttu-id="274ed-111">Относительный путь состоит из имени класса, за которым следуют имена и значения ключевых свойств этого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="274ed-111">The relative path consists of the class name followed by the names and values of the key properties of this instance.</span></span>

    <span data-ttu-id="274ed-112">В следующем примере показано определение пути к объекту относительного экземпляра.</span><span class="sxs-lookup"><span data-stu-id="274ed-112">The following example shows the definition of the relative instance object path.</span></span>

    ``` syntax
    MyClass.MyProp="e:"
    ```

-   <span data-ttu-id="274ed-113">Относительно одного ключа</span><span class="sxs-lookup"><span data-stu-id="274ed-113">Relative with a single key</span></span>

    <span data-ttu-id="274ed-114">Для классов с одним свойством, назначенным в качестве ключа, можно опустить имя ключевого свойства.</span><span class="sxs-lookup"><span data-stu-id="274ed-114">For classes with only one property designated as the key, you can omit the name of the key property.</span></span>

    <span data-ttu-id="274ed-115">В следующем примере показано определение пути к объекту относительного экземпляра с одним ключом.</span><span class="sxs-lookup"><span data-stu-id="274ed-115">The following example shows the definition of the relative instance object path with a single key.</span></span>

    ``` syntax
    MyClass="e:"
    ```

-   <span data-ttu-id="274ed-116">Относительно нескольких ключей</span><span class="sxs-lookup"><span data-stu-id="274ed-116">Relative with multiple keys</span></span>

    <span data-ttu-id="274ed-117">Используйте запятую для различения ключей экземпляра с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="274ed-117">Use a comma to distinguish between the keys of an instance with multiple keys.</span></span>

    <span data-ttu-id="274ed-118">В следующем примере показаны определения пути к объекту относительного экземпляра с несколькими ключами.</span><span class="sxs-lookup"><span data-stu-id="274ed-118">The following example shows the definitions of the relative instance object path with multiple keys.</span></span>

    ``` syntax
    MyOtherClass.FirstKey=1,SecondKey=2
    ```

-   <span data-ttu-id="274ed-119">Относительно одноэлементного класса</span><span class="sxs-lookup"><span data-stu-id="274ed-119">Relative for a singleton class</span></span>

    <span data-ttu-id="274ed-120">Относительный путь к объекту для одноэлементного класса состоит из имени класса, за которым следует нотация "= @".</span><span class="sxs-lookup"><span data-stu-id="274ed-120">The relative object path for a singleton class consists of the class name followed by the "=@" notation.</span></span>

    <span data-ttu-id="274ed-121">В следующем примере показано определение пути к объекту относительного экземпляра для одноэлементного класса.</span><span class="sxs-lookup"><span data-stu-id="274ed-121">The following example shows the definition of the relative instance object path for a singleton class.</span></span>

    ``` syntax
    MySingletonClass=@
    ```

<span data-ttu-id="274ed-122">В следующей процедуре описывается извлечение экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="274ed-122">The following procedure describes how to retrieve a class instance.</span></span>

<span data-ttu-id="274ed-123">**Извлечение экземпляра класса**</span><span class="sxs-lookup"><span data-stu-id="274ed-123">**To retrieve a class instance**</span></span>

1.  <span data-ttu-id="274ed-124">Инициализируйте строку, содержащую путь к объекту, с помощью вызова функции [**сисаллокстринг**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) .</span><span class="sxs-lookup"><span data-stu-id="274ed-124">Initialize a string that contains the object path with a call to the [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) function.</span></span>
2.  <span data-ttu-id="274ed-125">Инициализируйте объект, который будет принимать экземпляр.</span><span class="sxs-lookup"><span data-stu-id="274ed-125">Initialize an object that will receive the instance.</span></span>
3.  <span data-ttu-id="274ed-126">Извлеките объект с помощью вызова [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) или [**IWbemServices:: жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="274ed-126">Retrieve the object with a call to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) or [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

    <span data-ttu-id="274ed-127">Чтобы использовать [**жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), необходимо реализовать интерфейс [**ивбемсинк**](swbemsink.md) .</span><span class="sxs-lookup"><span data-stu-id="274ed-127">To use [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), you must implement the [**IWbemSink**](swbemsink.md) interface.</span></span>

<span data-ttu-id="274ed-128">Следующая \# Инструкция include необходима для правильной компиляции кода, приведенного далее в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="274ed-128">The following \#include statement is required for the code that is listed later in this topic to compile correctly.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="274ed-129">В следующем примере кода показано, как получить экземпляр класса, используя путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="274ed-129">The following code example describes how to retrieve a class instance using an object path.</span></span>


```C++
IWbemServices* pWbemSvcs = 0;

BSTR Path = SysAllocString(L"ComPort=2");    
IWbemClassObject *pComPort = 0;
pWbemSvcs->GetObject(Path, 0, 0, &pComPort, 0);
```



<span data-ttu-id="274ed-130">Для экземпляров классов, в которых в качестве ключа задано несколько свойств, инструментарию WMI не требуется конкретное упорядочение ключевых свойств в путях объектов.</span><span class="sxs-lookup"><span data-stu-id="274ed-130">For instances of classes that specify multiple properties as the key, WMI requires no specific ordering of key properties in object paths.</span></span> <span data-ttu-id="274ed-131">Необходимо указать только значение каждого свойства в пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="274ed-131">You need only specify the value of each of the properties in the object path.</span></span>

<span data-ttu-id="274ed-132">В следующем примере кода описаны два эквивалентных описания ключа.</span><span class="sxs-lookup"><span data-stu-id="274ed-132">The following code example describes two equivalent key descriptions.</span></span>

``` syntax
MyClass.IntVal=33,StrVal="AAA"
MyClass.StrVal="AAA",IntVal=33
```

 

 
