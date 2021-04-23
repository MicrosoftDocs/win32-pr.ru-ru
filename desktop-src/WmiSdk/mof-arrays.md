---
description: Массив — это индексированный список значений данных, имеющих один и тот же тип данных, на которые можно ссылаться. Помимо строковых и числовых массивов, MOF поддерживает массивы внедренных объектов и ссылок.
ms.assetid: f63c222f-499d-4776-8901-65cb8b142d2b
ms.tgt_platform: multiple
title: Массивы MOF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0443f2ef3b3fe8fca398e281de71b0927a4f06f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263461"
---
# <a name="mof-arrays"></a><span data-ttu-id="86c01-104">Массивы MOF</span><span class="sxs-lookup"><span data-stu-id="86c01-104">MOF Arrays</span></span>

<span data-ttu-id="86c01-105">Массив — это индексированный список значений данных, имеющих один и тот же тип данных, на которые можно ссылаться.</span><span class="sxs-lookup"><span data-stu-id="86c01-105">An array is an indexed list of data values that are of the same data type, which you can reference.</span></span> <span data-ttu-id="86c01-106">Помимо строковых и числовых массивов, MOF поддерживает массивы внедренных объектов и ссылок.</span><span class="sxs-lookup"><span data-stu-id="86c01-106">In addition to string and numeric arrays, MOF supports arrays of embedded objects and references.</span></span>

<span data-ttu-id="86c01-107">В следующих правилах определяется MOF-массив:</span><span class="sxs-lookup"><span data-stu-id="86c01-107">The following rules define a MOF array:</span></span>

-   <span data-ttu-id="86c01-108">Скобки, используемые после идентификатора свойства, задают массив в определении класса.</span><span class="sxs-lookup"><span data-stu-id="86c01-108">Brackets used after the property identifier specify an array in a class definition.</span></span>

    ``` syntax
    Class ArrayDataSample1
    {
        string strArray1[];
    };
    ```

-   <span data-ttu-id="86c01-109">Все массивы должны быть одномерными.</span><span class="sxs-lookup"><span data-stu-id="86c01-109">All arrays must be one-dimensional.</span></span>
-   <span data-ttu-id="86c01-110">Массивы могут быть неограниченными или иметь явный размер.</span><span class="sxs-lookup"><span data-stu-id="86c01-110">Arrays can be unbounded or have an explicit size.</span></span>

    ``` syntax
    Class MyClass
    {
        sint32 MyMethod1 ([in, id(0)] Win32_LogicalDisk DiskArray1[]);
        sint32 MyMethod2 ([in, id(0)] Win32_LogicalDisk DiskArray2[32]);
    };
    ```

    <span data-ttu-id="86c01-111">Инструментарий WMI реализует ограниченные и неограниченные массивы как структуры **SAFEARRAY** , что позволяет инструментарию WMI изменять измерения массива во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="86c01-111">WMI implements bounded and unbounded arrays as **SAFEARRAY** structures, which allows WMI to vary array dimensions at run time.</span></span> <span data-ttu-id="86c01-112">При объявлении массива с явно заданным размером WMI сохраняет размер как квалификатор и обрабатывает его как рекомендуемый максимальный размер.</span><span class="sxs-lookup"><span data-stu-id="86c01-112">When you declare an array with an explicit size, WMI stores the size as a qualifier, and treats the size as the suggested maximum size.</span></span> <span data-ttu-id="86c01-113">Однако при необходимости Инструментарий WMI может расширить размер.</span><span class="sxs-lookup"><span data-stu-id="86c01-113">However, WMI can expand the size if necessary.</span></span> <span data-ttu-id="86c01-114">Изменение явного размера не влияет на реальные данные.</span><span class="sxs-lookup"><span data-stu-id="86c01-114">Changing the explicit size has no effect on the actual data.</span></span>

-   <span data-ttu-id="86c01-115">Массивы инициализируются путем указания значений соответствующего типа в списке с разделителями-запятыми.</span><span class="sxs-lookup"><span data-stu-id="86c01-115">Arrays are initialized by specifying values of the appropriate type in a comma-separated list.</span></span>

    ``` syntax
    Class ArrayDataSample2
    {
        [key] string s;
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
    };
    ```

-   <span data-ttu-id="86c01-116">Массив ссылок объявляется как массив строк пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="86c01-116">An array of references is declared as an array of object path strings.</span></span>

    <span data-ttu-id="86c01-117">При объявлении строки пути к объекту не размещайте пробелы между элементами пути к объекту.</span><span class="sxs-lookup"><span data-stu-id="86c01-117">When declaring an object path string, do not place white space between the elements of the object path.</span></span> <span data-ttu-id="86c01-118">В следующем примере показано, как объявить ссылку на путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="86c01-118">The following example describes how to declare an object path reference.</span></span>

    ``` syntax
    Class ClassWithRefArray
        { 
        [key] string s; 
        object ref refArray[]; 
        };

    instance of ClassWithRefArray
        {
        s = 23;
        refArray = {"Disk.Name=\"C:\"", "Disk.Name=\"E:\""};
        };
    ```

-   <span data-ttu-id="86c01-119">Массив можно использовать в качестве параметра для метода, но не в качестве возвращаемого значения входного или входного параметра.</span><span class="sxs-lookup"><span data-stu-id="86c01-119">You can use an array as a parameter for a method, but not as a return value for an input or input-output parameter.</span></span>
-   <span data-ttu-id="86c01-120">Все элементы массива создаются как значения одного типа.</span><span class="sxs-lookup"><span data-stu-id="86c01-120">All elements in an array are created as values of the same type.</span></span>

    <span data-ttu-id="86c01-121">Если элементы массива имеют тип **объекта** , можно поместить любой тип объекта в массив.</span><span class="sxs-lookup"><span data-stu-id="86c01-121">If the elements of an array are of the **object** type, then you can place any kind of object in the array.</span></span> <span data-ttu-id="86c01-122">С другой стороны, при объявлении определенного типа объекта WMI разрешает только объекты этого класса или подкласса в массиве.</span><span class="sxs-lookup"><span data-stu-id="86c01-122">On the other hand, if you declare a specific type of object, then WMI allows only objects of that class or subclass in the array.</span></span> <span data-ttu-id="86c01-123">В следующих примерах показаны объявления массивов, включающие использование типа **объекта** .</span><span class="sxs-lookup"><span data-stu-id="86c01-123">The following examples show array declarations that includes using the **object** type.</span></span>

    ``` syntax
    Class EmbedClass
    {
        [key] sint32 PropOfClass;
    };

    Class ArrayDataClass
    {
        [key] string s;
        string strArray1[];
        string strArray2[] = {"hello", "there"};
        sint32 dwArray[] = {1,2,3};
        EmbedClass objArray[];
    };

    instance of ArrayDataClass
    { 
        s = "keyStuff";
        strArray1 = { "1.2.3.4", "1.2.3.5", "1.2.3.7"};
        strArray2 = 
            {
                "SELECT * FROM RegistryKeyChangeEvent",
                "SELECT * FROM RegistryValueChangeEvent",
                "SELECT * FROM RegistryTreeChangeEvent"
            };
        dwArray  = { 1,2,3,5,6 };
        objArray = {
                       instance of EmbedClass{PropOfClass=3;},
                       instance of EmbedClass{PropOfClass=4;}
                   };
    };
    ```

 

 



