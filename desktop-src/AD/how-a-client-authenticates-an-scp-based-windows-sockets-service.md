---
title: проверка подлинности клиента службы сокетов Windows на основе SCP
description: В этом разделе показан код, используемый клиентским приложением для создания имени субъекта-службы.
ms.assetid: b5ef79c6-e321-435c-b3de-817fdea8836a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40d35ad62e05ab925d2dedc10506ddb339c2aafd188487f2e1591713189f451a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188668"
---
# <a name="how-a-client-authenticates-an-scp-based-windows-sockets-service"></a>проверка подлинности клиента службы сокетов Windows на основе SCP

В этом разделе показан код, используемый клиентским приложением для создания имени субъекта-службы. Клиент привязывается к точке подключения службы (SCP) службы для получения данных, необходимых для подключения к службе. Точка подключения службы также содержит данные, которые клиент может использовать для составления имени участника-службы. Дополнительные сведения и пример кода, который выполняет привязку к точке подключения службы и извлекает необходимые свойства, см. в разделе [как клиенты находят и используют точку подключения службы](how-clients-find-and-use-a-service-connection-point.md).

в этом разделе также показано, как клиент использует пакет безопасности SSPI и SPN службы для установления взаимной проверки подлинности подключения к службе сокетов Windows. имейте в виду, что этот код практически идентичен коду, который необходим в Microsoft Windows NT 4,0 и более ранних версиях только для проверки подлинности клиента на сервере. Единственное отличие заключается в том, что клиент должен предоставить имя субъекта-службы и указать \_ \_ флаг взаимной \_ проверки подлинности ISC.

## <a name="client-code-to-make-an-spn-for-a-service"></a>Клиентский код для создания SPN для службы


```C++
// Initialize these strings by querying the service's SCP.
TCHAR szDn[MAX_PATH],     // DN of the service's SCP.
      szServer[MAX_PATH], // DNS name of the service's server.
      szClass[MAX_PATH];  // Service class.
 
TCHAR szSpn[MAX_PATH];    // Buffer for SPN.
SOCKET sockServer;        // Socket connected to service.
DWORD dwRes, dwLen;
.
.
.
// Compose the SPN for the service using the DN, Class, and Server
// returned by ScpLocate.
dwLen = sizeof(szSpn);
dwRes = DsMakeSpn(
     szClass,    // Service class.
     szDn,       // DN of the service's SCP.
     szServer,   // DNS name of the server on which service is running.
     0,          // No port component in SPN.
     NULL,       // No referrer.
     &dwLen,     // Size of szSpn buffer.
     szSpn);     // Buffer to receive the SPN.

if (!DoAuthentication (sockServer, szSpn)) {
    closesocket (sockServer);
    return(FALSE);
}
.
.
.
```



## <a name="client-code-to-authenticate-the-service"></a>Клиентский код для проверки подлинности службы

Этот пример кода состоит из двух подпрограмм: **доаусентикатион** и **женклиентконтекст**. После вызова [**дсмакеспн**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna) для создания имени субъекта-службы, клиент передает имя участника-службы в подпрограммы **доаусентикатион** , которая вызывает **женклиентконтекст** для создания исходного буфера для отправки в службу. **Доаусентикатион** использует маркер сокета для отправки буфера и получения ответа службы, переданного в пакет SSPI, с помощью другого вызова **женклиентконтекст**. Этот цикл повторяется до тех пор, пока не будет выполнена проверка подлинности или **женклиентконтекст** устанавливает флаг, указывающий на успешную проверку подлинности

Процедура **женклиентконтекст** взаимодействует с пакетом SSPI для создания данных проверки подлинности для отправки в службу и обработки данных, полученных от службы. Ключевые компоненты данных проверки подлинности, предоставляемые клиентом, включают:

-   Имя субъекта-службы, которое определяет учетные данные, которые служба должна проверять подлинность.
-   Учетные данные клиента. Функция [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) пакета безопасности извлекает эти учетные данные из контекста безопасности клиента, установленного при входе в систему.
-   Чтобы запросить взаимную проверку подлинности, клиент должен \_ указать \_ флаг взаимной проверки \_ подлинности ISC, если он вызывает функцию [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) во время выполнения процедуры **женклиентконтекст** .


