---
description: Подготовка файла конфигурации ресурса
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Подготовка файла конфигурации ресурса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144665"
---
# <a name="preparing-a-resource-configuration-file"></a><span data-ttu-id="f43e3-103">Подготовка файла конфигурации ресурса</span><span class="sxs-lookup"><span data-stu-id="f43e3-103">Preparing a Resource Configuration File</span></span>

<span data-ttu-id="f43e3-104">Служебные программы компилятора МУИРКТ и RC, описанные в разделе [Служебные программы](resource-utilities.md) , предоставляют параметр командной строки, который позволяет указать файл конфигурации ресурса для базовых ресурсов языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-104">Both the MUIRCT and the RC Compiler utilities described in [Resource Utilities](resource-utilities.md) provide a command line option that allows you to specify a resource configuration file for the base language resources.</span></span> <span data-ttu-id="f43e3-105">Использование этого общедоступного, удобочитаемый XML-файл позволяет больше контролировать разделение ресурсов, чем можно получить с помощью обычных параметров командной строки программ.</span><span class="sxs-lookup"><span data-stu-id="f43e3-105">Use of this public, human-readable XML file allows more control over the splitting of resources than can be obtained using the regular command line switches of the utilities.</span></span> <span data-ttu-id="f43e3-106">Однако даже если вы не предложит файл конфигурации ресурсов в качестве входных данных, то файлы ресурсов LN и Language будут содержать данные конфигурации ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f43e3-106">However, even if you do not provide a resource configuration file as an input, the LN and language-specific resource files will contain resource configuration data.</span></span>

<span data-ttu-id="f43e3-107">Все файлы конфигурации ресурсов для приложений Win32 начинаются и заканчиваются одинаково:</span><span class="sxs-lookup"><span data-stu-id="f43e3-107">All resource configuration files for Win32 applications begin and end identically:</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



<span data-ttu-id="f43e3-108">В этом разделе рассматриваются аспекты схемы XML, которые полезны при создании неуправляемого кода в Windows Vista и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="f43e3-108">This topic focuses on the aspects of the XML schema that are useful in building unmanaged code on Windows Vista and later.</span></span> <span data-ttu-id="f43e3-109">В частности, это касается только поведения элемента win32Resources.</span><span class="sxs-lookup"><span data-stu-id="f43e3-109">In particular, it is only concerned with the behavior of the win32Resources element.</span></span>

## <a name="win32resources-element"></a><span data-ttu-id="f43e3-110">win32Resources, элемент</span><span class="sxs-lookup"><span data-stu-id="f43e3-110">win32Resources Element</span></span>

<span data-ttu-id="f43e3-111">Элемент win32Resources содержит атрибуты, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f43e3-111">The win32Resources element has the attributes described in the following table.</span></span>



