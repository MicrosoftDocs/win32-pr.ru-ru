---
description: Возвращает коллекцию OID, представляющую политики сертификатов, используемые для создания объекта цепочки.
ms.assetid: 7fe7d3ea-28fc-4c0a-9b43-a97518ac65db
title: Цертификатестатус. ЦертификатеполиЦиес, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.CertificatePolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 98c9e22c0cad40252cc9eebebf9aa32dc4d89b65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665519"
---
# <a name="certificatestatuscertificatepolicies-method"></a><span data-ttu-id="635b5-103">Цертификатестатус. ЦертификатеполиЦиес, метод</span><span class="sxs-lookup"><span data-stu-id="635b5-103">CertificateStatus.CertificatePolicies method</span></span>

<span data-ttu-id="635b5-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="635b5-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="635b5-105">Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="635b5-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="635b5-106">Метод **цертификатеполиЦиес** Возвращает коллекцию [**OID**](oids.md) , представляющую политики сертификатов, используемые для создания объекта [**цепочки**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="635b5-106">The **CertificatePolicies** method returns an [**OIDs**](oids.md) collection that represents the certificate policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="635b5-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="635b5-107">Syntax</span></span>


```VB
CertificateStatus.CertificatePolicies()
```



## <a name="parameters"></a><span data-ttu-id="635b5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="635b5-108">Parameters</span></span>

<span data-ttu-id="635b5-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="635b5-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="635b5-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="635b5-110">Return value</span></span>

<span data-ttu-id="635b5-111">Коллекция [**OID**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="635b5-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="635b5-112">Каждый объект [**OID**](oid.md) в коллекции представляет OID политики сертификата.</span><span class="sxs-lookup"><span data-stu-id="635b5-112">Each [**OID**](oid.md) object in the collection represents a certificate policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="635b5-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="635b5-113">Remarks</span></span>

<span data-ttu-id="635b5-114">Добавьте в коллекцию идентификаторы объектов политики сертификатов, чтобы указать политики сертификатов, которые должны использоваться для создания цепочки доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="635b5-114">Add certificate policy OIDs to the collection to specify the certificate policies that should be used to build the certificate trust chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="635b5-115">Требования</span><span class="sxs-lookup"><span data-stu-id="635b5-115">Requirements</span></span>



| <span data-ttu-id="635b5-116">Требование</span><span class="sxs-lookup"><span data-stu-id="635b5-116">Requirement</span></span> | <span data-ttu-id="635b5-117">Значение</span><span class="sxs-lookup"><span data-stu-id="635b5-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="635b5-118">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="635b5-118">End of client support</span></span><br/> | <span data-ttu-id="635b5-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="635b5-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="635b5-120">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="635b5-120">End of server support</span></span><br/> | <span data-ttu-id="635b5-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="635b5-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="635b5-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="635b5-122">Redistributable</span></span><br/>       | <span data-ttu-id="635b5-123">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="635b5-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="635b5-124">DLL</span><span class="sxs-lookup"><span data-stu-id="635b5-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="635b5-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="635b5-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
