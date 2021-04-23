---
description: Извлекает объект атрибута, представляющий индексированный атрибут.
ms.assetid: 35c54c5f-f83f-40eb-b341-129c1aac6181
title: Свойство Attributes. Item
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 208e36fd8d4d7e3effc2c0f59b7db921fed76d79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668697"
---
# <a name="attributesitem-property"></a><span data-ttu-id="92453-103">Свойство Attributes. Item</span><span class="sxs-lookup"><span data-stu-id="92453-103">Attributes.Item property</span></span>

<span data-ttu-id="92453-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="92453-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="92453-105">Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="92453-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="92453-106">Свойство **Item** извлекает объект [**атрибута**](attribute.md) , представляющий индексированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="92453-106">The **Item** property retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="92453-107">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92453-107">This is the default property.</span></span>

<span data-ttu-id="92453-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="92453-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="92453-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92453-109">Syntax</span></span>


```VB
Attributes.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="92453-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="92453-110">Property value</span></span>

<span data-ttu-id="92453-111">Объект [**атрибута**](attribute.md) , представляющий индексированный атрибут.</span><span class="sxs-lookup"><span data-stu-id="92453-111">An [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="92453-112">Требования</span><span class="sxs-lookup"><span data-stu-id="92453-112">Requirements</span></span>



| <span data-ttu-id="92453-113">Требование</span><span class="sxs-lookup"><span data-stu-id="92453-113">Requirement</span></span> | <span data-ttu-id="92453-114">Значение</span><span class="sxs-lookup"><span data-stu-id="92453-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92453-115">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="92453-115">End of client support</span></span><br/> | <span data-ttu-id="92453-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92453-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="92453-117">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="92453-117">End of server support</span></span><br/> | <span data-ttu-id="92453-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92453-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="92453-119">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="92453-119">Redistributable</span></span><br/>       | <span data-ttu-id="92453-120">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="92453-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="92453-121">DLL</span><span class="sxs-lookup"><span data-stu-id="92453-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="92453-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92453-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
