---
description: Удаляет объект индексированного атрибута из коллекции.
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Метод Attributes. Remove
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5981176afb332254d98171d40027e43383cb557
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668908"
---
# <a name="attributesremove-method"></a><span data-ttu-id="cfd5e-103">Метод Attributes. Remove</span><span class="sxs-lookup"><span data-stu-id="cfd5e-103">Attributes.Remove method</span></span>

<span data-ttu-id="cfd5e-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP.</span><span class="sxs-lookup"><span data-stu-id="cfd5e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="cfd5e-105">Вместо этого используйте [**класс криптографикаттрибутеобжектколлектион**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="cfd5e-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="cfd5e-106">Метод **Remove** удаляет объект индексированного [**атрибута**](attribute.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="cfd5e-106">The **Remove** method removes an indexed [**Attribute**](attribute.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfd5e-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cfd5e-107">Syntax</span></span>


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="cfd5e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cfd5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfd5e-109">*Индекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cfd5e-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfd5e-110">Индекс удаляемого объекта [**атрибута**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="cfd5e-110">Index of the [**Attribute**](attribute.md) object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfd5e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cfd5e-111">Return value</span></span>

<span data-ttu-id="cfd5e-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="cfd5e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfd5e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cfd5e-113">Remarks</span></span>

<span data-ttu-id="cfd5e-114">Приложения, использующие этот метод, должны содержать код, обрабатывающий исключение, вызванное этим методом.</span><span class="sxs-lookup"><span data-stu-id="cfd5e-114">Applications that use this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfd5e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cfd5e-115">Requirements</span></span>



| <span data-ttu-id="cfd5e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="cfd5e-116">Requirement</span></span> | <span data-ttu-id="cfd5e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="cfd5e-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfd5e-118">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="cfd5e-118">End of client support</span></span><br/> | <span data-ttu-id="cfd5e-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cfd5e-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="cfd5e-120">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="cfd5e-120">End of server support</span></span><br/> | <span data-ttu-id="cfd5e-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfd5e-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="cfd5e-122">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="cfd5e-122">Redistributable</span></span><br/>       | <span data-ttu-id="cfd5e-123">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="cfd5e-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="cfd5e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="cfd5e-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="cfd5e-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfd5e-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfd5e-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cfd5e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfd5e-127">Криптографические объекты</span><span class="sxs-lookup"><span data-stu-id="cfd5e-127">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="cfd5e-128">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="cfd5e-128">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
