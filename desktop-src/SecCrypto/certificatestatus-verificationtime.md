---
description: Задает или получает время проверки сертификата.
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: Цертификатестатус. Верификатионтиме, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685060"
---
# <a name="certificatestatusverificationtime-property"></a><span data-ttu-id="14d3c-103">Цертификатестатус. Верификатионтиме, свойство</span><span class="sxs-lookup"><span data-stu-id="14d3c-103">CertificateStatus.VerificationTime property</span></span>

<span data-ttu-id="14d3c-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="14d3c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="14d3c-105">Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="14d3c-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="14d3c-106">Свойство **верификатионтиме** задает или получает время проверки сертификата.</span><span class="sxs-lookup"><span data-stu-id="14d3c-106">The **VerificationTime** property sets or retrieves the time that the certificate was verified.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d3c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14d3c-107">Syntax</span></span>


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a><span data-ttu-id="14d3c-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="14d3c-108">Property value</span></span>

<span data-ttu-id="14d3c-109">Время проверки сертификата.</span><span class="sxs-lookup"><span data-stu-id="14d3c-109">The time that the certificate was verified.</span></span>

## <a name="remarks"></a><span data-ttu-id="14d3c-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14d3c-110">Remarks</span></span>

<span data-ttu-id="14d3c-111">Если это свойство не задано, используется текущее время.</span><span class="sxs-lookup"><span data-stu-id="14d3c-111">If this property is not set, the current time is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="14d3c-112">Требования</span><span class="sxs-lookup"><span data-stu-id="14d3c-112">Requirements</span></span>



| <span data-ttu-id="14d3c-113">Требование</span><span class="sxs-lookup"><span data-stu-id="14d3c-113">Requirement</span></span> | <span data-ttu-id="14d3c-114">Значение</span><span class="sxs-lookup"><span data-stu-id="14d3c-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14d3c-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="14d3c-115">End of client support</span></span><br/> | <span data-ttu-id="14d3c-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="14d3c-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="14d3c-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="14d3c-117">End of server support</span></span><br/> | <span data-ttu-id="14d3c-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="14d3c-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="14d3c-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="14d3c-119">Redistributable</span></span><br/>       | <span data-ttu-id="14d3c-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="14d3c-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="14d3c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="14d3c-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="14d3c-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14d3c-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
