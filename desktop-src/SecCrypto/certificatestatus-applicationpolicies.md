---
description: Возвращает коллекцию OID, которая представляет политики приложения, используемые для создания объекта цепочки.
ms.assetid: dca0acbf-e369-4216-a4f6-44ed965011d0
title: Цертификатестатус. АппликатионполиЦиес, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.ApplicationPolicies
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b02503590a64c1c14e3f66dc5d07d9d61034bd60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685286"
---
# <a name="certificatestatusapplicationpolicies-method"></a><span data-ttu-id="cda0c-103">Цертификатестатус. АппликатионполиЦиес, метод</span><span class="sxs-lookup"><span data-stu-id="cda0c-103">CertificateStatus.ApplicationPolicies method</span></span>

<span data-ttu-id="cda0c-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cda0c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="cda0c-105">Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cda0c-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cda0c-106">Метод **аппликатионполиЦиес** Возвращает коллекцию [**OID**](oids.md) , которая представляет политики приложения, используемые для создания объекта [**цепочки**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="cda0c-106">The **ApplicationPolicies** method returns an [**OIDs**](oids.md) collection that represents the application policies used to create the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda0c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cda0c-107">Syntax</span></span>


```VB
CertificateStatus.ApplicationPolicies()
```



## <a name="parameters"></a><span data-ttu-id="cda0c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cda0c-108">Parameters</span></span>

<span data-ttu-id="cda0c-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="cda0c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cda0c-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cda0c-110">Return value</span></span>

<span data-ttu-id="cda0c-111">Коллекция [**OID**](oids.md) .</span><span class="sxs-lookup"><span data-stu-id="cda0c-111">An [**OIDs**](oids.md) collection.</span></span> <span data-ttu-id="cda0c-112">Каждый объект [**OID**](oid.md) в коллекции представляет OID политики приложения.</span><span class="sxs-lookup"><span data-stu-id="cda0c-112">Each [**OID**](oid.md) object in the collection represents an application policy OID.</span></span>

## <a name="remarks"></a><span data-ttu-id="cda0c-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cda0c-113">Remarks</span></span>

<span data-ttu-id="cda0c-114">Добавьте идентификаторы объектов политики приложений в коллекцию, чтобы указать политики приложений, которые должны использоваться для создания цепочки доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cda0c-114">Add application policy OIDs to the collection to specify the application policies that should be used to build the certificate trust chain.</span></span> <span data-ttu-id="cda0c-115">Если коллекция содержит по крайней мере один объект [**OID**](oid.md) , то объект [**EKU**](eku.md) , возвращенный методом [**цертификатестатус. EKU**](certificatestatus-eku.md) , игнорируется.</span><span class="sxs-lookup"><span data-stu-id="cda0c-115">If the collection contains at least one [**OID**](oid.md) object, the [**EKU**](eku.md) object returned by the [**CertificateStatus.EKU**](certificatestatus-eku.md) method is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="cda0c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="cda0c-116">Requirements</span></span>



| <span data-ttu-id="cda0c-117">Требование</span><span class="sxs-lookup"><span data-stu-id="cda0c-117">Requirement</span></span> | <span data-ttu-id="cda0c-118">Значение</span><span class="sxs-lookup"><span data-stu-id="cda0c-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cda0c-119">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cda0c-119">End of client support</span></span><br/> | <span data-ttu-id="cda0c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cda0c-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cda0c-121">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cda0c-121">End of server support</span></span><br/> | <span data-ttu-id="cda0c-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cda0c-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cda0c-123">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cda0c-123">Redistributable</span></span><br/>       | <span data-ttu-id="cda0c-124">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="cda0c-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cda0c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cda0c-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cda0c-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cda0c-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
