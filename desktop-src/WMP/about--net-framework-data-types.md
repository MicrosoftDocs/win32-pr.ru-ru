---
title: Сведения о типах данных платформа .NET Framework
description: Сведения о типах данных платформа .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Проигрыватель Windows Media, .NET Framework
- Объектная модель проигрывателя Windows Media, NET Framework
- Объектная модель, .NET Framework
- Проигрыватель Windows Media Mobile, .NET Framework
- Элемент управления ActiveX проигрывателя Windows Media, .NET Framework
- Элемент управления ActiveX проигрывателя Windows Media Mobile, NET Framework
- Элемент управления ActiveX, NET Framework
- Платформа .NET Framework, типы данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104068474"
---
# <a name="about-net-framework-data-types"></a><span data-ttu-id="2778b-111">Сведения о типах данных платформа .NET Framework</span><span class="sxs-lookup"><span data-stu-id="2778b-111">About .NET Framework Data Types</span></span>

<span data-ttu-id="2778b-112">В этом разделе содержатся сведения, необходимые для преобразования справочника по объектно-ориентированной модели объектов в базовые типы данных платформы Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="2778b-112">This section contains the information you need to translate the script-oriented Object Model Reference into Microsoft .NET Framework base data types.</span></span> <span data-ttu-id="2778b-113">Ссылка на сценарий проигрывателя Windows Media содержит почти всю информацию, необходимую для использования элемента управления проигрывателя Windows Media в программе на основе платформа .NET Framework, и в большинстве случаев синтаксис будет похож на тот, что используется в других языках сценариев, таких как Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="2778b-113">The Windows Media Player script reference has almost all the information you need to use the Windows Media Player control in a .NET Framework-based program, and in most cases, the syntax will be similar to that of other scripting languages such as Microsoft JScript.</span></span>

