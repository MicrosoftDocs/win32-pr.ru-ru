---
title: проверка подлинности клиента службой сокетов Windows
description: когда клиент подключается к службе сокетов Windows, служба начинает работу над последовательностью взаимной проверки подлинности, которая показана в следующих примерах кода.
ms.assetid: 32f62fb9-41c6-4932-9b91-753174919707
ms.tgt_platform: multiple
keywords:
- как служба сокетов Windows проверяет подлинность клиента AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2975d356de011818514d6999f03d1998e066a4b8bdadd6eaba8835541e4b8e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188526"
---
# <a name="how-a-windows-sockets-service-authenticates-a-client"></a>проверка подлинности клиента службой сокетов Windows

когда клиент подключается к службе сокетов Windows, служба начинает работу над последовательностью взаимной проверки подлинности, которая показана в следующих примерах кода.

Подпрограммы **доаусентикатион** используют маркер сокета для получения первого пакета проверки подлинности от клиента. Клиентский буфер передается функции **женсерверконтекст** , которая передает буфер в пакет безопасности SSPI для проверки подлинности. Затем **доаусентикатион** отправляет клиенту выходные данные пакета безопасности. Этот цикл повторяется до тех пор, пока не будет выполнена проверка подлинности или **женсерверконтекст** не установит флаг, указывающий на успешную проверку

**Женсерверконтекст** вызывает следующие функции из пакета безопасности SSPI:

-   [**AcquireCredentialsHandle**](../SecAuthN/acquirecredentialshandle--general.md) извлекает учетные данные службы из контекста безопасности службы, который был установлен при запуске службы.
-   [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) пытается выполнить взаимную проверку подлинности, используя учетные данные службы и данные проверки подлинности, полученные от клиента. Чтобы запросить взаимную проверку подлинности, вызов **AcceptSecurityContext** должен \_ указать \_ флаг взаимной проверки \_ подлинности ASC req.
-   [**CompleteAuthToken**](/windows/desktop/api/sspi/nf-sspi-completeauthtoken) вызывается при необходимости для завершения операции проверки подлинности.

В следующем примере кода используется пакет Negotiate из Secur32.dll библиотеки пакетов безопасности.


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



 

 