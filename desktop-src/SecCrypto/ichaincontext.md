---
description: Предоставляет доступ к контексту объекта CAPICOM Chain. Этот контекст позволяет использовать цепочку доверия CAPICOM Certificate в других производных классах CryptoAPI.
ms.assetid: ee258586-028e-486e-8129-07f43b6cc468
title: Интерфейс Ичаинконтекст
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34ba471c50ceb9475121139c3ecb997cf1d26f2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665037"
---
# <a name="ichaincontext-interface"></a><span data-ttu-id="2d4ca-104">Интерфейс Ичаинконтекст</span><span class="sxs-lookup"><span data-stu-id="2d4ca-104">IChainContext interface</span></span>

<span data-ttu-id="2d4ca-105">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]</span><span class="sxs-lookup"><span data-stu-id="2d4ca-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.\]</span></span>

<span data-ttu-id="2d4ca-106">Интерфейс **ичаинконтекст** предоставляет доступ к контексту объекта CAPICOM [**chain**](chain.md) .</span><span class="sxs-lookup"><span data-stu-id="2d4ca-106">The **IChainContext** interface provides access to the context of a CAPICOM [**Chain**](chain.md) object.</span></span> <span data-ttu-id="2d4ca-107">Этот контекст позволяет использовать цепочку доверия CAPICOM Certificate в других производных классах CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="2d4ca-107">This context allows the CAPICOM certificate trust chain to be used in other derivations of CryptoAPI.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="2d4ca-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="2d4ca-108">When to use</span></span>

<span data-ttu-id="2d4ca-109">Этот интерфейс следует использовать, если необходимо использовать объект- [**цепочку**](chain.md) CAPICOM в другом производном интерфейсе CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="2d4ca-109">Use this interface when you need to use a CAPICOM [**Chain**](chain.md) object in another derivation of CryptoAPI.</span></span>

## <a name="members"></a><span data-ttu-id="2d4ca-110">Элементы</span><span class="sxs-lookup"><span data-stu-id="2d4ca-110">Members</span></span>

<span data-ttu-id="2d4ca-111">Интерфейс **ичаинконтекст** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2d4ca-111">The **IChainContext** interface has these types of members:</span></span>

-   [<span data-ttu-id="2d4ca-112">Методы</span><span class="sxs-lookup"><span data-stu-id="2d4ca-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="2d4ca-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d4ca-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d4ca-114">Методы</span><span class="sxs-lookup"><span data-stu-id="2d4ca-114">Methods</span></span>

<span data-ttu-id="2d4ca-115">Интерфейс **ичаинконтекст** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2d4ca-115">The **IChainContext** interface has these methods.</span></span>



| <span data-ttu-id="2d4ca-116">Метод</span><span class="sxs-lookup"><span data-stu-id="2d4ca-116">Method</span></span>                                           | <span data-ttu-id="2d4ca-117">Описание</span><span class="sxs-lookup"><span data-stu-id="2d4ca-117">Description</span></span>                                                                                                                    |
|:-------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2d4ca-118">**фриконтекст**</span><span class="sxs-lookup"><span data-stu-id="2d4ca-118">**FreeContext**</span></span>](ichaincontext-freecontext.md) | <span data-ttu-id="2d4ca-119">Освобождает \_ контекст цепочки пкцерт, \_ полученный через свойство [**чаинконтекст**](ichaincontext-chaincontext.md) .</span><span class="sxs-lookup"><span data-stu-id="2d4ca-119">Releases a PCCERT\_CHAIN\_CONTEXT acquired through the [**ChainContext**](ichaincontext-chaincontext.md) property.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2d4ca-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d4ca-120">Properties</span></span>

<span data-ttu-id="2d4ca-121">Интерфейс **ичаинконтекст** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="2d4ca-121">The **IChainContext** interface has these properties.</span></span>



| <span data-ttu-id="2d4ca-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="2d4ca-122">Property</span></span>                                                      | <span data-ttu-id="2d4ca-123">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="2d4ca-123">Access type</span></span>           | <span data-ttu-id="2d4ca-124">Описание</span><span class="sxs-lookup"><span data-stu-id="2d4ca-124">Description</span></span>                                                               |
|:--------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="2d4ca-125">**чаинконтекст**</span><span class="sxs-lookup"><span data-stu-id="2d4ca-125">**ChainContext**</span></span>](ichaincontext-chaincontext.md)<br/> | <span data-ttu-id="2d4ca-126">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="2d4ca-126">Read/write</span></span><br/> | <span data-ttu-id="2d4ca-127">Задает или получает \_ контекст цепочки пкцерт \_ сертификата.</span><span class="sxs-lookup"><span data-stu-id="2d4ca-127">Sets or retrieves the PCCERT\_CHAIN\_CONTEXT of a certificate.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2d4ca-128">Требования</span><span class="sxs-lookup"><span data-stu-id="2d4ca-128">Requirements</span></span>



| <span data-ttu-id="2d4ca-129">Требование</span><span class="sxs-lookup"><span data-stu-id="2d4ca-129">Requirement</span></span> | <span data-ttu-id="2d4ca-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2d4ca-130">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d4ca-131">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="2d4ca-131">Redistributable</span></span><br/> | <span data-ttu-id="2d4ca-132">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="2d4ca-132">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2d4ca-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2d4ca-133">DLL</span></span><br/>             | <dl> <span data-ttu-id="2d4ca-134"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d4ca-134"><dt>Capicom.dll</dt></span></span> </dl> |



 

 




