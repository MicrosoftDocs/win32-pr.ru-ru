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
# <a name="retrieving-documentation-for-raw-and-formatted-performance-data-objects"></a>Получение документации для необработанных и отформатированных объектов данных о производительности

В следующем разделе описано, как получить документацию по интерактивному программированию для динамически созданного необработанного или неформатированного объекта данных.

Инструментарий WMI содержит ряд объектов, которые следят за производительностью. Классы, производные от [**Win32 \_ перфравдата**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) , содержат необработанные данные о производительности, а также поддерживаются [поставщиком счетчика производительности](performance-counter-provider.md). В отличие от этого, классы, производные от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) , содержат данные в формате «обработанные» или отформатированные, и поддерживаются [поставщиком данных о производительности](formatted-performance-data-provider.md).

Однако оба поставщика поддерживают несколько динамически создаваемых дочерних классов. Так как свойства добавляются во время выполнения, эти классы могут содержать недокументированные свойства. Можно использовать следующий код, чтобы определить, какие свойства имеют данный динамически созданный класс.

**Получение описания динамически созданного класса**

1.  Создайте экземпляр элемента и присвойте измененному квалификатору значение true.

    ```PowerShell
    $osClass = New-Object System.Management.ManagementClass Win32_ClassNameHere  
    $osClass.Options.UseAmendedQualifiers = $true
    ```

    

2.  Извлеките свойства класса.

    ```PowerShell
    $properties = $osClass.Properties  
    "This class has {0} properties as follows:" -f $properties.count
    ```

    

3.  Отображение свойств.

    ```PowerShell
    foreach ($property in $properties) {  
    "Property Name: {0}" -f $property.Name  
    "Description:   {0}" -f $($property.Qualifiers["Description"].Value)  
    "Type:          {0}" -f $property.Type  
    "-------"
    }
    ```

    

Следующий код получает описания свойств для указанного объекта [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .


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



 

 
