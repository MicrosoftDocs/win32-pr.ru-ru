---
description: Возвращает строку, содержащую дополнительные сведения об ошибке индексированной записи.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: 'Метод IChain2:: Екстендедерроринфо'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688982"
---
# <a name="ichain2extendederrorinfo-method"></a><span data-ttu-id="e7caf-103">Метод IChain2:: Екстендедерроринфо</span><span class="sxs-lookup"><span data-stu-id="e7caf-103">IChain2::ExtendedErrorInfo method</span></span>

<span data-ttu-id="e7caf-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e7caf-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e7caf-105">Вместо этого используйте [**класс X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="e7caf-105">Instead, use the [**X509Chain Class**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e7caf-106">Метод **екстендедерроринфо** возвращает строку, которая содержит дополнительные сведения об ошибке индексированной записи.</span><span class="sxs-lookup"><span data-stu-id="e7caf-106">The **ExtendedErrorInfo** method returns a string that contains additional error information about the indexed entry.</span></span>

<span data-ttu-id="e7caf-107">Этот метод появился в CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="e7caf-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7caf-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7caf-108">Syntax</span></span>


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e7caf-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7caf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7caf-110">*Индекс* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="e7caf-110">*Index* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e7caf-111">Значение **типа Long** , представляющее индекс записи.</span><span class="sxs-lookup"><span data-stu-id="e7caf-111">A **Long** representing the index of the entry.</span></span> <span data-ttu-id="e7caf-112">Значение по умолчанию — 1, возвращающее сведения об ошибке для конечного сертификата в цепочке.</span><span class="sxs-lookup"><span data-stu-id="e7caf-112">The default value is 1, which returns error information for the end certificate in the chain.</span></span> <span data-ttu-id="e7caf-113">**Certificates. Count** возвращает сведения о корневом сертификате цепочки.</span><span class="sxs-lookup"><span data-stu-id="e7caf-113">**Certificates.Count** returns information about the root certificate of the chain.</span></span> <span data-ttu-id="e7caf-114">0 возвращает расширенные сведения об ошибке для всей цепочки.</span><span class="sxs-lookup"><span data-stu-id="e7caf-114">0 returns extended error information for the entire chain.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7caf-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e7caf-115">Return value</span></span>

<span data-ttu-id="e7caf-116">Строка, содержащая расширенные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="e7caf-116">A string that contains the extended error information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7caf-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e7caf-117">Requirements</span></span>



| <span data-ttu-id="e7caf-118">Требование</span><span class="sxs-lookup"><span data-stu-id="e7caf-118">Requirement</span></span> | <span data-ttu-id="e7caf-119">Значение</span><span class="sxs-lookup"><span data-stu-id="e7caf-119">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7caf-120">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e7caf-120">End of client support</span></span><br/> | <span data-ttu-id="e7caf-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e7caf-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e7caf-122">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e7caf-122">End of server support</span></span><br/> | <span data-ttu-id="e7caf-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e7caf-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e7caf-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e7caf-124">Redistributable</span></span><br/>       | <span data-ttu-id="e7caf-125">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e7caf-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e7caf-126">DLL</span><span class="sxs-lookup"><span data-stu-id="e7caf-126">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e7caf-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7caf-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7caf-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e7caf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7caf-129">**Цепочк**</span><span class="sxs-lookup"><span data-stu-id="e7caf-129">**Chain**</span></span>](chain.md)
</dt> </dl>

 

 
