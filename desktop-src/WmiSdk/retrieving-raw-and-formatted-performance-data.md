---
description: В следующем разделе описано, как получить документацию по интерактивному программированию для динамически созданного необработанного или неформатированного объекта данных.
ms.assetid: B3CD7E2C-9FCF-42FB-8713-01A696E905B0
ms.tgt_platform: multiple
title: Получение документации для необработанных и отформатированных объектов данных о производительности
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ab9cf66aa4536da25102511fdcbcab6bdd5202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349242"
---
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a><span data-ttu-id="b26fd-103">Получение документации для необработанных и отформатированных объектов данных о производительности</span><span class="sxs-lookup"><span data-stu-id="b26fd-103">Retrieving Documentation for Raw and Formatted Performance Data Objects</span></span>

<span data-ttu-id="b26fd-104">В следующем разделе описано, как получить документацию по интерактивному программированию для динамически созданного необработанного или неформатированного объекта данных.</span><span class="sxs-lookup"><span data-stu-id="b26fd-104">The following topic describes how to retrieve the on-line programming documentation for a dynamically-created raw or formatted data object.</span></span>

<span data-ttu-id="b26fd-105">Инструментарий WMI содержит ряд объектов, которые следят за производительностью.</span><span class="sxs-lookup"><span data-stu-id="b26fd-105">WMI contains a number of objects that track performance.</span></span> <span data-ttu-id="b26fd-106">Классы, производные от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) , содержат необработанные данные о производительности, а также поддерживаются [поставщиком счетчика производительности](performance-counter-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b26fd-106">Classes derived from [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) contain raw, or "uncooked" performance data, and are supported by the [Performance Counter provider](performance-counter-provider.md).</span></span> <span data-ttu-id="b26fd-107">В отличие от этого, классы, производные от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) , содержат данные в формате «обработанные» или отформатированные, и поддерживаются [поставщиком данных о производительности](formatted-performance-data-provider.md).</span><span class="sxs-lookup"><span data-stu-id="b26fd-107">In contrast, classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) contain "cooked", or formatted data, and are supported by the [Formatted Performance Data Provider](formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="b26fd-108">Однако оба поставщика поддерживают несколько динамически создаваемых дочерних классов.</span><span class="sxs-lookup"><span data-stu-id="b26fd-108">However, both providers support a number of dynamically-created child classes.</span></span> <span data-ttu-id="b26fd-109">Так как свойства добавляются во время выполнения, эти классы могут содержать недокументированные свойства.</span><span class="sxs-lookup"><span data-stu-id="b26fd-109">Because the properties are added at run-time, these classes may contain undocumented properties.</span></span> <span data-ttu-id="b26fd-110">Можно использовать следующий код, чтобы определить, какие свойства имеют данный динамически созданный класс.</span><span class="sxs-lookup"><span data-stu-id="b26fd-110">You can use the following code to identify what properties a given dynamically-created class has.</span></span>

<span data-ttu-id="b26fd-111">**Получение описания динамически созданного класса**</span><span class="sxs-lookup"><span data-stu-id="b26fd-111">**To retrieve a description of a dynamically-created class**</span></span>

1.  <span data-ttu-id="b26fd-112">Создайте экземпляр элемента и присвойте измененному квалификатору значение true.</span><span class="sxs-lookup"><span data-stu-id="b26fd-112">Create an instance of the item, and set the amended qualifier to true.</span></span>

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  <span data-ttu-id="b26fd-113">Извлеките свойства класса.</span><span class="sxs-lookup"><span data-stu-id="b26fd-113">Retrieve the properties of the class.</span></span>

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  <span data-ttu-id="b26fd-114">Отображение свойств.</span><span class="sxs-lookup"><span data-stu-id="b26fd-114">Display the properties.</span></span>

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

<span data-ttu-id="b26fd-115">Следующий код получает описания свойств для указанного объекта [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="b26fd-115">The following code retrieves the property descriptions for the specified [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) object.</span></span>


```PowerShell
$osClass = New-Object System.Management.ManagementClass Win32_PerfFormattedData_APPPOOLCountersProvider_APPPOOLWAS  
$osClass.Options.UseAmendedQualifiers = $true  
  
# Get the Properties in the class  
$properties = $osClass.Properties  
"This class has {0} properties as follows:" -f $properties.count  
  
  
# display the Property name, description, type, qualifiers and instance values  
  
foreach ($property in $properties) {  
"Property Name: {0}" -f $property.Name  
"Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
"Type:          {0}" -f $property.Type  
"-------"  
}
```



 

 
