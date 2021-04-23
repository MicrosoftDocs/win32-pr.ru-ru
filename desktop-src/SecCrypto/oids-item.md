---
description: Извлекает объект OID из коллекции. Это свойство по умолчанию.
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: OID. Item, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685182"
---
# <a name="oidsitem-property"></a><span data-ttu-id="e5858-104">OID. Item, свойство</span><span class="sxs-lookup"><span data-stu-id="e5858-104">OIDs.Item property</span></span>

<span data-ttu-id="e5858-105">\[Свойство **Item** доступно для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e5858-105">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e5858-106">Вместо этого используйте [**класс оидколлектион**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="e5858-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e5858-107">Свойство **Item** извлекает объект [**OID**](oid.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="e5858-107">The **Item** property retrieves an [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="e5858-108">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e5858-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5858-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5858-109">Syntax</span></span>


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="e5858-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e5858-110">Property value</span></span>

<span data-ttu-id="e5858-111">Объект [**OID**](oid.md) по указанному индексу или объект **OID** с указанным пунктирным значением.</span><span class="sxs-lookup"><span data-stu-id="e5858-111">The [**OID**](oid.md) object at the specified index, or the **OID** object with the specified dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5858-112">Требования</span><span class="sxs-lookup"><span data-stu-id="e5858-112">Requirements</span></span>



| <span data-ttu-id="e5858-113">Требование</span><span class="sxs-lookup"><span data-stu-id="e5858-113">Requirement</span></span> | <span data-ttu-id="e5858-114">Значение</span><span class="sxs-lookup"><span data-stu-id="e5858-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5858-115">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e5858-115">Redistributable</span></span><br/> | <span data-ttu-id="e5858-116">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e5858-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e5858-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e5858-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="e5858-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e5858-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5858-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5858-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5858-120">**OID**</span><span class="sxs-lookup"><span data-stu-id="e5858-120">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
