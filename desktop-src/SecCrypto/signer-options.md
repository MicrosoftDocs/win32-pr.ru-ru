---
description: Задает или получает параметр сертификата подписывания.
ms.assetid: 2362b9d4-d4d8-46fb-8791-7e856827fb31
title: Свойство SignIn. Options
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Options
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c22cf7b9d9ebe7e98e534d62b0a2771391c6cacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668904"
---
# <a name="signeroptions-property"></a><span data-ttu-id="dbe81-103">Свойство SignIn. Options</span><span class="sxs-lookup"><span data-stu-id="dbe81-103">Signer.Options property</span></span>

<span data-ttu-id="dbe81-104">\[Свойство **Options** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="dbe81-104">\[The **Options** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="dbe81-105">Вместо этого используйте [**класс кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="dbe81-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="dbe81-106">Свойство **Options** задает или получает параметр сертификата подписывания.</span><span class="sxs-lookup"><span data-stu-id="dbe81-106">The **Options** property sets or retrieves the signer's certificate option.</span></span>

<span data-ttu-id="dbe81-107">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="dbe81-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbe81-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dbe81-108">Syntax</span></span>


```VB
Signer.Options As CAPICOM_CERTIFICATE_INCLUDE_OPTION
```



## <a name="property-value"></a><span data-ttu-id="dbe81-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dbe81-109">Property value</span></span>

<span data-ttu-id="dbe81-110">Значение элемента [**CAPICOM \_ Certificate \_ включает \_**](capicom-certificate-include-option.md) перечисление параметров, которое указывает параметр сертификата подписывания.</span><span class="sxs-lookup"><span data-stu-id="dbe81-110">A value of the [**CAPICOM\_CERTIFICATE\_INCLUDE\_OPTION**](capicom-certificate-include-option.md) enumeration that specifies the signer's certificate option.</span></span> <span data-ttu-id="dbe81-111">Значение по умолчанию — \_ это \_ цепочка include-сертификатов, \_ \_ кроме \_ root.</span><span class="sxs-lookup"><span data-stu-id="dbe81-111">The default value is CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT.</span></span> <span data-ttu-id="dbe81-112">В следующей таблице приводятся возможные значения.</span><span class="sxs-lookup"><span data-stu-id="dbe81-112">The following table shows the possible values.</span></span>



| <span data-ttu-id="dbe81-113">Значение</span><span class="sxs-lookup"><span data-stu-id="dbe81-113">Value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="dbe81-114">Значение</span><span class="sxs-lookup"><span data-stu-id="dbe81-114">Meaning</span></span>                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <span data-ttu-id="dbe81-115"><dt>**CAPICOM \_ Certificate \_ включает \_ цепочку, \_ кроме \_ root**</dt></span><span class="sxs-lookup"><span data-stu-id="dbe81-115"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_CHAIN\_EXCEPT\_ROOT**</dt></span></span> </dl> | <span data-ttu-id="dbe81-116">Сохраняет все сертификаты в цепочке, за исключением корневой сущности.</span><span class="sxs-lookup"><span data-stu-id="dbe81-116">Saves all certificates in the chain with the exception of the root entity.</span></span><br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <span data-ttu-id="dbe81-117"><dt>**CAPICOM \_ Certificate \_ включает \_ всю \_ цепочку**</dt></span><span class="sxs-lookup"><span data-stu-id="dbe81-117"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_WHOLE\_CHAIN**</dt></span></span> </dl>                    | <span data-ttu-id="dbe81-118">Сохраняет всю цепочку сертификатов.</span><span class="sxs-lookup"><span data-stu-id="dbe81-118">Saves the complete certificate chain.</span></span><br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <span data-ttu-id="dbe81-119"><dt>**CAPICOM \_ Certificate \_ — \_ только конечная \_ сущность \_**</dt></span><span class="sxs-lookup"><span data-stu-id="dbe81-119"><dt>**CAPICOM\_CERTIFICATE\_INCLUDE\_END\_ENTITY\_ONLY**</dt></span></span> </dl>       | <span data-ttu-id="dbe81-120">Сохраняет только сертификат конечного объекта.</span><span class="sxs-lookup"><span data-stu-id="dbe81-120">Saves only the end entity certificate.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="dbe81-121">Требования</span><span class="sxs-lookup"><span data-stu-id="dbe81-121">Requirements</span></span>



| <span data-ttu-id="dbe81-122">Требование</span><span class="sxs-lookup"><span data-stu-id="dbe81-122">Requirement</span></span> | <span data-ttu-id="dbe81-123">Значение</span><span class="sxs-lookup"><span data-stu-id="dbe81-123">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dbe81-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="dbe81-124">Redistributable</span></span><br/> | <span data-ttu-id="dbe81-125">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="dbe81-125">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="dbe81-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dbe81-126">DLL</span></span><br/>             | <dl> <span data-ttu-id="dbe81-127"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbe81-127"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbe81-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dbe81-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbe81-129">**Автор подписи**</span><span class="sxs-lookup"><span data-stu-id="dbe81-129">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
