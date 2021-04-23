---
title: Уровень поддержки схемы
description: В этом разделе рассматриваются сведения о уровне поддержки схем.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Веб-службы уровня поддержки схемы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/12/2021
ms.locfileid: "104555968"
---
# <a name="schema-support-level"></a><span data-ttu-id="90ace-106">Уровень поддержки схемы</span><span class="sxs-lookup"><span data-stu-id="90ace-106">Schema support level</span></span>

<span data-ttu-id="90ace-107">В этом разделе рассматриваются сведения о уровне поддержки схем.</span><span class="sxs-lookup"><span data-stu-id="90ace-107">This section covers the details around the level of schema support.</span></span>


<span data-ttu-id="90ace-108">Схема напрямую поддерживает следующее:</span><span class="sxs-lookup"><span data-stu-id="90ace-108">The schema directly supports the following:</span></span>

-   <span data-ttu-id="90ace-109">Последовательности элементов.</span><span class="sxs-lookup"><span data-stu-id="90ace-109">Sequences of elements.</span></span>
-   <span data-ttu-id="90ace-110">Наследование типов элементов.</span><span class="sxs-lookup"><span data-stu-id="90ace-110">Derivation of element types.</span></span>
-   <span data-ttu-id="90ace-111">Простые варианты элементов (те, которые соответствуют объединению с тегами).</span><span class="sxs-lookup"><span data-stu-id="90ace-111">Simple choices of elements (those that map to a tagged union).</span></span>
-   <span data-ttu-id="90ace-112">Базовые типы, определяемые двоичным форматом XSD/.NET, включая диапазоны (min/max).</span><span class="sxs-lookup"><span data-stu-id="90ace-112">Basic types defined by XSD / .NET binary format including ranges (min/max).</span></span>
-   <span data-ttu-id="90ace-113">Простая поддержка любого элемента (без ограничений на тип элемента).</span><span class="sxs-lookup"><span data-stu-id="90ace-113">Simple support for any element (no restrictions on type of element).</span></span>
-   <span data-ttu-id="90ace-114">Необязательные элементы и атрибуты со значениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90ace-114">Optional elements and attributes with default values.</span></span>
-   <span data-ttu-id="90ace-115">Повторяющиеся элементы с диапазонами (min/max).</span><span class="sxs-lookup"><span data-stu-id="90ace-115">Repeating elements with ranges (min/max).</span></span>
-   <span data-ttu-id="90ace-116">Элементы, допускающие нулевое.</span><span class="sxs-lookup"><span data-stu-id="90ace-116">Nillable elements.</span></span>

<span data-ttu-id="90ace-117">Схема не поддерживает следующее напрямую (что подразумевает «резервное поведение»):</span><span class="sxs-lookup"><span data-stu-id="90ace-117">The schema does not support the following directly (which imply the "fallback" behavior):</span></span>

-   <span data-ttu-id="90ace-118">Базовые типы, определяемые пользователем.</span><span class="sxs-lookup"><span data-stu-id="90ace-118">User defined basic types.</span></span>
-   <span data-ttu-id="90ace-119">Более сложные варианты.</span><span class="sxs-lookup"><span data-stu-id="90ace-119">More complicated choices.</span></span>
-   <span data-ttu-id="90ace-120">Отклонение неизвестных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="90ace-120">Rejecting unknown attributes.</span></span>
-   <span data-ttu-id="90ace-121">Округление неизвестных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="90ace-121">Round tripping unknown attributes.</span></span>
-   <span data-ttu-id="90ace-122">Более сложная поддержка для любого элемента.</span><span class="sxs-lookup"><span data-stu-id="90ace-122">More complicated support for any element.</span></span>
-   <span data-ttu-id="90ace-123">Конструкция ALL.</span><span class="sxs-lookup"><span data-stu-id="90ace-123">The all construct.</span></span>
-   <span data-ttu-id="90ace-124">Key/keyref.</span><span class="sxs-lookup"><span data-stu-id="90ace-124">Key/keyref.</span></span>

<span data-ttu-id="90ace-125">Ниже приведено подробное разбиение поддержки различных компонентов схемы.</span><span class="sxs-lookup"><span data-stu-id="90ace-125">Following is a detailed breakdown of different schema component support.</span></span> <span data-ttu-id="90ace-126">Он сравнивается с контрактом данных в WCF, так как он имеет сходство в функциональности.</span><span class="sxs-lookup"><span data-stu-id="90ace-126">It is compared with data contract in WCF because the similarity in functionality.</span></span> <span data-ttu-id="90ace-127">Разница будет описана.</span><span class="sxs-lookup"><span data-stu-id="90ace-127">The difference will be described.</span></span>

<span data-ttu-id="90ace-128">Как правило, для резервного поведения:</span><span class="sxs-lookup"><span data-stu-id="90ace-128">Generally, for fallback behaviors:</span></span>

