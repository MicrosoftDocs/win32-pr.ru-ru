---
description: Предоставляет доступ к контексту объекта CAPICOM-хранилища. Этот контекст позволяет использовать хранилище CAPICOM Certificate в других производных классах CryptoAPI.
ms.assetid: dc108e2d-d6ec-4972-9c8e-e6e738c25756
title: Интерфейс Ицертсторе
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 119609399709340049bc43693ac51f6259021416
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688897"
---
# <a name="icertstore-interface"></a><span data-ttu-id="c18a8-104">Интерфейс Ицертсторе</span><span class="sxs-lookup"><span data-stu-id="c18a8-104">ICertStore interface</span></span>

<span data-ttu-id="c18a8-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="c18a8-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="c18a8-106">Интерфейс **ицертсторе** предоставляет доступ к контексту объекта CAPICOM- [**хранилища**](store.md) .</span><span class="sxs-lookup"><span data-stu-id="c18a8-106">The **ICertStore** interface provides access to the context of a CAPICOM [**Store**](store.md) object.</span></span> <span data-ttu-id="c18a8-107">Этот контекст позволяет использовать хранилище CAPICOM Certificate в других производных классах CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="c18a8-107">This context allows the CAPICOM certificate store to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="c18a8-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="c18a8-108">When to use</span></span>

<span data-ttu-id="c18a8-109">Используйте этот интерфейс, если необходимо использовать объект CAPICOM- [**Store**](store.md) в другом производном от CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="c18a8-109">Use this interface when you need to use a CAPICOM [**Store**](store.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="c18a8-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="c18a8-110">Members</span></span>

<span data-ttu-id="c18a8-111">Интерфейс **ицертсторе** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c18a8-111">The **ICertStore** interface has these types of members:</span></span>

-   [<span data-ttu-id="c18a8-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c18a8-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="c18a8-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="c18a8-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c18a8-114">Методы</span><span class="sxs-lookup"><span data-stu-id="c18a8-114">Methods</span></span>

<span data-ttu-id="c18a8-115">Интерфейс **ицертсторе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="c18a8-115">The **ICertStore** interface has these methods.</span></span>



| <span data-ttu-id="c18a8-116">Метод</span><span class="sxs-lookup"><span data-stu-id="c18a8-116">Method</span></span>                                        | <span data-ttu-id="c18a8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="c18a8-117">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c18a8-118">**CloseHandle**</span><span class="sxs-lookup"><span data-stu-id="c18a8-118">**CloseHandle**</span></span>](icertstore-closehandle.md) | <span data-ttu-id="c18a8-119">Закрывает обработчик ХЦЕРТСТОРЕ, полученный через свойство [**сторехандле**](icertstore-storehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="c18a8-119">Closes an HCERTSTORE handle acquired through the [**StoreHandle**](icertstore-storehandle.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c18a8-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="c18a8-120">Properties</span></span>

<span data-ttu-id="c18a8-121">Интерфейс **ицертсторе** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c18a8-121">The **ICertStore** interface has these properties.</span></span>



| <span data-ttu-id="c18a8-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="c18a8-122">Property</span></span>                                                     | <span data-ttu-id="c18a8-123">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="c18a8-123">Access type</span></span>           | <span data-ttu-id="c18a8-124">Описание</span><span class="sxs-lookup"><span data-stu-id="c18a8-124">Description</span></span>                                                                                                         |
|:-------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c18a8-125">**сторехандле**</span><span class="sxs-lookup"><span data-stu-id="c18a8-125">**StoreHandle**</span></span>](icertstore-storehandle.md)<br/>     | <span data-ttu-id="c18a8-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c18a8-126">Read/write</span></span><br/> | <span data-ttu-id="c18a8-127">Задает или получает маркер ХЦЕРТСТОРЕ хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c18a8-127">Sets or retrieves the HCERTSTORE handle of a certificate store.</span></span><br/>                                          |
| [<span data-ttu-id="c18a8-128">**StoreLocation**</span><span class="sxs-lookup"><span data-stu-id="c18a8-128">**StoreLocation**</span></span>](icertstore-storelocation.md)<br/> | <span data-ttu-id="c18a8-129">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="c18a8-129">Read/write</span></span><br/> | <span data-ttu-id="c18a8-130">Задает или получает [**\_ \_ Расположение CAPICOM-хранилища**](capicom-store-location.md) для хранилища сертификатов.</span><span class="sxs-lookup"><span data-stu-id="c18a8-130">Sets or retrieves the [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) of a certificate store.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c18a8-131">Требования</span><span class="sxs-lookup"><span data-stu-id="c18a8-131">Requirements</span></span>



| <span data-ttu-id="c18a8-132">Требование</span><span class="sxs-lookup"><span data-stu-id="c18a8-132">Requirement</span></span> | <span data-ttu-id="c18a8-133">Значение</span><span class="sxs-lookup"><span data-stu-id="c18a8-133">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c18a8-134">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="c18a8-134">Redistributable</span></span><br/> | <span data-ttu-id="c18a8-135">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="c18a8-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c18a8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c18a8-136">DLL</span></span><br/>             | <dl> <span data-ttu-id="c18a8-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c18a8-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




