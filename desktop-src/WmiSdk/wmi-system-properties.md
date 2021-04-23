---
description: Инструментарий управления Windows (WMI) (WMI) определяет набор системных свойств, связанных со всеми классами и экземплярами классов.
ms.assetid: e812c0cb-3e08-4cac-8d05-2cd7abc922d1
ms.tgt_platform: multiple
title: Свойства системы WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3ee541d9de0d37c9aa1eae4ded07d3cb70ff1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263920"
---
# <a name="wmi-system-properties"></a><span data-ttu-id="ef1c8-103">Свойства системы WMI</span><span class="sxs-lookup"><span data-stu-id="ef1c8-103">WMI System Properties</span></span>

<span data-ttu-id="ef1c8-104">Инструментарий управления Windows (WMI) (WMI) определяет набор системных свойств, связанных со всеми классами и экземплярами классов.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-104">Windows Management Instrumentation (WMI) defines a set of system properties that are associated with all classes and instances of classes.</span></span> <span data-ttu-id="ef1c8-105">Как и системные классы, имена системных свойств начинаются с двойного символа подчеркивания, что отличает их от свойств, созданных приложениями или поставщиками, которые не должны начинаться с одинарной или двойной подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-105">As with system classes, system property names begin with a double underscore, distinguishing them from properties created by applications or providers that must not start with a single or double underscore.</span></span> <span data-ttu-id="ef1c8-106">Другой способ указать системное свойство — использовать метод [**ивбемклассобжект:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) .</span><span class="sxs-lookup"><span data-stu-id="ef1c8-106">Another way to identify a system property is to use the [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get) method.</span></span>

<span data-ttu-id="ef1c8-107">Системные свойства доступны в любое время, но значения могут быть **равны NULL**.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-107">System properties are available at any time, but values might be **NULL**.</span></span> <span data-ttu-id="ef1c8-108">**Значение NULL** указывает, что свойство не применимо к конкретному объекту.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-108">**NULL** indicates a property does not apply to a specific object.</span></span> <span data-ttu-id="ef1c8-109">Однако свойства системы могут быть недоступными все время для всех классов или экземпляров.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-109">However, system properties might not be available all the time for all classes or instances.</span></span>

## <a name="system-properties"></a><span data-ttu-id="ef1c8-110">Свойства системы</span><span class="sxs-lookup"><span data-stu-id="ef1c8-110">System Properties</span></span>

<span data-ttu-id="ef1c8-111">В следующем списке описываются свойства системы WMI.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-111">The following list describes the WMI system properties.</span></span> <span data-ttu-id="ef1c8-112">Приведенные примеры взяты из системных свойств класса [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , который описан в нижней части этого раздела.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-112">The examples given are taken from the system properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which is described at the bottom of this topic.</span></span>

<dl> <dt>

<span data-ttu-id="ef1c8-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_См**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-113"><span id="__Class"></span><span id="__class"></span><span id="__CLASS"></span>**\_\_Class**</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-114">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-114">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="ef1c8-115">Тип доступа: только для чтения для экземпляров; чтение и запись для классов</span><span class="sxs-lookup"><span data-stu-id="ef1c8-115">Access type: Read-only for instances; read/write for classes</span></span>

<span data-ttu-id="ef1c8-116">Имя класса.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-116">The name of the class.</span></span>

<span data-ttu-id="ef1c8-117">Пример: Win32 \_ оптионалфеатуре</span><span class="sxs-lookup"><span data-stu-id="ef1c8-117">Example: Win32\_OptionalFeature</span></span>

</dd> <dt>

<span data-ttu-id="ef1c8-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Рожден**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-118"><span id="__Derivation"></span><span id="__derivation"></span><span id="__DERIVATION"></span>**\_\_Derivation**</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-119">Тип данных: **массив \_ строк CIM**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-119">Data type: **CIM\_STRING** array</span></span>

<span data-ttu-id="ef1c8-120">Тип доступа: только для чтения для экземпляров и классов</span><span class="sxs-lookup"><span data-stu-id="ef1c8-120">Access type: Read-only for both instances and classes</span></span>

