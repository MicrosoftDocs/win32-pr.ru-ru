---
description: Извлекает шестнадцатеричную строку, содержащую хэш SHA-1 сертификата.
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Свойство Certificate. Thumbprint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c576c46ecf669d215c5bd20a80a0e5a65e3d4706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685150"
---
# <a name="certificatethumbprint-property"></a><span data-ttu-id="52754-103">Свойство Certificate. Thumbprint</span><span class="sxs-lookup"><span data-stu-id="52754-103">Certificate.Thumbprint property</span></span>

<span data-ttu-id="52754-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="52754-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="52754-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="52754-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="52754-106">Свойство **Thumbprint** извлекает шестнадцатеричную строку, содержащую хэш [*SHA-1*](../secgloss/s-gly.md) сертификата.</span><span class="sxs-lookup"><span data-stu-id="52754-106">The **Thumbprint** property retrieves a hexadecimal string that contains the [*SHA-1*](../secgloss/s-gly.md) hash of the certificate.</span></span>

<span data-ttu-id="52754-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="52754-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52754-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="52754-108">Syntax</span></span>


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a><span data-ttu-id="52754-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="52754-109">Property value</span></span>

<span data-ttu-id="52754-110">Шестнадцатеричная строка, содержащая хэш SHA-1 сертификата.</span><span class="sxs-lookup"><span data-stu-id="52754-110">A hexadecimal string that contains the SHA-1 hash of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="52754-111">Требования</span><span class="sxs-lookup"><span data-stu-id="52754-111">Requirements</span></span>



| <span data-ttu-id="52754-112">Требование</span><span class="sxs-lookup"><span data-stu-id="52754-112">Requirement</span></span> | <span data-ttu-id="52754-113">Значение</span><span class="sxs-lookup"><span data-stu-id="52754-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52754-114">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="52754-114">End of client support</span></span><br/> | <span data-ttu-id="52754-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="52754-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="52754-116">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="52754-116">End of server support</span></span><br/> | <span data-ttu-id="52754-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="52754-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="52754-118">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="52754-118">Redistributable</span></span><br/>       | <span data-ttu-id="52754-119">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="52754-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="52754-120">DLL</span><span class="sxs-lookup"><span data-stu-id="52754-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="52754-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52754-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52754-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52754-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52754-123">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="52754-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