-   <span data-ttu-id="90ace-129">атрибуты передаются в строку WS \_ ;</span><span class="sxs-lookup"><span data-stu-id="90ace-129">attributes are fall backed to WS\_STRING;</span></span>
-   <span data-ttu-id="90ace-130">содержимое элемента \_ \_ перемещается в буфер WS XML.</span><span class="sxs-lookup"><span data-stu-id="90ace-130">element content are fall backed to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="90ace-131">complexType перемещается в структуру, содержащую поле \_ буфера WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="90ace-131">complexType are fall backed to structure containing a field of WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="90ace-132">Простые типы передаются в строку WS \_ .</span><span class="sxs-lookup"><span data-stu-id="90ace-132">Simple types are fall backed to WS\_STRING.</span></span>

<span data-ttu-id="90ace-133">всутил создает предупреждения для компонентов схемы, которые в настоящее время не поддерживаются полностью.</span><span class="sxs-lookup"><span data-stu-id="90ace-133">wsutil generates warnings for schema components that are not currently fully supported.</span></span> <span data-ttu-id="90ace-134">Приложению может потребоваться дополнительная проверка этих компонентов.</span><span class="sxs-lookup"><span data-stu-id="90ace-134">Application might need to do additional verification for those components are needed.</span></span> <span data-ttu-id="90ace-135">Всутил сверхурочной работы можно улучшить, чтобы обрабатывать некоторые функции, которые в настоящее время поддерживаются в среде выполнения, например поддержку значений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="90ace-135">Overtime wsutil can be improved to handle some of the features that are currently supported in runtime, like default value support.</span></span> <span data-ttu-id="90ace-136">всутил также можно улучшить вместе с сериализацией для поддержки других функций, таких как abstract.</span><span class="sxs-lookup"><span data-stu-id="90ace-136">wsutil can also be improved together with serialization to support other features like abstract.</span></span> <span data-ttu-id="90ace-137">Количество неподдерживаемых компонентов схемы можно сократить с течением времени.</span><span class="sxs-lookup"><span data-stu-id="90ace-137">The number of unsupported schema components can be reduced over time.</span></span>

## <a name="the-overall-schema-document"></a><span data-ttu-id="90ace-138">Документ общей схемы</span><span class="sxs-lookup"><span data-stu-id="90ace-138">The Overall Schema Document</span></span>

<span data-ttu-id="90ace-139">Глобальное определение, которое может повлиять на внедренные определения в схеме.</span><span class="sxs-lookup"><span data-stu-id="90ace-139">Global definition that might affect embedded definitions in the schema.</span></span> <span data-ttu-id="90ace-140">Это глобальные атрибуты, применимые ко всем определениям в схеме.</span><span class="sxs-lookup"><span data-stu-id="90ace-140">These are global attributes that are applicable to all definitions in the schema.</span></span>

<span data-ttu-id="90ace-141">Атрибуты <xs: schema></span><span class="sxs-lookup"><span data-stu-id="90ace-141"><xs:schema> attributes</span></span>

-   <span data-ttu-id="90ace-142">Аттрибутефромдефаулт игнорируется.</span><span class="sxs-lookup"><span data-stu-id="90ace-142">attributeFromDefault Ignored.</span></span>
-   <span data-ttu-id="90ace-143">blockDefault игнорируется.</span><span class="sxs-lookup"><span data-stu-id="90ace-143">blockDefault Ignored.</span></span>
-   <span data-ttu-id="90ace-144">elementFormDefault игнорируется.</span><span class="sxs-lookup"><span data-stu-id="90ace-144">elementFormDefault Ignored.</span></span> <span data-ttu-id="90ace-145">Это отличается от DataContract, так как неквалифицированные элементы поддерживаются во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="90ace-145">This is different from dataContract as unqualified elements are supported in runtime.</span></span>
-   <span data-ttu-id="90ace-146">finalDefault игнорируется.</span><span class="sxs-lookup"><span data-stu-id="90ace-146">finalDefault Ignored.</span></span> <span data-ttu-id="90ace-147">Нет поддержки языка C для концепции Final.</span><span class="sxs-lookup"><span data-stu-id="90ace-147">There is no C language support for the concept of final.</span></span>
-   <span data-ttu-id="90ace-148">Идентификатор проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="90ace-148">id Ignored.</span></span>
-   <span data-ttu-id="90ace-149">targetNamespace поддерживается и сопоставляется с пространством имен службы.</span><span class="sxs-lookup"><span data-stu-id="90ace-149">targetNamespace Supported and mapped to the service namespace.</span></span>
-   <span data-ttu-id="90ace-150">Версия пропущена.</span><span class="sxs-lookup"><span data-stu-id="90ace-150">version Ignored.</span></span>

