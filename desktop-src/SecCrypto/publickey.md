---
description: Объект PublicKey представляет открытый ключ в объекте сертификата.
title: Объект PublicKey
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 12ab8fcf61d30b47fc809fb05e1ffa524bb2488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649099"
---
# <a name="publickey-object"></a><span data-ttu-id="3cee6-103">Объект PublicKey</span><span class="sxs-lookup"><span data-stu-id="3cee6-103">PublicKey object</span></span>

<span data-ttu-id="3cee6-104">\[Объект **PublicKey** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="3cee6-104">\[The **PublicKey** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3cee6-105">Вместо этого используйте [**свойство X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3cee6-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3cee6-106">Объект **PublicKey** представляет открытый ключ в объекте [**сертификата**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="3cee6-106">The **PublicKey** object represents a public key in a [**Certificate**](certificate.md) object.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="3cee6-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="3cee6-107">When to use</span></span>

<span data-ttu-id="3cee6-108">Объект **PublicKey** используется для получения данных об открытом ключе.</span><span class="sxs-lookup"><span data-stu-id="3cee6-108">The **PublicKey** object is used to retrieve data about the public key.</span></span>

## <a name="members"></a><span data-ttu-id="3cee6-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="3cee6-109">Members</span></span>

<span data-ttu-id="3cee6-110">Объект **PublicKey** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="3cee6-110">The **PublicKey** object has these types of members:</span></span>

-   [<span data-ttu-id="3cee6-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="3cee6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cee6-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="3cee6-112">Properties</span></span>

<span data-ttu-id="3cee6-113">Объект **PublicKey** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="3cee6-113">The **PublicKey** object has these properties.</span></span>



| <span data-ttu-id="3cee6-114">Свойство</span><span class="sxs-lookup"><span data-stu-id="3cee6-114">Property</span></span>                                                            | <span data-ttu-id="3cee6-115">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="3cee6-115">Access type</span></span>          | <span data-ttu-id="3cee6-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3cee6-116">Description</span></span>                                                                                                                            |
|:--------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3cee6-117">**Алгоритм**</span><span class="sxs-lookup"><span data-stu-id="3cee6-117">**Algorithm**</span></span>](publickey-algorithm.md)<br/>                 | <span data-ttu-id="3cee6-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cee6-118">Read-only</span></span><br/> | <span data-ttu-id="3cee6-119">Извлекает объект [**OID**](oid.md) , определяющий алгоритм, используемый открытым ключом.</span><span class="sxs-lookup"><span data-stu-id="3cee6-119">Retrieves the [**OID**](oid.md) object that identifies the algorithm used by the public key.</span></span> <span data-ttu-id="3cee6-120">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3cee6-120">This is the default property.</span></span><br/> |
| [<span data-ttu-id="3cee6-121">**енкодедкэй**</span><span class="sxs-lookup"><span data-stu-id="3cee6-121">**EncodedKey**</span></span>](publickey-encodedkey.md)<br/>               | <span data-ttu-id="3cee6-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cee6-122">Read-only</span></span><br/> | <span data-ttu-id="3cee6-123">Извлекает объект [**енкодеддата**](encodeddata.md) , который предоставляет доступ к значению открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="3cee6-123">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span><br/>                 |
| [<span data-ttu-id="3cee6-124">**енкодедпараметерс**</span><span class="sxs-lookup"><span data-stu-id="3cee6-124">**EncodedParameters**</span></span>](publickey-encodedparameters.md)<br/> | <span data-ttu-id="3cee6-125">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cee6-125">Read-only</span></span><br/> | <span data-ttu-id="3cee6-126">Извлекает объект [**енкодеддата**](encodeddata.md) , предоставляющий доступ к параметрам алгоритма открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="3cee6-126">Retrieves an [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span><br/>  |
| [<span data-ttu-id="3cee6-127">**Длина**</span><span class="sxs-lookup"><span data-stu-id="3cee6-127">**Length**</span></span>](publickey-length.md)<br/>                       | <span data-ttu-id="3cee6-128">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="3cee6-128">Read-only</span></span><br/> | <span data-ttu-id="3cee6-129">Возвращает длину открытого ключа в битах.</span><span class="sxs-lookup"><span data-stu-id="3cee6-129">Retrieves the length of the public key in bits.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="3cee6-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3cee6-130">Remarks</span></span>

<span data-ttu-id="3cee6-131">Не удается создать объект **PublicKey** .</span><span class="sxs-lookup"><span data-stu-id="3cee6-131">The **PublicKey** object cannot be created.</span></span>

<span data-ttu-id="3cee6-132">Объект **PublicKey** используется методом [**Certificate. publickey**](certificate-publickey.md) .</span><span class="sxs-lookup"><span data-stu-id="3cee6-132">The **PublicKey** object is used by the [**Certificate.PublicKey**](certificate-publickey.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cee6-133">Требования</span><span class="sxs-lookup"><span data-stu-id="3cee6-133">Requirements</span></span>



| <span data-ttu-id="3cee6-134">Требование</span><span class="sxs-lookup"><span data-stu-id="3cee6-134">Requirement</span></span> | <span data-ttu-id="3cee6-135">Значение</span><span class="sxs-lookup"><span data-stu-id="3cee6-135">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cee6-136">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="3cee6-136">Redistributable</span></span><br/> | <span data-ttu-id="3cee6-137">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="3cee6-137">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3cee6-138">DLL</span><span class="sxs-lookup"><span data-stu-id="3cee6-138">DLL</span></span><br/>             | <dl> <span data-ttu-id="3cee6-139"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cee6-139"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
