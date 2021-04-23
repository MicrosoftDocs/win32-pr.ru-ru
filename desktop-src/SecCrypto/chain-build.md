---
description: Создает цепочку проверки сертификатов от конечного сертификата до доверенного корневого сертификата и возвращает логическое значение, указывающее общую достоверность цепочки.
ms.assetid: 878f09ba-d79b-4f14-b4f6-ecb54771f56f
title: 'Метод IChain2:: Build'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.Build
- IChain2.Build
- IChain.Build
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 66ad51d94fdbd361a34e25b4b76289139abb87f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665038"
---
# <a name="ichain2build-method"></a><span data-ttu-id="1106f-103">Метод IChain2:: Build</span><span class="sxs-lookup"><span data-stu-id="1106f-103">IChain2::Build method</span></span>

<span data-ttu-id="1106f-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="1106f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1106f-105">Вместо этого используйте [**класс X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="1106f-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1106f-106">Метод **Build** создает цепочку проверки сертификатов от конечного сертификата до доверенного [*корневого сертификата*](../secgloss/r-gly.md) и возвращает логическое значение, указывающее на общую достоверность цепочки.</span><span class="sxs-lookup"><span data-stu-id="1106f-106">The **Build** method builds a certificate verification chain from an end certificate to the trusted [*root certificate*](../secgloss/r-gly.md) and returns a Boolean value that indicates the overall validity of the chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="1106f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1106f-107">Syntax</span></span>


```VB
Chain.Build( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="1106f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="1106f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1106f-109">*Сертификат* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1106f-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1106f-110">Объект [**сертификата**](certificate.md) , представляющий конечный сертификат, на основе которого будет построена цепочка проверки.</span><span class="sxs-lookup"><span data-stu-id="1106f-110">A [**Certificate**](certificate.md) object that represents the end certificate upon which the verification chain is to be built.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1106f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1106f-111">Return value</span></span>

<span data-ttu-id="1106f-112">Логическое значение, указывающее общую достоверность цепочки.</span><span class="sxs-lookup"><span data-stu-id="1106f-112">A Boolean value that indicates the overall validity of the chain.</span></span> <span data-ttu-id="1106f-113">Общая достоверность основывается на политике проверки достоверности.</span><span class="sxs-lookup"><span data-stu-id="1106f-113">Overall validity is based on the validity checking policy in place.</span></span>

## <a name="remarks"></a><span data-ttu-id="1106f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1106f-114">Remarks</span></span>

<span data-ttu-id="1106f-115">Цепочка создается с помощью свойства [**цертификатестатус. чеккфлаг**](certificatestatus-checkflag.md) , а также политик приложений и сертификатов, заданных объектом [**цертификатестатус**](certificatestatus.md) .</span><span class="sxs-lookup"><span data-stu-id="1106f-115">The chain is built using the [**CertificateStatus.CheckFlag**](certificatestatus-checkflag.md) property as well as application and certificate policies specified by a [**CertificateStatus**](certificatestatus.md) object.</span></span> <span data-ttu-id="1106f-116">Возвращенная коллекция упорядочена; Первый сертификат в коллекции **Certificates. Item**(1) является конечным сертификатом цепочки.</span><span class="sxs-lookup"><span data-stu-id="1106f-116">The returned collection is ordered; the first certificate in the collection, **Certificates.Item**(1), is the end certificate of the chain.</span></span> <span data-ttu-id="1106f-117">Последний сертификат в коллекции **Certificates. Item**(**Certificates. Count**) — это [*корневой сертификат*](../secgloss/r-gly.md) цепочки.</span><span class="sxs-lookup"><span data-stu-id="1106f-117">The last certificate in the collection, **Certificates.Item**(**Certificates.Count**), is the [*root certificate*](../secgloss/r-gly.md) of the chain.</span></span> <span data-ttu-id="1106f-118">**Certificates. Item**(0) представляет всю цепочку.</span><span class="sxs-lookup"><span data-stu-id="1106f-118">**Certificates.Item**(0) represents the entire chain.</span></span>

<span data-ttu-id="1106f-119">При каждом вызове метода **Chain. Build** [*состояние*](../secgloss/s-gly.md) объекта [**цепочки**](chain.md) сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="1106f-119">Each time the **Chain.Build** method is called, the [*state*](../secgloss/s-gly.md) of the [**Chain**](chain.md) object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="1106f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1106f-120">Requirements</span></span>



| <span data-ttu-id="1106f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1106f-121">Requirement</span></span> | <span data-ttu-id="1106f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1106f-122">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1106f-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="1106f-123">End of client support</span></span><br/> | <span data-ttu-id="1106f-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1106f-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1106f-125">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="1106f-125">End of server support</span></span><br/> | <span data-ttu-id="1106f-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1106f-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1106f-127">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="1106f-127">Redistributable</span></span><br/>       | <span data-ttu-id="1106f-128">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="1106f-128">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1106f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1106f-129">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1106f-130"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1106f-130"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1106f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1106f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1106f-132">**Криптографические объекты**</span><span class="sxs-lookup"><span data-stu-id="1106f-132">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="1106f-133">**Цепочк**</span><span class="sxs-lookup"><span data-stu-id="1106f-133">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
