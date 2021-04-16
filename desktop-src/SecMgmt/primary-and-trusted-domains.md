---
description: Следующие термины описывают домены, существующие в удаленных системах.
ms.assetid: a6ce5356-682a-46ae-a101-15227c3b8d1e
title: Первичный и доверенный домены
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30d69a8bf5f5a8363f8de726c6183fd4de820665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540983"
---
# <a name="primary-and-trusted-domains"></a><span data-ttu-id="eead8-103">Первичный и доверенный домены</span><span class="sxs-lookup"><span data-stu-id="eead8-103">Primary and Trusted Domains</span></span>

<span data-ttu-id="eead8-104">Следующие термины описывают домены, существующие в удаленных системах.</span><span class="sxs-lookup"><span data-stu-id="eead8-104">The following terms describe domains that exist on remote systems.</span></span>

-   [<span data-ttu-id="eead8-105">Основной домен</span><span class="sxs-lookup"><span data-stu-id="eead8-105">Primary Domain</span></span>](#primary-domain)
-   [<span data-ttu-id="eead8-106">Доверенный домен</span><span class="sxs-lookup"><span data-stu-id="eead8-106">Trusted Domain</span></span>](#primary-and-trusted-domains)

## <a name="primary-domain"></a><span data-ttu-id="eead8-107">Основной домен</span><span class="sxs-lookup"><span data-stu-id="eead8-107">Primary Domain</span></span>

<span data-ttu-id="eead8-108">Основной домен — это домен, отвечающий за установку дополнительных отношений доверия и проверку подлинности (или передачу запроса на проверку подлинности в соответствующий доверенный домен).</span><span class="sxs-lookup"><span data-stu-id="eead8-108">A primary domain is the domain that is responsible for establishing further trust relationships and performing authentication (or for passing an authentication request on to an appropriate trusted domain).</span></span> <span data-ttu-id="eead8-109">Контроллеры домена в основном домене обработают или передают запросы проверки подлинности, поступающие на рабочую станцию.</span><span class="sxs-lookup"><span data-stu-id="eead8-109">The domain controllers in the primary domain handle or pass along authentication requests that originate at the workstation.</span></span>

<span data-ttu-id="eead8-110">При входе LSA проверяет встроенные домены и домен учетной записи на наличие сведений для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="eead8-110">When logon occurs, the LSA checks the built-in and account domains for authentication information.</span></span> <span data-ttu-id="eead8-111">Если учетная запись, которая входит в систему, не находится ни в одном из этих доменов, запрос на вход передается в основной домен системы.</span><span class="sxs-lookup"><span data-stu-id="eead8-111">If the account being logged on to is not in either of these domains, the logon request is handed off to the system's primary domain.</span></span>

## <a name="trusted-domain"></a><span data-ttu-id="eead8-112">Доверенный домен</span><span class="sxs-lookup"><span data-stu-id="eead8-112">Trusted Domain</span></span>

<span data-ttu-id="eead8-113">Доверенный домен — это домен, которому локальная система доверяет проверке подлинности пользователей.</span><span class="sxs-lookup"><span data-stu-id="eead8-113">A trusted domain is a domain that the local system trusts to authenticate users.</span></span> <span data-ttu-id="eead8-114">Иными словами, если пользователь или приложение проходят проверку подлинности в доверенном домене, эта проверка подлинности принимается всеми доменами, которые доверяют домену, используемому для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="eead8-114">In other words, if a user or application is authenticated by a trusted domain, this authentication is accepted by all domains that trust the authenticating domain.</span></span>

<span data-ttu-id="eead8-115">Каждый подчиненный домен автоматически имеет двустороннее отношение доверия с основным доменом.</span><span class="sxs-lookup"><span data-stu-id="eead8-115">Each subordinate domain automatically has a two-way trust relationship with the main domain.</span></span> <span data-ttu-id="eead8-116">По умолчанию это отношение доверия является транзитивным, то есть если система доверяет домену а, она также доверяет всем доменам, которым доверяет домен.</span><span class="sxs-lookup"><span data-stu-id="eead8-116">By default, this trust is transitive, meaning that if a system trusts Domain A, it also trusts all domains that Domain A trusts.</span></span> <span data-ttu-id="eead8-117">Односторонние отношения доверия также поддерживаются для операционных систем, предшествующих Windows 2000, которые не поддерживают транзитивные двусторонние отношения доверия.</span><span class="sxs-lookup"><span data-stu-id="eead8-117">One-way trusts are also supported for operating systems earlier than Windows 2000, which do not support transitive, two-way trusts.</span></span>

<span data-ttu-id="eead8-118">[*Локальный центр безопасности*](/windows/desktop/SecGloss/l-gly) (LSA) имеет тип объекта [**трустеддомаин**](the-trusteddomain-object-type.md), который используется для хранения сведений о доверительных отношениях, включая имя и [*идентификатор безопасности*](/windows/desktop/SecGloss/s-gly) (SID) доверенного домена, учетную запись в домене, используемую для запросов проверки подлинности, запросы на преобразование имен и SID, а также имена контроллеров домена в доверенном домене.</span><span class="sxs-lookup"><span data-stu-id="eead8-118">The [*Local Security Authority*](/windows/desktop/SecGloss/l-gly) (LSA) has an object type, [**TrustedDomain**](the-trusteddomain-object-type.md), that is used to store information about trust relationships, including the name and [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) of the trusted domain, the account in the domain to use for authentication requests, name and SID translation requests, and the names of domain controllers in the trusted domain.</span></span>

<span data-ttu-id="eead8-119">В контроллерах домена LSA создает экземпляр объекта [**трустеддомаин**](the-trusteddomain-object-type.md) для каждого домена, которому доверяет локальная система.</span><span class="sxs-lookup"><span data-stu-id="eead8-119">On domain controllers, the LSA creates an instance of a [**TrustedDomain**](the-trusteddomain-object-type.md) object for each domain trusted by the local system.</span></span>

<span data-ttu-id="eead8-120">Например, если Рабочая станция Windows XP доверяет контроллеру домена Windows 2000, который в свою очередь доверяет четырем другим системам, Рабочая станция, подключенная с использованием транзитивные доверительных отношений, будет иметь пять объектов [**трустеддомаин**](the-trusteddomain-object-type.md) в своей локальной системе.</span><span class="sxs-lookup"><span data-stu-id="eead8-120">For example, if a Windows XP workstation trusts a Windows 2000 domain controller that in turn trusts four other systems, the workstation, connected using transitive trust, will have five [**TrustedDomain**](the-trusteddomain-object-type.md) objects on its local system.</span></span>

 

 
