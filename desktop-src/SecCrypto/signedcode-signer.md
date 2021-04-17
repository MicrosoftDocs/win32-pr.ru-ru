---
description: Получает подписывание подписанного исполняемого файла.
ms.assetid: aafa7006-b47c-4f4e-a5c4-bd96d297f939
title: Сигнедкоде. Подписавши, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Signer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 053bb6c98c5b8776da2ca890de24359f41be1389
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668906"
---
# <a name="signedcodesigner-property"></a><span data-ttu-id="fc60d-103">Сигнедкоде. Подписавши, свойство</span><span class="sxs-lookup"><span data-stu-id="fc60d-103">SignedCode.Signer property</span></span>

<span data-ttu-id="fc60d-104">\[Свойство **подписавши** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="fc60d-104">\[The **Signer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fc60d-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="fc60d-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="fc60d-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="fc60d-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="fc60d-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="fc60d-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="fc60d-108">Свойство **подписавшего** извлекает подписавшего подписанный исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="fc60d-108">The **Signer** property retrieves the signer of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc60d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fc60d-109">Syntax</span></span>


```VB
SignedCode.Signer As Signer
```



## <a name="property-value"></a><span data-ttu-id="fc60d-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fc60d-110">Property value</span></span>

<span data-ttu-id="fc60d-111">Объект- [**подписавший**](signer.md) , предоставляющий доступ к подписанному исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="fc60d-111">A [**Signer**](signer.md) object that provides access to the signer of the signed executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc60d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="fc60d-112">Requirements</span></span>



| <span data-ttu-id="fc60d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="fc60d-113">Requirement</span></span> | <span data-ttu-id="fc60d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="fc60d-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc60d-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="fc60d-115">Redistributable</span></span><br/> | <span data-ttu-id="fc60d-116">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc60d-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fc60d-117">DLL</span><span class="sxs-lookup"><span data-stu-id="fc60d-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="fc60d-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc60d-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc60d-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fc60d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc60d-120">**сигнедкоде**</span><span class="sxs-lookup"><span data-stu-id="fc60d-120">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
