---
description: Свойство Item извлекает из коллекции расширение по индексу. Это свойство по умолчанию.
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Свойство Extensions. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2cefe9ac1dd278c17161cc8e2349c051dccabff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685327"
---
# <a name="extensionsitem-property"></a><span data-ttu-id="682ca-104">Свойство Extensions. Item</span><span class="sxs-lookup"><span data-stu-id="682ca-104">Extensions.Item property</span></span>

<span data-ttu-id="682ca-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="682ca-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="682ca-106">Вместо этого используйте [**класс X509ExtensionCollection**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="682ca-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="682ca-107">Свойство **Item** извлекает из коллекции расширение по индексу.</span><span class="sxs-lookup"><span data-stu-id="682ca-107">The **Item** property retrieves an extension, by index, from the collection.</span></span> <span data-ttu-id="682ca-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="682ca-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="682ca-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="682ca-109">Syntax</span></span>


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="682ca-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="682ca-110">Property value</span></span>

<span data-ttu-id="682ca-111">Объект [**расширения**](extension.md) , представляющий индексированное расширение сертификата коллекции.</span><span class="sxs-lookup"><span data-stu-id="682ca-111">An [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="682ca-112">Требования</span><span class="sxs-lookup"><span data-stu-id="682ca-112">Requirements</span></span>



| <span data-ttu-id="682ca-113">Требование</span><span class="sxs-lookup"><span data-stu-id="682ca-113">Requirement</span></span> | <span data-ttu-id="682ca-114">Значение</span><span class="sxs-lookup"><span data-stu-id="682ca-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="682ca-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="682ca-115">End of client support</span></span><br/> | <span data-ttu-id="682ca-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="682ca-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="682ca-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="682ca-117">End of server support</span></span><br/> | <span data-ttu-id="682ca-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="682ca-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="682ca-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="682ca-119">Redistributable</span></span><br/>       | <span data-ttu-id="682ca-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="682ca-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="682ca-121">DLL</span><span class="sxs-lookup"><span data-stu-id="682ca-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="682ca-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="682ca-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="682ca-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="682ca-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="682ca-124">**Модули**</span><span class="sxs-lookup"><span data-stu-id="682ca-124">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
