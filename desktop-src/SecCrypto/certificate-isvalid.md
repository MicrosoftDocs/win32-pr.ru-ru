---
description: Создает цепочку проверки сертификатов для сертификата и возвращает объект Цертификатестатус, который содержит состояние действия сертификата.
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: 'Метод ICertificate2:: IsValid'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39fec7c1bd2b369ee512834ed1b58b59871d8ae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665225"
---
# <a name="icertificate2isvalid-method"></a><span data-ttu-id="49386-103">Метод ICertificate2:: IsValid</span><span class="sxs-lookup"><span data-stu-id="49386-103">ICertificate2::IsValid method</span></span>

<span data-ttu-id="49386-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="49386-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="49386-105">Вместо этого используйте [**класс X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="49386-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="49386-106">Метод **IsValid** создает цепочку проверки сертификата для сертификата и возвращает объект [**цертификатестатус**](certificatestatus.md) , который содержит состояние действия сертификата.</span><span class="sxs-lookup"><span data-stu-id="49386-106">The **IsValid** method builds a certificate verification chain for a certificate and returns a [**CertificateStatus**](certificatestatus.md) object that contains the validity status of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="49386-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="49386-107">Syntax</span></span>


```VB
Certificate.IsValid()
```



## <a name="parameters"></a><span data-ttu-id="49386-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="49386-108">Parameters</span></span>

<span data-ttu-id="49386-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="49386-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="49386-110">Требования</span><span class="sxs-lookup"><span data-stu-id="49386-110">Requirements</span></span>



| <span data-ttu-id="49386-111">Требование</span><span class="sxs-lookup"><span data-stu-id="49386-111">Requirement</span></span> | <span data-ttu-id="49386-112">Значение</span><span class="sxs-lookup"><span data-stu-id="49386-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49386-113">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="49386-113">End of client support</span></span><br/> | <span data-ttu-id="49386-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49386-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="49386-115">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="49386-115">End of server support</span></span><br/> | <span data-ttu-id="49386-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49386-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="49386-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="49386-117">Redistributable</span></span><br/>       | <span data-ttu-id="49386-118">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="49386-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="49386-119">DLL</span><span class="sxs-lookup"><span data-stu-id="49386-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="49386-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49386-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49386-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49386-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49386-122">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="49386-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="49386-123">**Certificate**</span><span class="sxs-lookup"><span data-stu-id="49386-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
