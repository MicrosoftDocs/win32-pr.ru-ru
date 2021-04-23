---
description: Возвращает объект Екстендедкэйусаже, указывающий допустимые варианты использования сертификата.
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: 'Метод ICertificate2:: Екстендедкэйусаже'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6f349b7267d58a9376b9295e3ffd5013954a0872
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668497"
---
# <a name="icertificate2extendedkeyusage-method"></a><span data-ttu-id="8903d-103">Метод ICertificate2:: Екстендедкэйусаже</span><span class="sxs-lookup"><span data-stu-id="8903d-103">ICertificate2::ExtendedKeyUsage method</span></span>

<span data-ttu-id="8903d-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="8903d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="8903d-105">Вместо этого используйте [**класс X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="8903d-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="8903d-106">Метод **екстендедкэйусаже** возвращает объект [**екстендедкэйусаже**](extendedkeyusage.md) , указывающий допустимые варианты использования сертификата.</span><span class="sxs-lookup"><span data-stu-id="8903d-106">The **ExtendedKeyUsage** method returns an [**ExtendedKeyUsage**](extendedkeyusage.md) object that indicates the valid uses of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="8903d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8903d-107">Syntax</span></span>


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="8903d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="8903d-108">Parameters</span></span>

<span data-ttu-id="8903d-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="8903d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8903d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8903d-110">Return value</span></span>

<span data-ttu-id="8903d-111">Объект [**екстендедкэйусаже**](extendedkeyusage.md) , связанный с сертификатом.</span><span class="sxs-lookup"><span data-stu-id="8903d-111">The [**ExtendedKeyUsage**](extendedkeyusage.md) object that is associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="8903d-112">Требования</span><span class="sxs-lookup"><span data-stu-id="8903d-112">Requirements</span></span>



| <span data-ttu-id="8903d-113">Требование</span><span class="sxs-lookup"><span data-stu-id="8903d-113">Requirement</span></span> | <span data-ttu-id="8903d-114">Значение</span><span class="sxs-lookup"><span data-stu-id="8903d-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8903d-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="8903d-115">End of client support</span></span><br/> | <span data-ttu-id="8903d-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8903d-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8903d-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="8903d-117">End of server support</span></span><br/> | <span data-ttu-id="8903d-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8903d-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8903d-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="8903d-119">Redistributable</span></span><br/>       | <span data-ttu-id="8903d-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="8903d-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8903d-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8903d-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8903d-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8903d-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8903d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8903d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8903d-124">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="8903d-124">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="8903d-125">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="8903d-125">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