| <span data-ttu-id="f43e3-112">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="f43e3-112">Attribute name</span></span>           | <span data-ttu-id="f43e3-113">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f43e3-113">Mandatory</span></span> | <span data-ttu-id="f43e3-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f43e3-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f43e3-115">fileType</span><span class="sxs-lookup"><span data-stu-id="f43e3-115">fileType</span></span>                 | <span data-ttu-id="f43e3-116">Нет</span><span class="sxs-lookup"><span data-stu-id="f43e3-116">No</span></span>        | <span data-ttu-id="f43e3-117">Тип файла.</span><span class="sxs-lookup"><span data-stu-id="f43e3-117">Type of file.</span></span> <span data-ttu-id="f43e3-118">Всегда должно быть "Application".</span><span class="sxs-lookup"><span data-stu-id="f43e3-118">Should always be "Application".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="f43e3-119">контрольная сумма</span><span class="sxs-lookup"><span data-stu-id="f43e3-119">checksum</span></span>                 | <span data-ttu-id="f43e3-120">Нет</span><span class="sxs-lookup"><span data-stu-id="f43e3-120">No</span></span>        | <span data-ttu-id="f43e3-121">Значение контрольной суммы отображается в данных конфигурации ресурсов для файлов ресурсов LN и Language.</span><span class="sxs-lookup"><span data-stu-id="f43e3-121">Checksum value to appear in the resource configuration data of the LN file and language-specific resource files.</span></span> <span data-ttu-id="f43e3-122">Например, этот атрибут позволяет скопировать контрольную сумму из одного файла ресурсов, зависящего от языка, с помощью соглашения для английского (США) и разместив контрольную сумму в другом файле ресурсов, относящемся к конкретному языку.</span><span class="sxs-lookup"><span data-stu-id="f43e3-122">For example, this attribute allows you to copy the checksum from a single language-specific resource file, by convention the one for English (United States), and place the checksum in a different language-specific resource file.</span></span> <span data-ttu-id="f43e3-123">Контрольную сумму можно указать в виде шестнадцатеричной числовой строки длиной не более 32 символов.</span><span class="sxs-lookup"><span data-stu-id="f43e3-123">The checksum can be specified as a hexadecimal number string that is no longer than 32 characters.</span></span> <span data-ttu-id="f43e3-124">Числовое значение должно быть содержаться в 128-разрядном числе.</span><span class="sxs-lookup"><span data-stu-id="f43e3-124">The numerical value must be containable in a 128-bit number.</span></span> |
| <span data-ttu-id="f43e3-125">Язык</span><span class="sxs-lookup"><span data-stu-id="f43e3-125">language</span></span>                 | <span data-ttu-id="f43e3-126">Нет</span><span class="sxs-lookup"><span data-stu-id="f43e3-126">No</span></span>        | <span data-ttu-id="f43e3-127">Язык, указанный в формате имени, совместимом с RFC 4646 (Windows Vista и более поздние версии), например en-US для английского языка (США).</span><span class="sxs-lookup"><span data-stu-id="f43e3-127">Language specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="f43e3-128">ултиматефаллбакклангуаже</span><span class="sxs-lookup"><span data-stu-id="f43e3-128">ultimateFallbackLanguage</span></span> | <span data-ttu-id="f43e3-129">Нет</span><span class="sxs-lookup"><span data-stu-id="f43e3-129">No</span></span>        | <span data-ttu-id="f43e3-130">Язык для вставки данных конфигурации ресурсов для LN-файла, представляющий конечный язык, который будет использоваться в поиске соответствующего файла ресурсов для конкретного языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-130">Language to insert into the resource configuration data for the LN file, representing the ultimate fallback language to use in a search for a corresponding language-specific resource file.</span></span> <span data-ttu-id="f43e3-131">Если загрузчику ресурсов не удается загрузить запрошенный файл ресурсов из предпочтительных языков пользовательского интерфейса потока, в качестве последней попытки используется конечный язык.</span><span class="sxs-lookup"><span data-stu-id="f43e3-131">If the resource loader fails to load a requested resource file from the thread preferred UI languages, it uses an ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="f43e3-132">Язык указывается с использованием формата имени, совместимого с RFC 4646 (Windows Vista и более поздние версии), например en-US для английского языка (США).</span><span class="sxs-lookup"><span data-stu-id="f43e3-132">The language is specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>       |
| <span data-ttu-id="f43e3-133">ултиматефаллбакклокатион</span><span class="sxs-lookup"><span data-stu-id="f43e3-133">ultimateFallbackLocation</span></span> | <span data-ttu-id="f43e3-134">Нет</span><span class="sxs-lookup"><span data-stu-id="f43e3-134">No</span></span>        | <span data-ttu-id="f43e3-135">Резервное расположение.</span><span class="sxs-lookup"><span data-stu-id="f43e3-135">Fallback location.</span></span> <span data-ttu-id="f43e3-136">Укажите "internal", если окончательные резервные ресурсы компилируются в LN File.</span><span class="sxs-lookup"><span data-stu-id="f43e3-136">Specify "internal" if ultimate fallback resources are compiled into the LN file.</span></span> <span data-ttu-id="f43e3-137">Укажите "External" (по умолчанию), если LN-файл ссылается на файл ресурсов, зависящий от языка, для своих окончательных резервных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f43e3-137">Specify "external" (default) if the LN file is to reference a language-specific resource file for its ultimate fallback resources.</span></span>                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="f43e3-138">В файле конфигурации ресурса элемент win32Resources содержит вложенные элементы, описанные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="f43e3-138">In the resource configuration file, the win32Resources element has the sub-elements described in the next table.</span></span>