```C++
// Structure for storing the state of the authentication sequence.
typedef struct _AUTH_SEQ 
{
    BOOL _fNewConversation;
    CredHandle _hcred;
    BOOL _fHaveCredHandle;
    BOOL _fHaveCtxtHandle;
    struct _SecHandle  _hctxt;
} AUTH_SEQ, *PAUTH_SEQ;
 
/***************************************************************/
//   DoAuthentication routine for the client.
//
//   Manages the client's authentication conversation with the service 
//   using the supplied socket handle.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL DoAuthentication (
        SOCKET s, 
        LPTSTR szSpn)
{
BOOL done = FALSE;
DWORD cbOut, cbIn;
 
// Call the security package to generate the initial buffer of 
// authentication data to send to the service.
cbOut = g_cbMaxMessage;
if (!GenClientContext (s, NULL, 0, g_pOutBuf, 
                       &cbOut, &done, szSpn))
    return(FALSE);
    
if (!SendMsg (s, g_pOutBuf, cbOut))
    return(FALSE);
 
// Pass the service's response back to the security package, and send 
// the package's output back to the service. Repeat until complete.
while (!done) 
{
    if (!ReceiveMsg (s, g_pInBuf, g_cbMaxMessage, &cbIn))
        return(FALSE);
 
    cbOut = g_cbMaxMessage;
    if (!GenClientContext (s, g_pInBuf, cbIn, g_pOutBuf, 
                           &cbOut, &done, szSpn))
        return(FALSE);
 
    if (!SendMsg (s, g_pOutBuf, cbOut))
        return(FALSE);
}
 
return(TRUE);
}
 
/***************************************************************/
//   GenClientContext routine
//
//   Handles the client's interactions with the security package.
//   Optionally takes an input buffer coming from the service 
//   and generates a buffer of data to send back to the 
//   service. Also returns an indication when the authentication
//   is complete.
//
//   Returns TRUE if the mutual authentication is successful.
//   Otherwise, it returns FALSE.
//
/***************************************************************/
BOOL GenClientContext (
            DWORD dwKey,     // Socket handle used as key.
            BYTE *pIn,
            DWORD cbIn,
            BYTE *pOut,
            DWORD *pcbOut,
            BOOL *pfDone,
            LPTSTR szSpn)
{
SECURITY_STATUS  ssStatus;
TimeStamp        Lifetime;
SecBufferDesc    OutBuffDesc;
SecBuffer        OutSecBuff;
SecBufferDesc    InBuffDesc;
SecBuffer        InSecBuff;
ULONG            ContextAttributes;
PAUTH_SEQ        pAS; // Structure to store state of authentication.
 
// Get structure that contains the state of the authentication sequence.
if (!GetEntry (dwKey, (PVOID*) &pAS))
    return(FALSE);
 
if (pAS->_fNewConversation)
{
    ssStatus = g_pFuncs->AcquireCredentialsHandle (
            NULL,    // Principal
            PACKAGE_NAME,
            SECPKG_CRED_OUTBOUND,
            NULL,    // LOGON id
            NULL,    // Authentication data
            NULL,    // Get key function.
            NULL,    // Get key argument.
            &pAS->_hcred,
            &Lifetime
            );
    if (SEC_SUCCESS (ssStatus))
        pAS->_fHaveCredHandle = TRUE;
    else 
    {
        fprintf (stderr, 
                 "AcquireCredentialsHandle failed: %u\n", ssStatus);
        return(FALSE);
    }
}
 
// Prepare output buffer.
OutBuffDesc.ulVersion = 0;
OutBuffDesc.cBuffers = 1;
OutBuffDesc.pBuffers = &OutSecBuff;
 
OutSecBuff.cbBuffer = *pcbOut;
OutSecBuff.BufferType = SECBUFFER_TOKEN;
OutSecBuff.pvBuffer = pOut;
 
// Prepare input buffer.
if (!pAS->_fNewConversation) 
{
    InBuffDesc.ulVersion = 0;
    InBuffDesc.cBuffers = 1;
    InBuffDesc.pBuffers = &InSecBuff;
 
    InSecBuff.cbBuffer = cbIn;
    InSecBuff.BufferType = SECBUFFER_TOKEN;
    InSecBuff.pvBuffer = pIn;
}
 
_tprintf(TEXT("InitializeSecurityContext: pszTarget=%s\n"),szSpn);
 
ssStatus = g_pFuncs->InitializeSecurityContext (
                     &pAS->_hcred,
                     pAS->_fNewConversation ? NULL : &pAS->_hctxt,
                     szSpn,
                     ISC_REQ_MUTUAL_AUTH,      // Context requirements
                     0,                        // Reserved1
                     SECURITY_NATIVE_DREP,
                     pAS->_fNewConversation ? NULL : &InBuffDesc,
                     0,                        // Reserved2
                     &pAS->_hctxt,
                     &OutBuffDesc,
                     &ContextAttributes,
                     &Lifetime
                     );
if (!SEC_SUCCESS (ssStatus)) 
{
    fprintf (stderr, "init context failed: %X\n", ssStatus);
    return FALSE;
}
 
pAS->_fHaveCtxtHandle = TRUE;
 
// Complete token if applicable.
if ( (SEC_I_COMPLETE_NEEDED == ssStatus) || 
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
 
// Check the ISC_RET_MUTUAL_AUTH flag to verify that 
// mutual authentication was performed.
if (*pfDone && !(ContextAttributes && ISC_RET_MUTUAL_AUTH) )
    _tprintf(TEXT("Mutual Auth not set in returned context.\n"));
 
return TRUE;
}
```



 

 