<span data-ttu-id="2778b-114">Ссылка на проигрыватель Windows Media предоставляет тип данных JScript и, при необходимости, преобразование C++.</span><span class="sxs-lookup"><span data-stu-id="2778b-114">The Windows Media Player reference provides the JScript data type and, if necessary, the C++ conversion.</span></span> <span data-ttu-id="2778b-115">Например, метод может вернуть **число** .</span><span class="sxs-lookup"><span data-stu-id="2778b-115">For example, a **Number** might be returned by a method.</span></span> <span data-ttu-id="2778b-116">В JScript все числа обрабатываются одинаково, но другие языки различают различные типы чисел (целые числа, плавающие точки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="2778b-116">JScript treats all numbers in the same way, but other languages distinguish between different types of numbers (integer, floating point, and so on).</span></span> <span data-ttu-id="2778b-117">Ссылка обеспечивает преобразование C++ для числовых типов данных, так как числа могут обрабатываться по-разному в C++.</span><span class="sxs-lookup"><span data-stu-id="2778b-117">The reference gives the C++ conversion for number data types because numbers can be processed differently by C++.</span></span> <span data-ttu-id="2778b-118">Например, C++ использует тип данных **int** для целочисленных арифметических операций и **float** для плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="2778b-118">For example, C++ uses the **int** data type for integer arithmetic and **float** for floating point.</span></span>

<span data-ttu-id="2778b-119">В платформа .NET Framework используется немного другая система базовых типов данных.</span><span class="sxs-lookup"><span data-stu-id="2778b-119">The .NET Framework uses a slightly different system of base data types.</span></span> <span data-ttu-id="2778b-120">В следующей таблице показаны различия в стандартных типах данных, которые, скорее всего, будут использоваться.</span><span class="sxs-lookup"><span data-stu-id="2778b-120">The following table shows the differences in the common data types you are likely to use.</span></span> <span data-ttu-id="2778b-121">Дополнительные сведения о платформа .NET Framework базовых типах данных и преобразовании в другие системы типов данных см. в разделе Пошаговое описание базовых типов данных пространства имен System для разработчиков платформа .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="2778b-121">For more information on .NET Framework base data types and the conversion to other data type systems, see the .NET Framework Developer's Guide discussion of System Namespace base data types.</span></span>

<span data-ttu-id="2778b-122">Эта таблица содержит платформа .NET Framework имя класса и тип данных C#.</span><span class="sxs-lookup"><span data-stu-id="2778b-122">This table gives the .NET Framework class name and the C# data type.</span></span> <span data-ttu-id="2778b-123">Типы данных для других языков определяются для каждого языка в соответствующих языковых ссылках.</span><span class="sxs-lookup"><span data-stu-id="2778b-123">Data types for other languages are defined for each language in their respective language references.</span></span>



| <span data-ttu-id="2778b-124">Тип данных сценария</span><span class="sxs-lookup"><span data-stu-id="2778b-124">Script data type</span></span> | <span data-ttu-id="2778b-125">Тип данных в C++</span><span class="sxs-lookup"><span data-stu-id="2778b-125">C++ data type</span></span>     | <span data-ttu-id="2778b-126">Класс платформа .NET Framework (тип данных C#)</span><span class="sxs-lookup"><span data-stu-id="2778b-126">.NET Framework class (C# data type )</span></span> |
|------------------|-------------------|---------------------------------------|
| <span data-ttu-id="2778b-127">**Число**</span><span class="sxs-lookup"><span data-stu-id="2778b-127">**Number**</span></span>       | <span data-ttu-id="2778b-128">**int**</span><span class="sxs-lookup"><span data-stu-id="2778b-128">**int**</span></span>           | <span data-ttu-id="2778b-129">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="2778b-129">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="2778b-130">**Число**</span><span class="sxs-lookup"><span data-stu-id="2778b-130">**Number**</span></span>       | <span data-ttu-id="2778b-131">**long**</span><span class="sxs-lookup"><span data-stu-id="2778b-131">**long**</span></span>          | <span data-ttu-id="2778b-132">**Int32** (**int**)</span><span class="sxs-lookup"><span data-stu-id="2778b-132">**Int32** (**int**)</span></span>                   |
| <span data-ttu-id="2778b-133">**Число**</span><span class="sxs-lookup"><span data-stu-id="2778b-133">**Number**</span></span>       | <span data-ttu-id="2778b-134">**double**</span><span class="sxs-lookup"><span data-stu-id="2778b-134">**double**</span></span>        | <span data-ttu-id="2778b-135">**Double** (**двойной**)</span><span class="sxs-lookup"><span data-stu-id="2778b-135">**Double** (**double**)</span></span>               |
| <span data-ttu-id="2778b-136">**Число**</span><span class="sxs-lookup"><span data-stu-id="2778b-136">**Number**</span></span>       | <span data-ttu-id="2778b-137">**float**</span><span class="sxs-lookup"><span data-stu-id="2778b-137">**float**</span></span>         | <span data-ttu-id="2778b-138">**Single** (**float**)</span><span class="sxs-lookup"><span data-stu-id="2778b-138">**Single** (**float**)</span></span>                |
| <span data-ttu-id="2778b-139">**String**</span><span class="sxs-lookup"><span data-stu-id="2778b-139">**String**</span></span>       | <span data-ttu-id="2778b-140">**ОСВОБОЖДАЕМОЙ**</span><span class="sxs-lookup"><span data-stu-id="2778b-140">**BSTR**</span></span>          | <span data-ttu-id="2778b-141">**String** (**строка**)</span><span class="sxs-lookup"><span data-stu-id="2778b-141">**String** (**string**)</span></span>               |
| <span data-ttu-id="2778b-142">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2778b-142">**Boolean**</span></span>      | <span data-ttu-id="2778b-143">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="2778b-143">**VARIANT\_BOOL**</span></span> | <span data-ttu-id="2778b-144">**Логическое значение** (**bool**)</span><span class="sxs-lookup"><span data-stu-id="2778b-144">**Boolean** (**bool**)</span></span>                |
| <span data-ttu-id="2778b-145">**Объект**</span><span class="sxs-lookup"><span data-stu-id="2778b-145">**Object**</span></span>       | <span data-ttu-id="2778b-146">**Объект**</span><span class="sxs-lookup"><span data-stu-id="2778b-146">**Object**</span></span>        | <span data-ttu-id="2778b-147">**Объект** (**объект**)</span><span class="sxs-lookup"><span data-stu-id="2778b-147">**Object** (**object**)</span></span>               |



 

<span data-ttu-id="2778b-148">При использовании Visual Studio для определения типа данных, ожидаемого для конкретной функции, можно использовать технологию Microsoft IntelliSense.</span><span class="sxs-lookup"><span data-stu-id="2778b-148">If you are using Visual Studio, you can use the Microsoft IntelliSense technology to determine what data type is expected for a specific function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2778b-149">См. также</span><span class="sxs-lookup"><span data-stu-id="2778b-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2778b-150">**Внедрение элемента управления проигрывателя Windows Media в платформа .NET Framework решение**</span><span class="sxs-lookup"><span data-stu-id="2778b-150">**Embedding the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[<span data-ttu-id="2778b-151">**Справочник по объектной модели для создания сценариев**</span><span class="sxs-lookup"><span data-stu-id="2778b-151">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




