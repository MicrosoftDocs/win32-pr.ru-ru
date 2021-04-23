---
description: Возвращает объект EKU, используемый для построения объекта цепочки.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: Цертификатестатус. EKU, метод
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665172"
---
# <a name="certificatestatuseku-method"></a><span data-ttu-id="98467-103">Цертификатестатус. EKU, метод</span><span class="sxs-lookup"><span data-stu-id="98467-103">CertificateStatus.EKU method</span></span>

<span data-ttu-id="98467-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98467-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="98467-105">Вместо этого используйте [**структуру X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="98467-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="98467-106">Метод **EKU** возвращает объект [**EKU**](eku.md) , используемый для построения объекта [**цепочки**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="98467-106">The **EKU** method returns the [**EKU**](eku.md) object used to build the [**Chain**](chain.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="98467-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98467-107">Syntax</span></span>


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a><span data-ttu-id="98467-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="98467-108">Parameters</span></span>

<span data-ttu-id="98467-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="98467-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="98467-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="98467-110">Return value</span></span>

<span data-ttu-id="98467-111">Этот метод возвращает объект [**EKU**](eku.md) , который указывает на параметр расширенного использования ключа [*сертификата*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="98467-111">This method returns an [**EKU**](eku.md) object that indicates the extended key usage setting of the [*certificate*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="98467-112">Параметр EKU устанавливает допустимое использование сертификата.</span><span class="sxs-lookup"><span data-stu-id="98467-112">The EKU setting establishes a certificate's valid use.</span></span> <span data-ttu-id="98467-113">Для каждого сертификата можно задать только один объект **EKU** .</span><span class="sxs-lookup"><span data-stu-id="98467-113">Only a single **EKU** object can be set for each certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="98467-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98467-114">Remarks</span></span>

<span data-ttu-id="98467-115">Метод [**цертификатестатус. аппликатионполиЦиес**](certificatestatus-applicationpolicies.md) предоставляет те же функциональные возможности, что и этот метод, но позволяет задавать множество параметров вместо одного.</span><span class="sxs-lookup"><span data-stu-id="98467-115">The [**CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md) method provides the same functionality as this method but allows many settings to be specified instead of only one.</span></span> <span data-ttu-id="98467-116">Если коллекция [**OID**](oids.md) , возвращенная методом **аппликатионполиЦиес** , содержит один или несколько объектов [**OID**](oid.md) , то объект [**EKU**](eku.md) , возвращаемый этим методом, игнорируется.</span><span class="sxs-lookup"><span data-stu-id="98467-116">If the [**OIDs**](oids.md) collection returned by the **ApplicationPolicies** method contains one or more [**OID**](oid.md) objects, the [**EKU**](eku.md) object returned by this method is ignored.</span></span> <span data-ttu-id="98467-117">Вместо этого метода используйте метод **аппликатионполиЦиес** .</span><span class="sxs-lookup"><span data-stu-id="98467-117">Use the **ApplicationPolicies** method instead of this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="98467-118">Требования</span><span class="sxs-lookup"><span data-stu-id="98467-118">Requirements</span></span>



| <span data-ttu-id="98467-119">Требование</span><span class="sxs-lookup"><span data-stu-id="98467-119">Requirement</span></span> | <span data-ttu-id="98467-120">Значение</span><span class="sxs-lookup"><span data-stu-id="98467-120">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="98467-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="98467-121">End of client support</span></span><br/> | <span data-ttu-id="98467-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="98467-122">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="98467-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="98467-123">End of server support</span></span><br/> | <span data-ttu-id="98467-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="98467-124">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="98467-125">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="98467-125">Redistributable</span></span><br/>       | <span data-ttu-id="98467-126">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="98467-126">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="98467-127">DLL</span><span class="sxs-lookup"><span data-stu-id="98467-127">DLL</span></span><br/>                   | <dl> <span data-ttu-id="98467-128"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98467-128"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98467-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="98467-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98467-130">**цертификатестатус**</span><span class="sxs-lookup"><span data-stu-id="98467-130">**CertificateStatus**</span></span>](certificatestatus.md)
</dt> <dt>

[<span data-ttu-id="98467-131">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="98467-131">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="98467-132">**EKU**</span><span class="sxs-lookup"><span data-stu-id="98467-132">**EKU**</span></span>](eku.md)
</dt> </dl>

 

 