<span data-ttu-id="90ace-151"><xs: schema> содержимое</span><span class="sxs-lookup"><span data-stu-id="90ace-151"><xs:schema> contents</span></span>

-   <span data-ttu-id="90ace-152">включить поддерживаемые; всутил требует, чтобы все необходимое определение было доступно в качестве входных файлов во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="90ace-152">include Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="90ace-153">Переопределение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="90ace-153">redefine Ignored.</span></span> <span data-ttu-id="90ace-154">всутил не поддерживает это.</span><span class="sxs-lookup"><span data-stu-id="90ace-154">wsutil does not support this.</span></span>
-   <span data-ttu-id="90ace-155">Импорт поддерживается; всутил требует, чтобы все необходимое определение было доступно в качестве входных файлов во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="90ace-155">import Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="90ace-156">Поддерживается simpleType — см. раздел Simple Type ниже.</span><span class="sxs-lookup"><span data-stu-id="90ace-156">simpleType Supported- see simple type section below.</span></span>
-   <span data-ttu-id="90ace-157">Поддерживается в complexType — см. раздел "complexType".</span><span class="sxs-lookup"><span data-stu-id="90ace-157">complexType Supported- see 'complexType' section</span></span>
-   <span data-ttu-id="90ace-158">Группа игнорируется.</span><span class="sxs-lookup"><span data-stu-id="90ace-158">group Ignored.</span></span>
-   <span data-ttu-id="90ace-159">attributeGroup игнорируется.</span><span class="sxs-lookup"><span data-stu-id="90ace-159">attributeGroup Ignored.</span></span>
-   <span data-ttu-id="90ace-160">элемент поддерживается; сопоставляется с определениями глобальных элементов.</span><span class="sxs-lookup"><span data-stu-id="90ace-160">element Supported; maps to global element definitions.</span></span>
-   <span data-ttu-id="90ace-161">Поддерживаемый атрибут; сопоставляется с определениями глобальных атрибутов.</span><span class="sxs-lookup"><span data-stu-id="90ace-161">attribute Supported; maps to global attribute definitions.</span></span>
-   <span data-ttu-id="90ace-162">Нотация пропущена</span><span class="sxs-lookup"><span data-stu-id="90ace-162">notation Ignored</span></span>

## <a name="complex-type"></a><span data-ttu-id="90ace-163">Сложный тип</span><span class="sxs-lookup"><span data-stu-id="90ace-163">Complex Type</span></span>

<span data-ttu-id="90ace-164">Сложный тип, представленный <xs: complexType>, может быть ограничен простым типом или сложным типом, расширением простого типа, массивов или структурой.</span><span class="sxs-lookup"><span data-stu-id="90ace-164">Complex type, represented by <xs:complexType>, could be restriction of simple type or complex type, extension of simple type, arrays or structure.</span></span> <span data-ttu-id="90ace-165">Обратите внимание, что в расширении простых типов отсутствует возможность наследования и не поддерживается xsi: Type.</span><span class="sxs-lookup"><span data-stu-id="90ace-165">Noticed that in extension of simple types, there is no inheritance and no xsi:type support.</span></span>

<span data-ttu-id="90ace-166">Атрибуты <xs: complexType></span><span class="sxs-lookup"><span data-stu-id="90ace-166"><xs:complexType> attributes</span></span>

-   <span data-ttu-id="90ace-167">abstract создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-167">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-168">блокировать создание предупреждения о неподдерживаемой функции, без изменения в создании кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-168">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-169">окончательное создание предупреждения о неподдерживаемой функции, отсутствие изменений в создании кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-169">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-170">Идентификатор проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="90ace-170">id Ignored.</span></span>
-   <span data-ttu-id="90ace-171">смешанное создание предупреждения о неподдерживаемой функции, откате к структуре с помощью \_ буфера WS XML, \_ Если значение равно true.</span><span class="sxs-lookup"><span data-stu-id="90ace-171">mixed Generate warning about unsupported feature, fallback to structure with WS\_XML\_BUFFER if true.</span></span>
-   <span data-ttu-id="90ace-172">имя поддерживается и сопоставлено с именем типа структуры.</span><span class="sxs-lookup"><span data-stu-id="90ace-172">name Supported and mapped to structure type name.</span></span>

<span data-ttu-id="90ace-173"><xs: complexType> содержимое</span><span class="sxs-lookup"><span data-stu-id="90ace-173"><xs:complexType> contents</span></span>

<span data-ttu-id="90ace-174">Это определение типа для Structure.</span><span class="sxs-lookup"><span data-stu-id="90ace-174">This is type definition for structure.</span></span> <span data-ttu-id="90ace-175">ограничение complexContent не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="90ace-175">complexContent restriction is not supported.</span></span>

