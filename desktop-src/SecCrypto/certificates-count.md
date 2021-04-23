---
description: Возвращает количество объектов сертификата в коллекции.
ms.assetid: 95931721-3b0c-4915-805f-039d1d5510fa
title: Свойство Certificates. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a67554530ce8c8dfdc1bfcfba1198cf778397ac2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688869"
---
# <a name="certificatescount-property"></a><span data-ttu-id="ff098-103">Свойство Certificates. Count</span><span class="sxs-lookup"><span data-stu-id="ff098-103">Certificates.Count property</span></span>

<span data-ttu-id="ff098-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff098-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ff098-105">Вместо этого используйте [**класс X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="ff098-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ff098-106">Свойство **Count** извлекает количество объектов [**сертификата**](certificate.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ff098-106">The **Count** property retrieves the number of [**Certificate**](certificate.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff098-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff098-107">Syntax</span></span>


```VB
Certificates.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="ff098-108">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ff098-108">Property value</span></span>

<span data-ttu-id="ff098-109">Число объектов [**сертификата**](certificate.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ff098-109">The number of [**Certificate**](certificate.md) objects in the collection.</span></span> <span data-ttu-id="ff098-110">Каждый объект **сертификата** представляет один сертификат в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ff098-110">Each **Certificate** object represents a single certificate in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff098-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ff098-111">Remarks</span></span>

<span data-ttu-id="ff098-112">CAPICOM поддерживает только один сертификат для хранилища [*смарт-карт*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="ff098-112">CAPICOM only supports a single certificate for the [*smart card*](../secgloss/s-gly.md) store.</span></span> <span data-ttu-id="ff098-113">Даже если хранилище смарт-карт содержит более одного сертификата, это свойство будет содержать значение 1.</span><span class="sxs-lookup"><span data-stu-id="ff098-113">Even if the smart card store contains more than one certificate, this property will contain 1.</span></span> <span data-ttu-id="ff098-114">Дополнительные сведения о хранилище смарт-карт см. в разделе **элемент \_ \_ \_ пользовательского \_ хранилища CAPICOM смарт-карты** перечисление [**\_ \_ расположения CAPICOM Store**](capicom-store-location.md) .</span><span class="sxs-lookup"><span data-stu-id="ff098-114">For more information about the smart card store, see the **CAPICOM\_SMART\_CARD\_USER\_STORE** member of the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff098-115">Требования</span><span class="sxs-lookup"><span data-stu-id="ff098-115">Requirements</span></span>



| <span data-ttu-id="ff098-116">Требование</span><span class="sxs-lookup"><span data-stu-id="ff098-116">Requirement</span></span> | <span data-ttu-id="ff098-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ff098-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff098-118">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ff098-118">End of client support</span></span><br/> | <span data-ttu-id="ff098-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff098-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ff098-120">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="ff098-120">End of server support</span></span><br/> | <span data-ttu-id="ff098-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff098-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ff098-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ff098-122">Redistributable</span></span><br/>       | <span data-ttu-id="ff098-123">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="ff098-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ff098-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ff098-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ff098-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff098-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff098-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff098-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff098-127">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="ff098-127">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
