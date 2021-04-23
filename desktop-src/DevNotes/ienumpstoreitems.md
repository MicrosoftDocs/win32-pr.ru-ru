---
description: Предоставляет стандартные методы перечисления COM для интерфейса Ипсторе.
ms.assetid: f5290e6c-8752-4380-9210-c96a87f000ba
title: Интерфейс Иенумпстореитемс (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreItems
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 11ca255cb13d998d16596bc7cc54d28d2415b227
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657093"
---
# <a name="ienumpstoreitems-interface"></a><span data-ttu-id="b142d-103">Интерфейс Иенумпстореитемс</span><span class="sxs-lookup"><span data-stu-id="b142d-103">IEnumPStoreItems interface</span></span>

<span data-ttu-id="b142d-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b142d-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="b142d-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="b142d-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="b142d-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="b142d-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="b142d-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="b142d-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="b142d-108">Предоставляет стандартные методы перечисления COM для интерфейса [**ипсторе**](ipstore.md) .</span><span class="sxs-lookup"><span data-stu-id="b142d-108">Provides the COM-standard enumeration methods for the [**IPStore**](ipstore.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="b142d-109">Элементы</span><span class="sxs-lookup"><span data-stu-id="b142d-109">Members</span></span>

<span data-ttu-id="b142d-110">Интерфейс **иенумпстореитемс** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="b142d-110">The **IEnumPStoreItems** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="b142d-111">**Иенумпстореитемс** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="b142d-111">**IEnumPStoreItems** also has these types of members:</span></span>

-   [<span data-ttu-id="b142d-112">Методы</span><span class="sxs-lookup"><span data-stu-id="b142d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b142d-113">Методы</span><span class="sxs-lookup"><span data-stu-id="b142d-113">Methods</span></span>

<span data-ttu-id="b142d-114">Интерфейс **иенумпстореитемс** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="b142d-114">The **IEnumPStoreItems** interface has these methods.</span></span>



| <span data-ttu-id="b142d-115">Метод</span><span class="sxs-lookup"><span data-stu-id="b142d-115">Method</span></span>                                  | <span data-ttu-id="b142d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="b142d-116">Description</span></span>                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b142d-117">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="b142d-117">**Clone**</span></span>](ienumpstoreitems-clone.md) | <span data-ttu-id="b142d-118">Создает другой перечислитель с тем же состоянием перечисления, что и текущий.</span><span class="sxs-lookup"><span data-stu-id="b142d-118">Creates another enumerator that contains the same enumeration state as the current one.</span></span><br/> |
| [<span data-ttu-id="b142d-119">**Далее**</span><span class="sxs-lookup"><span data-stu-id="b142d-119">**Next**</span></span>](ienumpstoreitems-next.md)   | <span data-ttu-id="b142d-120">Возвращает следующий указанный элемент данных в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="b142d-120">Gets the next specified data item in the enumeration sequence.</span></span><br/>                          |
| [<span data-ttu-id="b142d-121">**Перезапуск**</span><span class="sxs-lookup"><span data-stu-id="b142d-121">**Reset**</span></span>](ienumpstoreitems-reset.md) | <span data-ttu-id="b142d-122">Выполняет сброс до начала последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="b142d-122">Resets to the beginning of the enumeration sequence.</span></span><br/>                                    |
| [<span data-ttu-id="b142d-123">**Пропустить**</span><span class="sxs-lookup"><span data-stu-id="b142d-123">**Skip**</span></span>](ienumpstoreitems-skip.md)   | <span data-ttu-id="b142d-124">Пропускает указанный элемент данных в последовательности перечисления.</span><span class="sxs-lookup"><span data-stu-id="b142d-124">Skips the specified data item in the enumeration sequence.</span></span><br/>                              |



 

## <a name="remarks"></a><span data-ttu-id="b142d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b142d-125">Remarks</span></span>

<span data-ttu-id="b142d-126">Необходимо освобождать каждый элемент после перечисления.</span><span class="sxs-lookup"><span data-stu-id="b142d-126">It is necessary to free each item after enumerating it.</span></span> <span data-ttu-id="b142d-127">Объект перечислителя также должен быть освобожден, если он больше не используется.</span><span class="sxs-lookup"><span data-stu-id="b142d-127">The enumerator object must also be released when it is no longer being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="b142d-128">Требования</span><span class="sxs-lookup"><span data-stu-id="b142d-128">Requirements</span></span>



| <span data-ttu-id="b142d-129">Требование</span><span class="sxs-lookup"><span data-stu-id="b142d-129">Requirement</span></span> | <span data-ttu-id="b142d-130">Значение</span><span class="sxs-lookup"><span data-stu-id="b142d-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b142d-131">Header</span><span class="sxs-lookup"><span data-stu-id="b142d-131">Header</span></span><br/> | <dl> <span data-ttu-id="b142d-132"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="b142d-132"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="b142d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b142d-133">DLL</span></span><br/>    | <dl> <span data-ttu-id="b142d-134"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b142d-134"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
