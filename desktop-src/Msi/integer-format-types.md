---
description: Типы целочисленных форматов настраиваемых данных могут использоваться в полях базы данных text или Integer. Атрибут Мсмконфигитемноннуллабле является неявным в этом формате данных и не требует установки. Значение NULL никогда не является допустимым значением для этого типа.
ms.assetid: 63fb9c0d-e7f1-4c1d-bb83-2833c5fff18d
title: Типы целочисленных форматов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184ef6380f25474a9e2ad07be7a4eb6d00706aee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103814401"
---
# <a name="integer-format-types"></a><span data-ttu-id="90adf-105">Типы целочисленных форматов</span><span class="sxs-lookup"><span data-stu-id="90adf-105">Integer Format Types</span></span>

<span data-ttu-id="90adf-106">Типы целочисленных форматов настраиваемых данных могут использоваться в полях базы данных text или Integer.</span><span class="sxs-lookup"><span data-stu-id="90adf-106">The Integer Format Types of configurable data may be used in either text or integer database fields.</span></span> <span data-ttu-id="90adf-107">Атрибут Мсмконфигитемноннуллабле является неявным в этом формате данных и не требует установки.</span><span class="sxs-lookup"><span data-stu-id="90adf-107">The msmConfigItemNonNullable attribute is implicit in this data format and does not need to be set.</span></span> <span data-ttu-id="90adf-108">Значение NULL никогда не является допустимым значением для этого типа.</span><span class="sxs-lookup"><span data-stu-id="90adf-108">Null is never a valid value for this type.</span></span>

<span data-ttu-id="90adf-109">Существует следующий тип целочисленного формата.</span><span class="sxs-lookup"><span data-stu-id="90adf-109">The following Integer Format type exists.</span></span>

[<span data-ttu-id="90adf-110">Произвольный целочисленный тип</span><span class="sxs-lookup"><span data-stu-id="90adf-110">Arbitrary Integer Type</span></span>](arbitrary-integer-type.md)

<span data-ttu-id="90adf-111">Настраиваемые элементы типа целочисленного формата используются в текстовых или целочисленных столбцах, а в целом могут быть заменены любым положительным или отрицательным целым числом.</span><span class="sxs-lookup"><span data-stu-id="90adf-111">Configurable items of the Integer Format Type are used in either text or integer columns and in general could be replaced by any positive or negative integer.</span></span> <span data-ttu-id="90adf-112">Однако некоторые настраиваемые элементы также могут иметь ограничения семантики характеристик.</span><span class="sxs-lookup"><span data-stu-id="90adf-112">However, particular configurable items may also have characteristic semantic restrictions.</span></span> <span data-ttu-id="90adf-113">Например, определенный настраиваемый элемент, который должен быть целым числом от 0 до 100, имеет и дополнительное семантическое ограничение.</span><span class="sxs-lookup"><span data-stu-id="90adf-113">For example, a particular configurable item required to be an integer between 0 and 100 has and additional semantic restriction.</span></span> <span data-ttu-id="90adf-114">Такие ограничения не применяются Mergemod.dll, поэтому авторы модулей должны быть готовы к обработке любой строки, удовлетворяющей определенному типу целочисленного формата.</span><span class="sxs-lookup"><span data-stu-id="90adf-114">Such restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Integer Format type.</span></span>

 

 