-   <span data-ttu-id="90ace-176">complexContent поддерживает комплексное расширение содержимого.</span><span class="sxs-lookup"><span data-stu-id="90ace-176">complexContent Support complex content extension.</span></span> <span data-ttu-id="90ace-177">Сопоставляется с наследованием структуры.</span><span class="sxs-lookup"><span data-stu-id="90ace-177">Maps to structure inheritance.</span></span>
-   <span data-ttu-id="90ace-178">Группирование в настоящее время для структурирования с помощью \_ \_ поля буфера WS XML.</span><span class="sxs-lookup"><span data-stu-id="90ace-178">group Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="90ace-179">Может поддерживаться в соответствии с нижней частью.</span><span class="sxs-lookup"><span data-stu-id="90ace-179">Can be supported according to the underneath particle.</span></span>
-   <span data-ttu-id="90ace-180">вариант, поддерживаемый как объединение.</span><span class="sxs-lookup"><span data-stu-id="90ace-180">choice supported as union.</span></span> <span data-ttu-id="90ace-181">Это не поддерживается в контракте данных.</span><span class="sxs-lookup"><span data-stu-id="90ace-181">This is not supported in data contract.</span></span>
-   <span data-ttu-id="90ace-182">Поддерживаемые последовательности — сопоставляется с полями структуры</span><span class="sxs-lookup"><span data-stu-id="90ace-182">sequence Supported - maps to fields of a structure</span></span>
-   <span data-ttu-id="90ace-183">поддерживается атрибут с одним исключением "запрещено".</span><span class="sxs-lookup"><span data-stu-id="90ace-183">attribute supported with one exception of 'prohibited'.</span></span> <span data-ttu-id="90ace-184">откат к структуре с помощью \_ буфера WS XML, \_ Если "запрещено".</span><span class="sxs-lookup"><span data-stu-id="90ace-184">fallback to structure with WS\_XML\_BUFFER if 'prohibited'.</span></span>
-   <span data-ttu-id="90ace-185">не поддерживается attributeGroup — сопоставление с последовательностью атрибутов</span><span class="sxs-lookup"><span data-stu-id="90ace-185">attributeGroup supported - maps to sequence of attributes</span></span>
-   <span data-ttu-id="90ace-186">anyAttribute игнорируется</span><span class="sxs-lookup"><span data-stu-id="90ace-186">anyAttribute Ignored</span></span>
-   <span data-ttu-id="90ace-187">Аттрибутеграупреф Supported — сопоставляется с последовательностью атрибутов.</span><span class="sxs-lookup"><span data-stu-id="90ace-187">AttributeGroupRef Supported - maps to sequence of attributes.</span></span>
-   <span data-ttu-id="90ace-188">Граупреф в настоящее время является резервным для структуры с \_ \_ полем буфера WS XML.</span><span class="sxs-lookup"><span data-stu-id="90ace-188">GroupRef Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="90ace-189">Может поддерживаться в соответствии с группой ниже.</span><span class="sxs-lookup"><span data-stu-id="90ace-189">Can be supported according to the underneath group.</span></span>
-   <span data-ttu-id="90ace-190">Любой поддерживаемый, сопоставляется с XML- \_ буфером</span><span class="sxs-lookup"><span data-stu-id="90ace-190">Any Supported, maps to XML\_BUFFER</span></span>
-   <span data-ttu-id="90ace-191">(пусто). поддерживается Map с пустым описанием структуры без создания структуры.</span><span class="sxs-lookup"><span data-stu-id="90ace-191">(blank) supported map to empty struct description with no struct generated.</span></span>

<span data-ttu-id="90ace-192"><xs:sequence> в сложном типе: содержимое</span><span class="sxs-lookup"><span data-stu-id="90ace-192"><xs:sequence> in a complex type: contents</span></span>

<span data-ttu-id="90ace-193">всутил только полностью поддерживает последовательность minOccurs = 1 и maxOccurs = 1; в противном случае сложный тип в настоящее время передается в \_ БУФЕР WS XML \_ .</span><span class="sxs-lookup"><span data-stu-id="90ace-193">wsutil only fully support sequence of minOccurs = 1 and maxOccurs = 1; otherwise the complex type is currently fall backed to WS\_XML\_BUFFER.</span></span> <span data-ttu-id="90ace-194">Он может поддерживаться в виде массива структур.</span><span class="sxs-lookup"><span data-stu-id="90ace-194">It can be supported as array of structures.</span></span>

