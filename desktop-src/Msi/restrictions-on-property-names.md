---
description: Все имена свойств должны соответствовать этим ограничениям.
ms.assetid: 4447013a-86c4-48a9-bfe1-5e758c799a2f
title: Ограничения по именам свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c137bc4902bdd62b42e4f3888243a11de43399b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265821"
---
# <a name="restrictions-on-property-names"></a><span data-ttu-id="84d0e-103">Ограничения по именам свойств</span><span class="sxs-lookup"><span data-stu-id="84d0e-103">Restrictions on Property Names</span></span>

<span data-ttu-id="84d0e-104">Все имена свойств должны соответствовать этим ограничениям.</span><span class="sxs-lookup"><span data-stu-id="84d0e-104">All property names must follow these restrictions.</span></span>

-   <span data-ttu-id="84d0e-105">Имя свойства — это [идентификатор](identifier.md), который представляет собой текстовую строку, которая должна начинаться с буквы или символа подчеркивания.</span><span class="sxs-lookup"><span data-stu-id="84d0e-105">A property name is an [Identifier](identifier.md), which is a text string that must begin with either a letter or an underscore.</span></span> <span data-ttu-id="84d0e-106">Идентификаторы и имена свойств могут содержать буквы, цифры, символы подчеркивания или точки; но не может начинаться с цифры или точки.</span><span class="sxs-lookup"><span data-stu-id="84d0e-106">Identifiers and property names may contain letters, numerals, underscores, or periods; but cannot begin with a numeral or period.</span></span>
-   <span data-ttu-id="84d0e-107">Имена [общедоступных свойств](public-properties.md) не могут содержать строчные буквы.</span><span class="sxs-lookup"><span data-stu-id="84d0e-107">[Public property](public-properties.md) names cannot contain lowercase letters.</span></span>
-   <span data-ttu-id="84d0e-108">Имена [частных свойств](private-properties.md) должны содержать несколько строчных букв.</span><span class="sxs-lookup"><span data-stu-id="84d0e-108">[Private property](private-properties.md) names must contain some lowercase letters.</span></span>
-   <span data-ttu-id="84d0e-109">Имена свойств с префиксом% представляют переменные среды системы и пользователя.</span><span class="sxs-lookup"><span data-stu-id="84d0e-109">Property names prefixed with % represent system and user environment variables.</span></span> <span data-ttu-id="84d0e-110">Они никогда не вносятся в [таблицу свойств](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="84d0e-110">These are never entered into the [Property table](property-table.md).</span></span> <span data-ttu-id="84d0e-111">Постоянные параметры переменных среды можно изменить только с помощью [таблицы Environment](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="84d0e-111">The permanent settings of environment variables can only be modified using the [Environment Table](environment-table.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="84d0e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="84d0e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="84d0e-113">Использование свойств</span><span class="sxs-lookup"><span data-stu-id="84d0e-113">Using Properties</span></span>](using-properties.md)
</dt> </dl>

 

 



