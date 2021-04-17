---
description: Каждое свойство в классе представления должно иметь квалификатор массива строк с именем Пропертисаурцес.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Квалификатор Пропертисаурцес
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711371"
---
# <a name="propertysources-qualifier"></a><span data-ttu-id="e20d1-103">Квалификатор Пропертисаурцес</span><span class="sxs-lookup"><span data-stu-id="e20d1-103">PropertySources Qualifier</span></span>

<span data-ttu-id="e20d1-104">Каждое свойство в классе представления должно иметь квалификатор массива строк с именем **пропертисаурцес**.</span><span class="sxs-lookup"><span data-stu-id="e20d1-104">Every property in a view class must have a string array qualifier called **PropertySources**.</span></span> <span data-ttu-id="e20d1-105">Квалификатор **пропертисаурцес** содержит имя свойства или свойств исходного класса, из которого это свойство класса представления получает данные.</span><span class="sxs-lookup"><span data-stu-id="e20d1-105">The **PropertySources** qualifier contains the name of the source class property or properties from which this view class property gets data.</span></span> <span data-ttu-id="e20d1-106">Порядок значений в этом массиве соответствует порядку исходных классов, определенных для [квалификатора виевсаурцес](viewsources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="e20d1-106">The order of the values in this array correspond to the order of the source classes defined for the [ViewSources qualifier](viewsources-qualifier.md).</span></span> <span data-ttu-id="e20d1-107">В следующем примере показано, как определить свойство для класса представления объединения, который является объединением класса [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) из двух разных компьютеров:</span><span class="sxs-lookup"><span data-stu-id="e20d1-107">The following example shows how to define a property for a union view class that is the union of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class from two different computers:</span></span>


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



<span data-ttu-id="e20d1-108">Первое свойство **DeviceID** соответствует свойству **DeviceID** из класса в первом исходном запросе.</span><span class="sxs-lookup"><span data-stu-id="e20d1-108">The first **DeviceID** property corresponds to the **DeviceID** property from the class in the first source query.</span></span> <span data-ttu-id="e20d1-109">Второе свойство **DeviceID** является свойством **DeviceID** из класса во втором исходном запросе.</span><span class="sxs-lookup"><span data-stu-id="e20d1-109">The second **DeviceID** property is the **DeviceID** property from the class in the second source query.</span></span>

<span data-ttu-id="e20d1-110">При определении свойств для классов представлений соединений необходимо определить отдельное свойство представления для каждого свойства исходного класса, если только свойства исходного класса не являются основанием класса представления объединения.</span><span class="sxs-lookup"><span data-stu-id="e20d1-110">When defining properties for join view classes, you must define a separate view property for each of the source class properties unless the source class properties are the basis of the join view class.</span></span> <span data-ttu-id="e20d1-111">В следующем примере создаются свойства в классе представления Join для аналогичных свойств из исходного [**класса \_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) и исходного класса [**Win32 \_ принтерконфигуратион**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :</span><span class="sxs-lookup"><span data-stu-id="e20d1-111">The following example creates properties in a join view class on similar properties from the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) source class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) source class:</span></span>


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



<span data-ttu-id="e20d1-112">Если два исходных класса соединены общим свойством, можно определить только одно свойство класса представления, так как значения обоих свойств исходного класса всегда одинаковы.</span><span class="sxs-lookup"><span data-stu-id="e20d1-112">If the two source classes are being joined by a common property, you can only define a single view class property because the value of both source class properties is always the same.</span></span> <span data-ttu-id="e20d1-113">В следующем примере показано, как присоединить [**класс \_ принтера Win32**](/windows/desktop/CIMWin32Prov/win32-printer) и [**\_ принтерконфигуратион Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) к общему значению свойства:</span><span class="sxs-lookup"><span data-stu-id="e20d1-113">The following example shows how to join the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) by a common property value:</span></span>


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a><span data-ttu-id="e20d1-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e20d1-114">Requirements</span></span>



| <span data-ttu-id="e20d1-115">Требование</span><span class="sxs-lookup"><span data-stu-id="e20d1-115">Requirement</span></span> | <span data-ttu-id="e20d1-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e20d1-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="e20d1-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e20d1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e20d1-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e20d1-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="e20d1-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e20d1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e20d1-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e20d1-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e20d1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e20d1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20d1-122">**Квалификаторы, относящиеся к поставщику представления**</span><span class="sxs-lookup"><span data-stu-id="e20d1-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

