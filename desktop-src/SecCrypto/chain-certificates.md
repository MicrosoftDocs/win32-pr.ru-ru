---
description: Свойство Certificates извлекает коллекцию сертификатов, представляющую сертификаты в цепочке. Это свойство по умолчанию.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'Свойство IChain2:: Certificates'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665454"
---
# <a name="ichain2certificates-property"></a><span data-ttu-id="4a8f1-104">Свойство IChain2:: Certificates</span><span class="sxs-lookup"><span data-stu-id="4a8f1-104">IChain2::Certificates property</span></span>

<span data-ttu-id="4a8f1-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4a8f1-106">Вместо этого используйте [**класс X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4a8f1-106">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4a8f1-107">Свойство **Certificates** извлекает коллекцию [**сертификатов**](certificates.md) , представляющую сертификаты в цепочке.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-107">The **Certificates** property retrieves a [**Certificates**](certificates.md) collection that represents the certificates in the chain.</span></span> <span data-ttu-id="4a8f1-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-108">This is the default property.</span></span>

<span data-ttu-id="4a8f1-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a8f1-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4a8f1-110">Syntax</span></span>


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="4a8f1-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4a8f1-111">Property value</span></span>

<span data-ttu-id="4a8f1-112">Коллекция [**сертификатов**](certificates.md) , которая используется для получения сведений о каждом сертификате в цепочке.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-112">A [**Certificates**](certificates.md) collection that is used to retrieve information about each certificate in the chain.</span></span> <span data-ttu-id="4a8f1-113">Первый сертификат в возвращенной коллекции **Certificates. Item**(1) является конечным сертификатом цепочки.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-113">The first certificate in the returned collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="4a8f1-114">Последний сертификат в коллекции **Certificates. Item**(**Certificates. Count**) — это [*корневой сертификат*](../secgloss/r-gly.md) цепочки.</span><span class="sxs-lookup"><span data-stu-id="4a8f1-114">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a8f1-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4a8f1-115">Requirements</span></span>



| <span data-ttu-id="4a8f1-116">Требование</span><span class="sxs-lookup"><span data-stu-id="4a8f1-116">Requirement</span></span> | <span data-ttu-id="4a8f1-117">Значение</span><span class="sxs-lookup"><span data-stu-id="4a8f1-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a8f1-118">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="4a8f1-118">End of client support</span></span><br/> | <span data-ttu-id="4a8f1-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4a8f1-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4a8f1-120">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="4a8f1-120">End of server support</span></span><br/> | <span data-ttu-id="4a8f1-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4a8f1-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4a8f1-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4a8f1-122">Redistributable</span></span><br/>       | <span data-ttu-id="4a8f1-123">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="4a8f1-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4a8f1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="4a8f1-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4a8f1-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a8f1-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