-   <span data-ttu-id="90ace-195">элемент поддерживается; Каждый экземпляр сопоставляется с полем в структуре.</span><span class="sxs-lookup"><span data-stu-id="90ace-195">element Supported; each instance maps to a field in the structure.</span></span>
-   <span data-ttu-id="90ace-196">Откат группы; элемент complexType является резервным для \_ XML- \_ буфера WS.</span><span class="sxs-lookup"><span data-stu-id="90ace-196">Group fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="90ace-197">Все резервные; элемент complexType является резервным для \_ XML- \_ буфера WS.</span><span class="sxs-lookup"><span data-stu-id="90ace-197">All fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="90ace-198">поддерживается вариант; Сопоставьте с полем объединения.</span><span class="sxs-lookup"><span data-stu-id="90ace-198">choice supported; map to union field.</span></span>
-   <span data-ttu-id="90ace-199">откат последовательности; элемент complexType является резервным для \_ XML- \_ буфера WS.</span><span class="sxs-lookup"><span data-stu-id="90ace-199">sequence fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="90ace-200">любой поддерживаемый; сопоставлено с XML- \_ буфером.</span><span class="sxs-lookup"><span data-stu-id="90ace-200">any Supported; mapped to XML\_BUFFER.</span></span>
-   <span data-ttu-id="90ace-201">(пусто) поддерживается; Если атрибуты отсутствуют, complexType может быть пустой структурой.</span><span class="sxs-lookup"><span data-stu-id="90ace-201">(blank) supported; complexType can be an empty structure if there is no attributes.</span></span>

## <a name="elements"></a><span data-ttu-id="90ace-202">Элементы</span><span class="sxs-lookup"><span data-stu-id="90ace-202">Elements</span></span>

<span data-ttu-id="90ace-203"><xs: element>может возникать в трех контекстах.</span><span class="sxs-lookup"><span data-stu-id="90ace-203"><xs:element>may occur in three contexts.</span></span>

-   <span data-ttu-id="90ace-204">Это может произойти в <xs: Sequence>, описывающем поле обычной структуры.</span><span class="sxs-lookup"><span data-stu-id="90ace-204">It may occur within an <xs:sequence>, describing a field of a regular struct.</span></span> <span data-ttu-id="90ace-205">В этом случае атрибут maxOccurs должен иметь значение 1.</span><span class="sxs-lookup"><span data-stu-id="90ace-205">In this case, the maxOccurs attribute must be 1.</span></span> <span data-ttu-id="90ace-206">Поле является необязательным, если minOccurs имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="90ace-206">The field is optional if minOccurs is 0.</span></span>
-   <span data-ttu-id="90ace-207">Это может произойти в <xs: Sequence>, описывающем поле массива.</span><span class="sxs-lookup"><span data-stu-id="90ace-207">It may occur within an <xs:sequence>, describing a field of an array.</span></span> <span data-ttu-id="90ace-208">В этом случае атрибут maxOccurs должен быть больше 1 или не привязан.</span><span class="sxs-lookup"><span data-stu-id="90ace-208">In this case, the maxOccurs attribute must be greater than 1 or 'unbounded'.</span></span>
-   <span data-ttu-id="90ace-209">Это может произойти в <xs: schema> как описание глобального элемента.</span><span class="sxs-lookup"><span data-stu-id="90ace-209">It may occur within an <xs:schema> as a global element description.</span></span>

<span data-ttu-id="90ace-210"><xs: element> в <xs: Sequence> или <xs: Choice как поле в структуре</span><span class="sxs-lookup"><span data-stu-id="90ace-210"><xs:element> within an <xs:sequence> or <xs:choice> as a field in a structure</span></span>

