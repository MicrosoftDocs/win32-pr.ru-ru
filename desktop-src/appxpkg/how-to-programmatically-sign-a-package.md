---
title: Как программно подписать пакет приложения (C++)
description: Узнайте, как подписать пакет приложения с помощью функции SignerSignEx2.
ms.assetid: 1183D665-83C9-4BE7-9C8D-834484B8C57F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310ba2a934a6986809329a12afa8ee20b2f6591
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789661"
---
# <a name="how-to-programmatically-sign-an-app-package-c"></a><span data-ttu-id="24ab0-103">Как программно подписать пакет приложения (C++)</span><span class="sxs-lookup"><span data-stu-id="24ab0-103">How to programmatically sign an app package (C++)</span></span>

<span data-ttu-id="24ab0-104">Узнайте, как подписать пакет приложения с помощью функции [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .</span><span class="sxs-lookup"><span data-stu-id="24ab0-104">Learn how to sign an app package by using the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span>

<span data-ttu-id="24ab0-105">Если вы хотите программно создавать пакеты приложений Windows с помощью [API упаковки](interfaces.md), необходимо также подписать пакеты приложений, прежде чем их можно будет развернуть.</span><span class="sxs-lookup"><span data-stu-id="24ab0-105">If you want to programmatically create Windows app packages by using the [Packaging API](interfaces.md), you also need to sign the app packages before they can be deployed.</span></span> <span data-ttu-id="24ab0-106">API упаковки не предоставляет специализированный метод для подписи пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="24ab0-106">The Packaging API doesn't provide a specialized method for signing app packages.</span></span> <span data-ttu-id="24ab0-107">Вместо этого используйте стандартные [криптографические функции](/windows/desktop/SecCrypto/cryptography-functions) для подписи пакетов приложений.</span><span class="sxs-lookup"><span data-stu-id="24ab0-107">Instead, use the standard [cryptography functions](/windows/desktop/SecCrypto/cryptography-functions) to sign your app packages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="24ab0-108">Что необходимо знать</span><span class="sxs-lookup"><span data-stu-id="24ab0-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="24ab0-109">Технологии</span><span class="sxs-lookup"><span data-stu-id="24ab0-109">Technologies</span></span>

-   <span data-ttu-id="24ab0-110">[Знакомство с подписыванием кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24ab0-110">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   [<span data-ttu-id="24ab0-111">Упаковка, развертывание и запрос приложений Windows</span><span class="sxs-lookup"><span data-stu-id="24ab0-111">Packaging, deployment, and query of Windows apps</span></span>](appx-portal.md)
-   [<span data-ttu-id="24ab0-112">криптографические функции</span><span class="sxs-lookup"><span data-stu-id="24ab0-112">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a><span data-ttu-id="24ab0-113">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="24ab0-113">Prerequisites</span></span>

-   <span data-ttu-id="24ab0-114">Необходимо иметь упакованное приложение Windows.</span><span class="sxs-lookup"><span data-stu-id="24ab0-114">You need to have a packaged Windows app.</span></span> <span data-ttu-id="24ab0-115">Сведения о создании пакета приложения см. в разделе [Создание пакета приложения](how-to-create-a-package.md).</span><span class="sxs-lookup"><span data-stu-id="24ab0-115">For info about creating an app package, see [How to create an app package](how-to-create-a-package.md).</span></span>
-   <span data-ttu-id="24ab0-116">Необходимо иметь сертификат подписи кода, который подходит для подписи пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="24ab0-116">You need to have a code signing certificate that is appropriate for signing the app package.</span></span> <span data-ttu-id="24ab0-117">Сведения о создании сертификата подписи тестового кода см. [в разделе Создание сертификата для подписи пакета приложения](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="24ab0-117">For info about creating a test code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span> <span data-ttu-id="24ab0-118">Загрузите этот сертификат для подписи в [**структуру \_ контекста сертификата**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="24ab0-118">Load this signing certificate into a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="24ab0-119">Например, можно использовать [**пфксимпортцертсторе**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) и [**цертфиндцертификатеинсторе**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) для загрузки сертификата подписи.</span><span class="sxs-lookup"><span data-stu-id="24ab0-119">For example, you can use [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) and [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) to load a signing certificate.</span></span>
-   <span data-ttu-id="24ab0-120">В Windows 8 появилась функция [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) .</span><span class="sxs-lookup"><span data-stu-id="24ab0-120">Windows 8 introduces the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span> <span data-ttu-id="24ab0-121">Используйте **SignerSignEx2** при подписывании пакетов приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="24ab0-121">Use **SignerSignEx2** when you sign Windows app packages.</span></span>

## <a name="instructions"></a><span data-ttu-id="24ab0-122">Инструкции</span><span class="sxs-lookup"><span data-stu-id="24ab0-122">Instructions</span></span>

### <a name="step-1-define-the-required-structures-for-signersignex2"></a><span data-ttu-id="24ab0-123">Шаг 1. Определение необходимых структур для SignerSignEx2</span><span class="sxs-lookup"><span data-stu-id="24ab0-123">Step 1: Define the required structures for SignerSignEx2</span></span>

<span data-ttu-id="24ab0-124">Помимо заголовка Винкрипт. h, функция [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) зависит от множества структур, которые не определены в файле заголовка пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="24ab0-124">In addition to the Wincrypt.h header, the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function depends on many structures that aren't defined in any SDK header file.</span></span> <span data-ttu-id="24ab0-125">Чтобы использовать **SignerSignEx2**, необходимо определить эти структуры самостоятельно:</span><span class="sxs-lookup"><span data-stu-id="24ab0-125">To use **SignerSignEx2**, you must define these structures yourself:</span></span>


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



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a><span data-ttu-id="24ab0-126">Шаг 2. вызов SignerSignEx2 для подписи пакета приложения</span><span class="sxs-lookup"><span data-stu-id="24ab0-126">Step 2: Call SignerSignEx2 to sign the app package</span></span>

<span data-ttu-id="24ab0-127">После определения необходимых структур, указанных на предыдущем шаге, можно использовать любой из параметров, доступных в функции [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) , чтобы подписать пакет приложения.</span><span class="sxs-lookup"><span data-stu-id="24ab0-127">After you define the required structures that are specified in the previous step, you can use any of the options available on the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function to sign an app package.</span></span> <span data-ttu-id="24ab0-128">При использовании **SignerSignEx2** с пакетами приложений Windows эти ограничения применяются.</span><span class="sxs-lookup"><span data-stu-id="24ab0-128">When you use **SignerSignEx2** with Windows app packages, these restrictions apply:</span></span>

-   <span data-ttu-id="24ab0-129">При подписывании пакета приложения необходимо указать указатель на структуру **\_ \_ \_ данных клиента APPX SIP** в качестве параметра *псипдата* .</span><span class="sxs-lookup"><span data-stu-id="24ab0-129">You must provide a pointer to an **APPX\_SIP\_CLIENT\_DATA** structure as the *pSipData* parameter when you sign an app package.</span></span> <span data-ttu-id="24ab0-130">Необходимо заполнить элемент **псигнерпарамс** **\_ \_ \_ данных клиента APPX SIP** теми же параметрами, которые используются для подписания пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="24ab0-130">You must populate the **pSignerParams** member of **APPX\_SIP\_CLIENT\_DATA** with the same parameters that you use to sign the app package.</span></span> <span data-ttu-id="24ab0-131">Чтобы сделать это, определите нужные параметры в структуре Signing **\_ \_ EX2 \_ params** , присвойте адрес этой структуры **псигнерпарамс**, а затем непосредственно сослаться на элементы структуры при вызове [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).</span><span class="sxs-lookup"><span data-stu-id="24ab0-131">To do this, define your desired parameters on the **SIGNER\_SIGN\_EX2\_PARAMS** structure, assign the address of this structure to **pSignerParams**, and then directly reference the structure's members as well when you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).</span></span>
-   <span data-ttu-id="24ab0-132">После вызова [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)необходимо освободить **паппкссипстате** на *псипдата* , вызвав [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) на **паппкссипстате** , если он не **равен null**.</span><span class="sxs-lookup"><span data-stu-id="24ab0-132">After you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), you must free the **pAppxSipState** on the *pSipData* by calling [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on **pAppxSipState** if it's not **NULL**.</span></span>
-   <span data-ttu-id="24ab0-133">Член **алгидхаш** структуры **\_ \_ сведений о подписи** должен быть тем же хэш-алгоритмом, который использовался при создании пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="24ab0-133">The **algidHash** member of the **SIGNER\_SIGNATURE\_INFO** structure must be the same hash algorithm that was used in creating the app package.</span></span> <span data-ttu-id="24ab0-134">Сведения о том, как определить хэш-алгоритм из пакета приложения, см. [в разделе как подписать пакет приложения с помощью средства SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="24ab0-134">For info about how to determine the hash algorithm from the app package, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="24ab0-135">Алгоритм по умолчанию Windows 8, который [программе makeappx](make-appx-package--makeappx-exe-.md) и Visual Studio использует для создания пакетов приложений, — это "АЛГИДХАШ = калг \_ SHA \_ 256".</span><span class="sxs-lookup"><span data-stu-id="24ab0-135">The Windows 8 default algorithm that [MakeAppx](make-appx-package--makeappx-exe-.md) and Visual Studio use to create app packages is “algidHash = CALG\_SHA\_256”.</span></span>
-   <span data-ttu-id="24ab0-136">Если вы хотите, чтобы метка времени была также подписана в пакете приложения, необходимо сделать это во время вызова [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) , указав необязательные параметры отметки времени **SignerSignEx2**(*двтиместампфлагс*, *псзтиместампалгорисмоид*, *пвсзттптиместамп*, *псрекуест*).</span><span class="sxs-lookup"><span data-stu-id="24ab0-136">If you want to time stamp the signature on the app package as well, you must do so during the call to [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) by providing **SignerSignEx2**'s optional time stamping parameters (*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*).</span></span> <span data-ttu-id="24ab0-137">Вызов [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) или его вариантов в пакете приложения, который уже подписан, не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="24ab0-137">Calling [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) or its variants on an app package that is already signed is unsupported.</span></span>

<span data-ttu-id="24ab0-138">Ниже приведен пример кода, в котором показано, как вызвать [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):</span><span class="sxs-lookup"><span data-stu-id="24ab0-138">Here is some example code that shows how to call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):</span></span>


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



## <a name="remarks"></a><span data-ttu-id="24ab0-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="24ab0-139">Remarks</span></span>

<span data-ttu-id="24ab0-140">После подписывания пакета приложения можно также попытаться проверить подпись программным способом с помощью функции [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) с **винтруст \_ действием \_ Generic \_ Проверка \_ версии 2**.</span><span class="sxs-lookup"><span data-stu-id="24ab0-140">After you sign the app package, you can also attempt to validate the signature programmatically by using the [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) function with **WINTRUST\_ACTION\_GENERIC\_VERIFY\_V2**.</span></span> <span data-ttu-id="24ab0-141">В этом случае нет особых соображений, касающихся использования **WinVerifyTrust** с пакетами приложений Windows.</span><span class="sxs-lookup"><span data-stu-id="24ab0-141">There are no special considerations in this case for using **WinVerifyTrust** with Windows app packages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24ab0-142">См. также</span><span class="sxs-lookup"><span data-stu-id="24ab0-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="24ab0-143">[Знакомство с подписыванием кода](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="24ab0-143">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="24ab0-144">API для упаковки</span><span class="sxs-lookup"><span data-stu-id="24ab0-144">Packaging API</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="24ab0-145">криптографические функции</span><span class="sxs-lookup"><span data-stu-id="24ab0-145">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 