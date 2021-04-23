---
description: Добавляет объект атрибута в коллекцию.
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: Метод Attributes. Add
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669290"
---
# <a name="attributesadd-method"></a><span data-ttu-id="f8193-103">Метод Attributes. Add</span><span class="sxs-lookup"><span data-stu-id="f8193-103">Attributes.Add method</span></span>

<span data-ttu-id="f8193-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f8193-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="f8193-105">Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="f8193-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="f8193-106">Метод **Add** добавляет объект [**атрибута**](attribute.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f8193-106">The **Add** method adds an [**Attribute**](attribute.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8193-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f8193-107">Syntax</span></span>


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a><span data-ttu-id="f8193-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f8193-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8193-109">*Атрибут* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f8193-109">*Attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8193-110">Объект [**атрибута**](attribute.md) , добавляемый в конец коллекции.</span><span class="sxs-lookup"><span data-stu-id="f8193-110">The [**Attribute**](attribute.md) object to be added at the end of the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8193-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f8193-111">Return value</span></span>

<span data-ttu-id="f8193-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f8193-112">This method does not return a value.</span></span> <span data-ttu-id="f8193-113">Приложение, использующее этот метод, должно содержать код, обрабатывающий исключение, вызванное этим методом.</span><span class="sxs-lookup"><span data-stu-id="f8193-113">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8193-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f8193-114">Requirements</span></span>



| <span data-ttu-id="f8193-115">Требование</span><span class="sxs-lookup"><span data-stu-id="f8193-115">Requirement</span></span> | <span data-ttu-id="f8193-116">Значение</span><span class="sxs-lookup"><span data-stu-id="f8193-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8193-117">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="f8193-117">End of client support</span></span><br/> | <span data-ttu-id="f8193-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8193-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f8193-119">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="f8193-119">End of server support</span></span><br/> | <span data-ttu-id="f8193-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8193-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f8193-121">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="f8193-121">Redistributable</span></span><br/>       | <span data-ttu-id="f8193-122">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="f8193-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f8193-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f8193-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f8193-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8193-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8193-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f8193-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8193-126">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="f8193-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="f8193-127">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="f8193-127">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