-   <span data-ttu-id="90ace-211">Поддержка ref; разрешено в ссылку на глобальный элемент.</span><span class="sxs-lookup"><span data-stu-id="90ace-211">ref Supported; resolved to reference to global element.</span></span>
-   <span data-ttu-id="90ace-212">имя поддерживается, сопоставляется с именем поля.</span><span class="sxs-lookup"><span data-stu-id="90ace-212">name Supported, maps to field name.</span></span>
-   <span data-ttu-id="90ace-213">тип поддерживается, сопоставляется с типом поля.</span><span class="sxs-lookup"><span data-stu-id="90ace-213">type Supported, maps to field type.</span></span> <span data-ttu-id="90ace-214">Дополнительные сведения см. в разделе "сопоставление типов".</span><span class="sxs-lookup"><span data-stu-id="90ace-214">For more information, see 'Type Mapping'.</span></span> <span data-ttu-id="90ace-215">Если не указано (и элемент не содержит анонимный тип), то принимается значение xs: anyType.</span><span class="sxs-lookup"><span data-stu-id="90ace-215">If not specified (and the element does not contain an anonymous type), xs:anyType is assumed.</span></span>
-   <span data-ttu-id="90ace-216">блокировать создание предупреждения о неподдерживаемой функции, без изменения в создании кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-216">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-217">по умолчанию выдается предупреждение о неподдерживаемой функции, но не влияет на создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-217">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-218">Исправлено создание предупреждения о неподдерживаемой функции, отсутствие изменений в создании кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-218">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-219">форма пропущена.</span><span class="sxs-lookup"><span data-stu-id="90ace-219">form Ignored.</span></span> <span data-ttu-id="90ace-220">Наш уровень сериализации поддерживает как квалифицированные, так и неквалифицированные формы.</span><span class="sxs-lookup"><span data-stu-id="90ace-220">Our serialization layer supports both qualified and unqualified forms.</span></span>
-   <span data-ttu-id="90ace-221">Идентификатор проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="90ace-221">id Ignored.</span></span>
-   <span data-ttu-id="90ace-222">maxOccurs сопоставляется с одним полем данных, если равно 1.</span><span class="sxs-lookup"><span data-stu-id="90ace-222">maxOccurs maps to a single data field if equals 1.</span></span> <span data-ttu-id="90ace-223">он сопоставляется с полем массива (повторяющийся элемент), если maxOccurs больше 1.</span><span class="sxs-lookup"><span data-stu-id="90ace-223">it is mapped to an array field (repeating element) if maxOccurs is larger than 1.</span></span>
-   <span data-ttu-id="90ace-224">minOccurs если значение равно 0, то параметры поля задаются как поле \_ необязательно, если не установлен параметр обнуляемых.</span><span class="sxs-lookup"><span data-stu-id="90ace-224">minOccurs if 0, the field options is set to FIELD\_OPTIONAL, if nillable is not set.</span></span>
-   <span data-ttu-id="90ace-225">пустое поле является нулевым.</span><span class="sxs-lookup"><span data-stu-id="90ace-225">nillable The field is nillable.</span></span> <span data-ttu-id="90ace-226">Дополнительные сведения см. в разделе о [сериализации](serialization.md) .</span><span class="sxs-lookup"><span data-stu-id="90ace-226">See [Serialization](serialization.md) for more detail.</span></span>

<span data-ttu-id="90ace-227"><xs: element> как глобальный элемент: атрибуты</span><span class="sxs-lookup"><span data-stu-id="90ace-227"><xs:element> as global element: attributes</span></span>

<span data-ttu-id="90ace-228">атрибуты minOccurs и maxOccurs являются недопустимыми в описании глобального элемента.</span><span class="sxs-lookup"><span data-stu-id="90ace-228">minOccurs and maxOccurs attributes are invalid as global element description.</span></span> <span data-ttu-id="90ace-229">Приложение может использовать описание созданного элемента непосредственно на уровне сериализации или на уровнях каналов.</span><span class="sxs-lookup"><span data-stu-id="90ace-229">Application can use generated element description in serialization layer or channel layers directly.</span></span>

-   <span data-ttu-id="90ace-230">abstract создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-230">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-231">блокировать создание предупреждения о неподдерживаемой функции, без изменения в создании кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-231">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-232">по умолчанию выдается предупреждение о неподдерживаемой функции, но не влияет на создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-232">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-233">окончательное создание предупреждения о неподдерживаемой функции, отсутствие изменений в создании кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-233">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-234">Исправлено создание предупреждения о неподдерживаемой функции, отсутствие изменений в создании кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-234">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-235">Идентификатор проигнорирован.</span><span class="sxs-lookup"><span data-stu-id="90ace-235">id Ignored.</span></span>
-   <span data-ttu-id="90ace-236">Поддерживаемое имя — сопоставьте с именем глобального элемента Description, а при указании — в качестве основы для анонимного типа.</span><span class="sxs-lookup"><span data-stu-id="90ace-236">name Supported- map to name of the global element description, and it is the base for the anonymous type when specified.</span></span>
-   <span data-ttu-id="90ace-237">обнуляемый игнорируется — приложение должно вызываться с флагом справа.</span><span class="sxs-lookup"><span data-stu-id="90ace-237">nillable Ignored-application needs to call with right flag.</span></span>
-   <span data-ttu-id="90ace-238">Субститутионграуп откат к структуре с помощью \_ буфера WS XML, \_ Если задано.</span><span class="sxs-lookup"><span data-stu-id="90ace-238">substitutionGroup fallback to structure with WS\_XML\_BUFFER if set.</span></span> <span data-ttu-id="90ace-239">всутил не поддерживает Субститутионграуп.</span><span class="sxs-lookup"><span data-stu-id="90ace-239">wsutil does not support substitutionGroup.</span></span>
-   <span data-ttu-id="90ace-240">тип поддерживается и сопоставляется с типом элемента.</span><span class="sxs-lookup"><span data-stu-id="90ace-240">type Supported and map to the type of the element.</span></span>

<span data-ttu-id="90ace-241"><xs: element> как глобальный элемент: содержимое</span><span class="sxs-lookup"><span data-stu-id="90ace-241"><xs:element> as global element: contents</span></span>

