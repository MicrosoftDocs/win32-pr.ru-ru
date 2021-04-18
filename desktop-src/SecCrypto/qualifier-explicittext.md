---
description: Извлекает содержимое уведомления пользователя.
ms.assetid: dcf73357-253d-4160-be4e-f826296f5eaa
title: Свойство квалификатора. ЕксплиЦиттекст
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.ExplicitText
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d2ba5e6bbf6bb46e28c5dbb6fa9754c72b66dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685388"
---
# <a name="qualifierexplicittext-property"></a><span data-ttu-id="f2206-103">Свойство квалификатора. ЕксплиЦиттекст</span><span class="sxs-lookup"><span data-stu-id="f2206-103">Qualifier.ExplicitText property</span></span>

<span data-ttu-id="f2206-104">\[Свойство **експлиЦиттекст** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f2206-104">\[The **ExplicitText** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f2206-105">Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]</span><span class="sxs-lookup"><span data-stu-id="f2206-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="f2206-106">Свойство **експлиЦиттекст** извлекает содержимое уведомления пользователя.</span><span class="sxs-lookup"><span data-stu-id="f2206-106">The **ExplicitText** property retrieves the content of the user notice.</span></span> <span data-ttu-id="f2206-107">Это свойство может быть пустым.</span><span class="sxs-lookup"><span data-stu-id="f2206-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2206-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2206-108">Syntax</span></span>


```VB
Qualifier.ExplicitText As String
```



## <a name="property-value"></a><span data-ttu-id="f2206-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2206-109">Property value</span></span>

<span data-ttu-id="f2206-110">Содержимое уведомления пользователя.</span><span class="sxs-lookup"><span data-stu-id="f2206-110">The content of the user notice.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2206-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f2206-111">Requirements</span></span>



| <span data-ttu-id="f2206-112">Требование</span><span class="sxs-lookup"><span data-stu-id="f2206-112">Requirement</span></span> | <span data-ttu-id="f2206-113">Значение</span><span class="sxs-lookup"><span data-stu-id="f2206-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2206-114">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f2206-114">Redistributable</span></span><br/> | <span data-ttu-id="f2206-115">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="f2206-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f2206-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f2206-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="f2206-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2206-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f2206-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f2206-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2206-119">**Квалификатор**</span><span class="sxs-lookup"><span data-stu-id="f2206-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
