---
description: Получает параметры алгоритма открытого ключа.
ms.assetid: 1d12f72e-0144-4b7b-b468-d2f35bf253d3
title: Свойство PublicKey. Енкодедпараметерс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublicKey.EncodedParameters
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 316e9737633bccea46cb644da24e4cc98fd118bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668723"
---
# <a name="publickeyencodedparameters-property"></a><span data-ttu-id="837f8-103">Свойство PublicKey. Енкодедпараметерс</span><span class="sxs-lookup"><span data-stu-id="837f8-103">PublicKey.EncodedParameters property</span></span>

<span data-ttu-id="837f8-104">\[Свойство **енкодедпараметерс** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="837f8-104">\[The **EncodedParameters** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="837f8-105">Вместо этого используйте [**свойство X509Certificate2. publickey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="837f8-105">Instead, use the [**X509Certificate2.PublicKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.publickey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="837f8-106">Свойство **енкодедпараметерс** получает параметры алгоритма открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="837f8-106">The **EncodedParameters** property retrieves the parameters of the public key algorithm.</span></span>

## <a name="syntax"></a><span data-ttu-id="837f8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="837f8-107">Syntax</span></span>


```VB
PublicKey.EncodedParameters As EncodedData
```



## <a name="property-value"></a><span data-ttu-id="837f8-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="837f8-108">Property value</span></span>

<span data-ttu-id="837f8-109">Объект [**енкодеддата**](encodeddata.md) , предоставляющий доступ к параметрам алгоритма открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="837f8-109">An [**EncodedData**](encodeddata.md) object that provides access to the parameters of the public key algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="837f8-110">Требования</span><span class="sxs-lookup"><span data-stu-id="837f8-110">Requirements</span></span>



| <span data-ttu-id="837f8-111">Требование</span><span class="sxs-lookup"><span data-stu-id="837f8-111">Requirement</span></span> | <span data-ttu-id="837f8-112">Значение</span><span class="sxs-lookup"><span data-stu-id="837f8-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="837f8-113">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="837f8-113">Redistributable</span></span><br/> | <span data-ttu-id="837f8-114">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="837f8-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="837f8-115">DLL</span><span class="sxs-lookup"><span data-stu-id="837f8-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="837f8-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="837f8-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="837f8-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="837f8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="837f8-118">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="837f8-118">**PublicKey**</span></span>](publickey.md)
</dt> </dl>

 

 
