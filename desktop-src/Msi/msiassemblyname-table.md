---
description: В таблице Мсиассембли и таблице Мсиассемблинаме указываются параметры установщик Windows для сборок среды CLR и сборок Win32.
ms.assetid: cfe9a0a3-e40f-4c59-b2e4-ad7654528e3b
title: Таблица Мсиассемблинаме
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12008682c82d7be20ed8713d8dc1c416f9c7065c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664586"
---
# <a name="msiassemblyname-table"></a><span data-ttu-id="a99d2-103">Таблица Мсиассемблинаме</span><span class="sxs-lookup"><span data-stu-id="a99d2-103">MsiAssemblyName Table</span></span>

<span data-ttu-id="a99d2-104">В [таблице мсиассембли](msiassembly-table.md) и таблице мсиассемблинаме указываются параметры установщик Windows для сборок среды CLR и сборок Win32.</span><span class="sxs-lookup"><span data-stu-id="a99d2-104">The [MsiAssembly Table](msiassembly-table.md) and MsiAssemblyName Table specify Windows Installer settings for common language runtime assemblies and Win32 assemblies.</span></span> <span data-ttu-id="a99d2-105">Дополнительные сведения см. в разделе [Установка сборок в глобальный кэш сборок](installation-of-assemblies-to-the-global-assembly-cache.md) и [Установка сборок Win32](installation-of-win32-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a99d2-105">For information see, [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md) and [Installation of Win32 Assemblies](installation-of-win32-assemblies.md).</span></span>

<span data-ttu-id="a99d2-106">В таблице Мсиассемблинаме указана схема для элементов имени строгого кэша сборок для платформа .NET Framework или сборки Win32.</span><span class="sxs-lookup"><span data-stu-id="a99d2-106">The MsiAssemblyName Table specifies the schema for the elements of a strong assembly cache name for a .NET Framework or Win32 assembly.</span></span> <span data-ttu-id="a99d2-107">Имя создается путем добавления всех элементов с одним и тем же ключом компонента \_ .</span><span class="sxs-lookup"><span data-stu-id="a99d2-107">The name is constructed by appending all elements with the same Component\_ key.</span></span> <span data-ttu-id="a99d2-108">См. следующий пример.</span><span class="sxs-lookup"><span data-stu-id="a99d2-108">See the following example.</span></span>

<span data-ttu-id="a99d2-109">Установщик Windows может устанавливать сборки Win32 как [Параллельные сборки](side-by-side-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a99d2-109">Windows Installer can install Win32 assemblies as [side-by-side assemblies](side-by-side-assemblies.md).</span></span> <span data-ttu-id="a99d2-110">Дополнительные сведения см. в разделе [параллельная сборка API](../sbscs/side-by-side-assembly-api.md).</span><span class="sxs-lookup"><span data-stu-id="a99d2-110">For more information, see the [Side-by-Side Assembly API](../sbscs/side-by-side-assembly-api.md).</span></span>

<span data-ttu-id="a99d2-111">Таблица Мсиассемблинаме содержит следующие столбцы.</span><span class="sxs-lookup"><span data-stu-id="a99d2-111">The MsiAssemblyName Table has the following columns.</span></span>



| <span data-ttu-id="a99d2-112">Столбец</span><span class="sxs-lookup"><span data-stu-id="a99d2-112">Column</span></span>      | <span data-ttu-id="a99d2-113">Type</span><span class="sxs-lookup"><span data-stu-id="a99d2-113">Type</span></span>                         | <span data-ttu-id="a99d2-114">Ключ</span><span class="sxs-lookup"><span data-stu-id="a99d2-114">Key</span></span> | <span data-ttu-id="a99d2-115">Допускает значения NULL</span><span class="sxs-lookup"><span data-stu-id="a99d2-115">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="a99d2-116">Компонент\_</span><span class="sxs-lookup"><span data-stu-id="a99d2-116">Component\_</span></span> | [<span data-ttu-id="a99d2-117">Идентификатор</span><span class="sxs-lookup"><span data-stu-id="a99d2-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="a99d2-118">Да</span><span class="sxs-lookup"><span data-stu-id="a99d2-118">Y</span></span>   | <span data-ttu-id="a99d2-119">Нет</span><span class="sxs-lookup"><span data-stu-id="a99d2-119">N</span></span>        |
| <span data-ttu-id="a99d2-120">Имя</span><span class="sxs-lookup"><span data-stu-id="a99d2-120">Name</span></span>        | [<span data-ttu-id="a99d2-121">Text</span><span class="sxs-lookup"><span data-stu-id="a99d2-121">Text</span></span>](text.md)             | <span data-ttu-id="a99d2-122">Да</span><span class="sxs-lookup"><span data-stu-id="a99d2-122">Y</span></span>   | <span data-ttu-id="a99d2-123">Нет</span><span class="sxs-lookup"><span data-stu-id="a99d2-123">N</span></span>        |
| <span data-ttu-id="a99d2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a99d2-124">Value</span></span>       | [<span data-ttu-id="a99d2-125">Text</span><span class="sxs-lookup"><span data-stu-id="a99d2-125">Text</span></span>](text.md)             | <span data-ttu-id="a99d2-126">Нет</span><span class="sxs-lookup"><span data-stu-id="a99d2-126">N</span></span>   | <span data-ttu-id="a99d2-127">Нет</span><span class="sxs-lookup"><span data-stu-id="a99d2-127">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="a99d2-128">Столбцы</span><span class="sxs-lookup"><span data-stu-id="a99d2-128">Columns</span></span>

<dl> <dt>

<span data-ttu-id="a99d2-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>См\_</span><span class="sxs-lookup"><span data-stu-id="a99d2-129"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="a99d2-130">Ключ в [таблицу Component](component-table.md) , указывающий компонент установщик Windows, который содержит эту сборку.</span><span class="sxs-lookup"><span data-stu-id="a99d2-130">Key into the [Component Table](component-table.md) that specifies the Windows Installer component that contains this assembly.</span></span>

</dd> <dt>

<span data-ttu-id="a99d2-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Безымян</span><span class="sxs-lookup"><span data-stu-id="a99d2-131"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="a99d2-132">Имя атрибута, связанного со значением, указанным в столбце значение.</span><span class="sxs-lookup"><span data-stu-id="a99d2-132">Name of the attribute associated with the value specified in the Value column.</span></span>

</dd> <dt>

<span data-ttu-id="a99d2-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Значений</span><span class="sxs-lookup"><span data-stu-id="a99d2-133"><span id="Value"></span><span id="value"></span><span id="VALUE"></span>Value</span></span>
</dt> <dd>

<span data-ttu-id="a99d2-134">Значение, связанное с именем, указанным в столбце имя.</span><span class="sxs-lookup"><span data-stu-id="a99d2-134">Value associated with the name specified in the Name column.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a99d2-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a99d2-135">Remarks</span></span>

<span data-ttu-id="a99d2-136">Информация, созданная в таблице Мсиассемблинаме, должна соответствовать информации в файле манифеста сборки.</span><span class="sxs-lookup"><span data-stu-id="a99d2-136">The information authored into the MsiAssemblyName Table must match the information in the manifest file of the assembly.</span></span> <span data-ttu-id="a99d2-137">Если данные в манифесте и таблице Мсиассемблинаме не совпадают, удаление приложения может привести к удалению сборки на компьютере.</span><span class="sxs-lookup"><span data-stu-id="a99d2-137">If the information in the manifest and MsiAssemblyName Table do not match, removal of the application can leave the assembly on the computer.</span></span>

<span data-ttu-id="a99d2-138">Для сборок Win32 в таблице Мсиассемблинаме должна быть строка для каждой из следующих записей в поле Name: Type, Name, Version, Language, publicKeyToken и processorArchitecture.</span><span class="sxs-lookup"><span data-stu-id="a99d2-138">For Win32 assemblies there must be a row in the MsiAssemblyName Table for each of the following entries in the Name field: type, name, version, language, publicKeyToken and processorArchitecture.</span></span> <span data-ttu-id="a99d2-139">Соответствующее значение для каждого имени можно указать в поле значение.</span><span class="sxs-lookup"><span data-stu-id="a99d2-139">The corresponding value for each name can be entered into the Value field.</span></span> <span data-ttu-id="a99d2-140">Пары "имя-значение" в таблице Мсиассемблинаме должны соответствовать атрибутам type, Name, Version, Language, publicKeyToken и processorArchitecture в манифесте сборки.</span><span class="sxs-lookup"><span data-stu-id="a99d2-140">The name-value pairs in MsiAssemblyName Table must match the type, name, version, language, publicKeyToken and processorArchitecture attributes in the manifest of the assembly.</span></span>

<span data-ttu-id="a99d2-141">Для частных сборок среды CLR (.NET Фрамеворкверсионс 1,0 и 1,1) таблица Мсиассемблинаме должна содержать строку для каждой из следующих записей в поле имени: имя, версия и язык и региональные параметры.</span><span class="sxs-lookup"><span data-stu-id="a99d2-141">For private common language runtime assemblies (.NET Frameworkversions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, and Culture.</span></span> <span data-ttu-id="a99d2-142">Соответствующее значение для каждого имени можно указать в поле значение.</span><span class="sxs-lookup"><span data-stu-id="a99d2-142">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="a99d2-143">Для глобальных сборок среды CLR (платформа .NET Framework версий 1,0 и 1,1) таблица Мсиассемблинаме должна содержать строку для каждой из следующих записей в поле имени: Name, Version, Culture и PublicKeyToken.</span><span class="sxs-lookup"><span data-stu-id="a99d2-143">For global common language runtime assemblies (.NET Framework versions 1.0 and 1.1), the MsiAssemblyName Table must include a row for each of the following entries in the Name field: Name, Version, Culture, and PublicKeyToken.</span></span> <span data-ttu-id="a99d2-144">Соответствующее значение для каждого имени можно указать в поле значение.</span><span class="sxs-lookup"><span data-stu-id="a99d2-144">The corresponding value for each Name can be entered into the Value field.</span></span>

<span data-ttu-id="a99d2-145">Платформа .NET Framework версии 1,1 — это минимальная версия, которую можно использовать для выполнения обновления на месте глобальной сборки среды CLR.</span><span class="sxs-lookup"><span data-stu-id="a99d2-145">The .NET Framework version 1.1 is the minimum version that can be used to perform an in-place update of a global common language runtime assembly.</span></span> <span data-ttu-id="a99d2-146">Можно проверить свойство [**мсинетассемблисуппорт**](msinetassemblysupport.md) для версии.</span><span class="sxs-lookup"><span data-stu-id="a99d2-146">You can check the [**MsiNetAssemblySupport**](msinetassemblysupport.md) property for the version.</span></span> <span data-ttu-id="a99d2-147">Таблица Мсиассемблинаме также должна иметь поле FileVersion, так как этот тип обновления сборки изменяет только FileVersion.</span><span class="sxs-lookup"><span data-stu-id="a99d2-147">The MsiAssemblyName Table must also have a FileVersion field because this type of assembly update only changes the FileVersion.</span></span> <span data-ttu-id="a99d2-148">Дополнительные сведения см. в разделе [Обновление сборок](updating-assemblies.md).</span><span class="sxs-lookup"><span data-stu-id="a99d2-148">For more information, see [Updating Assemblies](updating-assemblies.md).</span></span>

<span data-ttu-id="a99d2-149">Например, манифест сборки для компонента a может иметь раздел assemblyIdentity, как показано ниже для сборки Win32.</span><span class="sxs-lookup"><span data-stu-id="a99d2-149">For example, the assembly manifest for ComponentA might have an assemblyIdentity section as follows for a Win32 assembly.</span></span>

``` syntax
<assemblyIdentity type="win32" name="ms-sxstest-simple" version="1.0.0.0" language="en" publicKeyToken="1111111111222222" processorArchitecture="x86"/>
```

<span data-ttu-id="a99d2-150">В этом случае заполните таблицу Мсиассемблинаме следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a99d2-150">In this case, populate the MsiAssemblyName Table as follows.</span></span>



| <span data-ttu-id="a99d2-151">Компонент</span><span class="sxs-lookup"><span data-stu-id="a99d2-151">Component</span></span>  | <span data-ttu-id="a99d2-152">Имя</span><span class="sxs-lookup"><span data-stu-id="a99d2-152">Name</span></span>                  | <span data-ttu-id="a99d2-153">Значение</span><span class="sxs-lookup"><span data-stu-id="a99d2-153">Value</span></span>             |
|------------|-----------------------|-------------------|
| <span data-ttu-id="a99d2-154">Компонент а</span><span class="sxs-lookup"><span data-stu-id="a99d2-154">ComponentA</span></span> | <span data-ttu-id="a99d2-155">тип</span><span class="sxs-lookup"><span data-stu-id="a99d2-155">type</span></span>                  | <span data-ttu-id="a99d2-156">Платформа</span><span class="sxs-lookup"><span data-stu-id="a99d2-156">win32</span></span>             |
| <span data-ttu-id="a99d2-157">Компонент а</span><span class="sxs-lookup"><span data-stu-id="a99d2-157">ComponentA</span></span> | <span data-ttu-id="a99d2-158">name</span><span class="sxs-lookup"><span data-stu-id="a99d2-158">name</span></span>                  | <span data-ttu-id="a99d2-159">MS-сксстест-Simple</span><span class="sxs-lookup"><span data-stu-id="a99d2-159">ms-sxstest-simple</span></span> |
| <span data-ttu-id="a99d2-160">Компонент а</span><span class="sxs-lookup"><span data-stu-id="a99d2-160">ComponentA</span></span> | <span data-ttu-id="a99d2-161">version</span><span class="sxs-lookup"><span data-stu-id="a99d2-161">version</span></span>               | <span data-ttu-id="a99d2-162">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="a99d2-162">1.0.0.0</span></span>           |
| <span data-ttu-id="a99d2-163">Компонент а</span><span class="sxs-lookup"><span data-stu-id="a99d2-163">ComponentA</span></span> | <span data-ttu-id="a99d2-164">Язык</span><span class="sxs-lookup"><span data-stu-id="a99d2-164">language</span></span>              | <span data-ttu-id="a99d2-165">en</span><span class="sxs-lookup"><span data-stu-id="a99d2-165">en</span></span>                |
| <span data-ttu-id="a99d2-166">Компонент а</span><span class="sxs-lookup"><span data-stu-id="a99d2-166">ComponentA</span></span> | <span data-ttu-id="a99d2-167">publicKeyToken</span><span class="sxs-lookup"><span data-stu-id="a99d2-167">publicKeyToken</span></span>        | <span data-ttu-id="a99d2-168">1111111111222222</span><span class="sxs-lookup"><span data-stu-id="a99d2-168">1111111111222222</span></span>  |
| <span data-ttu-id="a99d2-169">Компонент а</span><span class="sxs-lookup"><span data-stu-id="a99d2-169">ComponentA</span></span> | <span data-ttu-id="a99d2-170">processorArchitecture</span><span class="sxs-lookup"><span data-stu-id="a99d2-170">processorArchitecture</span></span> | <span data-ttu-id="a99d2-171">x86</span><span class="sxs-lookup"><span data-stu-id="a99d2-171">x86</span></span>               |



 

## <a name="validation"></a><span data-ttu-id="a99d2-172">Проверка</span><span class="sxs-lookup"><span data-stu-id="a99d2-172">Validation</span></span>

<dl>

[<span data-ttu-id="a99d2-173">ICE03</span><span class="sxs-lookup"><span data-stu-id="a99d2-173">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="a99d2-174">ICE06</span><span class="sxs-lookup"><span data-stu-id="a99d2-174">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="a99d2-175">ICE32</span><span class="sxs-lookup"><span data-stu-id="a99d2-175">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="a99d2-176">ICE66</span><span class="sxs-lookup"><span data-stu-id="a99d2-176">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="a99d2-177">ICE83</span><span class="sxs-lookup"><span data-stu-id="a99d2-177">ICE83</span></span>](ice83.md)  
</dl>

 

 
