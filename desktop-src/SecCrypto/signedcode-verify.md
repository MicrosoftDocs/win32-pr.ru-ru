---
description: Проверяет подпись Authenticode для подписанного кода.
ms.assetid: eecd692d-6b20-4644-a3d9-fba07ee667d7
title: Сигнедкоде. Verify, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Verify
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ad9ad2cdbf9c8b7970f50446bba0da7a3afdcd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689379"
---
# <a name="signedcodeverify-method"></a><span data-ttu-id="5929c-103">Сигнедкоде. Verify, метод</span><span class="sxs-lookup"><span data-stu-id="5929c-103">SignedCode.Verify method</span></span>

<span data-ttu-id="5929c-104">\[Метод **Verify** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="5929c-104">\[The **Verify** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5929c-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="5929c-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="5929c-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="5929c-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="5929c-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="5929c-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="5929c-108">Метод **Verify** проверяет подпись Authenticode на подписанном коде.</span><span class="sxs-lookup"><span data-stu-id="5929c-108">The **Verify** method verifies the Authenticode signature on the signed code.</span></span>

## <a name="syntax"></a><span data-ttu-id="5929c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5929c-109">Syntax</span></span>


```VB
SignedCode.Verify( _
  [ ByVal bUIAllowed ] _
)
```



## <a name="parameters"></a><span data-ttu-id="5929c-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="5929c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5929c-111">*буиалловед* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="5929c-111">*bUIAllowed* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="5929c-112">Логическое значение, указывающее, используется ли диалоговое окно для проверки подписи.</span><span class="sxs-lookup"><span data-stu-id="5929c-112">A Boolean value that specifies whether a dialog box is used to verify the signature.</span></span> <span data-ttu-id="5929c-113">Если значение — true, создается диалоговое окно для определения, является ли код доверенным.</span><span class="sxs-lookup"><span data-stu-id="5929c-113">If true, a dialog box is generated to determine whether the code is trusted.</span></span> <span data-ttu-id="5929c-114">Значением по умолчанию является false.</span><span class="sxs-lookup"><span data-stu-id="5929c-114">The default value is false.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5929c-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5929c-115">Return value</span></span>

<span data-ttu-id="5929c-116">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="5929c-116">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5929c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="5929c-117">Requirements</span></span>



| <span data-ttu-id="5929c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="5929c-118">Requirement</span></span> | <span data-ttu-id="5929c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="5929c-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5929c-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="5929c-120">Redistributable</span></span><br/> | <span data-ttu-id="5929c-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="5929c-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5929c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="5929c-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="5929c-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5929c-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5929c-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5929c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5929c-125">**сигнедкоде**</span><span class="sxs-lookup"><span data-stu-id="5929c-125">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
