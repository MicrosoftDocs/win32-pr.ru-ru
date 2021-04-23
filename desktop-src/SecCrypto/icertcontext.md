---
description: Предоставляет доступ к контексту объекта сертификата CAPICOM X. 509v3. Этот контекст позволяет использовать CAPICOM Certificate в других производных классах CryptoAPI.
ms.assetid: 084a3a7b-7523-419f-a504-6fd397030d78
title: Интерфейс Ицертконтекст
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f282b97e2257292849a76bc42017e48a95204d01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669289"
---
# <a name="icertcontext-interface"></a><span data-ttu-id="48af6-104">Интерфейс Ицертконтекст</span><span class="sxs-lookup"><span data-stu-id="48af6-104">ICertContext interface</span></span>

<span data-ttu-id="48af6-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="48af6-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="48af6-106">Интерфейс **ицертконтекст** предоставляет доступ к контексту объекта [**сертификата**](certificate.md) CAPICOM X. 509v3.</span><span class="sxs-lookup"><span data-stu-id="48af6-106">The **ICertContext** interface provides access to the context of a CAPICOM X.509v3 [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="48af6-107">Этот контекст позволяет использовать CAPICOM Certificate в других производных классах CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="48af6-107">This context allows the CAPICOM certificate to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="48af6-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="48af6-108">When to use</span></span>

<span data-ttu-id="48af6-109">Этот интерфейс следует использовать, если необходимо использовать объект CAPICOM [**Certificate**](certificate.md) в другом производном от CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="48af6-109">Use this interface when you need to use a CAPICOM [**Certificate**](certificate.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="48af6-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="48af6-110">Members</span></span>

<span data-ttu-id="48af6-111">Интерфейс **ицертконтекст** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="48af6-111">The **ICertContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="48af6-112">Методы</span><span class="sxs-lookup"><span data-stu-id="48af6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="48af6-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="48af6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48af6-114">Методы</span><span class="sxs-lookup"><span data-stu-id="48af6-114">Methods</span></span>

<span data-ttu-id="48af6-115">Интерфейс **ицертконтекст** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="48af6-115">The **ICertContext** interface has these methods.</span></span>



| <span data-ttu-id="48af6-116">Метод</span><span class="sxs-lookup"><span data-stu-id="48af6-116">Method</span></span>                                          | <span data-ttu-id="48af6-117">Описание</span><span class="sxs-lookup"><span data-stu-id="48af6-117">Description</span></span>                                                                                                          |
|:------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="48af6-118">**фриконтекст**</span><span class="sxs-lookup"><span data-stu-id="48af6-118">**FreeContext**</span></span>](icertcontext-freecontext.md) | <span data-ttu-id="48af6-119">Освобождает контекст ПКЦЕРТ, \_ полученный через свойство [**цертконтекст**](icertcontext-certcontext.md) .</span><span class="sxs-lookup"><span data-stu-id="48af6-119">Releases a PCCERT\_CONTEXT acquired through the [**CertContext**](icertcontext-certcontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="48af6-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="48af6-120">Properties</span></span>

<span data-ttu-id="48af6-121">Интерфейс **ицертконтекст** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="48af6-121">The **ICertContext** interface has these properties.</span></span>



| <span data-ttu-id="48af6-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="48af6-122">Property</span></span>                                                   | <span data-ttu-id="48af6-123">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="48af6-123">Access type</span></span>           | <span data-ttu-id="48af6-124">Описание</span><span class="sxs-lookup"><span data-stu-id="48af6-124">Description</span></span>                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="48af6-125">**цертконтекст**</span><span class="sxs-lookup"><span data-stu-id="48af6-125">**CertContext**</span></span>](icertcontext-certcontext.md)<br/> | <span data-ttu-id="48af6-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="48af6-126">Read/write</span></span><br/> | <span data-ttu-id="48af6-127">Задает или получает контекст ПКЦЕРТ \_ сертификата.</span><span class="sxs-lookup"><span data-stu-id="48af6-127">Sets or retrieves the PCCERT\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="48af6-128">Требования</span><span class="sxs-lookup"><span data-stu-id="48af6-128">Requirements</span></span>



| <span data-ttu-id="48af6-129">Требование</span><span class="sxs-lookup"><span data-stu-id="48af6-129">Requirement</span></span> | <span data-ttu-id="48af6-130">Значение</span><span class="sxs-lookup"><span data-stu-id="48af6-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48af6-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="48af6-131">Redistributable</span></span><br/> | <span data-ttu-id="48af6-132">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="48af6-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="48af6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="48af6-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="48af6-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48af6-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




