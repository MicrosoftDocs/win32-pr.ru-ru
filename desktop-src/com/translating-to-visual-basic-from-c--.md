---
title: Преобразование в Visual Basic из C++
description: Преобразование в Visual Basic из C++
ms.assetid: fce7ea25-cb24-4cc4-8f36-0e8aed2f3ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba519cbdb0305fe3a2eae4cc8e658fdde1eac3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654241"
---
# <a name="translating-to-visual-basic-from-c"></a><span data-ttu-id="baf34-103">Преобразование в Visual Basic из C++</span><span class="sxs-lookup"><span data-stu-id="baf34-103">Translating to Visual Basic from C++</span></span>

<span data-ttu-id="baf34-104">Используя язык программирования C++, разработчики могут напрямую обращаться к памяти, в которой хранится определенная переменная.</span><span class="sxs-lookup"><span data-stu-id="baf34-104">Using the C++ programming language, developers can directly access the memory that stores a particular variable.</span></span> <span data-ttu-id="baf34-105">Указатели памяти обеспечивают прямой доступ.</span><span class="sxs-lookup"><span data-stu-id="baf34-105">Memory pointers provide this direct access.</span></span> <span data-ttu-id="baf34-106">В Visual Basic указатели обрабатываются самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="baf34-106">In Visual Basic, pointers are handled for you.</span></span> <span data-ttu-id="baf34-107">Например, параметр, объявленный как указатель на **int** в C++, эквивалентен параметру, объявленному в Visual Basic как  **целое число** **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="baf34-107">For example, a parameter declared as a pointer to an **int** in C++ is equivalent to a parameter declared in Visual Basic as a **ByRef** **Integer**.</span></span>

<span data-ttu-id="baf34-108">Параметр, объявленный **как String** в Visual Basic, объявляется как указатель на **BSTR** в C++.</span><span class="sxs-lookup"><span data-stu-id="baf34-108">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="baf34-109">Установка указателя строки на **null** в C++ эквивалентна установке строки константы **вбнуллстринг** в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="baf34-109">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="baf34-110">Передача строки нулевой длины ("") в функцию, предназначенную для получения **значения NULL** , не работает, так как она передает указатель на строку нулевой длины вместо нулевого указателя.</span><span class="sxs-lookup"><span data-stu-id="baf34-110">Passing in a zero-length string ("") to a function designed to receive **NULL** does not work, as this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="baf34-111">C++ поддерживает контейнеры данных, а именно структуры и объединения, не имеющие эквивалента в ранних версиях Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="baf34-111">C++ supports data containers, namely structures and unions, that have no equivalent in early versions of Visual Basic.</span></span> <span data-ttu-id="baf34-112">По этой причине COM-объекты обычно переносят информацию, которая обычно хранится в структурах и объединениях в классах объектов.</span><span class="sxs-lookup"><span data-stu-id="baf34-112">For this reason, COM objects typically wrap information that usually is stored in structures and unions in object classes.</span></span> <span data-ttu-id="baf34-113">Однако некоторые COM-объекты могут содержать структуры, что приводит к недоступности частей методов или функций объекта к Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="baf34-113">Some COM objects, however, may contain structures, causing portions of the object's methods or functionality to be inaccessible to Visual Basic.</span></span>

<span data-ttu-id="baf34-114">Некоторые типы данных C++ не поддерживаются в Visual Basic, например неподписанные типы и типы **HWND** .</span><span class="sxs-lookup"><span data-stu-id="baf34-114">Some C++ data types are not supported in Visual Basic, for example unsigned types and **HWND** types.</span></span> <span data-ttu-id="baf34-115">Методы, которые принимают или возвращают эти типы данных, недоступны в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="baf34-115">Methods that accept or return these data types are not available in Visual Basic.</span></span>

<span data-ttu-id="baf34-116">В Visual Basic в качестве внутренних типов данных используются совместимые с автоматизацией типы данных.</span><span class="sxs-lookup"><span data-stu-id="baf34-116">Visual Basic uses Automation-compatible data types as its internal data types.</span></span> <span data-ttu-id="baf34-117">Поэтому типы данных C++, совместимые с автоматизацией, также совместимы с Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="baf34-117">Thus, C++ data types that are Automation-compatible are also compatible with Visual Basic.</span></span> <span data-ttu-id="baf34-118">Типы данных, несовместимые с автоматизацией, не могут быть преобразованы в Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="baf34-118">Data types that are not Automation-compatible may not be able to be converted to Visual Basic.</span></span>

<span data-ttu-id="baf34-119">В следующей таблице перечислены типы данных, поддерживаемые Visual Basic и их эквиваленты **VarType** .</span><span class="sxs-lookup"><span data-stu-id="baf34-119">The following table lists the data types are supported by Visual Basic and their **VARTYPE** equivalents.</span></span> <span data-ttu-id="baf34-120">**VarType** — это перечисление, в котором перечислены типы вариантов автоматизации.</span><span class="sxs-lookup"><span data-stu-id="baf34-120">**VARTYPE** is an enumeration that lists the Automation variant types.</span></span>



