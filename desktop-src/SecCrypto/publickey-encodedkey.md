---
description: Получает значение открытого ключа.
ms.assetid: d9846ebe-44df-4ee0-8f15-cc96883d9d53
title: Свойство PublicKey. Енкодедкэй
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: de2c7b2bfbbdaf28345ae29e260bfd30c5754ffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689356"
---
# <a name="publickeyencodedkey-property"></a><span data-ttu-id="19999-103">Свойство PublicKey. Енкодедкэй</span><span class="sxs-lookup"><span data-stu-id="19999-103">PublicKey.EncodedKey property</span></span>

<span data-ttu-id="19999-104">\[Свойство **енкодедкэй** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="19999-104">\[The **EncodedKey** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="19999-105">Вместо этого используйте [**свойство X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="19999-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="19999-106">Свойство **енкодедкэй** извлекает значение открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="19999-106">The **EncodedKey** property retrieves the value of the public key.</span></span>

## <a name="syntax"></a><span data-ttu-id="19999-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="19999-107">Syntax</span></span>


```VB
PublicKey.EncodedKey As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="19999-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="19999-108">Property value</span></span>

<span data-ttu-id="19999-109">Объект [**енкодеддата**](encodeddata.md) , предоставляющий доступ к значению открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="19999-109">An [**EncodedData**](encodeddata.md) object that provides access to the value of the public key.</span></span>

## <a name="requirements"></a><span data-ttu-id="19999-110">Требования</span><span class="sxs-lookup"><span data-stu-id="19999-110">Requirements</span></span>



| <span data-ttu-id="19999-111">Требование</span><span class="sxs-lookup"><span data-stu-id="19999-111">Requirement</span></span> | <span data-ttu-id="19999-112">Значение</span><span class="sxs-lookup"><span data-stu-id="19999-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19999-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="19999-113">Redistributable</span></span><br/> | <span data-ttu-id="19999-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="19999-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="19999-115">DLL</span><span class="sxs-lookup"><span data-stu-id="19999-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="19999-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19999-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19999-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="19999-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19999-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="19999-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
