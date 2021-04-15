---
description: Извлекает спецификацию ключа.
ms.assetid: 93c909cb-b1d1-4c2b-a66c-9d3f6dd9b340
title: PrivateKey. KeySpec, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.KeySpec
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f9d0ba55ca48d5257a038845f84374544b7615b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668973"
---
# <a name="privatekeykeyspec-property"></a><span data-ttu-id="4c3cd-103">PrivateKey. KeySpec, свойство</span><span class="sxs-lookup"><span data-stu-id="4c3cd-103">PrivateKey.KeySpec property</span></span>

<span data-ttu-id="4c3cd-104">\[Свойство **keySpec** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-104">\[The **KeySpec** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4c3cd-105">Вместо этого используйте [**свойство X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4c3cd-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4c3cd-106">Свойство **keySpec** извлекает спецификацию ключа.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-106">The **KeySpec** property retrieves the key specification.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c3cd-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c3cd-107">Syntax</span></span>


```VB
PrivateKey.KeySpec As CAPICOM_KEY_SPEC
```



## <a name="property-value"></a><span data-ttu-id="4c3cd-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4c3cd-108">Property value</span></span>

<span data-ttu-id="4c3cd-109">Значение перечисления " [**CAPICOM \_ \_ Spec**](capicom-key-spec.md) ", которое указывает спецификацию ключа.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-109">A value of the [**CAPICOM\_KEY\_SPEC**](capicom-key-spec.md) enumeration that indicates the key specification.</span></span> <span data-ttu-id="4c3cd-110">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-110">The following table shows the possible values.</span></span>



| <span data-ttu-id="4c3cd-111">Значение</span><span class="sxs-lookup"><span data-stu-id="4c3cd-111">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="4c3cd-112">Значение</span><span class="sxs-lookup"><span data-stu-id="4c3cd-112">Meaning</span></span>                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="CAPICOM_KEY_SPEC_KEYEXCHANGE"></span><span id="capicom_key_spec_keyexchange"></span><dl> <span data-ttu-id="4c3cd-113"><dt>**\_ \_ КЭЙЕКСЧАНЖЕ спецификация CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4c3cd-113"><dt>**CAPICOM\_KEY\_SPEC\_KEYEXCHANGE**</dt></span></span> </dl> | <span data-ttu-id="4c3cd-114">Ключ можно использовать для шифрования и подписывания.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-114">The key can be used for encryption and signing.</span></span><br/> |
| <span id="CAPICOM_KEY_SPEC_SIGNATURE"></span><span id="capicom_key_spec_signature"></span><dl> <span data-ttu-id="4c3cd-115"><dt>**\_ \_ подпись спецификации CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4c3cd-115"><dt>**CAPICOM\_KEY\_SPEC\_SIGNATURE**</dt></span></span> </dl>       | <span data-ttu-id="4c3cd-116">Ключ можно использовать только для подписывания.</span><span class="sxs-lookup"><span data-stu-id="4c3cd-116">The key can be used only for signing.</span></span><br/>           |



 

## <a name="requirements"></a><span data-ttu-id="4c3cd-117">Требования</span><span class="sxs-lookup"><span data-stu-id="4c3cd-117">Requirements</span></span>



| <span data-ttu-id="4c3cd-118">Требование</span><span class="sxs-lookup"><span data-stu-id="4c3cd-118">Requirement</span></span> | <span data-ttu-id="4c3cd-119">Значение</span><span class="sxs-lookup"><span data-stu-id="4c3cd-119">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c3cd-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="4c3cd-120">Redistributable</span></span><br/> | <span data-ttu-id="4c3cd-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="4c3cd-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4c3cd-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4c3cd-122">DLL</span></span><br/>             | <dl> <span data-ttu-id="4c3cd-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c3cd-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c3cd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c3cd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c3cd-125">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="4c3cd-125">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