| <span data-ttu-id="baf34-121">Тип данных в Visual Basic</span><span class="sxs-lookup"><span data-stu-id="baf34-121">Visual Basic data type</span></span>  | <span data-ttu-id="baf34-122">Эквивалент VARTYPE</span><span class="sxs-lookup"><span data-stu-id="baf34-122">VARTYPE equivalent</span></span>                |
|-------------------------|-----------------------------------|
| <span data-ttu-id="baf34-123">**Integer**</span><span class="sxs-lookup"><span data-stu-id="baf34-123">**Integer**</span></span><br/>  | <span data-ttu-id="baf34-124">16 бит, со знаком, VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="baf34-124">16 bit, signed, VT\_I2</span></span><br/> |
| <span data-ttu-id="baf34-125">**Long**</span><span class="sxs-lookup"><span data-stu-id="baf34-125">**Long**</span></span><br/>     | <span data-ttu-id="baf34-126">32 бит, с подписью, VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="baf34-126">32 bit, signed, VT\_I4</span></span><br/> |
| <span data-ttu-id="baf34-127">**Дата**</span><span class="sxs-lookup"><span data-stu-id="baf34-127">**Date**</span></span><br/>     | <span data-ttu-id="baf34-128">\_Дата VT</span><span class="sxs-lookup"><span data-stu-id="baf34-128">VT\_DATE</span></span><br/>               |
| <span data-ttu-id="baf34-129">**Денежный формат**</span><span class="sxs-lookup"><span data-stu-id="baf34-129">**Currency**</span></span><br/> | <span data-ttu-id="baf34-130">VT \_ CY</span><span class="sxs-lookup"><span data-stu-id="baf34-130">VT\_CY</span></span><br/>                 |
| <span data-ttu-id="baf34-131">**Объект**</span><span class="sxs-lookup"><span data-stu-id="baf34-131">**Object**</span></span><br/>   | <span data-ttu-id="baf34-132">\*\_Диспетчер VT</span><span class="sxs-lookup"><span data-stu-id="baf34-132">\*VT\_DISPATCH</span></span><br/>         |
| <span data-ttu-id="baf34-133">**String**</span><span class="sxs-lookup"><span data-stu-id="baf34-133">**String**</span></span><br/>   | <span data-ttu-id="baf34-134">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="baf34-134">VT\_BSTR</span></span><br/>               |
| <span data-ttu-id="baf34-135">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="baf34-135">**Boolean**</span></span><br/>  | <span data-ttu-id="baf34-136">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="baf34-136">VT\_BOOL</span></span><br/>               |
| <span data-ttu-id="baf34-137">**Денежный формат**</span><span class="sxs-lookup"><span data-stu-id="baf34-137">**Currency**</span></span><br/> | <span data-ttu-id="baf34-138">VT \_ Decimal</span><span class="sxs-lookup"><span data-stu-id="baf34-138">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="baf34-139">**Single**</span><span class="sxs-lookup"><span data-stu-id="baf34-139">**Single**</span></span><br/>   | <span data-ttu-id="baf34-140">VT \_ R4</span><span class="sxs-lookup"><span data-stu-id="baf34-140">VT\_R4</span></span><br/>                 |
| <span data-ttu-id="baf34-141">**Double**</span><span class="sxs-lookup"><span data-stu-id="baf34-141">**Double**</span></span><br/>   | <span data-ttu-id="baf34-142">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="baf34-142">VT\_R8</span></span><br/>                 |
| <span data-ttu-id="baf34-143">**Десятичное число**</span><span class="sxs-lookup"><span data-stu-id="baf34-143">**Decimal**</span></span><br/>  | <span data-ttu-id="baf34-144">VT \_ Decimal</span><span class="sxs-lookup"><span data-stu-id="baf34-144">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="baf34-145">**Byte**</span><span class="sxs-lookup"><span data-stu-id="baf34-145">**Byte**</span></span><br/>     | <span data-ttu-id="baf34-146">VT \_ Decimal</span><span class="sxs-lookup"><span data-stu-id="baf34-146">VT\_DECIMAL</span></span><br/>            |
| <span data-ttu-id="baf34-147">**Значение**</span><span class="sxs-lookup"><span data-stu-id="baf34-147">**Variant**</span></span><br/>  | <span data-ttu-id="baf34-148">\_вариант VT</span><span class="sxs-lookup"><span data-stu-id="baf34-148">VT\_VARIANT</span></span><br/>            |



 

<span data-ttu-id="baf34-149">Все параметры в Visual Basic, кроме ключевого слова **ByVal**, передаются по ссылке (как указатели), а не по значению.</span><span class="sxs-lookup"><span data-stu-id="baf34-149">All parameters in Visual Basic, unless labeled with the keyword **ByVal**, are passed by reference (as pointers) instead of by value.</span></span>

<span data-ttu-id="baf34-150">C++ и Visual Basic немного отличаются в том, как они представляют свойства.</span><span class="sxs-lookup"><span data-stu-id="baf34-150">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="baf34-151">В C++ свойства представлены в виде набора функций доступа, который задает значение свойства и одно из них, которое получает значение свойства.</span><span class="sxs-lookup"><span data-stu-id="baf34-151">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="baf34-152">В Visual Basic свойства представлены как один элемент, который можно использовать для получения или задания значения свойства.</span><span class="sxs-lookup"><span data-stu-id="baf34-152">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="baf34-153">См. также</span><span class="sxs-lookup"><span data-stu-id="baf34-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baf34-154">Перевод в Visual Basic</span><span class="sxs-lookup"><span data-stu-id="baf34-154">Translating to Visual Basic</span></span>](translating-to-visual-basic.md)
</dt> </dl>

 

 





