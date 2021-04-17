---
description: Задает или получает объект сертификата, представляющий сертификат для подписи данных.
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: Свойство SignIn. Certificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685090"
---
# <a name="signercertificate-property"></a><span data-ttu-id="9386f-103">Свойство SignIn. Certificate</span><span class="sxs-lookup"><span data-stu-id="9386f-103">Signer.Certificate property</span></span>

<span data-ttu-id="9386f-104">\[Свойство **Certificate** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="9386f-104">\[The **Certificate** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9386f-105">Вместо этого используйте [**класс кмссигнер**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="9386f-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="9386f-106">Свойство **Certificate** задает или получает объект [**сертификата**](certificate.md) , представляющий сертификат для подписи данных.</span><span class="sxs-lookup"><span data-stu-id="9386f-106">The **Certificate** property sets or retrieves the [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span> <span data-ttu-id="9386f-107">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9386f-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9386f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9386f-108">Syntax</span></span>


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a><span data-ttu-id="9386f-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9386f-109">Property value</span></span>

<span data-ttu-id="9386f-110">Объект [**сертификата**](certificate.md) , представляющий сертификат подписи данных.</span><span class="sxs-lookup"><span data-stu-id="9386f-110">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span>

## <a name="remarks"></a><span data-ttu-id="9386f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9386f-111">Remarks</span></span>

<span data-ttu-id="9386f-112">Когда значение этого свойства сбрасывается прямо или косвенно, полное [*состояние*](../secgloss/s-gly.md) объекта сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="9386f-112">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="9386f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9386f-113">Requirements</span></span>



| <span data-ttu-id="9386f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9386f-114">Requirement</span></span> | <span data-ttu-id="9386f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9386f-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9386f-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="9386f-116">Redistributable</span></span><br/> | <span data-ttu-id="9386f-117">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="9386f-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9386f-118">DLL</span><span class="sxs-lookup"><span data-stu-id="9386f-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="9386f-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9386f-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9386f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9386f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9386f-121">**Автор подписи**</span><span class="sxs-lookup"><span data-stu-id="9386f-121">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