-   <span data-ttu-id="90ace-242">simpleType поддерживается; сопоставляется с определением типа.</span><span class="sxs-lookup"><span data-stu-id="90ace-242">simpleType Supported; maps to type definition.</span></span>
-   <span data-ttu-id="90ace-243">поддерживается complexType; сопоставляется со сложным типом.</span><span class="sxs-lookup"><span data-stu-id="90ace-243">complexType supported; maps to a complex type.</span></span>
-   <span data-ttu-id="90ace-244">уникальный создает предупреждение о неподдерживаемой функции, не влияет на создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-244">unique Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="90ace-245">всутил не поддерживает ограничения элементов.</span><span class="sxs-lookup"><span data-stu-id="90ace-245">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="90ace-246">KEY создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-246">key Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="90ace-247">всутил не поддерживает ограничения элементов.</span><span class="sxs-lookup"><span data-stu-id="90ace-247">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="90ace-248">элемент keyref создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-248">keyref Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="90ace-249">всутил не поддерживает ограничения элементов.</span><span class="sxs-lookup"><span data-stu-id="90ace-249">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="90ace-250">свобод Поддерживается элемент без спецификации типа рассматривается как xs: anyType.</span><span class="sxs-lookup"><span data-stu-id="90ace-250">(blank) Supported; element with no type specification is treated as xs:anyType.</span></span>

## <a name="simple-types"></a><span data-ttu-id="90ace-251">Простые типы</span><span class="sxs-lookup"><span data-stu-id="90ace-251">Simple Types</span></span>

<span data-ttu-id="90ace-252">Атрибуты <xs: simpleType></span><span class="sxs-lookup"><span data-stu-id="90ace-252"><xs:simpleType> attributes</span></span>

-   <span data-ttu-id="90ace-253">Окончательное создание предупреждения о неподдерживаемой функции, отсутствие изменений в создании кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-253">Final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-254">Идентификатор пропущен</span><span class="sxs-lookup"><span data-stu-id="90ace-254">Id Ignored</span></span>
-   <span data-ttu-id="90ace-255">Имя поддерживается, сопоставляется с именем типа.</span><span class="sxs-lookup"><span data-stu-id="90ace-255">Name Supported, maps to type name.</span></span>

<span data-ttu-id="90ace-256"><xs: simpleType> содержимое</span><span class="sxs-lookup"><span data-stu-id="90ace-256"><xs:simpleType> contents</span></span>

-   <span data-ttu-id="90ace-257">Поддерживаемое ограничение, сопоставляется с типом перечисления или диапазоном.</span><span class="sxs-lookup"><span data-stu-id="90ace-257">Restriction Supported, maps to enum type or range.</span></span> <span data-ttu-id="90ace-258">См. раздел «ограничения типа "xs: simpleType"».</span><span class="sxs-lookup"><span data-stu-id="90ace-258">See "xs:simpleType restrictions" section.</span></span>
-   <span data-ttu-id="90ace-259">В списке выдается предупреждение о неподдерживаемой функции, резервном восстановлении в \_ БУФЕР XML.</span><span class="sxs-lookup"><span data-stu-id="90ace-259">List Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>
-   <span data-ttu-id="90ace-260">Union создает предупреждение о неподдерживаемой функции, резерве в \_ буфере XML.</span><span class="sxs-lookup"><span data-stu-id="90ace-260">Union Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>

## <a name="simple-type-restriction"></a><span data-ttu-id="90ace-261">Ограничение простого типа</span><span class="sxs-lookup"><span data-stu-id="90ace-261">Simple Type restriction</span></span>

<span data-ttu-id="90ace-262">Некоторые аспекты допускаются в целочисленных типах и типах строк, чтобы обеспечить поддержку диапазона и перечисления.</span><span class="sxs-lookup"><span data-stu-id="90ace-262">Certain facets are allowed in integral types and strings type to allow range and enum support.</span></span>

<span data-ttu-id="90ace-263">поддержка перечисления</span><span class="sxs-lookup"><span data-stu-id="90ace-263">enumeration support</span></span>

<span data-ttu-id="90ace-264"><xs: enumeration> ограничение простого типа для базового типа строки рассматривается как тип перечисления.</span><span class="sxs-lookup"><span data-stu-id="90ace-264"><xs:enumeration> simple type restriction for base type of string is treated as enum type.</span></span> <span data-ttu-id="90ace-265">В этом случае базовый атрибут должен иметь строковый тип.</span><span class="sxs-lookup"><span data-stu-id="90ace-265">In this case, the Base attribute MUST be string type.</span></span> <span data-ttu-id="90ace-266">В случае перечисления все остальные аспекты игнорируются.</span><span class="sxs-lookup"><span data-stu-id="90ace-266">In enumeration case, all other facets are ignored.</span></span>

