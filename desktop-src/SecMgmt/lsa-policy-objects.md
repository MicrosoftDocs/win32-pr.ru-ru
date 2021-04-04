---
description: LSA сохраняет сведения о локальной политике безопасности в наборе объектов. Приложение может запрашивать или изменять локальную политику безопасности, обращаясь к этим объектам.
ms.assetid: c8ed5cd8-55cf-43e7-92a3-9bd17a1147a9
title: Объекты политики LSA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1481b6a6f49e973ecc2a2e1b53830bf22c67a77f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998621"
---
# <a name="lsa-policy-objects"></a><span data-ttu-id="222c1-104">Объекты политики LSA</span><span class="sxs-lookup"><span data-stu-id="222c1-104">LSA Policy Objects</span></span>

<span data-ttu-id="222c1-105">LSA сохраняет сведения о локальной политике безопасности в наборе объектов.</span><span class="sxs-lookup"><span data-stu-id="222c1-105">The LSA stores local security policy information in a set of objects.</span></span> <span data-ttu-id="222c1-106">Приложение может запрашивать или изменять локальную политику безопасности, обращаясь к этим объектам.</span><span class="sxs-lookup"><span data-stu-id="222c1-106">Your application can query or edit the local security policy by accessing these objects.</span></span>

<span data-ttu-id="222c1-107">Набор состоит из следующих четырех объектов:</span><span class="sxs-lookup"><span data-stu-id="222c1-107">The set consists of the following four objects:</span></span>

-   <span data-ttu-id="222c1-108">[Политика](policy-object.md) содержит сведения о глобальных политиках.</span><span class="sxs-lookup"><span data-stu-id="222c1-108">[Policy](policy-object.md) contains global policy information.</span></span>
-   <span data-ttu-id="222c1-109">[Трустеддомаин](trusteddomain-object.md) содержит сведения о доверенном домене.</span><span class="sxs-lookup"><span data-stu-id="222c1-109">[TrustedDomain](trusteddomain-object.md) contains information about a trusted domain.</span></span>
-   <span data-ttu-id="222c1-110">[Учетная запись](account-object.md) содержит сведения о пользователе, группе или учетной записи локальной группы.</span><span class="sxs-lookup"><span data-stu-id="222c1-110">[Account](account-object.md) contains information about a user, group, or local group account.</span></span>
-   <span data-ttu-id="222c1-111">[Личные данные](private-data-object.md) содержат защищенную информацию, например пароли учетной записи сервера.</span><span class="sxs-lookup"><span data-stu-id="222c1-111">[Private Data](private-data-object.md) contains protected information, such as server account passwords.</span></span> <span data-ttu-id="222c1-112">Эти сведения хранятся в виде зашифрованных строк.</span><span class="sxs-lookup"><span data-stu-id="222c1-112">This information is stored as encrypted strings.</span></span>

<span data-ttu-id="222c1-113">Дополнительные сведения об использовании функций политики LSA для управления данными, хранящимися в этих объектах, см. в разделе [Использование политики LSA](using-lsa-policy.md).</span><span class="sxs-lookup"><span data-stu-id="222c1-113">For more information on how to use the LSA Policy functions to manage the information stored in these objects, see [Using LSA Policy](using-lsa-policy.md).</span></span>

 

 