| <span data-ttu-id="f43e3-139">Имя элемента</span><span class="sxs-lookup"><span data-stu-id="f43e3-139">Element Name</span></span>       | <span data-ttu-id="f43e3-140">Описание</span><span class="sxs-lookup"><span data-stu-id="f43e3-140">Description</span></span>                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f43e3-141">localizedResources</span><span class="sxs-lookup"><span data-stu-id="f43e3-141">localizedResources</span></span> | <span data-ttu-id="f43e3-142">Ресурсы, инкапсулирующие сведения о типах ресурсов и отдельных ресурсах, содержащихся в файле ресурсов конкретного языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-142">Resources that encapsulate information about the resource types and individual resources contained in a language-specific resource file.</span></span> |
| <span data-ttu-id="f43e3-143">неутралресаурцес</span><span class="sxs-lookup"><span data-stu-id="f43e3-143">neutralResources</span></span>   | <span data-ttu-id="f43e3-144">Ресурсы, инкапсулирующие сведения о типах ресурсов, содержащихся в LN файле.</span><span class="sxs-lookup"><span data-stu-id="f43e3-144">Resources that encapsulate information about the resource types contained in an LN file.</span></span>                                                 |



 

## <a name="localizedresources-element"></a><span data-ttu-id="f43e3-145">localizedResources, элемент</span><span class="sxs-lookup"><span data-stu-id="f43e3-145">localizedResources Element</span></span>

<span data-ttu-id="f43e3-146">Локализованный элемент Resources.</span><span class="sxs-lookup"><span data-stu-id="f43e3-146">Localized resources element.</span></span> <span data-ttu-id="f43e3-147">По умолчанию этот элемент не имеет атрибутов и только одного типа вложенного элемента.</span><span class="sxs-lookup"><span data-stu-id="f43e3-147">By default, this element has no attributes and only one type of sub-element.</span></span> <span data-ttu-id="f43e3-148">Это просто контейнер для элементов resourceType.</span><span class="sxs-lookup"><span data-stu-id="f43e3-148">It is just a container for resourceType elements.</span></span>



| <span data-ttu-id="f43e3-149">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="f43e3-149">Attribute Name</span></span> | <span data-ttu-id="f43e3-150">Описание</span><span class="sxs-lookup"><span data-stu-id="f43e3-150">Description</span></span>                                                                    |
|----------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="f43e3-151">тип_ресурса</span><span class="sxs-lookup"><span data-stu-id="f43e3-151">resourceType</span></span>   | <span data-ttu-id="f43e3-152">Тип отдельного ресурса, содержащегося в файле ресурсов, зависящем от языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-152">Type of an individual resource contained in a language-specific resource file.</span></span> |



 

## <a name="neutralresources-element"></a><span data-ttu-id="f43e3-153">Неутралресаурцес, элемент</span><span class="sxs-lookup"><span data-stu-id="f43e3-153">neutralResources Element</span></span>

<span data-ttu-id="f43e3-154">Нейтральный элемент Resources.</span><span class="sxs-lookup"><span data-stu-id="f43e3-154">Neutral resources element.</span></span> <span data-ttu-id="f43e3-155">Этот элемент является просто контейнером для элементов resourceType.</span><span class="sxs-lookup"><span data-stu-id="f43e3-155">This element is just a container for resourceType elements.</span></span>



| <span data-ttu-id="f43e3-156">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="f43e3-156">Attribute Name</span></span> | <span data-ttu-id="f43e3-157">Описание</span><span class="sxs-lookup"><span data-stu-id="f43e3-157">Description</span></span>                                        |
|----------------|----------------------------------------------------|
| <span data-ttu-id="f43e3-158">тип_ресурса</span><span class="sxs-lookup"><span data-stu-id="f43e3-158">resourceType</span></span>   | <span data-ttu-id="f43e3-159">Тип одного ресурса, содержащегося в LN-файле.</span><span class="sxs-lookup"><span data-stu-id="f43e3-159">Type of a single resource contained in an LN file.</span></span> |



 