<span data-ttu-id="ef1c8-121">Иерархия классов текущего класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-121">Class hierarchy of the current class or instance.</span></span> <span data-ttu-id="ef1c8-122">Первый элемент является непосредственным родительским классом, далее — родительским и т. д. последний элемент является базовым классом.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-122">The first element is the immediate parent class, the next is its parent, and so on; the last element is the base class.</span></span>

<span data-ttu-id="ef1c8-123">Пример: {CIM \_ логикалелемент, CIM \_ манажедсистемелемент}</span><span class="sxs-lookup"><span data-stu-id="ef1c8-123">Example: {CIM\_LogicalElement, CIM\_ManagedSystemElement}</span></span>

</dd> <dt>

<span data-ttu-id="ef1c8-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Династию**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-124"><span id="__Dynasty"></span><span id="__dynasty"></span><span id="__DYNASTY"></span>**\_\_Dynasty**</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-125">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-125">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="ef1c8-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef1c8-126">Access type: Read-only</span></span>

<span data-ttu-id="ef1c8-127">Имя класса верхнего уровня, от которого производятся экземпляры класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-127">Name of the top-level class from which the class or instance is derived.</span></span> <span data-ttu-id="ef1c8-128">Если этот класс или экземпляр является классом верхнего уровня, значения **\_ \_ династию** и **\_ \_ Class** одинаковы.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-128">When this class or instance is the top-level class, the values of **\_\_Dynasty** and **\_\_Class** are the same.</span></span>

<span data-ttu-id="ef1c8-129">Пример: CIM \_ манажедсистемелемент</span><span class="sxs-lookup"><span data-stu-id="ef1c8-129">Example: CIM\_ManagedSystemElement</span></span>

</dd> <dt>

<span data-ttu-id="ef1c8-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_женус**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-130"><span id="__Genus"></span><span id="__genus"></span><span id="__GENUS"></span>**\_\_Genus**</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-131">Тип данных: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-131">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="ef1c8-132">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef1c8-132">Access type: Read-only</span></span>

<span data-ttu-id="ef1c8-133">Значение, используемое для различения классов и экземпляров.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-133">Value that is used to distinguish between classes and instances.</span></span> <span data-ttu-id="ef1c8-134">Это значение является **\_ \_ классом WBEM женус** (1) для классов и **\_ \_ экземпляром WBEM женус** (2) для экземпляров и событий.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-134">This value is **WBEM\_GENUS\_CLASS** (1) for classes, and **WBEM\_GENUS\_INSTANCE** (2) for instances and events.</span></span>

<span data-ttu-id="ef1c8-135">Пример: 2</span><span class="sxs-lookup"><span data-stu-id="ef1c8-135">Example: 2</span></span>

</dd> <dt>

