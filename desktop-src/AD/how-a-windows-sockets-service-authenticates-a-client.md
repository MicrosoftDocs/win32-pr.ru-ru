---
title: Проверка подлинности клиента службой сокетов Windows
description: Когда клиент подключается к службе сокетов Windows, служба начинает работу над последовательностью взаимной проверки подлинности, которая показана в следующих примерах кода.
ms.assetid: 32f62fb9-41c6-4932-9b91-753174919707
ms.tgt_platform: multiple
keywords:
- Проверка подлинности клиента AD службой сокетов Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad096ddfb9569d6289c1e775465232431c20ad6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103987330"
---
# <a name="how-a-windows-sockets-service-authenticates-a-client"></a><span data-ttu-id="ca2be-104">Проверка подлинности клиента службой сокетов Windows</span><span class="sxs-lookup"><span data-stu-id="ca2be-104">How a Windows Sockets Service Authenticates a Client</span></span>

<span data-ttu-id="ca2be-105">Когда клиент подключается к службе сокетов Windows, служба начинает работу над последовательностью взаимной проверки подлинности, которая показана в следующих примерах кода.</span><span class="sxs-lookup"><span data-stu-id="ca2be-105">When a client connects to the Windows Sockets service, the service begins its operations for the mutual authentication sequence, which is shown in the following code examples.</span></span>

<span data-ttu-id="ca2be-106">Подпрограммы **доаусентикатион** используют маркер сокета для получения первого пакета проверки подлинности от клиента.</span><span class="sxs-lookup"><span data-stu-id="ca2be-106">The **DoAuthentication** routine uses the socket handle to receive the first authentication packet from the client.</span></span> <span data-ttu-id="ca2be-107">Клиентский буфер передается функции **женсерверконтекст** , которая передает буфер в пакет безопасности SSPI для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ca2be-107">The client buffer is passed to the **GenServerContext** function, which then passes the buffer to the SSPI security package for authentication.</span></span> <span data-ttu-id="ca2be-108">Затем **доаусентикатион** отправляет клиенту выходные данные пакета безопасности.</span><span class="sxs-lookup"><span data-stu-id="ca2be-108">**DoAuthentication** then sends the security package output back to the client.</span></span> <span data-ttu-id="ca2be-109">Этот цикл повторяется до тех пор, пока не будет выполнена проверка подлинности или **женсерверконтекст** не установит флаг, указывающий на успешную проверку</span><span class="sxs-lookup"><span data-stu-id="ca2be-109">This loop is repeated until the authentication fails or **GenServerContext** sets a flag indicating the authentication succeeded.</span></span>

<span data-ttu-id="ca2be-110">**Женсерверконтекст** вызывает следующие функции из пакета безопасности SSPI:</span><span class="sxs-lookup"><span data-stu-id="ca2be-110">**GenServerContext** calls the following functions from an SSPI security package:</span></span>

-   <span data-ttu-id="ca2be-111">[**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) извлекает учетные данные службы из контекста безопасности службы, который был установлен при запуске службы.</span><span class="sxs-lookup"><span data-stu-id="ca2be-111">[**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) extracts the service credentials from the service security context that was established when the service started.</span></span>
-   <span data-ttu-id="ca2be-112">[**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) пытается выполнить взаимную проверку подлинности, используя учетные данные службы и данные проверки подлинности, полученные от клиента.</span><span class="sxs-lookup"><span data-stu-id="ca2be-112">[**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) attempts to perform the mutual authentication using the service credentials and the authentication data received from the client.</span></span> <span data-ttu-id="ca2be-113">Чтобы запросить взаимную проверку подлинности, вызов **AcceptSecurityContext** должен \_ указать \_ флаг взаимной проверки \_ подлинности ASC req.</span><span class="sxs-lookup"><span data-stu-id="ca2be-113">To request mutual authentication, the **AcceptSecurityContext** call must specify the ASC\_REQ\_MUTUAL\_AUTH flag.</span></span>
-   <span data-ttu-id="ca2be-114">[**CompleteAuthToken**](/windows/desktop/api/sspi/nf-sspi-completeauthtoken) вызывается при необходимости для завершения операции проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ca2be-114">[**CompleteAuthToken**](/windows/desktop/api/sspi/nf-sspi-completeauthtoken) is called, if necessary, to complete the authentication operation.</span></span>

<span data-ttu-id="ca2be-115">В следующем примере кода используется пакет Negotiate из Secur32.dll библиотеки пакетов безопасности.</span><span class="sxs-lookup"><span data-stu-id="ca2be-115">The following code example uses the negotiate package from the Secur32.dll library of security packages.</span></span>


