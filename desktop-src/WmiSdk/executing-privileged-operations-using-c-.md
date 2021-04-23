---
description: Специальные клиентские приложения могут вызывать привилегированные операции.
ms.assetid: e09fcadc-282f-4f07-b69c-b15bfdb07a7d
ms.tgt_platform: multiple
title: Выполнение привилегированных операций с помощью C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fbc0468fef7531586020f55032bff94c977c4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344915"
---
# <a name="executing-privileged-operations-using-c"></a><span data-ttu-id="4e781-103">Выполнение привилегированных операций с помощью C++</span><span class="sxs-lookup"><span data-stu-id="4e781-103">Executing Privileged Operations Using C++</span></span>

<span data-ttu-id="4e781-104">Специальные клиентские приложения могут вызывать привилегированные операции.</span><span class="sxs-lookup"><span data-stu-id="4e781-104">Special client applications might invoke privileged operations.</span></span> <span data-ttu-id="4e781-105">Например, приложение может позволить диспетчеру перезагружать Неотвечающий компьютер с Office.</span><span class="sxs-lookup"><span data-stu-id="4e781-105">For example, an application could allow a manager to reboot an unresponsive office computer.</span></span> <span data-ttu-id="4e781-106">С помощью инструментарий управления Windows (WMI) (WMI) можно выполнить привилегированную операцию, вызвав поставщик WMI для привилегированной операции.</span><span class="sxs-lookup"><span data-stu-id="4e781-106">By using Windows Management Instrumentation (WMI), you can execute a privileged operation by calling the WMI provider for the privileged operation.</span></span>

<span data-ttu-id="4e781-107">Следующая процедура описывает, как вызвать поставщик для привилегированной операции.</span><span class="sxs-lookup"><span data-stu-id="4e781-107">The following procedure describes how to call a provider for a privileged operation.</span></span>

<span data-ttu-id="4e781-108">**Вызов поставщика для привилегированной операции**</span><span class="sxs-lookup"><span data-stu-id="4e781-108">**To call a provider for a privileged operation**</span></span>

1.  <span data-ttu-id="4e781-109">Получите разрешения на выполнение привилегированной операции для клиентского процесса.</span><span class="sxs-lookup"><span data-stu-id="4e781-109">Obtain permissions for the client process to execute the privileged operation.</span></span>

    <span data-ttu-id="4e781-110">Как правило, администратор устанавливает разрешения с помощью средств администрирования системы, прежде чем выполнять процесс.</span><span class="sxs-lookup"><span data-stu-id="4e781-110">Typically, an administrator sets the permissions using system administrative tools—prior to running the process.</span></span>

