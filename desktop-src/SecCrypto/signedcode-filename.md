---
description: Свойство FileName задает или получает путь к исполняемому файлу. Это свойство по умолчанию.
ms.assetid: 2d2ea87b-86db-40b4-b052-8503beafa08c
title: Сигнедкоде. FileName, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.FileName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e6e31e57376f987b2b5cb47e5e6bd8a0d5e85fba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669455"
---
# <a name="signedcodefilename-property"></a><span data-ttu-id="9571c-104">Сигнедкоде. FileName, свойство</span><span class="sxs-lookup"><span data-stu-id="9571c-104">SignedCode.FileName property</span></span>

<span data-ttu-id="9571c-105">\[Свойство **filename** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9571c-105">\[The **FileName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9571c-106">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="9571c-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="9571c-107">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="9571c-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="9571c-108">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="9571c-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="9571c-109">Свойство **filename** задает или получает путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="9571c-109">The **FileName** property sets or retrieves the path to the executable file.</span></span> <span data-ttu-id="9571c-110">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9571c-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9571c-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9571c-111">Syntax</span></span>


```VB
SignedCode.FileName As String
```



## <a name="property-value"></a><span data-ttu-id="9571c-112">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9571c-112">Property value</span></span>

<span data-ttu-id="9571c-113">Путь к исполняемому файлу.</span><span class="sxs-lookup"><span data-stu-id="9571c-113">The path to the executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="9571c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9571c-114">Remarks</span></span>

<span data-ttu-id="9571c-115">Если значение свойства **filename** изменено, состояние всего объекта [**сигнедкоде**](signedcode.md) сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="9571c-115">If the value of the **FileName** property is modified, the state of the entire [**SignedCode**](signedcode.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="9571c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="9571c-116">Requirements</span></span>



| <span data-ttu-id="9571c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="9571c-117">Requirement</span></span> | <span data-ttu-id="9571c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="9571c-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9571c-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9571c-119">Redistributable</span></span><br/> | <span data-ttu-id="9571c-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9571c-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9571c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="9571c-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="9571c-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9571c-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9571c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9571c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9571c-124">**сигнедкоде**</span><span class="sxs-lookup"><span data-stu-id="9571c-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
