---
description: Задает или получает URL-адрес для описания подписанного исполняемого файла.
ms.assetid: 854c76fb-5cb3-4200-bab0-fa3fa5bd3abe
title: Сигнедкоде. Дескриптионурл, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.DescriptionURL
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 628d176595031f2b87b9fcb5f58ff81838d49be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685209"
---
# <a name="signedcodedescriptionurl-property"></a><span data-ttu-id="56e23-103">Сигнедкоде. Дескриптионурл, свойство</span><span class="sxs-lookup"><span data-stu-id="56e23-103">SignedCode.DescriptionURL property</span></span>

<span data-ttu-id="56e23-104">\[Свойство **дескриптионурл** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="56e23-104">\[The **DescriptionURL** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="56e23-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="56e23-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="56e23-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="56e23-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="56e23-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="56e23-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="56e23-108">Свойство **дескриптионурл** задает или получает URL-адрес для описания подписанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="56e23-108">The **DescriptionURL** property sets or retrieves the URL of a description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="56e23-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56e23-109">Syntax</span></span>


```VB
SignedCode.DescriptionURL As String
```



## <a name="property-value"></a><span data-ttu-id="56e23-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="56e23-110">Property value</span></span>

<span data-ttu-id="56e23-111">URL-адрес описания подписанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="56e23-111">The URL of a description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="56e23-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56e23-112">Remarks</span></span>

<span data-ttu-id="56e23-113">**Дескриптионурл** — это URL-адрес, по которому отображается [**Описание**](signedcode-description.md) в диалоговых окнах проверки Authenticode.</span><span class="sxs-lookup"><span data-stu-id="56e23-113">The **DescriptionURL** is the URL to which the [**Description**](signedcode-description.md) that appears in the Authenticode verification dialog box links.</span></span> <span data-ttu-id="56e23-114">Если это свойство имеет **значение NULL**, **Описание** не работает как ссылка.</span><span class="sxs-lookup"><span data-stu-id="56e23-114">If this property is **NULL**, the **Description** does not function as a link.</span></span>

## <a name="requirements"></a><span data-ttu-id="56e23-115">Требования</span><span class="sxs-lookup"><span data-stu-id="56e23-115">Requirements</span></span>



| <span data-ttu-id="56e23-116">Требование</span><span class="sxs-lookup"><span data-stu-id="56e23-116">Requirement</span></span> | <span data-ttu-id="56e23-117">Значение</span><span class="sxs-lookup"><span data-stu-id="56e23-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56e23-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="56e23-118">Redistributable</span></span><br/> | <span data-ttu-id="56e23-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="56e23-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="56e23-120">DLL</span><span class="sxs-lookup"><span data-stu-id="56e23-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="56e23-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56e23-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56e23-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56e23-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56e23-123">**сигнедкоде**</span><span class="sxs-lookup"><span data-stu-id="56e23-123">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
