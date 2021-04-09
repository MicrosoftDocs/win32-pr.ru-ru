---
description: Запросы схемы — это инструкции WQL, которые запрашивают определения классов и сведения о связях схем.
ms.assetid: cb65e99f-9046-4c63-ab56-60dedc45bcef
ms.tgt_platform: multiple
title: Получение определений классов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d865b1a85eefa7e67b12ed4c0acc16ea9e19f9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155858"
---
# <a name="retrieving-class-definitions"></a><span data-ttu-id="6884f-103">Получение определений классов</span><span class="sxs-lookup"><span data-stu-id="6884f-103">Retrieving Class Definitions</span></span>

<span data-ttu-id="6884f-104">Запросы схемы — это инструкции WQL, которые запрашивают определения классов и сведения о [связях схем](schema-associations.md).</span><span class="sxs-lookup"><span data-stu-id="6884f-104">Schema queries are WQL statements that request class definitions and information about [schema associations](schema-associations.md).</span></span> <span data-ttu-id="6884f-105">Поставщики классов используют запросы схемы в своих экземплярах класса [**\_ \_ класспровидеррегистратион**](--classproviderregistration.md) для указания классов, которые они поддерживают при регистрации в WMI.</span><span class="sxs-lookup"><span data-stu-id="6884f-105">Class providers use schema queries in their instances of the [**\_\_ClassProviderRegistration**](--classproviderregistration.md) class to specify the classes that they support when they register with WMI.</span></span> <span data-ttu-id="6884f-106">Запросы схемы размещаются в свойствах **ресултсеткуериес**, **референцедсеткуериес** и **унсуппортедкуериес** экземпляра **\_ \_ класспровидеррегистратион** .</span><span class="sxs-lookup"><span data-stu-id="6884f-106">Schema queries are placed in the **ResultSetQueries**, **ReferencedSetQueries**, and **UnsupportedQueries** properties of the **\_\_ClassProviderRegistration** instance.</span></span>

<span data-ttu-id="6884f-107">Запросы схемы похожи на запросы данных в том, что они поддерживают следующие инструкции WQL:</span><span class="sxs-lookup"><span data-stu-id="6884f-107">Schema queries are similar to data queries in that they support the following WQL statements:</span></span>

-   [<span data-ttu-id="6884f-108">SELECT</span><span class="sxs-lookup"><span data-stu-id="6884f-108">SELECT</span></span>](select-statement-for-schema-queries.md)
-   [<span data-ttu-id="6884f-109">СОЕДИНИТЕЛи</span><span class="sxs-lookup"><span data-stu-id="6884f-109">ASSOCIATORS OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="6884f-110">ССЫЛКИ НА</span><span class="sxs-lookup"><span data-stu-id="6884f-110">REFERENCES OF</span></span>](schema-associations.md)
-   [<span data-ttu-id="6884f-111">ISA</span><span class="sxs-lookup"><span data-stu-id="6884f-111">ISA</span></span>](isa-operator-for-schema-queries.md)

<span data-ttu-id="6884f-112">Запрос схемы похож на [ссылку](references-of-statement.md) на запрос данных, указывающий ключевое слово **классдефсонли** . Иными словами, он возвращает результирующий набор объектов определения класса, а не фактические экземпляры классов взаимосвязей.</span><span class="sxs-lookup"><span data-stu-id="6884f-112">A schema query is similar to a [REFERENCES OF](references-of-statement.md) data query that specifies the **ClassDefsOnly** keyword; in other words, that returns a result set of class definition objects rather than actual instances of association classes.</span></span> <span data-ttu-id="6884f-113">Однако ссылки на определения класса возвращаются только при наличии экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6884f-113">However, REFERENCES OF returns class definitions only if there are instances present.</span></span> <span data-ttu-id="6884f-114">Запрос схемы возвращает определения классов независимо от наличия экземпляров.</span><span class="sxs-lookup"><span data-stu-id="6884f-114">A schema query returns class definitions whether or not instances are present.</span></span>

 

 



