---
description: Возвращает объект Кэйусаже, указывающий допустимое использование ключа сертификата.
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: 'Метод ICertificate2:: Кэйусаже'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85fe008880d9613586d38dba7afaca39bb29f72f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669334"
---
# <a name="icertificate2keyusage-method"></a><span data-ttu-id="763e2-103">Метод ICertificate2:: Кэйусаже</span><span class="sxs-lookup"><span data-stu-id="763e2-103">ICertificate2::KeyUsage method</span></span>

<span data-ttu-id="763e2-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="763e2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="763e2-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="763e2-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="763e2-106">Метод **кэйусаже** возвращает объект [**кэйусаже**](keyusage.md) , указывающий допустимое использование ключа сертификата.</span><span class="sxs-lookup"><span data-stu-id="763e2-106">The **KeyUsage** method returns a [**KeyUsage**](keyusage.md) object that indicates the valid key usage of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="763e2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="763e2-107">Syntax</span></span>


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="763e2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="763e2-108">Parameters</span></span>

<span data-ttu-id="763e2-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="763e2-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="763e2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="763e2-110">Requirements</span></span>



| <span data-ttu-id="763e2-111">Требование</span><span class="sxs-lookup"><span data-stu-id="763e2-111">Requirement</span></span> | <span data-ttu-id="763e2-112">Значение</span><span class="sxs-lookup"><span data-stu-id="763e2-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="763e2-113">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="763e2-113">End of client support</span></span><br/> | <span data-ttu-id="763e2-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="763e2-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="763e2-115">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="763e2-115">End of server support</span></span><br/> | <span data-ttu-id="763e2-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="763e2-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="763e2-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="763e2-117">Redistributable</span></span><br/>       | <span data-ttu-id="763e2-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="763e2-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="763e2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="763e2-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="763e2-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="763e2-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="763e2-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="763e2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="763e2-122">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="763e2-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="763e2-123">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="763e2-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
