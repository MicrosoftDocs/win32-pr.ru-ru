---
description: Возвращает имя хранилища сертификатов, которое представляет этот объект.
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Store.Name, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649113"
---
# <a name="storename-property"></a><span data-ttu-id="cd9b8-103">Store.Name, свойство</span><span class="sxs-lookup"><span data-stu-id="cd9b8-103">Store.Name property</span></span>

<span data-ttu-id="cd9b8-104">\[Свойство [**Name**](store-location.md) доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="cd9b8-104">\[The [**Name**](store-location.md) property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cd9b8-105">Вместо этого используйте [**класс X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="cd9b8-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="cd9b8-106">Свойство [**Name**](store-location.md) извлекает имя хранилища сертификатов, которое представляет этот объект.</span><span class="sxs-lookup"><span data-stu-id="cd9b8-106">The [**Name**](store-location.md) property retrieves the name of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd9b8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cd9b8-107">Syntax</span></span>


```VB
Store.Name As String
```



## <a name="property-value"></a><span data-ttu-id="cd9b8-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="cd9b8-108">Property value</span></span>

<span data-ttu-id="cd9b8-109">**Строковое** значение, представляющее имя хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cd9b8-109">The **String** value that represents the name of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd9b8-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd9b8-110">Remarks</span></span>

<span data-ttu-id="cd9b8-111">Примерами имен хранилищ сертификатов являются My и root.</span><span class="sxs-lookup"><span data-stu-id="cd9b8-111">Examples of certificate store names include My and Root.</span></span>

<span data-ttu-id="cd9b8-112">Значение свойства [**Name**](store-location.md) совпадает со значением, заданным для параметра *StoreName* метода [**Open**](store-open.md) при открытии хранилища.</span><span class="sxs-lookup"><span data-stu-id="cd9b8-112">The value of the [**Name**](store-location.md) property is the same as the value supplied for the *StoreName* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd9b8-113">Требования</span><span class="sxs-lookup"><span data-stu-id="cd9b8-113">Requirements</span></span>



| <span data-ttu-id="cd9b8-114">Требование</span><span class="sxs-lookup"><span data-stu-id="cd9b8-114">Requirement</span></span> | <span data-ttu-id="cd9b8-115">Значение</span><span class="sxs-lookup"><span data-stu-id="cd9b8-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9b8-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cd9b8-116">Redistributable</span></span><br/> | <span data-ttu-id="cd9b8-117">CAPICOM 2,1 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="cd9b8-117">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cd9b8-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cd9b8-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="cd9b8-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd9b8-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd9b8-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd9b8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9b8-121">**Магазин**</span><span class="sxs-lookup"><span data-stu-id="cd9b8-121">**Store**</span></span>](store.md)
</dt> </dl>

 

 
