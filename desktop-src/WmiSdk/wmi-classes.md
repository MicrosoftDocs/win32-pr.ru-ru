---
description: В этом разделе содержатся сведения о классе WMI и справочной странице.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: Классы WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa764d39c1fb048e125898a1f7e6d5cadf7f127d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702058"
---
# <a name="wmi-classes"></a><span data-ttu-id="2ae1a-103">Классы WMI</span><span class="sxs-lookup"><span data-stu-id="2ae1a-103">WMI Classes</span></span>

<span data-ttu-id="2ae1a-104">В этом разделе содержатся сведения о классе WMI и справочной странице.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-104">This section provides WMI class and reference page information.</span></span> <span data-ttu-id="2ae1a-105">Дополнительные сведения о получении данных класса или экземпляра см. в разделе [Управление сведениями о классе и экземпляре](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-105">For more information about how to retrieve class or instance data, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="2ae1a-106">В следующем списке перечислены, описаны и ссылки на сведения о конкретных классах WMI.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-106">The following list lists, describes, and provides links to specific WMI class information.</span></span> <span data-ttu-id="2ae1a-107">Дополнительные сведения и примеры кода сценариев использования классов WMI для получения различных операционных систем и данных оборудования см. в разделе [задачи WMI для сценариев и приложений](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-107">For more information and script code examples of using WMI classes to obtain a variety of operating system and hardware data, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="2ae1a-108">Примеры в C++ см. в разделе [примеры приложений WMI на c++](wmi-c---application-examples.md).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-108">For examples in C++, see [WMI C++ Application Examples](wmi-c---application-examples.md).</span></span> <span data-ttu-id="2ae1a-109">[При подключении к инструментарию WMI на удаленном компьютере](connecting-to-wmi-on-a-remote-computer.md) показано, как получить удаленные данные.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-109">[Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) shows how to obtain remote data.</span></span> <span data-ttu-id="2ae1a-110">Можно также использовать PowerShell для доступа к объектам WMI. Список классов WMI, включающих примеры кода PowerShell, см. [здесь](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-110">You can also use PowerShell do access WMI objects; for a list of WMI classes that include PowerShell code samples, see [here](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).</span></span>



| <span data-ttu-id="2ae1a-111">Section</span><span class="sxs-lookup"><span data-stu-id="2ae1a-111">Section</span></span>                                                    | <span data-ttu-id="2ae1a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="2ae1a-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ae1a-113">Системные классы WMI</span><span class="sxs-lookup"><span data-stu-id="2ae1a-113">WMI System Classes</span></span>](wmi-system-classes.md)               | <span data-ttu-id="2ae1a-114">Стандартные классы, которые включены в каждое пространство имен в ядре инструментарий управления Windows (WMI) (WMI).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-114">Predefined classes that are included in every namespace in the Windows Management Instrumentation (WMI) core.</span></span> <span data-ttu-id="2ae1a-115">Системный класс WMI можно распознать, поскольку имя начинается с двойного символа подчеркивания ( \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-115">You can recognize a WMI system class because the name begins with a double underscore (\_\_).</span></span> <span data-ttu-id="2ae1a-116">Эти классы предоставляют большую часть базовой функциональности для инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-116">These classes provide much of the basic functionality for WMI.</span></span> <span data-ttu-id="2ae1a-117">Системные классы WMI аналогичны системным таблицам в SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-117">The WMI system classes are similar in purpose to the system tables in SQL server.</span></span> |
| [<span data-ttu-id="2ae1a-118">Классы MSFT</span><span class="sxs-lookup"><span data-stu-id="2ae1a-118">MSFT Classes</span></span>](msft-classes.md)                           | <span data-ttu-id="2ae1a-119">Другие классы Майкрософт, которые предоставляют средства для работы с несколькими функциями операционной системы, например удаленные события и расширения политик.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-119">Other Microsoft classes that offer the means to manipulate several operating system features, such as remote events and policy extensions.</span></span> <span data-ttu-id="2ae1a-120">Классы [устранения неполадок WMI](wmi-troubleshooting.md) — это классы MSFT, предоставляющие данные об операциях WMI.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-120">The [WMI Troubleshooting](wmi-troubleshooting.md) classes are MSFT classes that provide data about WMI operations.</span></span>                                                                                               |
| [<span data-ttu-id="2ae1a-121">Классы CIM</span><span class="sxs-lookup"><span data-stu-id="2ae1a-121">CIM Classes</span></span>](cimclas.md)                                 | <span data-ttu-id="2ae1a-122">Классы схемы [*модель CIM (CIM)*](gloss-c.md) .</span><span class="sxs-lookup"><span data-stu-id="2ae1a-122">[*Common Information Model (CIM)*](gloss-c.md) schema classes.</span></span> <span data-ttu-id="2ae1a-123">Если вы хотите написать собственные классы WMI, можно наследовать от одного или нескольких из этих классов.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-123">If you want to write your own WMI classes then you can inherit from one or more of these classes.</span></span> <span data-ttu-id="2ae1a-124">[Классы Win32](/windows/desktop/CIMWin32Prov/win32-provider) инструментария WMI наследуются от классов CIM.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-124">The WMI [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) inherit from the CIM classes.</span></span>                                                                          |
| [<span data-ttu-id="2ae1a-125">Классы стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="2ae1a-125">Standard Consumer Classes</span></span>](standard-consumer-classes.md) | <span data-ttu-id="2ae1a-126">Набор потребителей событий WMI, которые активируют действие при получении произвольного события.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-126">A set of WMI event consumers which trigger an action upon receipt of an arbitrary event.</span></span> <span data-ttu-id="2ae1a-127">Дополнительные сведения см. в разделе [наблюдение за событиями](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-127">For more information, see [Monitoring Events](monitoring-events.md).</span></span>                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a><span data-ttu-id="2ae1a-128">Примеры кода центра сценариев класса WMI</span><span class="sxs-lookup"><span data-stu-id="2ae1a-128">WMI Class Scripting Center Code Examples</span></span>

<span data-ttu-id="2ae1a-129">Следующие примеры кода в центре сценариев затрагивают несколько классов WMI в нескольких пространствах имен.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-129">The following Scripting Center code samples affect multiple WMI classes across multiple namespaces.</span></span>



| <span data-ttu-id="2ae1a-130">Ссылка</span><span class="sxs-lookup"><span data-stu-id="2ae1a-130">Link</span></span>                                                                                                                                      | <span data-ttu-id="2ae1a-131">Описание</span><span class="sxs-lookup"><span data-stu-id="2ae1a-131">Description</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ae1a-132">Обозреватель WMI графического пользовательского интерфейса и генератор справки по методам WMI</span><span class="sxs-lookup"><span data-stu-id="2ae1a-132">GUI WMI Explorer and WMI Method Help Generator</span></span>](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | <span data-ttu-id="2ae1a-133">Пример скрипта, который предоставляет пользовательский интерфейс проводника WMI и генератора справки для методов WMI.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-133">Sample script that provides a GUI WMI Explorer and WMI Method Help Generator.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="2ae1a-134">Обозреватель WMI. Поиск пространств имен WMI</span><span class="sxs-lookup"><span data-stu-id="2ae1a-134">WMI Explorer Search WMI NameSpaces</span></span>](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | <span data-ttu-id="2ae1a-135">Позволяет пользователям искать классы во всех доступных пространствах имен на указанных компьютерах.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-135">Allows users to search for classes in all of the available namespaces on the specified computers.</span></span> <span data-ttu-id="2ae1a-136">Этот пример представляет собой виртуализации командной строки в образце проводника WMI GUI и может считаться расширением Get-WmiObject-List.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-136">This sample is the command-line verison of the GUI WMI Explorer sample, and may be considered an extension of Get-WmiObject -List.</span></span> |
| [<span data-ttu-id="2ae1a-137">Арпош средство администрирования системы Windows</span><span class="sxs-lookup"><span data-stu-id="2ae1a-137">Arposh Windows System Administration tool</span></span>](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | <span data-ttu-id="2ae1a-138">АВСА был создан с учетом системного администратора.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-138">AWSA was built with the System Administrator in mind.</span></span> <span data-ttu-id="2ae1a-139">Для устранения неполадок, связанных с Windows, требуется обширный набор средств и знаний.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-139">Troubleshooting Windows issues requires a vast array of tools and knowledge.</span></span> <span data-ttu-id="2ae1a-140">АВСА объединяет эти средства в одном централизованном расположении и добавляет дополнительные функции.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-140">AWSA brings those tools together in one central location and adds additional functionality.</span></span>       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a><span data-ttu-id="2ae1a-141">Соглашения об именовании для классов и свойств WMI</span><span class="sxs-lookup"><span data-stu-id="2ae1a-141">Naming Conventions for WMI Classes and Properties</span></span>

<span data-ttu-id="2ae1a-142">Имена свойств должны соответствовать синтаксису MOF-файл (MOF), определенному в распределенной задаче управления (DTMF).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-142">Property names must conform to the Managed Object Format (MOF) syntax defined by the Distributed Management Task Force (DTMF).</span></span> <span data-ttu-id="2ae1a-143">Начальные символы идентификатора должны быть от букв a до z и символа подчеркивания ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-143">The initial identifier characters must be from the letters a through z and the underscore character (\_).</span></span> <span data-ttu-id="2ae1a-144">Все дополнительные символы должны быть от букв a до z, символа подчеркивания и цифр от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-144">All additional characters must be from the letters a through z, the underscore character, and the numerals 0 through 9.</span></span> <span data-ttu-id="2ae1a-145">Дополнительные сведения см. в разделе Использование Юникода [спецификации CIM версии 2,2](https://www.dmtf.org/standards/cim).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-145">For more information, see the Unicode Usage section of the [CIM Specification Version 2.2](https://www.dmtf.org/standards/cim).</span></span>

<span data-ttu-id="2ae1a-146">Не следует использовать резервные слова SQL в именах классов и свойств.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-146">SQL reserve words should not be used in class and property names.</span></span> <span data-ttu-id="2ae1a-147">Полный список слов SQL Reserve и дополнительные сведения см. в разделе рекомендации [спецификации CIM версии 2,2](https://www.dmtf.org/standards/cim).</span><span class="sxs-lookup"><span data-stu-id="2ae1a-147">For a complete list of the SQL reserve words and for more information, see the Guidelines section of the [CIM Specification Version 2.2](https://www.dmtf.org/standards/cim).</span></span>

## <a name="document-conventions-for-a-wmi-class-reference-page"></a><span data-ttu-id="2ae1a-148">Соглашения о документе для страницы справочника по классам WMI</span><span class="sxs-lookup"><span data-stu-id="2ae1a-148">Document Conventions for a WMI Class Reference Page</span></span>

<span data-ttu-id="2ae1a-149">В этом разделе указаны и описаны соглашения о документе для страницы справочника по классам WMI.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-149">This section identifies and describes the document conventions for a WMI class reference page.</span></span>

<span data-ttu-id="2ae1a-150">Типичная эталонная страница содержит блок синтаксиса, таблицу методов и список свойств.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-150">A typical reference page contains a syntax block, methods table, and a properties list.</span></span>

-   <span data-ttu-id="2ae1a-151">Блок синтаксиса</span><span class="sxs-lookup"><span data-stu-id="2ae1a-151">Syntax block</span></span>

    <span data-ttu-id="2ae1a-152">Упрощенная версия MOF-кода, включающая имя класса, родительский класс (если таковые имеются) и свойства класса в алфавитном порядке с типами данных.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-152">A simplified version of MOF code that includes the class name, parent class (if any), and class properties, in alphabetical order, with data types.</span></span>

-   <span data-ttu-id="2ae1a-153">Таблица методов</span><span class="sxs-lookup"><span data-stu-id="2ae1a-153">Methods table</span></span>

    <span data-ttu-id="2ae1a-154">Если класс содержит методы, то методы перечисляются в таблице сразу после блока синтаксиса.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-154">If a class has methods, the methods are listed in the table immediately following the syntax block.</span></span> <span data-ttu-id="2ae1a-155">Каждый реализованный метод связан со страницей ссылки.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-155">Each implemented method is linked to a reference page.</span></span>

-   <span data-ttu-id="2ae1a-156">Список свойств</span><span class="sxs-lookup"><span data-stu-id="2ae1a-156">Properties list</span></span>

    <span data-ttu-id="2ae1a-157">Каждое свойство класса отображается с типом данных, типом доступа (только для чтения или для чтения и записи), квалификаторами и описанием свойства.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-157">Each class property is listed with a data type, access type (read-only or read/write), qualifiers, and a description of the property.</span></span>

## <a name="syntax-block"></a><span data-ttu-id="2ae1a-158">Блок синтаксиса</span><span class="sxs-lookup"><span data-stu-id="2ae1a-158">Syntax block</span></span>

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a><span data-ttu-id="2ae1a-159">Таблица методов</span><span class="sxs-lookup"><span data-stu-id="2ae1a-159">Methods table</span></span>



| <span data-ttu-id="2ae1a-160">\_Методы Win32 XYZ</span><span class="sxs-lookup"><span data-stu-id="2ae1a-160">Win32\_xyz methods</span></span> | <span data-ttu-id="2ae1a-161">Описание</span><span class="sxs-lookup"><span data-stu-id="2ae1a-161">Description</span></span>                                |
|--------------------|--------------------------------------------|
| <span data-ttu-id="2ae1a-162">*SomeMethod*</span><span class="sxs-lookup"><span data-stu-id="2ae1a-162">*SomeMethod*</span></span>       | <span data-ttu-id="2ae1a-163">Краткое описание того, что делает метод.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-163">Brief description of what the method does.</span></span> |



 

## <a name="properties-list"></a><span data-ttu-id="2ae1a-164">Список свойств</span><span class="sxs-lookup"><span data-stu-id="2ae1a-164">Properties list</span></span>

<dl> <dt>

<span data-ttu-id="2ae1a-165"><span id="abc"></span><span id="ABC"></span>ABC</span><span class="sxs-lookup"><span data-stu-id="2ae1a-165"><span id="abc"></span><span id="ABC"></span>abc</span></span>
</dt> <dd>

<span data-ttu-id="2ae1a-166">Тип данных: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2ae1a-166">Data type: **uint16**</span></span>

<span data-ttu-id="2ae1a-167">Тип доступа: показывает, есть ли у вас доступ к этому свойству для чтения и записи или только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-167">Access type: Shows whether you have read/write or read-only access to this property.</span></span>

<span data-ttu-id="2ae1a-168">Квалификаторы. при наличии отображает квалификаторы для свойства.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-168">Qualifiers: If present, shows the qualifiers for the property.</span></span> <span data-ttu-id="2ae1a-169">Например, **Key**, **reoverride**.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-169">For example, **Key**, **Override**.</span></span>

<span data-ttu-id="2ae1a-170">Описывает свойство и предоставляет сведения о наследовании для свойства.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-170">Describes the property and provides inheritance information for the property.</span></span> <span data-ttu-id="2ae1a-171">Например, это свойство наследуется от \**CIM \_* XYZ \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-171">For example, this property is inherited from \**CIM\_* xyz\*\*\*.</span></span> <span data-ttu-id="2ae1a-172">Существует ссылка на родительский класс, если корпорация Майкрософт предоставляет реализацию этого класса.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-172">There is a link to the parent class if Microsoft provides an implementation of that class.</span></span> <span data-ttu-id="2ae1a-173">Однако классы CIM недоступны.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-173">However, the CIM classes are not available.</span></span>

</dd> <dt>

<span data-ttu-id="2ae1a-174"><span id="def"></span><span id="DEF"></span>DEF</span><span class="sxs-lookup"><span data-stu-id="2ae1a-174"><span id="def"></span><span id="DEF"></span>def</span></span>
</dt> <dd>

<span data-ttu-id="2ae1a-175">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="2ae1a-175">Data type: **string**</span></span>

<span data-ttu-id="2ae1a-176">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="2ae1a-176">Access type: Read-only</span></span>

<span data-ttu-id="2ae1a-177">Описание свойства.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-177">Description of the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ae1a-178">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ae1a-178">Remarks</span></span>

<span data-ttu-id="2ae1a-179">Предоставляет дополнительные сведения о классе, если применимо.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-179">Gives more information about the class, if applicable.</span></span> <span data-ttu-id="2ae1a-180">Также предоставляет сведения о наследовании, если это применимо.</span><span class="sxs-lookup"><span data-stu-id="2ae1a-180">Also provides derivation information, if applicable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ae1a-181">См. также</span><span class="sxs-lookup"><span data-stu-id="2ae1a-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ae1a-182">Справочник по инструментарию WMI</span><span class="sxs-lookup"><span data-stu-id="2ae1a-182">WMI Reference</span></span>](wmi-reference.md)
</dt> </dl>

 

 
