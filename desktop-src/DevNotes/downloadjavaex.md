---
description: Загружает подпись CAB-файла, проверяет разрешения, связанные с пакетами, и выполняет их на основе проверки подлинности.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: Функция Довнлоаджаваекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657378"
---
# <a name="downloadjavaex-function"></a><span data-ttu-id="4b060-103">Функция Довнлоаджаваекс</span><span class="sxs-lookup"><span data-stu-id="4b060-103">DownloadJavaEX function</span></span>

<span data-ttu-id="4b060-104">Загружает подпись CAB-файла, проверяет разрешения, связанные с пакетами, и выполняет их на основе проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="4b060-104">Downloads the .cab file signature, verifies the permissions associated with the packages, and executes them based on authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b060-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b060-105">Syntax</span></span>


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a><span data-ttu-id="4b060-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b060-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b060-107">*Зарезервировано* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b060-107">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b060-108">Этот параметр зарезервирован.</span><span class="sxs-lookup"><span data-stu-id="4b060-108">This parameter is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="4b060-109">*ппровидердата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b060-109">*pProviderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b060-110">Структура [**\_ \_ данных поставщика шифрования**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) , содержащая данные сертификата, такие как разрешения файла и зоны.</span><span class="sxs-lookup"><span data-stu-id="4b060-110">A [**CRYPT\_PROVIDER\_DATA**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) structure that contains certificate data such as file and zone permissions.</span></span>

</dd> <dt>

<span data-ttu-id="4b060-111">*пжава* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b060-111">*pJava* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b060-112">Структура [**\_ \_ поставщика политики Java**](/previous-versions//bb432350(v=vs.85)) , которая содержит данные, связанные с поставщиком политики.</span><span class="sxs-lookup"><span data-stu-id="4b060-112">A [**JAVA\_POLICY\_PROVIDER**](/previous-versions//bb432350(v=vs.85)) structure that contains data related to the policy provider.</span></span>

</dd> <dt>

<span data-ttu-id="4b060-113">*пфунктионс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b060-113">*pFunctions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b060-114">Структура [**\_ \_ функций поставщика**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) , которая содержит список методов для проверки объектов сертификата, подписей и окончательных политик.</span><span class="sxs-lookup"><span data-stu-id="4b060-114">A [**CRYPT\_PROVIDER\_FUNCTIONS**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) structure that contains a list of methods to verify certificate objects, signatures, and final policies.</span></span>

</dd> <dt>

<span data-ttu-id="4b060-115">*фцертификате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b060-115">*fCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b060-116">Если сертификат имеется, этот параметр имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="4b060-116">If a certificate is present, this parameter is **TRUE**.</span></span> <span data-ttu-id="4b060-117">В противном случае — **false**.</span><span class="sxs-lookup"><span data-stu-id="4b060-117">Otherwise, it is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="4b060-118">*птруст* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="4b060-118">*pTrust* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4b060-119">Структура [**\_ доверия Java**](/windows/desktop/api/Capi/ns-capi-java_trust) , содержащая сведения о доверии, такие как закодированное разрешение, сигнатура кодировщика и подлинное возвращение кода политики.</span><span class="sxs-lookup"><span data-stu-id="4b060-119">A [**JAVA\_TRUST**](/windows/desktop/api/Capi/ns-capi-java_trust) structure that contains trust information such as encoded permission, encoder signature, and authentic return policy code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b060-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b060-120">Return value</span></span>

<span data-ttu-id="4b060-121">Если функция выполнена успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="4b060-121">If the function succeeds, the return value is **S\_OK**.</span></span> <span data-ttu-id="4b060-122">В противном случае возвращаемое значение является кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="4b060-122">Otherwise, the return value is an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b060-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4b060-123">Remarks</span></span>

<span data-ttu-id="4b060-124">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4b060-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b060-125">Требования</span><span class="sxs-lookup"><span data-stu-id="4b060-125">Requirements</span></span>



| <span data-ttu-id="4b060-126">Требование</span><span class="sxs-lookup"><span data-stu-id="4b060-126">Requirement</span></span> | <span data-ttu-id="4b060-127">Значение</span><span class="sxs-lookup"><span data-stu-id="4b060-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b060-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4b060-128">DLL</span></span><br/> | <dl> <span data-ttu-id="4b060-129"><dt>Javacypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b060-129"><dt>Javacypt.dll</dt></span></span> </dl> |



 

 