<span data-ttu-id="ef1c8-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Имен**](--namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ef1c8-136"><span id="__Namespace"></span><span id="__namespace"></span><span id="__NAMESPACE"></span>[**\_\_Namespace**](--namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-137">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-137">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="ef1c8-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef1c8-138">Access type: Read-only</span></span>

<span data-ttu-id="ef1c8-139">Имя [*пространства имен*](gloss-n.md) класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-139">Name of the [*namespace*](gloss-n.md) of the class or instance.</span></span>

<span data-ttu-id="ef1c8-140">Пример: root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ef1c8-140">Example: root\\cimv2</span></span>

</dd> <dt>

<span data-ttu-id="ef1c8-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Путь**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-141"><span id="__Path"></span><span id="__path"></span><span id="__PATH"></span>**\_\_Path**</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-142">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-142">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="ef1c8-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef1c8-143">Access type: Read-only</span></span>

<span data-ttu-id="ef1c8-144">Полный путь к классу или экземпляру, включая сервер и пространство имен.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-144">Full path to the class or instance—including server and namespace.</span></span>

<span data-ttu-id="ef1c8-145">Пример: \\ \\ MyServer \\ root \\ CIMV2: Win32 \_ Оптионалфеатуре. Name = "телнетклиент"</span><span class="sxs-lookup"><span data-stu-id="ef1c8-145">Example: \\\\MyServer\\root\\cimv2:Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="ef1c8-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_\_Число свойств**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-146"><span id="__Property_Count"></span><span id="__property_count"></span><span id="__PROPERTY_COUNT"></span>**\_\_Property\_Count**</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-147">Тип данных: **CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-147">Data type: **CIM\_SINT32**</span></span>

<span data-ttu-id="ef1c8-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef1c8-148">Access type: Read-only</span></span>

<span data-ttu-id="ef1c8-149">Количество несистемных свойств, определенных для класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-149">Number of nonsystem properties defined for the class or instance.</span></span>

<span data-ttu-id="ef1c8-150">Пример: 6</span><span class="sxs-lookup"><span data-stu-id="ef1c8-150">Example: 6</span></span>

</dd> <dt>

<span data-ttu-id="ef1c8-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_релпас**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-151"><span id="__Relpath"></span><span id="__relpath"></span><span id="__RELPATH"></span>**\_\_Relpath**</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-152">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-152">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="ef1c8-153">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef1c8-153">Access type: Read-only</span></span>

<span data-ttu-id="ef1c8-154">Относительный путь к классу или экземпляру.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-154">Relative path to the class or instance.</span></span>

<span data-ttu-id="ef1c8-155">Пример: Win32 \_ оптионалфеатуре. Name = "телнетклиент"</span><span class="sxs-lookup"><span data-stu-id="ef1c8-155">Example: Win32\_OptionalFeature.Name="TelnetClient"</span></span>

</dd> <dt>

<span data-ttu-id="ef1c8-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Сервером**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-156"><span id="__Server"></span><span id="__server"></span><span id="__SERVER"></span>**\_\_Server**</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-157">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-157">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="ef1c8-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef1c8-158">Access type: Read-only</span></span>

<span data-ttu-id="ef1c8-159">Имя сервера, предоставляющего класс или экземпляр.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-159">Name of the server supplying the class or instance.</span></span>

<span data-ttu-id="ef1c8-160">Пример: MyServer</span><span class="sxs-lookup"><span data-stu-id="ef1c8-160">Example: MyServer</span></span>

</dd> <dt>

<span data-ttu-id="ef1c8-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Суперкласс**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-161"><span id="__Superclass"></span><span id="__superclass"></span><span id="__SUPERCLASS"></span>**\_\_Superclass**</span></span>
</dt> <dd>

<span data-ttu-id="ef1c8-162">Тип данных: **\_ строка CIM**</span><span class="sxs-lookup"><span data-stu-id="ef1c8-162">Data type: **CIM\_STRING**</span></span>

<span data-ttu-id="ef1c8-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ef1c8-163">Access type: Read-only</span></span>

<span data-ttu-id="ef1c8-164">Имя непосредственный родительский класс класса или экземпляра.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-164">Name of the immediate parent class of the class or instance.</span></span>

<span data-ttu-id="ef1c8-165">Пример: CIM \_ логикалелемент</span><span class="sxs-lookup"><span data-stu-id="ef1c8-165">Example: CIM\_LogicalElement</span></span>

</dd> </dl>

<span data-ttu-id="ef1c8-166">Следующий код PowerShell извлекает свойства класса [**Win32 \_ оптионалфеатуре**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) , который включает в себя свойства системы.</span><span class="sxs-lookup"><span data-stu-id="ef1c8-166">The following PowerShell code retrieves the properties of the [**Win32\_OptionalFeature**](/windows/desktop/CIMWin32Prov/win32-optionalfeature) class, which includes the system properties.</span></span>


```PowerShell
Get-WmiObject win32_OptionalFeature | Where-Object {$_.name -eq "TelnetClient"}
```



<span data-ttu-id="ef1c8-167">Предыдущий пример кода возвращает следующее:</span><span class="sxs-lookup"><span data-stu-id="ef1c8-167">The previous code sample returns the following:</span></span>


```PowerShell
__GENUS          : 2
__CLASS          : Win32_OptionalFeature
__SUPERCLASS     : CIM_LogicalElement
__DYNASTY        : CIM_ManagedSystemElement
__RELPATH        : Win32_OptionalFeature.Name="TelnetClient"
__PROPERTY_COUNT : 6
__DERIVATION     : {CIM_LogicalElement, CIM_ManagedSystemElement}
__SERVER         : myServer
__NAMESPACE      : root\cimv2
__PATH           : \\myServer\root\cimv2:Win32_OptionalFeature.Name="TelnetClient"
Caption          : Telnet Client
Description      : 
InstallDate      : 
InstallState     : 2
Name             : TelnetClient
Status           : 
PSComputerName   : myServer
```



 

 
