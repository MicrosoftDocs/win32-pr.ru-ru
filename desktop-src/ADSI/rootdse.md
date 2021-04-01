---
title: RootDSE (ADSI)
description: Каждый сервер каталога имеет уникальную запись RootDSE. Он предоставляет данные о сервере, например его возможности, поддерживаемую версию LDAP и используемые контексты именования.
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103793831"
---
# <a name="rootdse-adsi"></a><span data-ttu-id="f2509-104">RootDSE (ADSI)</span><span class="sxs-lookup"><span data-stu-id="f2509-104">RootDSE (ADSI)</span></span>

<span data-ttu-id="f2509-105">Каждый сервер каталога имеет уникальную запись **RootDSE**.</span><span class="sxs-lookup"><span data-stu-id="f2509-105">Each directory server has a unique entry called **RootDSE**.</span></span> <span data-ttu-id="f2509-106">Он предоставляет данные о сервере, например его возможности, поддерживаемую версию LDAP и используемые контексты именования.</span><span class="sxs-lookup"><span data-stu-id="f2509-106">It provides data about the server, such as its capabilities, the LDAP version it supports, and the naming contexts it uses.</span></span>

<span data-ttu-id="f2509-107">Например, для создания скрипта или приложения, которое может выполняться в любой среде домена Windows.</span><span class="sxs-lookup"><span data-stu-id="f2509-107">For example, to create a script, or application, that can run on any Windows domain environment.</span></span> <span data-ttu-id="f2509-108">При подключении к Active Directory можно указать различающееся имя, имя сервера или доменное имя.</span><span class="sxs-lookup"><span data-stu-id="f2509-108">You can specify either the distinguished name, server name, or domain name when connecting to Active Directory.</span></span> <span data-ttu-id="f2509-109">Если эти сведения отсутствуют, можно использовать объект **RootDSE** для установления соединения.</span><span class="sxs-lookup"><span data-stu-id="f2509-109">If you do not have this information, you can then use the **RootDSE** object to establish a connection.</span></span> <span data-ttu-id="f2509-110">В следующем примере кода показано изменение описания домена в любом домене.</span><span class="sxs-lookup"><span data-stu-id="f2509-110">The following code example changes the domain description in any domain.</span></span>


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



<span data-ttu-id="f2509-111">Получив атрибут **дефаултнамингконтекст** из **RootDSE**, можно выполнить привязку к текущему домену, например, Fabrikam **дефаултнамингконтекст** — DC = Fabrikam, DC = com.</span><span class="sxs-lookup"><span data-stu-id="f2509-111">By getting the **defaultNamingContext** attribute from **RootDSE**, you can bind to the current domain, for example, the Fabrikam **defaultNamingContext** is DC=Fabrikam, DC=COM.</span></span>

<span data-ttu-id="f2509-112">Чтобы перечислить свойства **RootDSE**, используйте интерфейс [**иадспропертилист**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) .</span><span class="sxs-lookup"><span data-stu-id="f2509-112">To enumerate the properties of the **RootDSE**, use the [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) interface.</span></span> <span data-ttu-id="f2509-113">[**Идиректорйобжект**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) нельзя использовать для этой задачи.</span><span class="sxs-lookup"><span data-stu-id="f2509-113">[**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) cannot be used for this task.</span></span>

<span data-ttu-id="f2509-114">Дополнительные сведения см. в статье [бессерверная привязка и RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span><span class="sxs-lookup"><span data-stu-id="f2509-114">For more information, see [Serverless Binding and RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse).</span></span>

 

 