---
description: Представляет цепочку доверия сертификатов.
ms.assetid: 45ed686f-4a7f-4df9-8366-98b825c3c657
title: Объект цепочки
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5fa3432767ccfdb60a2e3bc0a50ddbbcf565e0aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685362"
---
# <a name="chain-object"></a><span data-ttu-id="1de6f-103">Объект цепочки</span><span class="sxs-lookup"><span data-stu-id="1de6f-103">Chain object</span></span>

<span data-ttu-id="1de6f-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1de6f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1de6f-105">Вместо этого используйте [**класс X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1de6f-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1de6f-106">Объект **цепочки** представляет цепочку доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="1de6f-106">The **Chain** object represents a certificate trust chain.</span></span>

<span data-ttu-id="1de6f-107">Этот объект предоставляет свойства и методы для создания цепочки доверия сертификатов для проверки действительности сертификатов.</span><span class="sxs-lookup"><span data-stu-id="1de6f-107">This object provides properties and methods to build a certificate trust chain to check the validity of certificates.</span></span> <span data-ttu-id="1de6f-108">Цепочка строится с использованием значения свойства [**цертификатестатус. чеккфлаг**](certificatestatus-checkflag.md) и параметров политики объекта [**цертификатестатус**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="1de6f-108">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property value and the policy settings of a [**CertificateStatus**](certificatestatus.md) object.</span></span>

<span data-ttu-id="1de6f-109">Объект **цепочки** предоставляет следующие интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="1de6f-109">The **Chain** object exposes the following interfaces:</span></span>

-   <span data-ttu-id="1de6f-110">**IChain2**: представлено в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="1de6f-110">**IChain2**: Introduced in CAPICOM 2.0.</span></span>
-   <span data-ttu-id="1de6f-111">**Ичаин**: представлено в CAPICOM 1,0.</span><span class="sxs-lookup"><span data-stu-id="1de6f-111">**IChain**: Introduced in CAPICOM 1.0.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="1de6f-112">Назначение</span><span class="sxs-lookup"><span data-stu-id="1de6f-112">When to use</span></span>

<span data-ttu-id="1de6f-113">Объект **цепочки** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="1de6f-113">The **Chain** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="1de6f-114">Создайте цепочку доверия сертификатов.</span><span class="sxs-lookup"><span data-stu-id="1de6f-114">Build a certificate trust chain.</span></span>
-   <span data-ttu-id="1de6f-115">Получите идентификаторы объектов для всех политик сертификатов и приложений, допустимых для цепочки.</span><span class="sxs-lookup"><span data-stu-id="1de6f-115">Obtain the OIDs of all the certificate and application policies valid for the chain.</span></span>
-   <span data-ttu-id="1de6f-116">Проверьте состояние сертификатов в цепочке.</span><span class="sxs-lookup"><span data-stu-id="1de6f-116">Verify the status of the certificates in the chain.</span></span>
-   <span data-ttu-id="1de6f-117">Получение расширенных сведений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="1de6f-117">Obtain extended error information.</span></span>
-   <span data-ttu-id="1de6f-118">Получение коллекции сертификатов в цепочке.</span><span class="sxs-lookup"><span data-stu-id="1de6f-118">Retrieve the collection of certificates in the chain.</span></span>

## <a name="members"></a><span data-ttu-id="1de6f-119">Элементы</span><span class="sxs-lookup"><span data-stu-id="1de6f-119">Members</span></span>

<span data-ttu-id="1de6f-120">Объект **цепочки** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1de6f-120">The **Chain** object has these types of members:</span></span>

-   [<span data-ttu-id="1de6f-121">Методы</span><span class="sxs-lookup"><span data-stu-id="1de6f-121">Methods</span></span>](#methods)
-   [<span data-ttu-id="1de6f-122">Свойства</span><span class="sxs-lookup"><span data-stu-id="1de6f-122">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1de6f-123">Методы</span><span class="sxs-lookup"><span data-stu-id="1de6f-123">Methods</span></span>

<span data-ttu-id="1de6f-124">Объект **цепочки** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="1de6f-124">The **Chain** object has these methods.</span></span>



| <span data-ttu-id="1de6f-125">Метод</span><span class="sxs-lookup"><span data-stu-id="1de6f-125">Method</span></span>                                                   | <span data-ttu-id="1de6f-126">Описание</span><span class="sxs-lookup"><span data-stu-id="1de6f-126">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|:---------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1de6f-127">**аппликатионполиЦиес**</span><span class="sxs-lookup"><span data-stu-id="1de6f-127">**ApplicationPolicies**</span></span>](chain-applicationpolicies.md) | <span data-ttu-id="1de6f-128">Возвращает коллекцию [**OID**](oids.md) , представляющую идентификатор объекта (OID) политики приложения, допустимый для цепочки.</span><span class="sxs-lookup"><span data-stu-id="1de6f-128">Returns an [**OIDs**](oids.md) collection that represents the application policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="1de6f-129">(Наследуется от **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="1de6f-129">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="1de6f-130">**Сборка**</span><span class="sxs-lookup"><span data-stu-id="1de6f-130">**Build**</span></span>](chain-build.md)                             | <span data-ttu-id="1de6f-131">Создает цепочку проверки сертификатов от конечного сертификата до доверенного [*корневого сертификата*](../secgloss/r-gly.md), возвращая логическое значение, которое указывает на общую достоверность цепочки.</span><span class="sxs-lookup"><span data-stu-id="1de6f-131">Builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md), returning a Boolean value that indicates the overall validity of the chain.</span></span><br/> <span data-ttu-id="1de6f-132">(Наследуется от **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="1de6f-132">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="1de6f-133">**цертификатеполиЦиес**</span><span class="sxs-lookup"><span data-stu-id="1de6f-133">**CertificatePolicies**</span></span>](chain-certificatepolicies.md) | <span data-ttu-id="1de6f-134">Возвращает коллекцию [**OID**](oids.md) , которая представляет идентификатор объекта политики сертификата, допустимый для цепочки.</span><span class="sxs-lookup"><span data-stu-id="1de6f-134">Returns an [**OIDs**](oids.md) collection that represents the certificate policy OIDs valid for the chain.</span></span><br/> <span data-ttu-id="1de6f-135">(Наследуется от **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="1de6f-135">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                          |
| [<span data-ttu-id="1de6f-136">**екстендедерроринфо**</span><span class="sxs-lookup"><span data-stu-id="1de6f-136">**ExtendedErrorInfo**</span></span>](chain-extendederrorinfo.md)     | <span data-ttu-id="1de6f-137">Возвращает строку, содержащую дополнительные сведения об ошибке индексированной записи.</span><span class="sxs-lookup"><span data-stu-id="1de6f-137">Returns a string that contains additional error information about the indexed entry.</span></span><br/> <span data-ttu-id="1de6f-138">(Наследуется от **ChainIChain2**)</span><span class="sxs-lookup"><span data-stu-id="1de6f-138">(Inherited from **ChainIChain2**)</span></span>                                                                                                                                                                                 |



 

### <a name="properties"></a><span data-ttu-id="1de6f-139">Свойства</span><span class="sxs-lookup"><span data-stu-id="1de6f-139">Properties</span></span>

<span data-ttu-id="1de6f-140">Объект **цепочки** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="1de6f-140">The **Chain** object has these properties.</span></span>



| <span data-ttu-id="1de6f-141">Свойство</span><span class="sxs-lookup"><span data-stu-id="1de6f-141">Property</span></span>                                              | <span data-ttu-id="1de6f-142">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="1de6f-142">Access type</span></span>          | <span data-ttu-id="1de6f-143">Описание</span><span class="sxs-lookup"><span data-stu-id="1de6f-143">Description</span></span>                                                                                                                                                                                 |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1de6f-144">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="1de6f-144">**Certificates**</span></span>](chain-certificates.md)<br/> | <span data-ttu-id="1de6f-145">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de6f-145">Read-only</span></span><br/> | <span data-ttu-id="1de6f-146">Извлекает коллекцию [**сертификатов**](certificates.md) , представляющую сертификаты в цепочке.</span><span class="sxs-lookup"><span data-stu-id="1de6f-146">Retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="1de6f-147">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1de6f-147">This is the default property.</span></span><br/> <span data-ttu-id="1de6f-148">(Наследуется от **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="1de6f-148">(Inherited from **ChainIChain2IChain**)</span></span> |
| [<span data-ttu-id="1de6f-149">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="1de6f-149">**Status**</span></span>](chain-status.md)<br/>             | <span data-ttu-id="1de6f-150">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="1de6f-150">Read-only</span></span><br/> | <span data-ttu-id="1de6f-151">Возвращает состояние допустимости цепочки или определенного сертификата в цепочке.</span><span class="sxs-lookup"><span data-stu-id="1de6f-151">Retrieves the validity status of the chain or a specific certificate in the chain.</span></span><br/> <span data-ttu-id="1de6f-152">(Наследуется от **ChainIChain2IChain**)</span><span class="sxs-lookup"><span data-stu-id="1de6f-152">(Inherited from **ChainIChain2IChain**)</span></span>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="1de6f-153">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1de6f-153">Remarks</span></span>

<span data-ttu-id="1de6f-154">Объект **цепочки** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="1de6f-154">The **Chain** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="1de6f-155">ProgID для объекта **цепочки** — CAPICOM. Chain. 2.</span><span class="sxs-lookup"><span data-stu-id="1de6f-155">The ProgID for the **Chain** object is "CAPICOM.Chain.2".</span></span>

<span data-ttu-id="1de6f-156">**CAPICOM 1. *x*:** идентификатор ProgID для объекта **цепочки** — CAPICOM. Chain. 1.</span><span class="sxs-lookup"><span data-stu-id="1de6f-156">**CAPICOM 1.*x*:** The ProgID for the **Chain** object is CAPICOM.Chain.1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de6f-157">Требования</span><span class="sxs-lookup"><span data-stu-id="1de6f-157">Requirements</span></span>



| <span data-ttu-id="1de6f-158">Требование</span><span class="sxs-lookup"><span data-stu-id="1de6f-158">Requirement</span></span> | <span data-ttu-id="1de6f-159">Значение</span><span class="sxs-lookup"><span data-stu-id="1de6f-159">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1de6f-160">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1de6f-160">End of client support</span></span><br/> | <span data-ttu-id="1de6f-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1de6f-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1de6f-162">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1de6f-162">End of server support</span></span><br/> | <span data-ttu-id="1de6f-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1de6f-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1de6f-164">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1de6f-164">Redistributable</span></span><br/>       | <span data-ttu-id="1de6f-165">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1de6f-165">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1de6f-166">DLL</span><span class="sxs-lookup"><span data-stu-id="1de6f-166">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1de6f-167"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1de6f-167"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1de6f-168">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1de6f-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1de6f-169">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="1de6f-169">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
