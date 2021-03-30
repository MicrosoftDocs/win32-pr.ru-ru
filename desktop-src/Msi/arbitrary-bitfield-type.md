---
description: '&\# 0034; Битовое&\# 0034; тип без запросов контекста, который пользователь предоставил целое число, значение которого используется для задания одного или нескольких битов в битовом наборе. Этот текст может быть на любом языке, совместимом с кодовой страницей базы данных.'
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Произвольный тип битового поля
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156342"
---
# <a name="arbitrary-bitfield-type"></a><span data-ttu-id="462c5-104">Произвольный тип битового поля</span><span class="sxs-lookup"><span data-stu-id="462c5-104">Arbitrary Bitfield Type</span></span>

<span data-ttu-id="462c5-105">Тип "битовый номер" без запросов контекста, который пользователь предоставил целое число, значение которого используется для задания одного или нескольких битов в битовом наборе.</span><span class="sxs-lookup"><span data-stu-id="462c5-105">The "Bitfield" type with no context requests that the user provide an integer whose value is used to set one or more bits in a bitfield.</span></span> <span data-ttu-id="462c5-106">Этот текст может быть на любом языке, совместимом с кодовой страницей базы данных.</span><span class="sxs-lookup"><span data-stu-id="462c5-106">This text may be in any language compatible with the code page of the database.</span></span>

<span data-ttu-id="462c5-107">Произвольный тип битов [семантического типа](semantic-types.md) является одним из битовых типов.</span><span class="sxs-lookup"><span data-stu-id="462c5-107">The Arbitrary Bitfield Type of [semantic type](semantic-types.md) is one of the Bitfield Types.</span></span> <span data-ttu-id="462c5-108">Этот тип состоит из целого числа, выбранного пользователем из набора вариантов.</span><span class="sxs-lookup"><span data-stu-id="462c5-108">This type consists of an integer chosen by the user from a set of choices.</span></span> <span data-ttu-id="462c5-109">Инструмент слияния заменяет выбранное целое число шаблонами, указанными в столбце значение [таблицы модулесубститутион](modulesubstitution-table.md).</span><span class="sxs-lookup"><span data-stu-id="462c5-109">The merge tool substitutes the selected integer into the templates specified in the Value column of the [ModuleSubstitution table](modulesubstitution-table.md).</span></span> <span data-ttu-id="462c5-110">Чтобы указать настраиваемый элемент этого типа, авторы модулей должны ввести имя элемента в столбец "имя", ввести "3" в столбец Format, оставить столбец типа пустым и ввести список возможных целых чисел в столбец Контекстдата [таблицы модулеконфигуратион](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="462c5-110">To specify a configurable item of this type, module authors should enter the name of the item into the Name column, enter "3" into the Format column, leave the Type column blank, and enter the list of possible integers in the ContextData column of the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span>

<span data-ttu-id="462c5-111">Столбец типа зарезервирован и должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="462c5-111">The Type column is reserved and must be null.</span></span> <span data-ttu-id="462c5-112">Запись в столбце Контекстдата для всех типов формата битовой записи должна быть в формате " <mask> ;<Name>=</span><span class="sxs-lookup"><span data-stu-id="462c5-112">The entry in the ContextData column for all Bitfield Format types must be in the form "<mask>;<Name>=</span></span><value><span data-ttu-id="462c5-113">;<Name>=</span><span class="sxs-lookup"><span data-stu-id="462c5-113">;<Name>=</span></span><value><span data-ttu-id="462c5-114">.... ", где <mask> — это целочисленное значение, обозначающее интересующие вас биты, <Name> — это локализуемое отображаемое имя для выбора, а</span><span class="sxs-lookup"><span data-stu-id="462c5-114">....", where <mask> is an integer value indicating the bits of interest, <Name> is a localizable display name for the choice, and</span></span> <value> <span data-ttu-id="462c5-115">Целочисленное значение типа Decimal.</span><span class="sxs-lookup"><span data-stu-id="462c5-115">is a decimal integer value.</span></span> <span data-ttu-id="462c5-116">В столбце контекста используется [Специальный формат кмсм](cmsm-special-format.md) и для всех битовых типов.</span><span class="sxs-lookup"><span data-stu-id="462c5-116">The context column is in use [CMSM Special Format](cmsm-special-format.md) and for all bitfield types.</span></span> <span data-ttu-id="462c5-117">В поле можно указать литерал "=" или ";", добавив перед <Name> ним символ обратной косой черты (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="462c5-117">A literal "=" or ";" character can be entered in the <Name> field by prefixing it with a backslash ('\\') character.</span></span>

 

 



