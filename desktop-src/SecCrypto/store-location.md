---
description: Извлекает расположение хранилища сертификатов, которое представляет этот объект.
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Свойство Store. Location
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649089"
---
# <a name="storelocation-property"></a><span data-ttu-id="f73c0-103">Свойство Store. Location</span><span class="sxs-lookup"><span data-stu-id="f73c0-103">Store.Location property</span></span>

<span data-ttu-id="f73c0-104">\[Свойство **Location** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="f73c0-104">\[The **Location** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f73c0-105">Вместо этого используйте [**класс X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="f73c0-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f73c0-106">Свойство **Location** извлекает расположение хранилища сертификатов, которое представляет этот объект.</span><span class="sxs-lookup"><span data-stu-id="f73c0-106">The **Location** property retrieves the location of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="f73c0-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f73c0-107">Syntax</span></span>


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="f73c0-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f73c0-108">Property value</span></span>

<span data-ttu-id="f73c0-109">Значение [**\_ \_ расположения CAPICOM Store**](capicom-store-location.md) , представляющее расположение хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="f73c0-109">The [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) value that represents the location of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="f73c0-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f73c0-110">Remarks</span></span>

<span data-ttu-id="f73c0-111">Значение свойства **Location** совпадает со значением, заданным для параметра *StoreLocation* метода [**Open**](store-open.md) при открытии хранилища.</span><span class="sxs-lookup"><span data-stu-id="f73c0-111">The value of the **Location** property is the same as the value supplied for the *StoreLocation* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="f73c0-112">Требования</span><span class="sxs-lookup"><span data-stu-id="f73c0-112">Requirements</span></span>



| <span data-ttu-id="f73c0-113">Требование</span><span class="sxs-lookup"><span data-stu-id="f73c0-113">Requirement</span></span> | <span data-ttu-id="f73c0-114">Значение</span><span class="sxs-lookup"><span data-stu-id="f73c0-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f73c0-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f73c0-115">Redistributable</span></span><br/> | <span data-ttu-id="f73c0-116">CAPICOM 2,1 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="f73c0-116">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f73c0-117">DLL</span><span class="sxs-lookup"><span data-stu-id="f73c0-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="f73c0-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f73c0-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f73c0-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f73c0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f73c0-120">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="f73c0-120">**Store**</span></span>](store.md)
</dt> </dl>

 

 
