---
description: Типы текстовых форматов с настраиваемыми данными могут быть текстовыми строками любой длины. Внедренные значения NULL не допускаются.
ms.assetid: 71b89f87-43ba-41cd-a969-765d45da4ba4
title: Типы текстовых форматов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a8f05a0804569667a74c52392d322f3fed2818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651191"
---
# <a name="text-format-types"></a><span data-ttu-id="f9054-104">Типы текстовых форматов</span><span class="sxs-lookup"><span data-stu-id="f9054-104">Text Format Types</span></span>

<span data-ttu-id="f9054-105">Типы текстовых форматов с настраиваемыми данными могут быть текстовыми строками любой длины.</span><span class="sxs-lookup"><span data-stu-id="f9054-105">The text format types of configurable data may be text strings of any length.</span></span> <span data-ttu-id="f9054-106">Внедренные значения NULL не допускаются.</span><span class="sxs-lookup"><span data-stu-id="f9054-106">Embedded nulls are not allowed.</span></span>

<span data-ttu-id="f9054-107">Существуют следующие типы форматов текста:</span><span class="sxs-lookup"><span data-stu-id="f9054-107">The following Text Format types exist:</span></span>

[<span data-ttu-id="f9054-108">Произвольный текст</span><span class="sxs-lookup"><span data-stu-id="f9054-108">Arbitrary Text</span></span>](arbitrary-text-type.md)

[<span data-ttu-id="f9054-109">RTF</span><span class="sxs-lookup"><span data-stu-id="f9054-109">RTF</span></span>](rtf-type.md)

[<span data-ttu-id="f9054-110">Формате</span><span class="sxs-lookup"><span data-stu-id="f9054-110">Formatted</span></span>](formatted-type.md)

[<span data-ttu-id="f9054-111">Enum</span><span class="sxs-lookup"><span data-stu-id="f9054-111">Enum</span></span>](enum-type.md)

[<span data-ttu-id="f9054-112">Тип идентификатора</span><span class="sxs-lookup"><span data-stu-id="f9054-112">Identifier Type</span></span>](identifier-type.md)

<span data-ttu-id="f9054-113">Настраиваемые элементы типа текстового формата используются в недвоичных полях базы данных, и в целом их можно заменить любой строкой любой длины.</span><span class="sxs-lookup"><span data-stu-id="f9054-113">Configurable items of the Text Format Type are used in non-binary database fields and in general could be replaced by any string of any length.</span></span> <span data-ttu-id="f9054-114">Однако некоторые настраиваемые элементы также имеют семантические ограничения.</span><span class="sxs-lookup"><span data-stu-id="f9054-114">However, particular configurable items also have semantic restrictions.</span></span> <span data-ttu-id="f9054-115">Например, настраиваемый элемент, который должен быть внешним ключом в определенной таблице, имеет дополнительные семантические ограничения.</span><span class="sxs-lookup"><span data-stu-id="f9054-115">For example, a configurable item that is required to be a foreign key into a specific table has additional semantic restrictions.</span></span> <span data-ttu-id="f9054-116">Такие семантические ограничения не применяются Mergemod.dll, поэтому авторы модулей должны быть готовы к обработке любой строки, удовлетворяющей заданному типу форматирования текста.</span><span class="sxs-lookup"><span data-stu-id="f9054-116">Such semantic restrictions are not enforced by Mergemod.dll and therefore module authors should be prepared to handle any string that satisfies the specified Text Format type.</span></span>

 

 



