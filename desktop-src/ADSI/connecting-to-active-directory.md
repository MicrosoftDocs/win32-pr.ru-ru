---
title: Подключение к Active Directory
description: Существует несколько методов, используемых для доступа к Active Directory.
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- Подключение к Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986113"
---
# <a name="connecting-to-active-directory"></a><span data-ttu-id="40073-104">Подключение к Active Directory</span><span class="sxs-lookup"><span data-stu-id="40073-104">Connecting to Active Directory</span></span>

<span data-ttu-id="40073-105">Существует несколько методов, используемых для доступа к Active Directory.</span><span class="sxs-lookup"><span data-stu-id="40073-105">There are several methods used to access Active Directory.</span></span> <span data-ttu-id="40073-106">Для доступа к Active Directory рекомендуется использовать API ADSI.</span><span class="sxs-lookup"><span data-stu-id="40073-106">It is recommended that you use the ADSI API to access Active Directory.</span></span> <span data-ttu-id="40073-107">ADSI реализует протокол LDAP для взаимодействия с Active Directory.</span><span class="sxs-lookup"><span data-stu-id="40073-107">ADSI implements the LDAP protocol to communicate with Active Directory.</span></span> <span data-ttu-id="40073-108">В следующем примере кода показано, как получить доступ к Active Directory.</span><span class="sxs-lookup"><span data-stu-id="40073-108">The following code examples show how to access Active Directory.</span></span>


```VB
Set ns = GetObject("LDAP:")
```



<span data-ttu-id="40073-109">Откроется поставщик LDAP и подготовится к получению данных.</span><span class="sxs-lookup"><span data-stu-id="40073-109">This opens the LDAP provider and prepares it to retrieve data.</span></span> <span data-ttu-id="40073-110">Подключение не устанавливается, пока не будут запрошены данные.</span><span class="sxs-lookup"><span data-stu-id="40073-110">No connection is established until data is requested.</span></span> <span data-ttu-id="40073-111">При запросе данных ADSI с помощью службы локатора пытается найти оптимальный контроллер домена для подключения и установит соединение с сервером.</span><span class="sxs-lookup"><span data-stu-id="40073-111">When data is requested, ADSI, with the help of the locator service, attempts to find the best domain controller (DC) for the connection and will establish a connection to the server.</span></span> <span data-ttu-id="40073-112">Этот процесс называется бессерверной привязкой.</span><span class="sxs-lookup"><span data-stu-id="40073-112">This process is known as serverless binding.</span></span>

<span data-ttu-id="40073-113">ADSI также позволяет указать имя сервера, которое будет использоваться для соединения.</span><span class="sxs-lookup"><span data-stu-id="40073-113">ADSI also enables you to specify the server name to use for the connection.</span></span>


```VB
Set obj = GetObject("LDAP://mysrv01")
```



<span data-ttu-id="40073-114">В другом сценарии может быть только известно имя домена, но не конкретное имя сервера.</span><span class="sxs-lookup"><span data-stu-id="40073-114">In another scenario, you may only know the domain name but not the specific server name.</span></span> <span data-ttu-id="40073-115">Опять же, ADSI позволяет указать доменное имя.</span><span class="sxs-lookup"><span data-stu-id="40073-115">Again, ADSI enables you to specify the domain name.</span></span> <span data-ttu-id="40073-116">В Windows 2000 имя домена представлено в виде DNS-имени.</span><span class="sxs-lookup"><span data-stu-id="40073-116">In Windows 2000, the domain name is represented as a DNS name.</span></span> <span data-ttu-id="40073-117">Например, если Джо Ворден, администратор сети, выбирает подключение с использованием доменного имени, он мог бы использовать следующий пример кода.</span><span class="sxs-lookup"><span data-stu-id="40073-117">For example, if Joe Worden, the network administrator, chooses to connect using the domain name, he could use the following code example.</span></span>


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



<span data-ttu-id="40073-118">ADSI будет подключаться к одному из контроллеров домена в домене fabrikam.com.</span><span class="sxs-lookup"><span data-stu-id="40073-118">ADSI will connect to one of the domain controllers in the fabrikam.com domain.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40073-119">См. также</span><span class="sxs-lookup"><span data-stu-id="40073-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40073-120">Привязка к Active Directory объектам</span><span class="sxs-lookup"><span data-stu-id="40073-120">Binding to Active Directory Objects</span></span>](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




