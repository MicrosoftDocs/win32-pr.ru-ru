---
description: В следующем примере реализуется процедура, описанная в разделе процедура подписывания данных.
ms.assetid: beaf3d67-de2b-4b30-812f-1659386a1bfc
title: 'Пример программы на языке C: подписывание сообщения и проверка подписи сообщения'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9022b165f586fb293b4de12ec7a8e9f00680b691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265389"
---
# <a name="example-c-program-signing-a-message-and-verifying-a-message-signature"></a><span data-ttu-id="6f409-103">Пример программы на языке C: подписывание сообщения и проверка подписи сообщения</span><span class="sxs-lookup"><span data-stu-id="6f409-103">Example C Program: Signing a Message and Verifying a Message Signature</span></span>

<span data-ttu-id="6f409-104">В следующем примере реализуется процедура, описанная в [разделе процедура подписывания данных](procedure-for-signing-data.md).</span><span class="sxs-lookup"><span data-stu-id="6f409-104">The following example implements the procedure described in [Procedure for Signing Data](procedure-for-signing-data.md).</span></span> <span data-ttu-id="6f409-105">Общие сведения см. в разделе [упрощенные сообщения](simplified-messages.md).</span><span class="sxs-lookup"><span data-stu-id="6f409-105">For general information, see [Simplified Messages](simplified-messages.md).</span></span> <span data-ttu-id="6f409-106">Подробные сведения о функциях и структурах можно найти в [статье основные функции шифрования](cryptography-functions.md), [упрощенные функции сообщений](cryptography-functions.md)и [структуры CryptoAPI](cryptography-structures.md).</span><span class="sxs-lookup"><span data-stu-id="6f409-106">Details about the functions and structures can be found in [Base Cryptography Functions](cryptography-functions.md), [Simplified Message Functions](cryptography-functions.md), and [CryptoAPI Structures](cryptography-structures.md).</span></span>

<span data-ttu-id="6f409-107">Этот пример также включает код для проверки созданной подписи сообщения.</span><span class="sxs-lookup"><span data-stu-id="6f409-107">This example also includes code to verify the message signature created.</span></span> <span data-ttu-id="6f409-108">Этот код обычно находится в отдельной программе, но включается здесь для полноты и ясности.</span><span class="sxs-lookup"><span data-stu-id="6f409-108">This code would usually be in a separate program but is included here for completeness and clarity.</span></span>

<span data-ttu-id="6f409-109">В этом примере показаны следующие функции CryptoAPI:</span><span class="sxs-lookup"><span data-stu-id="6f409-109">This example illustrates the following CryptoAPI functions:</span></span>

-   [<span data-ttu-id="6f409-110">**цертопенсторе**</span><span class="sxs-lookup"><span data-stu-id="6f409-110">**CertOpenStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)
-   [<span data-ttu-id="6f409-111">**криптсигнмессаже**</span><span class="sxs-lookup"><span data-stu-id="6f409-111">**CryptSignMessage**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)
-   [<span data-ttu-id="6f409-112">**криптверифимессажесигнатуре**</span><span class="sxs-lookup"><span data-stu-id="6f409-112">**CryptVerifyMessageSignature**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)
-   [<span data-ttu-id="6f409-113">**цертфрицертификатеконтекст**</span><span class="sxs-lookup"><span data-stu-id="6f409-113">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)
-   [<span data-ttu-id="6f409-114">**цертклосесторе**</span><span class="sxs-lookup"><span data-stu-id="6f409-114">**CertCloseStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)