## <a name="resourcetype-element"></a><span data-ttu-id="f43e3-160">resourceType, элемент</span><span class="sxs-lookup"><span data-stu-id="f43e3-160">resourceType Element</span></span>

<span data-ttu-id="f43e3-161">Элемент resourceType инкапсулирует сведения об отдельном типе ресурса или отдельном ресурсе.</span><span class="sxs-lookup"><span data-stu-id="f43e3-161">The resourceType element encapsulates information about a single resource type or individual resource.</span></span> <span data-ttu-id="f43e3-162">Он имеет перечисленные ниже атрибуты.</span><span class="sxs-lookup"><span data-stu-id="f43e3-162">It has the attributes listed below.</span></span>

> [!Caution]  
> <span data-ttu-id="f43e3-163">Некоторые дефекты конфигурации ресурсов перехватываются только компилятором RC или МУИРКТ, в зависимости от файла входного ресурса или содержимого двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="f43e3-163">Some resource configuration defects are caught only by RC Compiler or MUIRCT, depending on the input resource file or binary file content.</span></span> <span data-ttu-id="f43e3-164">Ошибки типа ресурса в файле конфигурации ресурсов, которые не существуют во входном файле, не перехватываются, что приводит к непредвиденному поведению.</span><span class="sxs-lookup"><span data-stu-id="f43e3-164">The resourceType errors in the resource configuration file that do not exist in the input file are not caught, resulting in unexpected behavior.</span></span> <span data-ttu-id="f43e3-165">Пользователи могут использовать поврежденный файл конфигурации ресурсов и не знакомы с тем, чтобы они предприняли двоичные файлы, которые используют поврежденные части файла конфигурации ресурсов, что создает внешний вид, который прерывается из текущих двоичных файлов.</span><span class="sxs-lookup"><span data-stu-id="f43e3-165">Users can be using a defective resource configuration file and do not know until they introduce binaries that use the broken parts of the resource configuration file, which creates the appearance that the breaks are from the current binaries.</span></span>

 