<span data-ttu-id="90ace-267">Поддержка простого типа в диапазоне</span><span class="sxs-lookup"><span data-stu-id="90ace-267">range on simple type support</span></span>

<span data-ttu-id="90ace-268">Некоторые аспекты поддерживаются простыми типами и поддерживают эффективный диапазон, допустимый для типа.</span><span class="sxs-lookup"><span data-stu-id="90ace-268">Some facets are support in simple types support effectively range allowed on the type.</span></span> <span data-ttu-id="90ace-269">Ниже приведены ограничения для целочисленных типов и типов float/Double.</span><span class="sxs-lookup"><span data-stu-id="90ace-269">Following are restriction for integral types and float/double types.</span></span> <span data-ttu-id="90ace-270">Простые типы с другими аспектами относятся к \_ типу WS String</span><span class="sxs-lookup"><span data-stu-id="90ace-270">Simple types with other facets are fall backed to WS\_STRING type</span></span>

-   <span data-ttu-id="90ace-271">Поддерживается minExclusive</span><span class="sxs-lookup"><span data-stu-id="90ace-271">minExclusive Supported</span></span>
-   <span data-ttu-id="90ace-272">minInclusive поддерживается</span><span class="sxs-lookup"><span data-stu-id="90ace-272">minInclusive Supported</span></span>
-   <span data-ttu-id="90ace-273">maxExclusive поддерживается</span><span class="sxs-lookup"><span data-stu-id="90ace-273">maxExclusive Supported</span></span>
-   <span data-ttu-id="90ace-274">maxInclusive поддерживается</span><span class="sxs-lookup"><span data-stu-id="90ace-274">maxInclusive Supported</span></span>
-   <span data-ttu-id="90ace-275">totalDigits создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-275">totalDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-276">Аспект fractionDigits создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-276">fractionDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-277">Длина создает предупреждение о неподдерживаемой функции, не влияет на создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-277">length Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-278">minLength создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-278">minLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-279">maxLength создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-279">maxLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-280">Перечисление создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-280">enumeration Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-281">Пустое пространство создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-281">whiteSpace Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-282">шаблон создает предупреждение о неподдерживаемой функции, не изменяет создание кода.</span><span class="sxs-lookup"><span data-stu-id="90ace-282">pattern Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="90ace-283">свобод Поддерживается.</span><span class="sxs-lookup"><span data-stu-id="90ace-283">(blank) Supported.</span></span>

<span data-ttu-id="90ace-284">minLength и maxLength в строке в настоящее время не поддерживаются, но является желательной функцией для поддержки.</span><span class="sxs-lookup"><span data-stu-id="90ace-284">minLength and maxLength on string is not supported currently but is a desirable feature to support.</span></span>

## <a name="inheritance"></a><span data-ttu-id="90ace-285">Наследование</span><span class="sxs-lookup"><span data-stu-id="90ace-285">Inheritance</span></span>

<span data-ttu-id="90ace-286">Всутил поддерживает наследование сложных типов, то есть структура может наследовать от другой структуры, подобно наследованию интерфейса в C++.</span><span class="sxs-lookup"><span data-stu-id="90ace-286">Wsutil supports inheritance of complex types, that is, a structure can inherit from another structure, similar to interface inheritance in C++.</span></span> <span data-ttu-id="90ace-287">Это выполняется с помощью <xs: Комплексконтентекстенсион>.</span><span class="sxs-lookup"><span data-stu-id="90ace-287">This is done through <xs:complexContentExtension>.</span></span> <span data-ttu-id="90ace-288"><xs: Симплеконтентекстенсион> поддерживается, но формируется как обычная структура с базовым типом в качестве первого поля вместо наследования типа.</span><span class="sxs-lookup"><span data-stu-id="90ace-288"><xs:simpleContentExtension> is supported but is generated as plain structure with base type as first field instead of type inheritance.</span></span>

## <a name="typeprimitive-mapping"></a><span data-ttu-id="90ace-289">Сопоставление тип-примитив</span><span class="sxs-lookup"><span data-stu-id="90ace-289">Type/primitive mapping</span></span>

<span data-ttu-id="90ace-290">При преобразовании из Нкнамес в XML идентификаторы должны быть нормализованы.</span><span class="sxs-lookup"><span data-stu-id="90ace-290">Identifiers needs to be normalized when translating from NCNames in XML.</span></span> <span data-ttu-id="90ace-291">Строки являются пустыми; типы указателей являются пустыми; целочисленные типы и float/Double являются пустыми, а defaultValue имеет значение 0.</span><span class="sxs-lookup"><span data-stu-id="90ace-291">Strings are nillable; pointer types are nillable; integral types and float/double are nillable and defaultValue is set to 0.</span></span>

![Таблица, в которой показано сопоставление типов XSD и типов данных Sapphire.](images/schematypemap.png)

 

 




