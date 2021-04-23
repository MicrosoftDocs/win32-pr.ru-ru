---
description: Задает или получает продолжительность времени до того, как URL-адрес будет определен как недоступный.
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: Цертификатестатус. Урлретриевалтимеаут, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fcaaafa1f2e870195b612eb225696f2c23a80ee1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685063"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a><span data-ttu-id="76bb6-103">Цертификатестатус. Урлретриевалтимеаут, свойство</span><span class="sxs-lookup"><span data-stu-id="76bb6-103">CertificateStatus.UrlRetrievalTimeout property</span></span>

<span data-ttu-id="76bb6-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76bb6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="76bb6-105">Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="76bb6-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="76bb6-106">Свойство **урлретриевалтимеаут** задает или получает продолжительность времени до того, как URL-адрес будет определен как недоступный.</span><span class="sxs-lookup"><span data-stu-id="76bb6-106">The **UrlRetrievalTimeout** property sets or retrieves the length of time before a URL is determined to be unreachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="76bb6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76bb6-107">Syntax</span></span>


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a><span data-ttu-id="76bb6-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="76bb6-108">Property value</span></span>

<span data-ttu-id="76bb6-109">Число секунд, по истечении которого URL-адрес будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="76bb6-109">The number of seconds before a URL is determined to be unreachable.</span></span>

## <a name="remarks"></a><span data-ttu-id="76bb6-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76bb6-110">Remarks</span></span>

<span data-ttu-id="76bb6-111">Если это свойство не задано, время ожидания по умолчанию — 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="76bb6-111">If this property is not set, the default time-out is 15 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="76bb6-112">Требования</span><span class="sxs-lookup"><span data-stu-id="76bb6-112">Requirements</span></span>



| <span data-ttu-id="76bb6-113">Требование</span><span class="sxs-lookup"><span data-stu-id="76bb6-113">Requirement</span></span> | <span data-ttu-id="76bb6-114">Значение</span><span class="sxs-lookup"><span data-stu-id="76bb6-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76bb6-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="76bb6-115">End of client support</span></span><br/> | <span data-ttu-id="76bb6-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76bb6-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="76bb6-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="76bb6-117">End of server support</span></span><br/> | <span data-ttu-id="76bb6-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76bb6-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="76bb6-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="76bb6-119">Redistributable</span></span><br/>       | <span data-ttu-id="76bb6-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="76bb6-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="76bb6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="76bb6-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="76bb6-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76bb6-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
