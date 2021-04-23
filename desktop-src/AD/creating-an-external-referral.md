---
title: Создание внешней ссылки
description: Если создается внешний объект crossRef, а контроллер домена использует его для создания ссылки, то объект crossRef предоставляет два важных элемента данных в следующих свойствах.
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- Внешние ссылки Active Directory
- Active Directory примеры Active Directory, создание внешней ссылки
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789594"
---
# <a name="creating-an-external-referral"></a><span data-ttu-id="ed26e-105">Создание внешней ссылки</span><span class="sxs-lookup"><span data-stu-id="ed26e-105">Creating an External Referral</span></span>

<span data-ttu-id="ed26e-106">Если создается внешний объект [**crossRef**](/windows/desktop/ADSchema/c-crossref) , а контроллер домена использует его для создания ссылки, то объект **crossRef** предоставляет два важных элемента данных в следующих свойствах.</span><span class="sxs-lookup"><span data-stu-id="ed26e-106">If an external [**crossRef**](/windows/desktop/ADSchema/c-crossref) object is created and a domain controller uses it to generate a referral, the **crossRef** object provides two important data elements in the following properties.</span></span> <span data-ttu-id="ed26e-107">Дополнительные сведения о ситуациях, в которых это может произойти, см. в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="ed26e-107">For more information about situations where this can occur, see the previous section.</span></span>



| <span data-ttu-id="ed26e-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="ed26e-108">Property</span></span>                           | <span data-ttu-id="ed26e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="ed26e-109">Description</span></span>                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed26e-110">**днсрут**</span><span class="sxs-lookup"><span data-stu-id="ed26e-110">**dnsRoot**</span></span>](/windows/desktop/ADSchema/a-dnsroot) | <span data-ttu-id="ed26e-111">Указывает сервер или домен, который может обрабатывать данные из контекста именования, указанного в [**NCName**](/windows/desktop/ADSchema/a-ncname).</span><span class="sxs-lookup"><span data-stu-id="ed26e-111">Specifies the server or domain that can serve data from the naming context specified in [**nCName**](/windows/desktop/ADSchema/a-ncname).</span></span>                                           |
| [<span data-ttu-id="ed26e-112">**Параметрами**</span><span class="sxs-lookup"><span data-stu-id="ed26e-112">**nCName**</span></span>](/windows/desktop/ADSchema/a-ncname)   | <span data-ttu-id="ed26e-113">Задает различающееся имя для домена, схемы или контейнера конфигурации, которые находятся в корне на сервере или в домене, указанном параметром [**днсрут**](/windows/desktop/ADSchema/a-dnsroot).</span><span class="sxs-lookup"><span data-stu-id="ed26e-113">Specifies the distinguished name for the domain, schema, or configuration container rooted at the server or domain specified by [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot).</span></span> |



 

<span data-ttu-id="ed26e-114">Например, если сервер с DNS-адресом serv1.northwest.Fabrikam.com выполняет контекст именования с корнем CN = MyContainer, OU = МИДом, O = Fabrikam, задайте для [**днсрут**](/windows/desktop/ADSchema/a-dnsroot) в качестве DNS-адреса этого сервера и [**NCName**](/windows/desktop/ADSchema/a-ncname) различающееся имя домена, схемы или контейнера конфигурации.</span><span class="sxs-lookup"><span data-stu-id="ed26e-114">For example, if the server with DNS address of serv1.northwest.Fabrikam.com serves the naming context rooted at CN=MyContainer,OU=MyDOM,O=Fabrikam, set the [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) to that server's DNS address and the [**nCName**](/windows/desktop/ADSchema/a-ncname) to the distinguished name of the domain, schema, or configuration container.</span></span>

<span data-ttu-id="ed26e-115">Дополнительные сведения и пример кода, демонстрирующий создание внешней ссылки, см. в разделе [пример кода для создания внешнего объекта crossRef](example-code-for-creating-an-external-crossref-object.md).</span><span class="sxs-lookup"><span data-stu-id="ed26e-115">For more information and a code example that shows how to create an external referral, see [Example Code for Creating an External crossRef Object](example-code-for-creating-an-external-crossref-object.md).</span></span>

 

 