| <span data-ttu-id="f43e3-166">Имя атрибута</span><span class="sxs-lookup"><span data-stu-id="f43e3-166">Attribute name</span></span> | <span data-ttu-id="f43e3-167">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f43e3-167">Mandatory</span></span> | <span data-ttu-id="f43e3-168">Описание</span><span class="sxs-lookup"><span data-stu-id="f43e3-168">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f43e3-169">типенамеид</span><span class="sxs-lookup"><span data-stu-id="f43e3-169">typeNameId</span></span>     | <span data-ttu-id="f43e3-170">Да</span><span class="sxs-lookup"><span data-stu-id="f43e3-170">Yes</span></span>       | <span data-ttu-id="f43e3-171">Имя типа или идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="f43e3-171">Type name or identifier for the resource.</span></span> <span data-ttu-id="f43e3-172">Укажите строковое имя или число.</span><span class="sxs-lookup"><span data-stu-id="f43e3-172">Specify a string name or a number.</span></span> <span data-ttu-id="f43e3-173">Если используется число, добавьте в начало строки знак " \# ", чтобы указать, что он представляет число.</span><span class="sxs-lookup"><span data-stu-id="f43e3-173">If using a number, prepend the string with a "\#" to indicate that it represents a number.</span></span> <span data-ttu-id="f43e3-174">Каждый элемент resourceType должен иметь только один атрибут *типенамеид* .</span><span class="sxs-lookup"><span data-stu-id="f43e3-174">Each resourceType element must have only one *typeNameId* attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="f43e3-175">itemName</span><span class="sxs-lookup"><span data-stu-id="f43e3-175">itemName</span></span>       | <span data-ttu-id="f43e3-176">Нет</span><span class="sxs-lookup"><span data-stu-id="f43e3-176">No</span></span>        | <span data-ttu-id="f43e3-177">Строка имени элемента для ресурса, помещаемого в файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-177">Item name string for the resource, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="f43e3-178">Можно указать несколько имен, разделенных пробелами, например "HTML МОФДАТА".</span><span class="sxs-lookup"><span data-stu-id="f43e3-178">You can specify multiple names, separated by white spaces, for example, "HTML MOFDATA".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="f43e3-179">itemId</span><span class="sxs-lookup"><span data-stu-id="f43e3-179">itemId</span></span>         | <span data-ttu-id="f43e3-180">Нет</span><span class="sxs-lookup"><span data-stu-id="f43e3-180">No</span></span>        | <span data-ttu-id="f43e3-181">Идентификатор отдельного элемента ресурса, помещаемого в файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-181">Identifier of individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="f43e3-182">Элемент можно указать в виде диапазона (например, "1-12") или отдельных идентификаторов, разделенных пробелами (например, "1 3 4").</span><span class="sxs-lookup"><span data-stu-id="f43e3-182">The item can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="f43e3-183">stringId</span><span class="sxs-lookup"><span data-stu-id="f43e3-183">stringId</span></span>       | <span data-ttu-id="f43e3-184">Нет</span><span class="sxs-lookup"><span data-stu-id="f43e3-184">No</span></span>        | <span data-ttu-id="f43e3-185">Идентификатор строки для отдельного элемента ресурса, помещаемый в файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-185">String identifier for individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="f43e3-186">Строку можно указать в виде диапазона (например, "1-12") или отдельных идентификаторов, разделенных пробелами (например, "1 3 4"). Этот атрибут позволяет указывать как локализуемые, так и нелокализуемые записи в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="f43e3-186">The string can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").This attribute allows the specification of both localizable and nonlocalizable string table entries.</span></span> <span data-ttu-id="f43e3-187">Его необходимо использовать в сочетании со значением *типенамеид* , равное "6", обозначая тип ресурса записи в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="f43e3-187">It must be used in conjunction with the *typeNameId* value of "6", denoting a string table entry resource type.</span></span><br/> <span data-ttu-id="f43e3-188">Строки хранятся в блоках 16 в таблице строк.</span><span class="sxs-lookup"><span data-stu-id="f43e3-188">Strings are stored in blocks of 16 in a string table.</span></span> <span data-ttu-id="f43e3-189">Например, строки от 0 до 15 хранятся в одном блоке элементов ресурсов, и на них можно ссылаться в файле конфигурации ресурсов как *ItemId* 1 или как *stringId* "0-15".</span><span class="sxs-lookup"><span data-stu-id="f43e3-189">For example, strings 0 to 15 are stored in a single resource item block and can be referenced in the resource configuration file as *itemId* 1, or as *stringId* "0-15".</span></span> <span data-ttu-id="f43e3-190">Например, если имеется пять локализуемых строк и три нелокализуемые строки, необходимо назначить строковые идентификаторы 0-4 для локализуемых строк и идентификаторы строк 16-18 для нелокализуемых строк.</span><span class="sxs-lookup"><span data-stu-id="f43e3-190">For example, if there are five localizable strings and three nonlocalizable strings, you should assign string identifiers 0-4 for the localizable strings, and string identifiers 16-18 for the nonlocalizable strings.</span></span> <span data-ttu-id="f43e3-191">Если не организовать строки таким образом, затронутые блоки строк помещаются как в LN-файл, так и в файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-191">If you do not organize strings this way, the affected blocks of strings are placed in both the LN file and the language-specific resource file.</span></span><br/> |



 

<span data-ttu-id="f43e3-192">Если указать атрибуты *ItemName*, *ItemId* и/или *stringId* для определенного типа ресурса в элементе локализедресаурце, то только указанные элементы или строки для указанного типа ресурса помещаются в файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-192">If you specify the *itemName*, *itemId*, and/or *stringId* attributes for a particular resource type under the localizedResource element, only these specified items or strings for the designated resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="f43e3-193">Если элемент resourceType указан без явного имени элемента, идентификатора элемента или идентификатора строки, все элементы указанного типа ресурса помещаются в файл ресурсов, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="f43e3-193">If a resourceType element is specified without any explicit item name, item identifier, or string identifier, all items of the specified resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="f43e3-194">Элементы или типы, не перечисленные ни в одном из элементов Локализедресаурце, помещаются в LN File.</span><span class="sxs-lookup"><span data-stu-id="f43e3-194">Items or types not listed in any localizedResource element are placed in the LN file.</span></span>