```C++
/***************************************************************/
//   DoAuthentication routine for the service
//
//   Manages the service authentication communication with the client 
//   using the supplied socket handle.
//
//   Returns TRUE if the mutual authentication succeeds.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
 
BOOL DoAuthentication (SOCKET s)
{
DWORD cbIn, cbOut;
BOOL done = FALSE;

if(s==INVALID_SOCKET)
{
    return(FALSE);
}
 
// Receive authentication data from the client and pass
// it to the security package. Send the package output back
// to the client. Repeat until complete.
do 
{
    if (!ReceiveMsg (s, g_pInBuf, g_cbMaxMessage, &cbIn))
        return(FALSE);
 
    cbOut = g_cbMaxMessage;
    if (!GenServerContext (s, g_pInBuf, cbIn, g_pOutBuf, 
                               &cbOut, &done))
        return(FALSE);
 
    if (!SendMsg (s, g_pOutBuf, cbOut))
        return(FALSE);
} 
while(!done);
 
return(TRUE);
}
 
/***************************************************************/
//   GenServerContext routine 
//
//   Handles the service interactions with the security package.
//   Takes an input buffer coming from the client and generates a 
//   buffer of data to send back to the client. Also returns 
//   an indication when the authentication is complete.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL GenServerContext (
            DWORD dwKey,
            BYTE *pIn,
            DWORD cbIn,
            BYTE *pOut,
            DWORD *pcbOut,
            BOOL *pfDone)
{
SECURITY_STATUS  ssStatus;
TimeStamp        Lifetime;
SecBufferDesc    OutBuffDesc;
SecBuffer        OutSecBuff;
SecBufferDesc    InBuffDesc;
SecBuffer        InSecBuff;
ULONG            ContextAttributes = 0;
PAUTH_SEQ        pAS = null;

if((pIn==NULL && cbIn>0) || (pOut==NULL) || (pcbOut==NULL) || (pfDone==NULL))
{
    return(FALSE);
}
 
// Get a structure that contains the state of the authentication sequence.
if (!GetEntry (dwKey, (PVOID*) &pAS))
    return(FALSE);
 
if (pAS->_fNewConversation)  
{
    ssStatus = g_pFuncs->AcquireCredentialsHandle (
                        NULL,    // principal
                        PACKAGE_NAME,
                        SECPKG_CRED_INBOUND,
                        NULL,    // LOGON id
                        NULL,    // authentication data
                        NULL,    // get key function
                        NULL,    // get key argument
                        &pAS->_hcred,
                        &Lifetime
                        );
    if (SEC_SUCCESS (ssStatus))
        pAS->_fHaveCredHandle = TRUE;
    else
    {
        fprintf (stderr, "AcquireCredentialsHandle failed: %u\n", 
                 ssStatus);
        return(FALSE);
    }
}
 
// Prepare the output buffer.
OutBuffDesc.ulVersion = 0;
OutBuffDesc.cBuffers  = 1;
OutBuffDesc.pBuffers  = &OutSecBuff;
 
OutSecBuff.cbBuffer   = *pcbOut;
OutSecBuff.BufferType = SECBUFFER_TOKEN;
OutSecBuff.pvBuffer   = pOut;
 
// Prepare the input buffer.
InBuffDesc.ulVersion  = 0;
InBuffDesc.cBuffers   = 1;
InBuffDesc.pBuffers   = &InSecBuff;
 
InSecBuff.cbBuffer    = cbIn;
InSecBuff.BufferType  = SECBUFFER_TOKEN;
InSecBuff.pvBuffer    = pIn;
 
ssStatus = g_pFuncs->AcceptSecurityContext (
                    &pAS->_hcred,
                    pAS->_fNewConversation ? NULL : &pAS->_hctxt,
                    &InBuffDesc,
                    ASC_REQ_MUTUAL_AUTH,  // Context requirements.
                    SECURITY_NATIVE_DREP,
                    &pAS->_hctxt,
                    &OutBuffDesc,
                    &ContextAttributes,
                    &Lifetime
                    );
if (!SEC_SUCCESS (ssStatus))  
{
    fprintf (stderr, "AcceptSecurityContext failed: %u\n", ssStatus);
    return FALSE;
}
if (!(ContextAttributes && ASC_RET_MUTUAL_AUTH)) 
    _tprintf(TEXT("Mutual Auth not set in returned context.\n"));
 
pAS->_fHaveCtxtHandle = TRUE;
 
// Complete the authentication token, if necessary.
if ((SEC_I_COMPLETE_NEEDED == ssStatus) || 
                        (SEC_I_COMPLETE_AND_CONTINUE == ssStatus)) 
{
    if (g_pFuncs->CompleteAuthToken) 
    {
        ssStatus = g_pFuncs->CompleteAuthToken (&pAS->_hctxt, 
                                                &OutBuffDesc);
        if (!SEC_SUCCESS(ssStatus)) 
        {
            fprintf (stderr, "complete failed: %u\n", ssStatus);
            return FALSE;
        }
    } else 
    {
        fprintf (stderr, "Complete not supported.\n");
        return FALSE;
    }
}
 
*pcbOut = OutSecBuff.cbBuffer;
 
if (pAS->_fNewConversation)
    pAS->_fNewConversation = FALSE;
 
*pfDone = !((SEC_I_CONTINUE_NEEDED == ssStatus) ||
                (SEC_I_COMPLETE_AND_CONTINUE == ssStatus));
 
return TRUE;
}
```



 

 