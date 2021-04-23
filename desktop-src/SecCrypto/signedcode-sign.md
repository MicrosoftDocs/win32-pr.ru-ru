---
description: Создает цифровую подпись Authenticode и подписывает исполняемый файл, указанный в свойстве Сигнедкоде. FileName.
ms.assetid: db17be29-35ec-4468-b5cc-5ba64c4cf3fb
title: Сигнедкоде. Sign, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Sign
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 36e5c813b997ae452d44764ed88f51b273c75528
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689179"
---
# <a name="signedcodesign-method"></a><span data-ttu-id="20aa8-103">Сигнедкоде. Sign, метод</span><span class="sxs-lookup"><span data-stu-id="20aa8-103">SignedCode.Sign method</span></span>

<span data-ttu-id="20aa8-104">\[Метод **Sign** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="20aa8-104">\[The **Sign** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="20aa8-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="20aa8-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="20aa8-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="20aa8-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="20aa8-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="20aa8-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="20aa8-108">Метод **Sign** создает цифровую подпись Authenticode и подписывает исполняемый файл, указанный в свойстве [**сигнедкоде. filename**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="20aa8-108">The **Sign** method creates an Authenticode digital signature and signs the executable file specified in the [**SignedCode.FileName**](signedcode-filename.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="20aa8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20aa8-109">Syntax</span></span>


```VB
SignedCode.Sign( _
  [ ByVal Signer ] _
)
```



## <a name="parameters"></a><span data-ttu-id="20aa8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="20aa8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20aa8-111">*Подписавший* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="20aa8-111">*Signer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="20aa8-112">Объект- [**подписавший**](signer.md) , который имеет доступ к закрытому ключу сертификата, используемого для подписания кода.</span><span class="sxs-lookup"><span data-stu-id="20aa8-112">A [**Signer**](signer.md) object that has access to the private key of the certificate used to sign the code.</span></span> <span data-ttu-id="20aa8-113">Значение по умолчанию — **null**.</span><span class="sxs-lookup"><span data-stu-id="20aa8-113">The default value is **Null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20aa8-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="20aa8-114">Return value</span></span>

<span data-ttu-id="20aa8-115">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="20aa8-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="20aa8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="20aa8-116">Remarks</span></span>

<span data-ttu-id="20aa8-117">Перед вызовом метода **Sign** файл, содержащий код, должен быть указан в свойстве [**filename**](signedcode-filename.md) .</span><span class="sxs-lookup"><span data-stu-id="20aa8-117">Before the **Sign** method is called, the file that contains the code must be specified in the [**FileName**](signedcode-filename.md) property.</span></span>

<span data-ttu-id="20aa8-118">Если исполняемый файл уже подписан, этот метод перезаписывает существующую сигнатуру.</span><span class="sxs-lookup"><span data-stu-id="20aa8-118">If the executable file is already signed, this method overwrites the existing signature.</span></span>

<span data-ttu-id="20aa8-119">Следующие результаты применяются к значению параметра *SignIn* :</span><span class="sxs-lookup"><span data-stu-id="20aa8-119">The following results apply to the *Signer* parameter value:</span></span>

-   <span data-ttu-id="20aa8-120">Если параметр- *подписывающий* имеет значение, отличное от **null**, этот метод использует закрытый ключ, указанный в соответствующем сертификате, для шифрования подписи.</span><span class="sxs-lookup"><span data-stu-id="20aa8-120">If the *Signer* parameter is not **NULL**, this method uses the private key pointed to by the associated certificate to encrypt the signature.</span></span> <span data-ttu-id="20aa8-121">Если закрытый ключ, на который указывает сертификат, недоступен, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="20aa8-121">If the private key pointed to by the certificate is not available, the method fails.</span></span>
-   <span data-ttu-id="20aa8-122">Если параметр- *подписывающий* имеет **значение NULL** и в хранилище текущего пользователя есть ровно один сертификат \_ , имеющий доступ к закрытому ключу с возможностью подписывания кода, то этот сертификат используется для создания подписи.</span><span class="sxs-lookup"><span data-stu-id="20aa8-122">If the *Signer* parameter is **NULL** and there is exactly one certificate in the CURRENT\_USER MY store that has access to a private key with code signing capability, that certificate is used to create the signature.</span></span>
-   <span data-ttu-id="20aa8-123">Если параметр- *подписывающий* имеет значение **null**, то значением свойства [**Settings. енаблепромптфорцертификатеуи**](settings-enablepromptforcertificateui.md) является true, и в \_ хранилище текущего пользователя, имеющего доступный закрытый ключ с возможностью подписывания кода, имеется несколько сертификатов. в этом случае появляется диалоговое окно, позволяющее пользователю выбрать используемый сертификат.</span><span class="sxs-lookup"><span data-stu-id="20aa8-123">If the *Signer* parameter is **NULL**, the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property value is true, and there is more than one certificate in the CURRENT\_USER MY store with an available private key with code signing capability, a dialog box appears that allows the user to select which certificate is used.</span></span>
-   <span data-ttu-id="20aa8-124">Если параметр- *подписывающий* имеет **значение NULL** , а свойство [**Settings. енаблепромптфорцертификатеуи**](settings-enablepromptforcertificateui.md) имеет значение false, то метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="20aa8-124">If the *Signer* parameter is **NULL** and the [**Settings.EnablePromptForCertificateUI**](settings-enablepromptforcertificateui.md) property is false, the method fails.</span></span>
-   <span data-ttu-id="20aa8-125">Если параметр- *подписывающий* имеет **значение NULL** и в хранилище текущего пользователя нет сертификатов \_ с доступным закрытым ключом с возможностью подписывания кода, метод завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="20aa8-125">If the *Signer* parameter is **NULL** and there are no certificates in the CURRENT\_USER MY store with an available private key with code signing capability, the method fails.</span></span>

<span data-ttu-id="20aa8-126">Этот метод использует алгоритм хэширования SHA-1.</span><span class="sxs-lookup"><span data-stu-id="20aa8-126">This method uses the SHA-1 hashing algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="20aa8-127">Требования</span><span class="sxs-lookup"><span data-stu-id="20aa8-127">Requirements</span></span>



| <span data-ttu-id="20aa8-128">Требование</span><span class="sxs-lookup"><span data-stu-id="20aa8-128">Requirement</span></span> | <span data-ttu-id="20aa8-129">Значение</span><span class="sxs-lookup"><span data-stu-id="20aa8-129">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="20aa8-130">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="20aa8-130">Redistributable</span></span><br/> | <span data-ttu-id="20aa8-131">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="20aa8-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="20aa8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="20aa8-132">DLL</span></span><br/>             | <dl> <span data-ttu-id="20aa8-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="20aa8-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