<span data-ttu-id="6f409-115">Подпись сообщения может быть выполнена только с доступом к сертификату с доступным [*закрытым ключом*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="6f409-115">Signing the message can only be done with access to a certificate that has an available [*private key*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="6f409-116">Проверка сообщения может быть выполнена только с доступом к открытому ключу, связанному с закрытым ключом, используемым для подписания сертификата.</span><span class="sxs-lookup"><span data-stu-id="6f409-116">Verification of the message can only be done with access to the public key related to the private key used to sign the certificate.</span></span> <span data-ttu-id="6f409-117">Пользователь может изменить инструкцию **\# define** на имя субъекта из одного из персональных сертификатов пользователя.</span><span class="sxs-lookup"><span data-stu-id="6f409-117">The user can change the **\#define** statement to the subject name from one of the user's personal certificates.</span></span>

<span data-ttu-id="6f409-118">В этом примере также демонстрируется инициализация сообщения со знаком шифрования « \_ \_ \_ абзац» и «шифрования», \_ \_ \_ необходимых для вызовов [**криптсигнмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) и [**криптверифимессажесигнатуре**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature).</span><span class="sxs-lookup"><span data-stu-id="6f409-118">This example also demonstrates the initialization of the CRYPT\_SIGN\_MESSAGE\_PARA and CRYPT\_VERIFY\_MESSAGE\_PARA structures needed for calls to [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage) and [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature).</span></span>

<span data-ttu-id="6f409-119">В этом примере также используется функция [**михандлиррор**](myhandleerror.md).</span><span class="sxs-lookup"><span data-stu-id="6f409-119">This example also uses the function [**MyHandleError**](myhandleerror.md).</span></span> <span data-ttu-id="6f409-120">Код для этой функции включен в пример программы, и его также можно увидеть в [общего назначения функциях](general-purpose-functions.md).</span><span class="sxs-lookup"><span data-stu-id="6f409-120">Code for this function is included with the example program and also can be seen in [General Purpose Functions](general-purpose-functions.md).</span></span>


```C++
//-------------------------------------------------------------------
//   Copyright (C) Microsoft.  All rights reserved.

#include <stdio.h>
#include <conio.h>
#include <tchar.h>
#include <windows.h>
#include <wincrypt.h>

// Link with the Crypt32.lib file.
#pragma comment (lib, "Crypt32")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

//-------------------------------------------------------------------
//   Define the name of a certificate subject.
//   To use this program, the definition of SIGNER_NAME
//   must be changed to the name of the subject of
//   a certificate that has access to a private key. That certificate
//   must have either the CERT_KEY_PROV_INFO_PROP_ID or 
//   CERT_KEY_CONTEXT_PROP_ID property set for the context to 
//   provide access to the private signature key.

//-------------------------------------------------------------------
//    You can use a command similar to the following to create a 
//    certificate that can be used with this example:
//
//    makecert -n "cn=Test" -sk Test -ss my

//#define SIGNER_NAME L"test"
#define SIGNER_NAME L"Insert_signer_name_here"

//-------------------------------------------------------------------
//    Define the name of the store where the needed certificate
//    can be found. 

#define CERT_STORE_NAME  L"MY"

//-------------------------------------------------------------------
//   Local function prototypes.
void MyHandleError(LPTSTR psz);
bool SignMessage(CRYPT_DATA_BLOB *pSignedMessageBlob);
bool VerifySignedMessage(
    CRYPT_DATA_BLOB *pSignedMessageBlob, 
    CRYPT_DATA_BLOB *pDecodedMessageBlob);

int _tmain(int argc, _TCHAR* argv[])
{
    UNREFERENCED_PARAMETER(argc);
    UNREFERENCED_PARAMETER(argv);
    
    CRYPT_DATA_BLOB SignedMessage;

    if(SignMessage(&SignedMessage))
    {
        CRYPT_DATA_BLOB DecodedMessage;

        if(VerifySignedMessage(&SignedMessage, &DecodedMessage))
        {
            free(DecodedMessage.pbData);
        }

        free(SignedMessage.pbData);
    }

    _tprintf(TEXT("Press any key to exit."));
    _getch();
}

//-------------------------------------------------------------------
//    MyHandleError
void MyHandleError(LPTSTR psz)
{
    _ftprintf(stderr, TEXT("An error occurred in the program. \n"));
    _ftprintf(stderr, TEXT("%s\n"), psz);
    _ftprintf(stderr, TEXT("Error number %x.\n"), GetLastError());
    _ftprintf(stderr, TEXT("Program terminating. \n"));
} // End of MyHandleError

//-------------------------------------------------------------------
//    SignMessage
bool SignMessage(CRYPT_DATA_BLOB *pSignedMessageBlob)
{
    bool fReturn = false;
    BYTE* pbMessage;
    DWORD cbMessage;
    HCERTSTORE hCertStore = NULL;   
    PCCERT_CONTEXT pSignerCert; 
    CRYPT_SIGN_MESSAGE_PARA  SigParams;
    DWORD cbSignedMessageBlob;
    BYTE  *pbSignedMessageBlob = NULL;

    // Initialize the output pointer.
    pSignedMessageBlob->cbData = 0;
    pSignedMessageBlob->pbData = NULL;

    // The message to be signed.
    // Usually, the message exists somewhere and a pointer is
    // passed to the application.
    pbMessage = 
        (BYTE*)TEXT("CryptoAPI is a good way to handle security");

    // Calculate the size of message. To include the 
    // terminating null character, the length is one more byte 
    // than the length returned by the strlen function.
    cbMessage = (lstrlen((TCHAR*) pbMessage) + 1) * sizeof(TCHAR);

    // Create the MessageArray and the MessageSizeArray.
    const BYTE* MessageArray[] = {pbMessage};
    DWORD_PTR MessageSizeArray[1];
    MessageSizeArray[0] = cbMessage;

    //  Begin processing. 
    _tprintf(TEXT("The message to be signed is \"%s\".\n"),
        pbMessage);

    // Open the certificate store.
    if ( !( hCertStore = CertOpenStore(
       CERT_STORE_PROV_SYSTEM,
       0,
       NULL,
       CERT_SYSTEM_STORE_CURRENT_USER,
       CERT_STORE_NAME)))
    {
         MyHandleError(TEXT("The MY store could not be opened."));
         goto exit_SignMessage;
    }

    // Get a pointer to the signer's certificate.
    // This certificate must have access to the signer's private key.
    if(pSignerCert = CertFindCertificateInStore(
       hCertStore,
       MY_ENCODING_TYPE,
       0,
       CERT_FIND_SUBJECT_STR,
       SIGNER_NAME,
       NULL))
    {
       _tprintf(TEXT("The signer's certificate was found.\n"));
    }
    else
    {
        MyHandleError( TEXT("Signer certificate not found."));
        goto exit_SignMessage;
    }

    // Initialize the signature structure.
    SigParams.cbSize = sizeof(CRYPT_SIGN_MESSAGE_PARA);
    SigParams.dwMsgEncodingType = MY_ENCODING_TYPE;
    SigParams.pSigningCert = pSignerCert;
    SigParams.HashAlgorithm.pszObjId = szOID_RSA_SHA1RSA;
    SigParams.HashAlgorithm.Parameters.cbData = NULL;
    SigParams.cMsgCert = 1;
    SigParams.rgpMsgCert = &pSignerCert;
    SigParams.cAuthAttr = 0;
    SigParams.dwInnerContentType = 0;
    SigParams.cMsgCrl = 0;
    SigParams.cUnauthAttr = 0;
    SigParams.dwFlags = 0;
    SigParams.pvHashAuxInfo = NULL;
    SigParams.rgAuthAttr = NULL;

    // First, get the size of the signed BLOB.
    if(CryptSignMessage(
        &SigParams,
        FALSE,
        1,
        MessageArray,
        MessageSizeArray,
        NULL,
        &cbSignedMessageBlob))
    {
        _tprintf(TEXT("%d bytes needed for the encoded BLOB.\n"),
            cbSignedMessageBlob);
    }
    else
    {
        MyHandleError(TEXT("Getting signed BLOB size failed"));
        goto exit_SignMessage;
    }

    // Allocate memory for the signed BLOB.
    if(!(pbSignedMessageBlob = 
       (BYTE*)malloc(cbSignedMessageBlob)))
    {
        MyHandleError(
            TEXT("Memory allocation error while signing."));
        goto exit_SignMessage;
    }

    // Get the signed message BLOB.
    if(CryptSignMessage(
          &SigParams,
          FALSE,
          1,
          MessageArray,
          MessageSizeArray,
          pbSignedMessageBlob,
          &cbSignedMessageBlob))
    {
        _tprintf(TEXT("The message was signed successfully. \n"));

        // pbSignedMessageBlob now contains the signed BLOB.
        fReturn = true;
    }
    else
    {
        MyHandleError(TEXT("Error getting signed BLOB"));
        goto exit_SignMessage;
    }

exit_SignMessage:

    // Clean up and free memory as needed.
    if(pSignerCert)
    {
        CertFreeCertificateContext(pSignerCert);
    }
    
    if(hCertStore)
    {
        CertCloseStore(hCertStore, CERT_CLOSE_STORE_CHECK_FLAG);
        hCertStore = NULL;
    }

    // Only free the signed message if a failure occurred.
    if(!fReturn)
    {
        if(pbSignedMessageBlob)
        {
            free(pbSignedMessageBlob);
            pbSignedMessageBlob = NULL;
        }
    }

    if(pbSignedMessageBlob)
    {
        pSignedMessageBlob->cbData = cbSignedMessageBlob;
        pSignedMessageBlob->pbData = pbSignedMessageBlob;
    }
    
    return fReturn;
}

//-------------------------------------------------------------------
//    VerifySignedMessage
//
//    Verify the message signature. Usually, this would be done in 
//    a separate program. 
bool VerifySignedMessage(
    CRYPT_DATA_BLOB *pSignedMessageBlob, 
    CRYPT_DATA_BLOB *pDecodedMessageBlob)
{
    bool fReturn = false;
    DWORD cbDecodedMessageBlob;
    BYTE *pbDecodedMessageBlob = NULL;
    CRYPT_VERIFY_MESSAGE_PARA VerifyParams;

    // Initialize the output.
    pDecodedMessageBlob->cbData = 0;
    pDecodedMessageBlob->pbData = NULL;

    // Initialize the VerifyParams data structure.
    VerifyParams.cbSize = sizeof(CRYPT_VERIFY_MESSAGE_PARA);
    VerifyParams.dwMsgAndCertEncodingType = MY_ENCODING_TYPE;
    VerifyParams.hCryptProv = 0;
    VerifyParams.pfnGetSignerCertificate = NULL;
    VerifyParams.pvGetArg = NULL;

    // First, call CryptVerifyMessageSignature to get the length 
    // of the buffer needed to hold the decoded message.
    if(CryptVerifyMessageSignature(
        &VerifyParams,
        0,
        pSignedMessageBlob->pbData,
        pSignedMessageBlob->cbData,
        NULL,
        &cbDecodedMessageBlob,
        NULL))
    {
        _tprintf(TEXT("%d bytes needed for the decoded message.\n"),
            cbDecodedMessageBlob);

    }
    else
    {
        _tprintf(TEXT("Verification message failed. \n"));
        goto exit_VerifySignedMessage;
    }

    //---------------------------------------------------------------
    //   Allocate memory for the decoded message.
    if(!(pbDecodedMessageBlob = 
       (BYTE*)malloc(cbDecodedMessageBlob)))
    {
        MyHandleError(
            TEXT("Memory allocation error allocating decode BLOB."));
        goto exit_VerifySignedMessage;
    }

    //---------------------------------------------------------------
    // Call CryptVerifyMessageSignature again to verify the signature
    // and, if successful, copy the decoded message into the buffer. 
    // This will validate the signature against the certificate in 
    // the local store.
    if(CryptVerifyMessageSignature(
        &VerifyParams,
        0,
        pSignedMessageBlob->pbData,
        pSignedMessageBlob->cbData,
        pbDecodedMessageBlob,
        &cbDecodedMessageBlob,
        NULL))
    {
        _tprintf(TEXT("The verified message is \"%s\".\n"),
            pbDecodedMessageBlob);

        fReturn = true;
    }
    else
    {
        _tprintf(TEXT("Verification message failed. \n"));
    }

exit_VerifySignedMessage:
    // If something failed and the decoded message buffer was 
    // allocated, free it.
    if(!fReturn)
    {
        if(pbDecodedMessageBlob)
        {
            free(pbDecodedMessageBlob);
            pbDecodedMessageBlob = NULL;
        }
    }

    // If the decoded message buffer is still around, it means the 
    // function was successful. Copy the pointer and size into the 
    // output parameter.
    if(pbDecodedMessageBlob)
    {
        pDecodedMessageBlob->cbData = cbDecodedMessageBlob;
        pDecodedMessageBlob->pbData = pbDecodedMessageBlob;
    }

    return fReturn;
}
```



 

 
