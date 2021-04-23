---
description: Извлекает URI, указывающий на заявление о сертификации (CPS), опубликованное центром сертификации (ЦС).
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Свойство квалификатора. Кпспоинтер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648947"
---
# <a name="qualifiercpspointer-property"></a><span data-ttu-id="24404-103">Свойство квалификатора. Кпспоинтер</span><span class="sxs-lookup"><span data-stu-id="24404-103">Qualifier.CPSPointer property</span></span>

<span data-ttu-id="24404-104">\[Свойство **кпспоинтер** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="24404-104">\[The **CPSPointer** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="24404-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="24404-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="24404-106">Свойство **кпспоинтер** Извлекает URI, указывающий на заявление о сертификации (CPS), опубликованное центром сертификации (ЦС).</span><span class="sxs-lookup"><span data-stu-id="24404-106">The **CPSPointer** property retrieves the URI that points to a Certification Practice Statement (CPS) published by the certification authority (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="24404-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24404-107">Syntax</span></span>


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a><span data-ttu-id="24404-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="24404-108">Property value</span></span>

<span data-ttu-id="24404-109">Универсальный код ресурса (URI), указывающий на сервер публикаций Contribute, опубликованный центром сертификации.</span><span class="sxs-lookup"><span data-stu-id="24404-109">The URI that points to a CPS published by the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="24404-110">Требования</span><span class="sxs-lookup"><span data-stu-id="24404-110">Requirements</span></span>



| <span data-ttu-id="24404-111">Требование</span><span class="sxs-lookup"><span data-stu-id="24404-111">Requirement</span></span> | <span data-ttu-id="24404-112">Значение</span><span class="sxs-lookup"><span data-stu-id="24404-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="24404-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="24404-113">Redistributable</span></span><br/> | <span data-ttu-id="24404-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="24404-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="24404-115">DLL</span><span class="sxs-lookup"><span data-stu-id="24404-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="24404-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24404-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24404-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="24404-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24404-118">**Квалификатор**</span><span class="sxs-lookup"><span data-stu-id="24404-118">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
