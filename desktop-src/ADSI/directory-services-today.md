---
title: Службы каталогов сегодня
description: Часто можно найти несколько административных каталогов, развернутых в одной организации.
ms.assetid: e6f05beb-d88d-46d5-85c7-3477a6af03c9
ms.tgt_platform: multiple
keywords:
- ADSI служб каталогов
- ADSI служб каталогов, фоновый режим для служб каталогов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38e6a6e5dfd1e0f8fc3f87d407bbbce28caa0696
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104252760"
---
# <a name="directory-services-today"></a><span data-ttu-id="845f0-105">Службы каталогов сегодня</span><span class="sxs-lookup"><span data-stu-id="845f0-105">Directory Services Today</span></span>

<span data-ttu-id="845f0-106">Часто можно найти несколько административных каталогов, развернутых в одной организации.</span><span class="sxs-lookup"><span data-stu-id="845f0-106">It is common to find multiple administrative directories deployed within a single organization.</span></span> <span data-ttu-id="845f0-107">К этим каталогам относятся каталоги сетевых ресурсов, такие как каталоги на основе LDAP, такие как служба Microsoft Active Directory Directory, Служба каталогов операционной системы Windows, а также каталоги приложений, такие как Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="845f0-107">These directories include network resource directories, such as LDAP-based directories like Microsoft Active Directory directory service, Windows operating system directory service, as well as application-specific directories, such as Microsoft Exchange.</span></span>

![Развертывание нескольких каталогов](images/ds2chal.png)

## <a name="the-directory-challenge"></a><span data-ttu-id="845f0-109">Запрос к каталогу</span><span class="sxs-lookup"><span data-stu-id="845f0-109">The Directory Challenge</span></span>

<span data-ttu-id="845f0-110">Несколько каталогов в организации имеют сложные задачи для пользователей, администраторов и разработчиков.</span><span class="sxs-lookup"><span data-stu-id="845f0-110">Multiple directories in the organization pose complex challenges to users, administrators, and developers.</span></span> <span data-ttu-id="845f0-111">Эти проблемы имеют ограниченное развертывание в каталоге.</span><span class="sxs-lookup"><span data-stu-id="845f0-111">These problems have limited wide-directory deployment.</span></span> <span data-ttu-id="845f0-112">Пользователи сталкиваются с несколькими входами и различными интерфейсами для информации в нескольких каталогах.</span><span class="sxs-lookup"><span data-stu-id="845f0-112">Users face multiple logons and a variety of interfaces to information across multiple directories.</span></span> <span data-ttu-id="845f0-113">Администраторы сталкиваются с сложностью управления несколькими каталогами.</span><span class="sxs-lookup"><span data-stu-id="845f0-113">Administrators face the complexity of managing multiple directories.</span></span> <span data-ttu-id="845f0-114">Конечным пользователям и администраторам необходимо, чтобы разработчики приложений использовали имеющийся административный каталог, но разработчики дилеммой о том, какой из них использовать.</span><span class="sxs-lookup"><span data-stu-id="845f0-114">End users and administrators want application developers to use an existing administrative directory, but developers face a dilemma about which one to use.</span></span> <span data-ttu-id="845f0-115">Каждый каталог предлагает уникальные интерфейсы приложений.</span><span class="sxs-lookup"><span data-stu-id="845f0-115">Each directory offers unique application interfaces.</span></span> <span data-ttu-id="845f0-116">Разработчик должен выбрать конкретную реализацию каталога или поддерживать несколько версий своего приложения.</span><span class="sxs-lookup"><span data-stu-id="845f0-116">A developer must choose a specific directory implementation, or support multiple versions of their application.</span></span> <span data-ttu-id="845f0-117">В результате разработчики редко используют существующие службы каталогов.</span><span class="sxs-lookup"><span data-stu-id="845f0-117">As a result, developers rarely use existing directory services.</span></span>

 

 




