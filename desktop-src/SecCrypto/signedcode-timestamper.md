---
description: Свойство отметки времени извлекает Стампер времени подписанного исполняемого файла.
ms.assetid: f630b94f-015a-4387-938f-1b8c6b7895e9
title: Сигнедкоде. TimeStamp, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.TimeStamper
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5594cf46e82e47103d456fc7fe147e0470333953
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669317"
---
# <a name="signedcodetimestamper-property"></a><span data-ttu-id="077f3-103">Сигнедкоде. TimeStamp, свойство</span><span class="sxs-lookup"><span data-stu-id="077f3-103">SignedCode.TimeStamper property</span></span>

<span data-ttu-id="077f3-104">\[Свойство **метки времени** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="077f3-104">\[The **TimeStamper** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="077f3-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="077f3-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="077f3-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="077f3-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="077f3-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="077f3-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="077f3-108">Свойство **отметки времени** извлекает Стампер времени подписанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="077f3-108">The **TimeStamper** property retrieves the time stamper of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="077f3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="077f3-109">Syntax</span></span>


```VB
SignedCode.TimeStamper As Signer
```



## <a name="property-value"></a><span data-ttu-id="077f3-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="077f3-110">Property value</span></span>

<span data-ttu-id="077f3-111">Объект- [**подписавший**](signer.md) , предоставляющий доступ к времени Стампер подписанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="077f3-111">A [**Signer**](signer.md) object that provides access to the time stamper of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="077f3-112">Требования</span><span class="sxs-lookup"><span data-stu-id="077f3-112">Requirements</span></span>



| <span data-ttu-id="077f3-113">Требование</span><span class="sxs-lookup"><span data-stu-id="077f3-113">Requirement</span></span> | <span data-ttu-id="077f3-114">Значение</span><span class="sxs-lookup"><span data-stu-id="077f3-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="077f3-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="077f3-115">Redistributable</span></span><br/> | <span data-ttu-id="077f3-116">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="077f3-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="077f3-117">DLL</span><span class="sxs-lookup"><span data-stu-id="077f3-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="077f3-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="077f3-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="077f3-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="077f3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="077f3-120">**сигнедкоде**</span><span class="sxs-lookup"><span data-stu-id="077f3-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
