---
description: Предоставляет функциональные возможности для хэширования строки.
ms.assetid: 893639c2-57b9-48f6-bf60-a21c3368ffeb
title: Объект Хашеддата
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6e54d7d2ca52ceafe500615af4063dfc7310b0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665313"
---
# <a name="hasheddata-object"></a><span data-ttu-id="788b1-103">Объект Хашеддата</span><span class="sxs-lookup"><span data-stu-id="788b1-103">HashedData object</span></span>

<span data-ttu-id="788b1-104">\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="788b1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="788b1-105">Вместо этого используйте [**класс HashAlgorithm**](/previous-versions/windows/) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="788b1-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="788b1-106">Объект **хашеддата** предоставляет функциональные возможности для хэширования строки.</span><span class="sxs-lookup"><span data-stu-id="788b1-106">The **HashedData** object provides functionality for hashing a string.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="788b1-107">Назначение</span><span class="sxs-lookup"><span data-stu-id="788b1-107">When to use</span></span>

<span data-ttu-id="788b1-108">Объект **хашеддата** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="788b1-108">The **HashedData** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="788b1-109">Укажите строку содержимого, содержащую данные для хэширования.</span><span class="sxs-lookup"><span data-stu-id="788b1-109">Specify the content string that contains the data to be hashed.</span></span>
-   <span data-ttu-id="788b1-110">Примените указанный хэш-алгоритм к строке содержимого.</span><span class="sxs-lookup"><span data-stu-id="788b1-110">Apply a specified hash algorithm to the content string.</span></span>

## <a name="members"></a><span data-ttu-id="788b1-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="788b1-111">Members</span></span>

<span data-ttu-id="788b1-112">Объект **хашеддата** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="788b1-112">The **HashedData** object has these types of members:</span></span>

-   [<span data-ttu-id="788b1-113">Методы</span><span class="sxs-lookup"><span data-stu-id="788b1-113">Methods</span></span>](#methods)
-   [<span data-ttu-id="788b1-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="788b1-114">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="788b1-115">Методы</span><span class="sxs-lookup"><span data-stu-id="788b1-115">Methods</span></span>

<span data-ttu-id="788b1-116">Объект **хашеддата** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="788b1-116">The **HashedData** object has these methods.</span></span>



| <span data-ttu-id="788b1-117">Метод</span><span class="sxs-lookup"><span data-stu-id="788b1-117">Method</span></span>                          | <span data-ttu-id="788b1-118">Описание</span><span class="sxs-lookup"><span data-stu-id="788b1-118">Description</span></span>                                        |
|:--------------------------------|:---------------------------------------------------|
| [<span data-ttu-id="788b1-119">**Функции**</span><span class="sxs-lookup"><span data-stu-id="788b1-119">**Hash**</span></span>](hasheddata-hash.md) | <span data-ttu-id="788b1-120">Создает хэш указанной строки.</span><span class="sxs-lookup"><span data-stu-id="788b1-120">Creates a hash of the specified string.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="788b1-121">Свойства</span><span class="sxs-lookup"><span data-stu-id="788b1-121">Properties</span></span>

<span data-ttu-id="788b1-122">Объект **хашеддата** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="788b1-122">The **HashedData** object has these properties.</span></span>



| <span data-ttu-id="788b1-123">Свойство</span><span class="sxs-lookup"><span data-stu-id="788b1-123">Property</span></span>                                             | <span data-ttu-id="788b1-124">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="788b1-124">Access type</span></span>           | <span data-ttu-id="788b1-125">Описание</span><span class="sxs-lookup"><span data-stu-id="788b1-125">Description</span></span>                                                                                                                                                                          |
|:-----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="788b1-126">**Алгоритм**</span><span class="sxs-lookup"><span data-stu-id="788b1-126">**Algorithm**</span></span>](hasheddata-algorithm.md)<br/> | <span data-ttu-id="788b1-127">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="788b1-127">Read/write</span></span><br/> | <span data-ttu-id="788b1-128">Задает или получает тип используемого алгоритма хэширования.</span><span class="sxs-lookup"><span data-stu-id="788b1-128">Sets or retrieves the type of hashing algorithm used.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="788b1-129">**Значение**</span><span class="sxs-lookup"><span data-stu-id="788b1-129">**Value**</span></span>](hasheddata-value.md)<br/>         | <span data-ttu-id="788b1-130">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="788b1-130">Read-only</span></span><br/>  | <span data-ttu-id="788b1-131">Извлекает хэшированные данные после успешного вызова метода [**хэширования**](hasheddata-hash.md) .</span><span class="sxs-lookup"><span data-stu-id="788b1-131">Retrieves the hashed data after successful calls to the [**Hash**](hasheddata-hash.md) method.</span></span> <span data-ttu-id="788b1-132">Хэш возвращается в шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="788b1-132">The hash is returned in hexadecimal format.</span></span> <span data-ttu-id="788b1-133">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="788b1-133">This is the default property.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="788b1-134">Комментарии</span><span class="sxs-lookup"><span data-stu-id="788b1-134">Remarks</span></span>

<span data-ttu-id="788b1-135">Чтобы создать хэш большого объема данных, вызовите метод [**хэширования**](hasheddata-hash.md) для каждого фрагмента данных.</span><span class="sxs-lookup"><span data-stu-id="788b1-135">To create the hash of a large amount of data, call the [**Hash**](hasheddata-hash.md) method for each piece of data.</span></span> <span data-ttu-id="788b1-136">Хэш каждого фрагмента данных объединяется со свойством [**value**](hasheddata-value.md) до тех пор, пока свойство не будет считано.</span><span class="sxs-lookup"><span data-stu-id="788b1-136">The hash of each piece of data is concatenated to the [**Value**](hasheddata-value.md) property until the property is read.</span></span> <span data-ttu-id="788b1-137">Содержимое свойства **value** сбрасывается при считывании свойства.</span><span class="sxs-lookup"><span data-stu-id="788b1-137">The contents of the **Value** property are reset when the property is read.</span></span>

<span data-ttu-id="788b1-138">Объект **хашеддата** может быть создан и защищен для создания скриптов.</span><span class="sxs-lookup"><span data-stu-id="788b1-138">The **HashedData** object can be created, and it is safe for scripting.</span></span> <span data-ttu-id="788b1-139">ProgID для объекта **хашеддата** — "CAPICOM. Хашеддата. 1 ".</span><span class="sxs-lookup"><span data-stu-id="788b1-139">The ProgID for the **HashedData** object is "CAPICOM.HashedData.1".</span></span>

## <a name="requirements"></a><span data-ttu-id="788b1-140">Требования</span><span class="sxs-lookup"><span data-stu-id="788b1-140">Requirements</span></span>



| <span data-ttu-id="788b1-141">Требование</span><span class="sxs-lookup"><span data-stu-id="788b1-141">Requirement</span></span> | <span data-ttu-id="788b1-142">Значение</span><span class="sxs-lookup"><span data-stu-id="788b1-142">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="788b1-143">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="788b1-143">End of client support</span></span><br/> | <span data-ttu-id="788b1-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="788b1-144">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="788b1-145">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="788b1-145">End of server support</span></span><br/> | <span data-ttu-id="788b1-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="788b1-146">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="788b1-147">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="788b1-147">Redistributable</span></span><br/>       | <span data-ttu-id="788b1-148">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="788b1-148">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="788b1-149">DLL</span><span class="sxs-lookup"><span data-stu-id="788b1-149">DLL</span></span><br/>                   | <dl> <span data-ttu-id="788b1-150"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="788b1-150"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
