---
description: Извлекает алгоритм для зашифрованных данных.
ms.assetid: 37bebe69-3c62-44c4-a5e5-c8cdbf087fa4
title: EncryptedData. algorithm, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cd73fbda4a5f77706ac2253782768e8487b8cbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648860"
---
# <a name="encrypteddataalgorithm-property"></a><span data-ttu-id="9a56e-103">EncryptedData. algorithm, свойство</span><span class="sxs-lookup"><span data-stu-id="9a56e-103">EncryptedData.Algorithm property</span></span>

<span data-ttu-id="9a56e-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9a56e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9a56e-105">Вместо этого используйте службы вызова платформы (PInvoke) для вызова функций API Win32 [**криптенкриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) и [**криптдекриптмессаже**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) для шифрования и расшифровки сообщений.</span><span class="sxs-lookup"><span data-stu-id="9a56e-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="9a56e-106">Дополнительные сведения о PInvoke см. в разделе [учебник по вызову неуправляемого](https://msdn.microsoft.com/library/aa288468.aspx)кода.</span><span class="sxs-lookup"><span data-stu-id="9a56e-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="9a56e-107">[.NET и CryptoAPI через p/Invoke: часть 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) и [.NET и CryptoAPI через p/Invoke: часть 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) подразделы [расширения шифрования .NET с помощью CAPICOM и P/Invoke](/previous-versions/ms867087(v=msdn.10)) также могут быть полезными.\]</span><span class="sxs-lookup"><span data-stu-id="9a56e-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="9a56e-108">Свойство **Algorithm** извлекает алгоритм для зашифрованных данных.</span><span class="sxs-lookup"><span data-stu-id="9a56e-108">The **Algorithm** property retrieves the algorithm for the encrypted data.</span></span>

<span data-ttu-id="9a56e-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9a56e-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a56e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9a56e-110">Syntax</span></span>


```VB
EncryptedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="9a56e-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9a56e-111">Property value</span></span>

<span data-ttu-id="9a56e-112">Объект [**алгоритма**](algorithm.md) , представляющий алгоритм шифрования.</span><span class="sxs-lookup"><span data-stu-id="9a56e-112">An [**Algorithm**](algorithm.md) object that represents the encryption algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a56e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9a56e-113">Requirements</span></span>



| <span data-ttu-id="9a56e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9a56e-114">Requirement</span></span> | <span data-ttu-id="9a56e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9a56e-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a56e-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="9a56e-116">End of client support</span></span><br/> | <span data-ttu-id="9a56e-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9a56e-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9a56e-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="9a56e-118">End of server support</span></span><br/> | <span data-ttu-id="9a56e-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9a56e-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9a56e-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9a56e-120">Redistributable</span></span><br/>       | <span data-ttu-id="9a56e-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9a56e-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9a56e-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9a56e-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9a56e-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a56e-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a56e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9a56e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a56e-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="9a56e-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
