---
description: Удаляет все объекты атрибутов из коллекции.
ms.assetid: 98b022f8-15aa-44b4-aaff-de09081d80b6
title: Метод Attributes. Clear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eec570200234f455467c30a3eb12429226400c60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668933"
---
# <a name="attributesclear-method"></a><span data-ttu-id="117b9-103">Метод Attributes. Clear</span><span class="sxs-lookup"><span data-stu-id="117b9-103">Attributes.Clear method</span></span>

<span data-ttu-id="117b9-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="117b9-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="117b9-105">Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="117b9-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="117b9-106">Метод **clear** удаляет все объекты [**атрибутов**](attribute.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="117b9-106">The **Clear** method clears all [**Attribute**](attribute.md) objects from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="117b9-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="117b9-107">Syntax</span></span>


```VB
Attributes.Clear()
```



## <a name="parameters"></a><span data-ttu-id="117b9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="117b9-108">Parameters</span></span>

<span data-ttu-id="117b9-109">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="117b9-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="117b9-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="117b9-110">Return value</span></span>

<span data-ttu-id="117b9-111">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="117b9-111">This method does not return a value.</span></span> <span data-ttu-id="117b9-112">Приложение, использующее этот метод, должно содержать код, обрабатывающий исключение, вызванное этим методом.</span><span class="sxs-lookup"><span data-stu-id="117b9-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="117b9-113">Требования</span><span class="sxs-lookup"><span data-stu-id="117b9-113">Requirements</span></span>



| <span data-ttu-id="117b9-114">Требование</span><span class="sxs-lookup"><span data-stu-id="117b9-114">Requirement</span></span> | <span data-ttu-id="117b9-115">Значение</span><span class="sxs-lookup"><span data-stu-id="117b9-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="117b9-116">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="117b9-116">End of client support</span></span><br/> | <span data-ttu-id="117b9-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="117b9-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="117b9-118">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="117b9-118">End of server support</span></span><br/> | <span data-ttu-id="117b9-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="117b9-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="117b9-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="117b9-120">Redistributable</span></span><br/>       | <span data-ttu-id="117b9-121">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="117b9-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="117b9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="117b9-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="117b9-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="117b9-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="117b9-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="117b9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="117b9-125">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="117b9-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="117b9-126">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="117b9-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
