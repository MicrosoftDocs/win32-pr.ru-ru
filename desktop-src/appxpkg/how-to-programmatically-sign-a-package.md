---
title: Как программно подписать пакет приложения (C++)
description: Узнайте, как подписать пакет приложения с помощью функции SignerSignEx2.
ms.assetid: 1183D665-83C9-4BE7-9C8D-834484B8C57F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a91cf2c7b7be674ff14d1ceada59be593a300d7ebf1964ddce4a7a5340ab74c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130246"
---
# <a name="how-to-programmatically-sign-an-app-package-c"></a>Как программно подписать пакет приложения (C++)

Узнайте, как подписать пакет приложения с помощью функции [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .

если требуется программное создание пакетов приложений Windows с помощью [API упаковки](interfaces.md), необходимо также подписать пакеты приложений, прежде чем их можно будет развернуть. API упаковки не предоставляет специализированный метод для подписи пакетов приложений. Вместо этого используйте стандартные [криптографические функции](/windows/desktop/SecCrypto/cryptography-functions) для подписи пакетов приложений.

## <a name="what-you-need-to-know"></a>Это важно знать

### <a name="technologies"></a>Технологии

-   [Знакомство с подписыванием кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [упаковка, развертывание и запрос приложений Windows](appx-portal.md)
-   [криптографические функции](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a>Обязательные условия

-   необходимо наличие упакованного Windows приложения. Сведения о создании пакета приложения см. в разделе [Создание пакета приложения](how-to-create-a-package.md).
-   Необходимо иметь сертификат подписи кода, который подходит для подписи пакета приложения. Сведения о создании сертификата подписи тестового кода см. [в разделе Создание сертификата для подписи пакета приложения](how-to-create-a-package-signing-certificate.md). Загрузите этот сертификат для подписи в [**структуру \_ контекста сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . Например, можно использовать [**пфксимпортцертсторе**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) и [**цертфиндцертификатеинсторе**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) для загрузки сертификата подписи.
-   в Windows 8 введена функция [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) . используйте **SignerSignEx2** при подписывании пакетов приложений Windows.

## <a name="instructions"></a>Инструкции

### <a name="step-1-define-the-required-structures-for-signersignex2"></a>Шаг 1. Определение необходимых структур для SignerSignEx2

Помимо заголовка Винкрипт. h, функция [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) зависит от множества структур, которые не определены в файле заголовка пакета SDK. Чтобы использовать **SignerSignEx2**, необходимо определить эти структуры самостоятельно:


```C++
typedef struct _SIGNER_FILE_INFO
{
    DWORD cbSize;
    LPCWSTR pwszFileName;
    HANDLE hFile;
}SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
 
typedef struct _SIGNER_BLOB_INFO
{
    DWORD cbSize;
    GUID *pGuidSubject;
    DWORD cbBlob;
    BYTE *pbBlob;
    LPCWSTR pwszDisplayName;
}SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
 
typedef struct _SIGNER_SUBJECT_INFO
{
    DWORD cbSize;
    DWORD *pdwIndex;
    DWORD dwSubjectChoice;
    union
    {
        SIGNER_FILE_INFO *pSignerFileInfo;
        SIGNER_BLOB_INFO *pSignerBlobInfo;
    };
}SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
 
// dwSubjectChoice should be one of the following:
#define SIGNER_SUBJECT_FILE    0x01
#define SIGNER_SUBJECT_BLOB    0x02
 
typedef struct _SIGNER_ATTR_AUTHCODE
{
    DWORD cbSize;
    BOOL fCommercial;
    BOOL fIndividual;
    LPCWSTR pwszName;
    LPCWSTR pwszInfo;
}SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
 
typedef struct _SIGNER_SIGNATURE_INFO
{
    DWORD cbSize;
    ALG_ID algidHash;
    DWORD dwAttrChoice;
    union
    {
        SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
    };
    PCRYPT_ATTRIBUTES psAuthenticated;
    PCRYPT_ATTRIBUTES psUnauthenticated;
}SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
 
// dwAttrChoice should be one of the following:
#define SIGNER_NO_ATTR          0x00
#define SIGNER_AUTHCODE_ATTR    0x01
 
typedef struct _SIGNER_PROVIDER_INFO
{
    DWORD cbSize;
    LPCWSTR pwszProviderName;
    DWORD dwProviderType;
    DWORD dwKeySpec;
    DWORD dwPvkChoice;
    union
    {
        LPWSTR pwszPvkFileName;
        LPWSTR pwszKeyContainer;
    };
}SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
 
//dwPvkChoice should be one of the following:
#define PVK_TYPE_FILE_NAME       0x01
#define PVK_TYPE_KEYCONTAINER    0x02
 
typedef struct _SIGNER_SPC_CHAIN_INFO
{
    DWORD cbSize;
    LPCWSTR pwszSpcFile;
    DWORD dwCertPolicy; 
    HCERTSTORE hCertStore;
}SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
 
typedef struct _SIGNER_CERT_STORE_INFO
{
    DWORD cbSize;
    PCCERT_CONTEXT pSigningCert;
    DWORD dwCertPolicy;
    HCERTSTORE hCertStore;
}SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
 
//dwCertPolicy can be a combination of the following flags:
#define SIGNER_CERT_POLICY_STORE            0x01
#define SIGNER_CERT_POLICY_CHAIN            0x02
#define SIGNER_CERT_POLICY_SPC              0x04
#define SIGNER_CERT_POLICY_CHAIN_NO_ROOT    0x08
 
typedef struct _SIGNER_CERT
{
    DWORD cbSize;
    DWORD dwCertChoice;
    union
    {
        LPCWSTR pwszSpcFile;
        SIGNER_CERT_STORE_INFO *pCertStoreInfo;
        SIGNER_SPC_CHAIN_INFO *pSpcChainInfo;
    };
    HWND hwnd;
}SIGNER_CERT, *PSIGNER_CERT;
 
//dwCertChoice should be one of the following
#define SIGNER_CERT_SPC_FILE     0x01
#define SIGNER_CERT_STORE        0x02
#define SIGNER_CERT_SPC_CHAIN    0x03
 
typedef struct _SIGNER_CONTEXT
{
    DWORD cbSize;
    DWORD cbBlob;
    BYTE *pbBlob;
}SIGNER_CONTEXT, *PSIGNER_CONTEXT;
 
typedef struct _SIGNER_SIGN_EX2_PARAMS
{
    DWORD dwFlags;
    PSIGNER_SUBJECT_INFO pSubjectInfo;
    PSIGNER_CERT pSigningCert;
    PSIGNER_SIGNATURE_INFO pSignatureInfo;
    PSIGNER_PROVIDER_INFO pProviderInfo;
    DWORD dwTimestampFlags;
    PCSTR pszAlgorithmOid;
    PCWSTR pwszTimestampURL;
    PCRYPT_ATTRIBUTES pCryptAttrs;
    PVOID pSipData;
    PSIGNER_CONTEXT *pSignerContext;
    PVOID pCryptoPolicy;
    PVOID pReserved;
} SIGNER_SIGN_EX2_PARAMS, *PSIGNER_SIGN_EX2_PARAMS;
 
typedef struct _APPX_SIP_CLIENT_DATA
{
    PSIGNER_SIGN_EX2_PARAMS pSignerParams;
    IUnknown* pAppxSipState;
} APPX_SIP_CLIENT_DATA, *PAPPX_SIP_CLIENT_DATA;
```



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a>Шаг 2. вызов SignerSignEx2 для подписи пакета приложения

После определения необходимых структур, указанных на предыдущем шаге, можно использовать любой из параметров, доступных в функции [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) , чтобы подписать пакет приложения. при использовании **SignerSignEx2** с пакетами приложений Windows применяются следующие ограничения.

-   При подписывании пакета приложения необходимо указать указатель на структуру **\_ \_ \_ данных клиента APPX SIP** в качестве параметра *псипдата* . Необходимо заполнить элемент **псигнерпарамс** **\_ \_ \_ данных клиента APPX SIP** теми же параметрами, которые используются для подписания пакета приложения. Чтобы сделать это, определите нужные параметры в структуре Signing **\_ \_ EX2 \_ params** , присвойте адрес этой структуры **псигнерпарамс**, а затем непосредственно сослаться на элементы структуры при вызове [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).
-   После вызова [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)необходимо освободить **паппкссипстате** на *псипдата* , вызвав [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) на **паппкссипстате** , если он не **равен null**.
-   Член **алгидхаш** структуры **\_ \_ сведений о подписи** должен быть тем же хэш-алгоритмом, который использовался при создании пакета приложения. Сведения о том, как определить хэш-алгоритм из пакета приложения, см. [в разделе как подписать пакет приложения с помощью средства SignTool](how-to-sign-a-package-using-signtool.md). алгоритм Windows 8 по умолчанию, который [программе makeappx](make-appx-package--makeappx-exe-.md) и Visual Studio использовать для создания пакетов приложений, — это "алгидхаш = калг \_ SHA \_ 256".
-   Если вы хотите, чтобы метка времени была также подписана в пакете приложения, необходимо сделать это во время вызова [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) , указав необязательные параметры отметки времени **SignerSignEx2**(*двтиместампфлагс*, *псзтиместампалгорисмоид*, *пвсзттптиместамп*, *псрекуест*). Вызов [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) или его вариантов в пакете приложения, который уже подписан, не поддерживается.

Ниже приведен пример кода, в котором показано, как вызвать [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):


```C++
HRESULT SignAppxPackage(
    _In_ PCCERT_CONTEXT signingCertContext,
    _In_ LPCWSTR packageFilePath)
{
    HRESULT hr = S_OK;
 
    // Initialize the parameters for SignerSignEx2
    DWORD signerIndex = 0;
 
    SIGNER_FILE_INFO fileInfo = {};
    fileInfo.cbSize = sizeof(SIGNER_FILE_INFO);
    fileInfo.pwszFileName = packageFilePath;
 
    SIGNER_SUBJECT_INFO subjectInfo = {};
    subjectInfo.cbSize = sizeof(SIGNER_SUBJECT_INFO);
    subjectInfo.pdwIndex = &signerIndex;
    subjectInfo.dwSubjectChoice = SIGNER_SUBJECT_FILE;
    subjectInfo.pSignerFileInfo = &fileInfo;
 
    SIGNER_CERT_STORE_INFO certStoreInfo = {};
    certStoreInfo.cbSize = sizeof(SIGNER_CERT_STORE_INFO);
    certStoreInfo.dwCertPolicy = SIGNER_CERT_POLICY_CHAIN_NO_ROOT;
    certStoreInfo.pSigningCert = signingCertContext;
 
    SIGNER_CERT cert = {};
    cert.cbSize = sizeof(SIGNER_CERT);
    cert.dwCertChoice = SIGNER_CERT_STORE;
    cert.pCertStoreInfo = &certStoreInfo;
 
    // The algidHash of the signature to be created must match the
    // hash algorithm used to create the app package
    SIGNER_SIGNATURE_INFO signatureInfo = {};
    signatureInfo.cbSize = sizeof(SIGNER_SIGNATURE_INFO);
    signatureInfo.algidHash = CALG_SHA_256; 
    signatureInfo.dwAttrChoice = SIGNER_NO_ATTR;
 
    SIGNER_SIGN_EX2_PARAMS signerParams = {};
    signerParams.pSubjectInfo = &subjectInfo;
    signerParams.pSigningCert = &cert;
    signerParams.pSignatureInfo = &signatureInfo;
 
    APPX_SIP_CLIENT_DATA sipClientData = {};
    sipClientData.pSignerParams = &signerParams;
    signerParams.pSipData = &sipClientData;
 
    // Type definition for invoking SignerSignEx2 via GetProcAddress
    typedef HRESULT (WINAPI *SignerSignEx2Function)(
        DWORD,
        PSIGNER_SUBJECT_INFO,
        PSIGNER_CERT,
        PSIGNER_SIGNATURE_INFO,
        PSIGNER_PROVIDER_INFO,
        DWORD,
        PCSTR,
        PCWSTR,
        PCRYPT_ATTRIBUTES,
        PVOID,
        PSIGNER_CONTEXT *,
        PVOID,
        PVOID); 
 
    // Load the SignerSignEx2 function from MSSign32.dll
    HMODULE msSignModule = LoadLibraryEx(
        L"MSSign32.dll", 
        NULL, 
        LOAD_LIBRARY_SEARCH_SYSTEM32);

    if (msSignModule)
    {
        SignerSignEx2Function SignerSignEx2 = reinterpret_cast<SignerSignEx2Function>(
            GetProcAddress(msSignModule, "SignerSignEx2"));
        if (SignerSignEx2)
        {
            hr = SignerSignEx2(
                signerParams.dwFlags,
                signerParams.pSubjectInfo,
                signerParams.pSigningCert,
                signerParams.pSignatureInfo,
                signerParams.pProviderInfo,
                signerParams.dwTimestampFlags,
                signerParams.pszAlgorithmOid,
                signerParams.pwszTimestampURL,
                signerParams.pCryptAttrs,
                signerParams.pSipData,
                signerParams.pSignerContext,
                signerParams.pCryptoPolicy,
                signerParams.pReserved);
        }
        else
        {
            DWORD lastError = GetLastError();
            hr = HRESULT_FROM_WIN32(lastError);
        }
 
        FreeLibrary(msSignModule);
    }
    else
    {
        DWORD lastError = GetLastError();
        hr = HRESULT_FROM_WIN32(lastError);
    }
 
    // Free any state used during app package signing
    if (sipClientData.pAppxSipState)
    {
        sipClientData.pAppxSipState->Release();
    }
 
    return hr;
}
```



## <a name="remarks"></a>Remarks

После подписывания пакета приложения можно также попытаться проверить подпись программным способом с помощью функции [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) с **винтруст \_ действием \_ Generic \_ Проверка \_ версии 2**. в этом случае нет особых соображений, касающихся использования **WinVerifyTrust** с пакетами приложений Windows.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Знакомство с подписыванием кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[API для упаковки](interfaces.md)
</dt> <dt>

[криптографические функции](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 