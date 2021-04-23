---
title: Составление и регистрация имен участников-служб для службы сокетов Windows на основе SCP
description: В следующем примере кода показано, как создать и зарегистрировать имена участников-служб для службы. Вызовите этот код из установщика службы после вызова CreateService и создания точки подключения службы (SCP) службы.
ms.assetid: 3957af10-974a-415f-b8fb-d9b52ac5a82d
ms.tgt_platform: multiple
keywords:
- имена субъектов-служб AD, составление и регистрация имен участников-служб для службы сокетов Windows на основе SCP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d754d51c0ad34b1623bdc84fc8178b04d33515ed
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789613"
---
# <a name="composing-and-registering-spns-for-scp-based-windows-sockets-service"></a><span data-ttu-id="fb1df-105">Составление и регистрация имен участников-служб для службы сокетов Windows на основе SCP</span><span class="sxs-lookup"><span data-stu-id="fb1df-105">Composing and registering SPNs for SCP-based Windows Sockets Service</span></span>

<span data-ttu-id="fb1df-106">В следующем примере кода показано, как создать и зарегистрировать имена участников-служб для службы.</span><span class="sxs-lookup"><span data-stu-id="fb1df-106">The following code example shows how to compose and register the SPNs for a service.</span></span> <span data-ttu-id="fb1df-107">Вызовите этот код из установщика службы после вызова [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) и создания точки подключения службы (SCP) службы.</span><span class="sxs-lookup"><span data-stu-id="fb1df-107">Call this code from your service installer after calling [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) and creating the service's service connection point (SCP).</span></span>

<span data-ttu-id="fb1df-108">В следующем примере кода вызываются примеры функций **спнкомпосе** и **спнрегистер** , которые создают и регистрируют имя участника-службы.</span><span class="sxs-lookup"><span data-stu-id="fb1df-108">The following code example calls the **SpnCompose** and **SpnRegister** example functions that compose and register the SPN.</span></span> <span data-ttu-id="fb1df-109">Дополнительные сведения и исходный код **спнкомпосе** см. в разделе [составление имен участников-служб для службы с SCP](composing-the-spns-for-a-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="fb1df-109">For more information and the **SpnCompose** source code, see [Composing the SPNs for a Service with an SCP](composing-the-spns-for-a-service-with-an-scp.md).</span></span> <span data-ttu-id="fb1df-110">Дополнительные сведения и исходный код **спнрегистер** см. в разделе [Регистрация имен участников-служб для службы](registering-the-spns-for-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="fb1df-110">For more information and the **SpnRegister** source code, see [Registering the SPNs for a Service](registering-the-spns-for-a-service.md).</span></span>

<span data-ttu-id="fb1df-111">В этом примере для создания имени субъекта-службы используется имя класса службы и различающееся имя его SCP.</span><span class="sxs-lookup"><span data-stu-id="fb1df-111">This example uses the service class name and the distinguished name of its SCP to create its service principal name.</span></span> <span data-ttu-id="fb1df-112">Дополнительные сведения и пример кода, демонстрирующий привязку клиента к SCP службы для получения этих строк имен, см. в разделе [как клиенты находят и используют точку подключения службы](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="fb1df-112">For more information and a code example that shows how the client binds to the service SCP to retrieve these name strings, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span> <span data-ttu-id="fb1df-113">Имейте в виду, что код для создания имени участника-службы зависит от типа службы и механизмов, используемых для публикации службы.</span><span class="sxs-lookup"><span data-stu-id="fb1df-113">Be aware that the code for composing an SPN varies depending on the type of service and the mechanisms used to publish the service.</span></span>

<span data-ttu-id="fb1df-114">Служба регистрирует свое имя участника-службы, сохраняя ее **в атрибуте** «перечислить» объекта учетной записи службы в каталоге.</span><span class="sxs-lookup"><span data-stu-id="fb1df-114">The service registers its SPN by storing it in the **servicePrincipalName** attribute of the service's account object in the directory.</span></span> <span data-ttu-id="fb1df-115">Если служба выполняется под учетной записью LocalSystem, а не под учетной записью службы, она регистрирует свое имя участника-службы в объекте учетной записи локального компьютера в каталоге.</span><span class="sxs-lookup"><span data-stu-id="fb1df-115">If the service runs under the LocalSystem account instead of under a service account, it registers its SPN under the local computer account's object in the directory.</span></span>


```C++
TCHAR szDNofSCP[MAX_PATH]; // DN of SCP. Initialize by querying SCP.
TCHAR szServiceClass[]=TEXT("ADSockAuth");
LPCTSTR szServiceAccountDN;   // DN of a service logon account. 
 
DWORD dwStatus;
TCHAR **pspn = NULL;
ULONG ulSpn = 1;
 
// Compose the SPNs.
dwStatus = SpnCompose(
        &pspn,              // Receives pointer to the SPN array.
        &ulSpn,             // Receives number of SPNs returned.
        szDNofSCP,          // Input: DN of the SCP.
        szServiceClass);    // Input: the service class string.
 
// Register the SPNs
if (dwStatus == NO_ERROR) 
    dwStatus = SpnRegister(
       szServiceAccountDN,  // Logon account to register SPNs on
       pspn,                // Array of SPNs
       ulSpn,               // Number of SPNs in array
       DS_SPN_ADD_SPN_OP);  // Add SPNs to the account
 
// Free the array of SPNs returned by SpnCompose.
DsFreeSpnArray(ulSpn, pspn); 
```



<span data-ttu-id="fb1df-116">Аналогичный код можно использовать для отмены регистрации имен участников-служб при удалении службы.</span><span class="sxs-lookup"><span data-stu-id="fb1df-116">You can use similar code to unregister your SPNs when your service is uninstalled.</span></span> <span data-ttu-id="fb1df-117">Укажите имя **субъекта-службы DS \_ \_ DELETE \_ SPN \_** вместо имени субъекта-службы **DS \_ \_ Add \_ SPN \_**.</span><span class="sxs-lookup"><span data-stu-id="fb1df-117">Specify the **DS\_SPN\_DELETE\_SPN\_OP** operation instead of **DS\_SPN\_ADD\_SPN\_OP**.</span></span>

 

 