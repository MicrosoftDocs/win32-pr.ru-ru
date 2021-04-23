---
title: Обнаружение режима работы домена
description: 'В Windows 2000 домен может работать в двух режимах работы: смешанный и машинный.'
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- Обнаружение режима работы домена AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890444"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a><span data-ttu-id="c0523-104">Обнаружение режима работы домена</span><span class="sxs-lookup"><span data-stu-id="c0523-104">Detecting the Operation Mode of a Domain</span></span>

<span data-ttu-id="c0523-105">В Windows 2000 домен может работать в двух режимах работы: Mixed и Native.</span><span class="sxs-lookup"><span data-stu-id="c0523-105">In Windows 2000, a domain can run in two operation modes: mixed and native.</span></span> <span data-ttu-id="c0523-106">Смешанный режим следует использовать для включения контроллеров домена под управлением Windows NT 4,0 в домене Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="c0523-106">Mixed mode should be used to include domain controllers running Windows NT 4.0 in a Windows 2000 domain.</span></span> <span data-ttu-id="c0523-107">Смешанный режим не поддерживает универсальные группы и вложенные группы.</span><span class="sxs-lookup"><span data-stu-id="c0523-107">Mixed mode does not support universal groups or nested groups.</span></span> <span data-ttu-id="c0523-108">Если все контроллеры домена в домене работают под Windows 2000, можно использовать собственный режим.</span><span class="sxs-lookup"><span data-stu-id="c0523-108">If all domain controllers in the domain are running Windows 2000, you can use native mode.</span></span>

<span data-ttu-id="c0523-109">Чтобы программно определить режим работы домена Windows 2000, прочтите свойство [**нтмикседдомаин**](/windows/desktop/ADSchema/a-ntmixeddomain) объекта [**домаинднс**](/windows/desktop/ADSchema/c-domaindns) для этого домена.</span><span class="sxs-lookup"><span data-stu-id="c0523-109">To programmatically detect the operation mode of a Windows 2000 domain, read the [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) property of the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object for that domain.</span></span> <span data-ttu-id="c0523-110">Нулевое значение (0) означает, что домен работает в собственном режиме.</span><span class="sxs-lookup"><span data-stu-id="c0523-110">A value of zero (0) means that the domain is in native mode.</span></span> <span data-ttu-id="c0523-111">Значение одного (1) указывает, что домен работает в смешанном режиме.</span><span class="sxs-lookup"><span data-stu-id="c0523-111">A value of one (1) indicates that the domain is in mixed mode.</span></span> <span data-ttu-id="c0523-112">Можно также использовать функцию [**дсролежетпримаридомаининформатион**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) для получения режима работы, а также других данных о домене и его состоянии.</span><span class="sxs-lookup"><span data-stu-id="c0523-112">You can also use the [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) function to get the operation mode as well as other data about the domain and its state.</span></span>

<span data-ttu-id="c0523-113">Чтобы выполнить привязку к объекту [**домаинднс**](/windows/desktop/ADSchema/c-domaindns) домена учетной записи пользователя, под которой выполняется приложение, используйте бессерверную привязку и RootDSE, чтобы получить различающееся имя для домена, а затем используйте это различающееся имя для привязки к объекту **домаинднс** , который представляет этот домен.</span><span class="sxs-lookup"><span data-stu-id="c0523-113">To bind to the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object of the domain of the user account under which your application is running, use serverless binding and rootDSE to get the distinguished name for the domain and then use that distinguished name to bind to the **domainDNS** object that represents that domain.</span></span> <span data-ttu-id="c0523-114">Дополнительные сведения о бессерверных привязках и rootDSE см. в статье [Привязка к серверу и RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="c0523-114">For more information about serverless binding and rootDSE, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="c0523-115">Дополнительные сведения и пример кода, в котором показано, как программным способом определить режим работы домена, см. в разделе [пример кода для определения режима работы](example-code-for-determining-the-operation-mode.md).</span><span class="sxs-lookup"><span data-stu-id="c0523-115">For more information and a code example that shows how to programmatically detect the operation mode of a domain, see [Example Code for Determining the Operation Mode](example-code-for-determining-the-operation-mode.md).</span></span>

 

 