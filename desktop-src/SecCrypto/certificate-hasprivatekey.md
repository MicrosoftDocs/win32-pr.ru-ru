---
description: Определяет, связан ли сертификат с закрытым ключом. Метод определяет это путем проверки наличия \_ \_ \_ свойства ID Prov сведений для ключа \_ сертификата \_ .
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: 'Метод ICertificate2:: HasPrivateKey'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665188"
---
# <a name="icertificate2hasprivatekey-method"></a><span data-ttu-id="1211f-104">Метод ICertificate2:: HasPrivateKey</span><span class="sxs-lookup"><span data-stu-id="1211f-104">ICertificate2::HasPrivateKey method</span></span>

<span data-ttu-id="1211f-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1211f-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1211f-106">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1211f-106">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1211f-107">Метод **HasPrivateKey** определяет, связан ли [*сертификат*](../secgloss/c-gly.md) с [*закрытым ключом*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="1211f-107">The **HasPrivateKey** method determines whether the [*certificate*](../secgloss/c-gly.md) has a [*private key*](../secgloss/p-gly.md) associated with it.</span></span> <span data-ttu-id="1211f-108">Метод определяет это путем проверки наличия \_ \_ \_ свойства ID Prov сведений для ключа \_ сертификата \_ .</span><span class="sxs-lookup"><span data-stu-id="1211f-108">The method determines this by checking whether the CERT\_KEY\_PROV\_INFO\_PROP\_ID property is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="1211f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1211f-109">Syntax</span></span>


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a><span data-ttu-id="1211f-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="1211f-110">Parameters</span></span>

<span data-ttu-id="1211f-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="1211f-111">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="1211f-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1211f-112">Requirements</span></span>



| <span data-ttu-id="1211f-113">Требование</span><span class="sxs-lookup"><span data-stu-id="1211f-113">Requirement</span></span> | <span data-ttu-id="1211f-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1211f-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1211f-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1211f-115">End of client support</span></span><br/> | <span data-ttu-id="1211f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1211f-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1211f-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1211f-117">End of server support</span></span><br/> | <span data-ttu-id="1211f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1211f-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1211f-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1211f-119">Redistributable</span></span><br/>       | <span data-ttu-id="1211f-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1211f-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1211f-121">DLL</span><span class="sxs-lookup"><span data-stu-id="1211f-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1211f-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1211f-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1211f-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1211f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1211f-124">**PrivateKey. Open**</span><span class="sxs-lookup"><span data-stu-id="1211f-124">**PrivateKey.Open**</span></span>](privatekey-open.md)
</dt> <dt>

[<span data-ttu-id="1211f-125">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="1211f-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="1211f-126">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="1211f-126">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
