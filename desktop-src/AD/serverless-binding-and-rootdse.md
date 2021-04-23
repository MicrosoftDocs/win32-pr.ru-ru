---
title: Бессерверная привязка и RootDSE
description: По возможности не следует жестко кодировать имя сервера.
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- Бессерверная привязка и RootDSE AD
- Бессерверная привязка AD
- RootDSE, реклама
- Active Directory, использование, привязка, бессерверная привязка
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 492a1ed115c4b0d9160305eb54b08c24db86abb8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487404"
---
# <a name="serverless-binding-and-rootdse"></a><span data-ttu-id="59dfb-107">Бессерверная привязка и RootDSE</span><span class="sxs-lookup"><span data-stu-id="59dfb-107">Serverless Binding and RootDSE</span></span>

<span data-ttu-id="59dfb-108">По возможности не следует жестко кодировать имя сервера.</span><span class="sxs-lookup"><span data-stu-id="59dfb-108">If possible, do not hard-code a server name.</span></span> <span data-ttu-id="59dfb-109">Более того, в большинстве случаев привязка не должна быть привязана к одному серверу.</span><span class="sxs-lookup"><span data-stu-id="59dfb-109">Furthermore, under most circumstances, binding should not be unnecessarily tied to a single server.</span></span> <span data-ttu-id="59dfb-110">Службы домен Active Directory Services поддерживают бессерверную привязку, то есть Active Directory могут быть привязаны к домену по умолчанию без указания имени контроллера домена.</span><span class="sxs-lookup"><span data-stu-id="59dfb-110">Active Directory Domain Services support serverless binding, which means that Active Directory can be bound to on the default domain without specifying the name of a domain controller.</span></span> <span data-ttu-id="59dfb-111">Для обычных приложений обычно это домен пользователя, выполнившего вход.</span><span class="sxs-lookup"><span data-stu-id="59dfb-111">For ordinary applications, this is typically the domain of the logged-on user.</span></span> <span data-ttu-id="59dfb-112">Для приложений служб это либо домен учетной записи входа в службу, либо клиент, который олицетворяет служба.</span><span class="sxs-lookup"><span data-stu-id="59dfb-112">For service applications, this is either the domain of the service logon account or that of the client that the service impersonates.</span></span>

<span data-ttu-id="59dfb-113">В LDAP 3,0 объект rootDSE определен как корень дерева данных каталога на сервере каталогов.</span><span class="sxs-lookup"><span data-stu-id="59dfb-113">In LDAP 3.0, rootDSE is defined as the root of the directory data tree on a directory server.</span></span> <span data-ttu-id="59dfb-114">RootDSE не является частью какого-либо пространства имен.</span><span class="sxs-lookup"><span data-stu-id="59dfb-114">The rootDSE is not part of any namespace.</span></span> <span data-ttu-id="59dfb-115">Целью rootDSE является предоставление данных о сервере каталогов.</span><span class="sxs-lookup"><span data-stu-id="59dfb-115">The purpose of the rootDSE is to provide data about the directory server.</span></span> <span data-ttu-id="59dfb-116">Ниже приведена строка привязки, используемая для привязки к rootDSE.</span><span class="sxs-lookup"><span data-stu-id="59dfb-116">The following is the binding string that is used to bind to rootDSE.</span></span>


```C++
LDAP://<servername>/rootDSE
```



<span data-ttu-id="59dfb-117"><servername>— Это DNS-имя сервера.</span><span class="sxs-lookup"><span data-stu-id="59dfb-117">The <servername> is the DNS name of a server.</span></span> <span data-ttu-id="59dfb-118"><servername>Является необязательным, как показано в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="59dfb-118">The <servername> is optional, as shown in the following format.</span></span>


```C++
LDAP://rootDSE
```



<span data-ttu-id="59dfb-119">В этом случае будет использоваться контроллер домена по умолчанию из домена, в котором находится контекст безопасности вызывающего потока.</span><span class="sxs-lookup"><span data-stu-id="59dfb-119">In this case, a default domain controller from the domain that the security context of the calling thread is in will be used.</span></span> <span data-ttu-id="59dfb-120">Если к контроллеру домена нельзя получить доступ внутри сайта, будет использоваться первый контроллер домена, который можно найти.</span><span class="sxs-lookup"><span data-stu-id="59dfb-120">If a domain controller cannot be accessed within the site, the first domain controller that can be found will be used.</span></span>

<span data-ttu-id="59dfb-121">RootDSE — это хорошо известное и надежное расположение на каждом сервере каталогов для получения различающихся имен контейнеров, схем и областей конфигурации, а также других данных о сервере и содержимом его дерева данных каталога.</span><span class="sxs-lookup"><span data-stu-id="59dfb-121">The rootDSE is a well-known and reliable location on every directory server to get distinguished names of the domain, schema, and configuration containers, and other data about the server and the contents of its directory data tree.</span></span> <span data-ttu-id="59dfb-122">Эти свойства редко меняются на конкретном сервере.</span><span class="sxs-lookup"><span data-stu-id="59dfb-122">These properties rarely change on a particular server.</span></span> <span data-ttu-id="59dfb-123">Приложение может считывать эти свойства при запуске и использовать их во время сеанса.</span><span class="sxs-lookup"><span data-stu-id="59dfb-123">An application can read these properties at startup and use them throughout the session.</span></span>

<span data-ttu-id="59dfb-124">В целом, приложение должно использовать бессерверную привязку для привязки к каталогу в текущем домене, использовать rootDSE для получения различающегося имени пространства имен и использовать это различающееся имя для привязки к объектам в пространстве имен.</span><span class="sxs-lookup"><span data-stu-id="59dfb-124">In summary, an application should use serverless binding to bind to the directory on the current domain, use rootDSE to get the distinguished name for a namespace, and use that distinguished name to bind to objects in the namespace.</span></span>

<span data-ttu-id="59dfb-125">Дополнительные сведения об атрибутах, поддерживаемых rootDSE, см. в разделе [RootDSE](/windows/desktop/ADSchema/rootdse) в документации по схеме Active Directory.</span><span class="sxs-lookup"><span data-stu-id="59dfb-125">For more information about attributes supported by rootDSE, see [RootDSE](/windows/desktop/ADSchema/rootdse) in the Active Directory Schema documentation.</span></span>

<span data-ttu-id="59dfb-126">Дополнительные сведения и пример кода, в котором показано, как использовать бессерверную привязку и rootDSE, см. в разделе [пример кода для получения различающегося имени домена](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span><span class="sxs-lookup"><span data-stu-id="59dfb-126">For more information and a code example that shows how to use serverless binding and rootDSE, see [Example Code for Getting the Distinguished Name of the Domain](example-code-for-getting-the-distinguished-name-of-the-domain.md).</span></span>

 

 