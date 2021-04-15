---
description: Возвращает количество объектов атрибутов в коллекции.
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Свойство Attributes. Count
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668698"
---
# <a name="attributescount-property"></a><span data-ttu-id="73057-103">Свойство Attributes. Count</span><span class="sxs-lookup"><span data-stu-id="73057-103">Attributes.Count property</span></span>

<span data-ttu-id="73057-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="73057-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="73057-105">Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="73057-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="73057-106">Свойство **Count** извлекает количество объектов [**атрибутов**](attribute.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="73057-106">The **Count** property retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span>

<span data-ttu-id="73057-107">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="73057-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="73057-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73057-108">Syntax</span></span>


```VB
Attributes.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="73057-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="73057-109">Property value</span></span>

<span data-ttu-id="73057-110">Число объектов [**атрибутов**](attribute.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="73057-110">The number of [**Attribute**](attribute.md) objects in the collection.</span></span> <span data-ttu-id="73057-111">Каждый объект **атрибута** представляет один атрибут в коллекции.</span><span class="sxs-lookup"><span data-stu-id="73057-111">Each **Attribute** object represents a single attribute in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="73057-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="73057-112">Remarks</span></span>

<span data-ttu-id="73057-113">Свойство **Count** можно использовать для указания последнего объекта [**атрибута**](attribute.md) в коллекции при извлечении определенного объекта **атрибута** с помощью свойства [**Attributes. Item**](attributes-item.md) .</span><span class="sxs-lookup"><span data-stu-id="73057-113">The **Count** property can be used to specify the last [**Attribute**](attribute.md) object in the collection when retrieving a specific **Attribute** object by using the [**Attributes.Item**](attributes-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="73057-114">Требования</span><span class="sxs-lookup"><span data-stu-id="73057-114">Requirements</span></span>



| <span data-ttu-id="73057-115">Требование</span><span class="sxs-lookup"><span data-stu-id="73057-115">Requirement</span></span> | <span data-ttu-id="73057-116">Значение</span><span class="sxs-lookup"><span data-stu-id="73057-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="73057-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="73057-117">End of client support</span></span><br/> | <span data-ttu-id="73057-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73057-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="73057-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="73057-119">End of server support</span></span><br/> | <span data-ttu-id="73057-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73057-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="73057-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="73057-121">Redistributable</span></span><br/>       | <span data-ttu-id="73057-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="73057-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="73057-123">DLL</span><span class="sxs-lookup"><span data-stu-id="73057-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="73057-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73057-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73057-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="73057-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73057-126">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="73057-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
