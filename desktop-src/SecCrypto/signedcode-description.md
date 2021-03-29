---
description: Задает или получает описание подписанного исполняемого файла.
ms.assetid: 39ce37bd-fe3e-4195-a132-93f3743f7370
title: Сигнедкоде. Description, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedCode.Description
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b5783dd5e662aed33722a1c587bfcdc3cab76c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668763"
---
# <a name="signedcodedescription-property"></a><span data-ttu-id="0fa1c-103">Сигнедкоде. Description, свойство</span><span class="sxs-lookup"><span data-stu-id="0fa1c-103">SignedCode.Description property</span></span>

<span data-ttu-id="0fa1c-104">\[Свойство **Description** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="0fa1c-104">\[The **Description** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="0fa1c-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций Win32 API [**сигнерсигнекс**](signersignex.md), [**сигнертиместампекс**](signertimestampex.md)и [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) для подписи содержимого цифровой подписью Authenticode.</span><span class="sxs-lookup"><span data-stu-id="0fa1c-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API [**SignerSignEx**](signersignex.md), [**SignerTimeStampEx**](signertimestampex.md), and [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust) functions to sign content with an Authenticode digital signature.</span></span> <span data-ttu-id="0fa1c-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="0fa1c-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="0fa1c-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="0fa1c-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="0fa1c-108">Свойство **Description** задает или получает описание подписанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="0fa1c-108">The **Description** property sets or retrieves the description of the signed executable file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fa1c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fa1c-109">Syntax</span></span>


```VB
SignedCode.Description As String
```



## <a name="property-value"></a><span data-ttu-id="0fa1c-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="0fa1c-110">Property value</span></span>

<span data-ttu-id="0fa1c-111">Описание подписанного исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="0fa1c-111">The description of the signed executable file.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fa1c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0fa1c-112">Remarks</span></span>

<span data-ttu-id="0fa1c-113">Описание — это текст, отображаемый в диалоговом окне проверки Authenticode.</span><span class="sxs-lookup"><span data-stu-id="0fa1c-113">The description is the text that appears in the Authenticode verification dialog box.</span></span> <span data-ttu-id="0fa1c-114">Текст должен описывать подписанный исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="0fa1c-114">The text should describe the signed executable file.</span></span> <span data-ttu-id="0fa1c-115">Если это свойство имеет **значение NULL**, в диалоговом окне отображается имя исполняемого файла.</span><span class="sxs-lookup"><span data-stu-id="0fa1c-115">If this property is **NULL**, the dialog box displays the name of the executable file.</span></span>

## <a name="requirements"></a><span data-ttu-id="0fa1c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0fa1c-116">Requirements</span></span>



| <span data-ttu-id="0fa1c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="0fa1c-117">Requirement</span></span> | <span data-ttu-id="0fa1c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="0fa1c-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0fa1c-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0fa1c-119">Redistributable</span></span><br/> | <span data-ttu-id="0fa1c-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="0fa1c-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0fa1c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0fa1c-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="0fa1c-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fa1c-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0fa1c-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0fa1c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fa1c-124">**сигнедкоде**</span><span class="sxs-lookup"><span data-stu-id="0fa1c-124">**SignedCode**</span></span>](signedcode.md)
</dt> </dl>

 

 
