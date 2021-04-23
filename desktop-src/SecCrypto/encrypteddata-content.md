---
description: Задает или получает содержимое для шифрования или расшифровки.
ms.assetid: fdab0f19-c69e-443b-b4b3-079d23028921
title: EncryptedData. Content, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Content
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4b873d40ed04270defe04fd59f0ce00a0f84040a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647974"
---
# <a name="encrypteddatacontent-property"></a><span data-ttu-id="6b18a-103">EncryptedData. Content, свойство</span><span class="sxs-lookup"><span data-stu-id="6b18a-103">EncryptedData.Content property</span></span>

<span data-ttu-id="6b18a-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6b18a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6b18a-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций API Win32 [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) и [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) для шифрования и расшифровки сообщений.</span><span class="sxs-lookup"><span data-stu-id="6b18a-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="6b18a-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="6b18a-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="6b18a-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="6b18a-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="6b18a-108">Свойство **Content** задает или получает содержимое для шифрования или расшифровки.</span><span class="sxs-lookup"><span data-stu-id="6b18a-108">The **Content** property sets or retrieves the content to be encrypted or decrypted.</span></span> <span data-ttu-id="6b18a-109">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b18a-109">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b18a-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b18a-110">Syntax</span></span>


```VB
EncryptedData.Content As String
```



## <a name="property-value"></a><span data-ttu-id="6b18a-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6b18a-111">Property value</span></span>

<span data-ttu-id="6b18a-112">Содержимое для шифрования или расшифровки.</span><span class="sxs-lookup"><span data-stu-id="6b18a-112">The content to be encrypted or decrypted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b18a-113">Требования</span><span class="sxs-lookup"><span data-stu-id="6b18a-113">Requirements</span></span>



| <span data-ttu-id="6b18a-114">Требование</span><span class="sxs-lookup"><span data-stu-id="6b18a-114">Requirement</span></span> | <span data-ttu-id="6b18a-115">Значение</span><span class="sxs-lookup"><span data-stu-id="6b18a-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b18a-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="6b18a-116">End of client support</span></span><br/> | <span data-ttu-id="6b18a-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6b18a-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6b18a-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="6b18a-118">End of server support</span></span><br/> | <span data-ttu-id="6b18a-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6b18a-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6b18a-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6b18a-120">Redistributable</span></span><br/>       | <span data-ttu-id="6b18a-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="6b18a-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6b18a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6b18a-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6b18a-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b18a-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b18a-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6b18a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b18a-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="6b18a-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