2.  <span data-ttu-id="4e781-111">Получите разрешение для процесса поставщика, чтобы включить привилегированную операцию.</span><span class="sxs-lookup"><span data-stu-id="4e781-111">Obtain permission for the provider process to enable the privileged operation.</span></span>

    <span data-ttu-id="4e781-112">Как правило, разрешения поставщика можно задать с помощью вызова функции [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) .</span><span class="sxs-lookup"><span data-stu-id="4e781-112">Typically, you can set provider permissions with a call to the [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function.</span></span>

3.  <span data-ttu-id="4e781-113">Получите разрешение для клиентского процесса, чтобы включить привилегированную операцию.</span><span class="sxs-lookup"><span data-stu-id="4e781-113">Obtain permission for the client process to enable the privileged operation.</span></span>

    <span data-ttu-id="4e781-114">Этот шаг необходим только в том случае, если поставщик является локальным для клиента.</span><span class="sxs-lookup"><span data-stu-id="4e781-114">This step is necessary only if the provider is local to the client.</span></span> <span data-ttu-id="4e781-115">Если клиент и поставщик существуют на одном компьютере, клиент должен специально включить привилегированную операцию с помощью одного из следующих методов:</span><span class="sxs-lookup"><span data-stu-id="4e781-115">If the client and provider exist on the same computer, the client must specifically enable the privileged operation by using one of the following techniques:</span></span>

    -   <span data-ttu-id="4e781-116">Если этот процесс принадлежит клиенту, клиент может использовать [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) для настройки маркера процесса перед ВЫЗОВом инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="4e781-116">If the client owns the process, the client can use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to adjust the process token before calling WMI.</span></span> <span data-ttu-id="4e781-117">В этом случае вам больше не нужно выполнять код.</span><span class="sxs-lookup"><span data-stu-id="4e781-117">In this case, you do not need to code any further.</span></span>
    -   <span data-ttu-id="4e781-118">Если клиенту не удается получить доступ к маркеру клиента, клиент может использовать следующую процедуру, чтобы создать токен потока и использовать [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) для этого маркера.</span><span class="sxs-lookup"><span data-stu-id="4e781-118">If the client cannot access the client token, the client can use the following procedure to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="4e781-119">В следующей процедуре описывается создание токена потока и использование [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) для этого маркера.</span><span class="sxs-lookup"><span data-stu-id="4e781-119">The following procedure describes how to create a thread token and use [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on that token.</span></span>

<span data-ttu-id="4e781-120">**Создание токена потока и использование AdjustTokenPrivileges для этого токена**</span><span class="sxs-lookup"><span data-stu-id="4e781-120">**To create a thread token and use AdjustTokenPrivileges on that token**</span></span>

1.  <span data-ttu-id="4e781-121">Создайте копию токена процесса, вызвав [**имперсонатеселф**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span><span class="sxs-lookup"><span data-stu-id="4e781-121">Create a copy of the process token by calling [**ImpersonateSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateself).</span></span>
2.  <span data-ttu-id="4e781-122">Получите только что созданный токен потока путем вызова [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span><span class="sxs-lookup"><span data-stu-id="4e781-122">Retrieve the newly created thread token by calling [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation).</span></span>
3.  <span data-ttu-id="4e781-123">Включите привилегированную операцию с помощью вызова [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) для нового маркера.</span><span class="sxs-lookup"><span data-stu-id="4e781-123">Enable the privileged operation with a call to [**AdjustTokenPrivileges**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) on the new token.</span></span>
4.  <span data-ttu-id="4e781-124">Получите указатель на [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span><span class="sxs-lookup"><span data-stu-id="4e781-124">Obtain a pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices).</span></span>
5.  <span data-ttu-id="4e781-125">Маскировка указателя на [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) с помощью вызова [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="4e781-125">Cloak the pointer to [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) with a call to [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>
6.  <span data-ttu-id="4e781-126">Повторите шаги с 1 по 5 при каждом вызове инструментария WMI.</span><span class="sxs-lookup"><span data-stu-id="4e781-126">Repeat steps 1 through 5 on each call to WMI.</span></span>

    > [!Note]  
    > <span data-ttu-id="4e781-127">Необходимо повторить шаги, так как COM кэширует маркеры неправильно.</span><span class="sxs-lookup"><span data-stu-id="4e781-127">You must repeat the steps because COM caches tokens incorrectly.</span></span>

     

<span data-ttu-id="4e781-128">В примере кода в этом разделе \# для правильной компиляции требуется следующая инструкция include.</span><span class="sxs-lookup"><span data-stu-id="4e781-128">The code example in this topic requires the following \#include statement to correctly compile.</span></span>


```C++
#include <wbemidl.h>
```



<span data-ttu-id="4e781-129">В следующем примере кода показано, как включить привилегии на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="4e781-129">The following code example shows how to enable privileges on a local machine.</span></span>


```C++
// Get the privileges 
// The token has been obtained outside the scope of this code sample
// ================== 
DWORD dwLen;
bool bRes;
HANDLE hToken;

// obtain dwLen
bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  NULL, 
  0,
  &dwLen
); 

BYTE* pBuffer = new BYTE[dwLen];
if(pBuffer == NULL)
{
  CloseHandle(hToken);
  return WBEM_E_OUT_OF_MEMORY;
} 

bRes = GetTokenInformation(
  hToken, 
  TokenPrivileges, 
  pBuffer,     
  dwLen,        
  &dwLen
);

if (!bRes)
{
  CloseHandle(hToken);
  delete [] pBuffer;
  return WBEM_E_ACCESS_DENIED;
} 

// Iterate through all the privileges and enable them all
// ====================================================== 
TOKEN_PRIVILEGES* pPrivs = (TOKEN_PRIVILEGES*)pBuffer;
for (DWORD i = 0; i < pPrivs->PrivilegeCount; i++)
{
  pPrivs->Privileges[i].Attributes |= SE_PRIVILEGE_ENABLED;
} 
// Store the information back in the token
// ========================================= 
bRes = AdjustTokenPrivileges(
  hToken, 
  FALSE, 
  pPrivs, 
  0, NULL, NULL
);

delete [] pBuffer;
CloseHandle(hToken); 

if (!bRes)
  return WBEM_E_ACCESS_DENIED;
else
  return WBEM_S_NO_ERROR;
```



 

 
