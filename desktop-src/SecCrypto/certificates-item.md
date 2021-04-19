---
description: Извлекает объект сертификата, представляющий индексированный сертификат коллекции. Это свойство по умолчанию.
ms.assetid: 733f2b93-c059-4041-b7cd-8c20218f1462
title: Свойство Certificates. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bbafaf20f74910e8ea5eb525f48374a2807fa030
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689381"
---
# <a name="certificatesitem-property"></a><span data-ttu-id="087b9-104">Свойство Certificates. Item</span><span class="sxs-lookup"><span data-stu-id="087b9-104">Certificates.Item property</span></span>

<span data-ttu-id="087b9-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="087b9-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="087b9-106">Вместо этого используйте [**класс X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="087b9-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="087b9-107">Свойство **Item** извлекает объект [**сертификата**](certificate.md) , представляющий индексированный сертификат коллекции.</span><span class="sxs-lookup"><span data-stu-id="087b9-107">The **Item** property retrieves a [**Certificate**](certificate.md) object that represents the indexed certificate of the collection.</span></span> <span data-ttu-id="087b9-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="087b9-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="087b9-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="087b9-109">Syntax</span></span>


```VB
Certificates.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="087b9-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="087b9-110">Property value</span></span>

<span data-ttu-id="087b9-111">Объект [**сертификата**](certificate.md) , представляющий индексированный сертификат.</span><span class="sxs-lookup"><span data-stu-id="087b9-111">A [**Certificate**](certificate.md) object that represents the indexed certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="087b9-112">Требования</span><span class="sxs-lookup"><span data-stu-id="087b9-112">Requirements</span></span>



| <span data-ttu-id="087b9-113">Требование</span><span class="sxs-lookup"><span data-stu-id="087b9-113">Requirement</span></span> | <span data-ttu-id="087b9-114">Значение</span><span class="sxs-lookup"><span data-stu-id="087b9-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="087b9-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="087b9-115">End of client support</span></span><br/> | <span data-ttu-id="087b9-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="087b9-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="087b9-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="087b9-117">End of server support</span></span><br/> | <span data-ttu-id="087b9-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="087b9-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="087b9-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="087b9-119">Redistributable</span></span><br/>       | <span data-ttu-id="087b9-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="087b9-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="087b9-121">DLL</span><span class="sxs-lookup"><span data-stu-id="087b9-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="087b9-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="087b9-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="087b9-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="087b9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="087b9-124">**Сертификаты**</span><span class="sxs-lookup"><span data-stu-id="087b9-124">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
