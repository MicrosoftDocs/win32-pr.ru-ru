---
description: Предоставляет стандартные методы перечисления COM для интерфейса Ипсторе.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Интерфейс Иенумпсторетипес (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 748f6e21701fdd27c2a88d1959b0b29cf56929f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649028"
---
# <a name="ienumpstoretypes-interface"></a><span data-ttu-id="76537-103">Интерфейс Иенумпсторетипес</span><span class="sxs-lookup"><span data-stu-id="76537-103">IEnumPStoreTypes interface</span></span>

<span data-ttu-id="76537-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="76537-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="76537-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="76537-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="76537-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="76537-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="76537-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="76537-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="76537-108">Предоставляет стандартные методы перечисления COM для интерфейса [**ипсторе**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="76537-108">Provides COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="76537-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="76537-109">Members</span></span>

<span data-ttu-id="76537-110">Интерфейс **иенумпсторетипес** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="76537-110">The **IEnumPStoreTypes** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="76537-111">**Иенумпсторетипес** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="76537-111">**IEnumPStoreTypes** also has these types of members:</span></span>

-   [<span data-ttu-id="76537-112">Методы</span><span class="sxs-lookup"><span data-stu-id="76537-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="76537-113">Методы</span><span class="sxs-lookup"><span data-stu-id="76537-113">Methods</span></span>

<span data-ttu-id="76537-114">Интерфейс **иенумпсторетипес** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="76537-114">The **IEnumPStoreTypes** interface has these methods.</span></span>



| <span data-ttu-id="76537-115">Метод</span><span class="sxs-lookup"><span data-stu-id="76537-115">Method</span></span>                                  | <span data-ttu-id="76537-116">Описание</span><span class="sxs-lookup"><span data-stu-id="76537-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="76537-117">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="76537-117">**Clone**</span></span>](ienumpstoretypes-clone.md) | <span data-ttu-id="76537-118">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="76537-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="76537-119">**Далее**</span><span class="sxs-lookup"><span data-stu-id="76537-119">**Next**</span></span>](ienumpstoretypes-next.md)   | <span data-ttu-id="76537-120">Возвращает следующий указанный тип поставщика в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="76537-120">Gets the next specified provider type in the enumeration sequence.</span></span><br/>                      |
| [<span data-ttu-id="76537-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="76537-121">**Reset**</span></span>](ienumpstoretypes-reset.md) | <span data-ttu-id="76537-122">Выполняет сброс до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="76537-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="76537-123">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="76537-123">**Skip**</span></span>](ienumpstoretypes-skip.md)   | <span data-ttu-id="76537-124">Пропускает указанный тип поставщика в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="76537-124">Skips the specified provider type in the enumeration sequence.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="76537-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76537-125">Remarks</span></span>

<span data-ttu-id="76537-126">Объект перечислителя должен быть освобожден, если он больше не используется.</span><span class="sxs-lookup"><span data-stu-id="76537-126">The enumerator object must be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="76537-127">Требования</span><span class="sxs-lookup"><span data-stu-id="76537-127">Requirements</span></span>



| <span data-ttu-id="76537-128">Требование</span><span class="sxs-lookup"><span data-stu-id="76537-128">Requirement</span></span> | <span data-ttu-id="76537-129">Значение</span><span class="sxs-lookup"><span data-stu-id="76537-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76537-130">Header</span><span class="sxs-lookup"><span data-stu-id="76537-130">Header</span></span><br/> | <dl> <span data-ttu-id="76537-131"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="76537-131"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="76537-132">DLL</span><span class="sxs-lookup"><span data-stu-id="76537-132">DLL</span></span><br/>    | <dl> <span data-ttu-id="76537-133"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76537-133"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
