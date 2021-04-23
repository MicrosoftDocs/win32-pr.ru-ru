---
description: Идентификаторы указывают имена столбцов (иногда называемых свойствами), каталоги и псевдонимы.
ms.assetid: 799afe2c-9217-4006-a4a3-644e5393993c
title: Идентификаторы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df79bd0d70564ea3e87ff4821a1cb59e3d0a5eb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144086"
---
# <a name="identifiers"></a><span data-ttu-id="97ae4-103">Идентификаторы</span><span class="sxs-lookup"><span data-stu-id="97ae4-103">Identifiers</span></span>

<span data-ttu-id="97ae4-104">Идентификаторы указывают имена столбцов (иногда называемых свойствами), каталоги и псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="97ae4-104">Identifiers specify the names of columns (sometimes referred to as properties), catalogs, and aliases.</span></span> <span data-ttu-id="97ae4-105">Например, System. ItemName и System. DateCreated являются идентификаторами двух определяемых системой столбцов свойств.</span><span class="sxs-lookup"><span data-stu-id="97ae4-105">For example, System.ItemName and System.DateCreated are the identifiers of two system-defined property columns.</span></span> <span data-ttu-id="97ae4-106">Литералы, напротив, указывают строковые и числовые значения.</span><span class="sxs-lookup"><span data-stu-id="97ae4-106">Literals, by contrast, specify string and numeric values.</span></span>


<span data-ttu-id="97ae4-107">Можно создавать идентификаторы длиной до 128 символов и в одном из двух типов, в отличие от символов, используемых в имени идентификатора:</span><span class="sxs-lookup"><span data-stu-id="97ae4-107">You can create identifiers that are up to 128 characters long, and in one of two types, distinguished by the characters used in the identifier name:</span></span>

-   <span data-ttu-id="97ae4-108">**Обычные идентификаторы** содержат только символы a – z, A – z, 0-9, символ подчеркивания ( \_ ) и точку (.) и начинаются с буквы.</span><span class="sxs-lookup"><span data-stu-id="97ae4-108">**Regular identifiers** contain only the characters A-Z, a-z, 0-9, underscore (\_), and dot (.), and they begin with a letter.</span></span> <span data-ttu-id="97ae4-109">Обычные идентификаторы не нужно заключать в двойные кавычки ("").</span><span class="sxs-lookup"><span data-stu-id="97ae4-109">You do not need to enclose regular identifiers in double quotation marks (" ").</span></span>
-   <span data-ttu-id="97ae4-110">**Идентификаторы с разделителями** могут содержать любой допустимый символ Юникода и должны быть заключены в двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="97ae4-110">**Delimited identifiers** can contain any valid Unicode character and must be enclosed in double quotation marks.</span></span>

> [!Note]  
> <span data-ttu-id="97ae4-111">В предложениях FREETEXT и CONTAINS можно использовать звездочку () в \* качестве специального идентификатора столбца, если необходимо указать, что в Windows Search будут включены все индексированные свойства в запросе.</span><span class="sxs-lookup"><span data-stu-id="97ae4-111">In FREETEXT and CONTAINS clauses, you can use the asterisk (\*) as a special column identifier when you want to specify that Windows Search includes all of the indexed properties in the query.</span></span> <span data-ttu-id="97ae4-112">Хотя это не обычный идентификатор, для него не требуются двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="97ae4-112">Although it is not a regular identifier, it does not require double quotation marks.</span></span>

 

 

 