<span data-ttu-id="f43e3-195">Ниже приведены стандартные типы ресурсов и их числовые идентификаторы.</span><span class="sxs-lookup"><span data-stu-id="f43e3-195">The following are the standard resource types and their numeric identifiers:</span></span>

-   <span data-ttu-id="f43e3-196">CURSOR (1)</span><span class="sxs-lookup"><span data-stu-id="f43e3-196">CURSOR(1)</span></span>
-   <span data-ttu-id="f43e3-197">ТОЧЕЧНЫЙ РИСУНОК (2)</span><span class="sxs-lookup"><span data-stu-id="f43e3-197">BITMAP(2)</span></span>
-   <span data-ttu-id="f43e3-198">ЗНАЧОК (3)</span><span class="sxs-lookup"><span data-stu-id="f43e3-198">ICON(3)</span></span>
-   <span data-ttu-id="f43e3-199">МЕНЮ (4)</span><span class="sxs-lookup"><span data-stu-id="f43e3-199">MENU(4)</span></span>
-   <span data-ttu-id="f43e3-200">ДИАЛОГОВОЕ ОКНО (5)</span><span class="sxs-lookup"><span data-stu-id="f43e3-200">DIALOG(5)</span></span>
-   <span data-ttu-id="f43e3-201">СТРОКА (6)</span><span class="sxs-lookup"><span data-stu-id="f43e3-201">STRING(6)</span></span>
-   <span data-ttu-id="f43e3-202">ФОНТДИР (7)</span><span class="sxs-lookup"><span data-stu-id="f43e3-202">FONTDIR(7)</span></span>
-   <span data-ttu-id="f43e3-203">ШРИФТ (8)</span><span class="sxs-lookup"><span data-stu-id="f43e3-203">FONT(8)</span></span>
-   <span data-ttu-id="f43e3-204">УСКОРИТЕЛИ (9)</span><span class="sxs-lookup"><span data-stu-id="f43e3-204">ACCELERATORS(9)</span></span>
-   <span data-ttu-id="f43e3-205">RCDATA (10)</span><span class="sxs-lookup"><span data-stu-id="f43e3-205">RCDATA(10)</span></span>
-   <span data-ttu-id="f43e3-206">МЕССАЖЕТАБЛЕ (11)</span><span class="sxs-lookup"><span data-stu-id="f43e3-206">MESSAGETABLE(11)</span></span>
-   <span data-ttu-id="f43e3-207">ГРУППИРОВАНие \_ курсора (12)</span><span class="sxs-lookup"><span data-stu-id="f43e3-207">GROUP\_CURSOR(12)</span></span>
-   <span data-ttu-id="f43e3-208">\_Значок группы (14)</span><span class="sxs-lookup"><span data-stu-id="f43e3-208">GROUP\_ICON(14)</span></span>
-   <span data-ttu-id="f43e3-209">ВЕРСИЯ (16)</span><span class="sxs-lookup"><span data-stu-id="f43e3-209">VERSION(16)</span></span>
-   <span data-ttu-id="f43e3-210">HTML (23)</span><span class="sxs-lookup"><span data-stu-id="f43e3-210">HTML(23)</span></span>

## <a name="example"></a><span data-ttu-id="f43e3-211">Пример</span><span class="sxs-lookup"><span data-stu-id="f43e3-211">Example</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a><span data-ttu-id="f43e3-212">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f43e3-212">Remarks</span></span>

<span data-ttu-id="f43e3-213">Если включить в элемент Неутралресаурцес любой тип ресурса ICON (3), DIALOG (5), STRING (6) или VERSION (16), необходимо дублировать эту запись в элементе localizedResources.</span><span class="sxs-lookup"><span data-stu-id="f43e3-213">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element.</span></span> <span data-ttu-id="f43e3-214">Это показано в приведенном выше примере, где тип ресурса 16 отображается в разделах как нейтральные, так и локализованные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="f43e3-214">You can see this illustrated in the example above, where resource type 16 appears in both neutral and localized resources sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f43e3-215">См. также</span><span class="sxs-lookup"><span data-stu-id="f43e3-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f43e3-216">Подготовка ресурсов</span><span class="sxs-lookup"><span data-stu-id="f43e3-216">Preparing Resources</span></span>](preparing-resources.md)
</dt> </dl>

 

 




