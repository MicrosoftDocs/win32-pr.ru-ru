---
description: Представляет коллекцию объектов Extension.
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: Объект Нотиценумберс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689254"
---
# <a name="noticenumbers-object"></a><span data-ttu-id="e4aa1-103">Объект Нотиценумберс</span><span class="sxs-lookup"><span data-stu-id="e4aa1-103">NoticeNumbers object</span></span>

<span data-ttu-id="e4aa1-104">\[Объект **нотиценумберс** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-104">\[The **NoticeNumbers** object is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e4aa1-105">Дополнительные сведения см. в разделе [**квалификатор**](qualifier.md).\]</span><span class="sxs-lookup"><span data-stu-id="e4aa1-105">For more information, see [**Qualifier**](qualifier.md).\]</span></span>

<span data-ttu-id="e4aa1-106">Объект **нотиценумберс** представляет коллекцию объектов [**Extension**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="e4aa1-106">The **NoticeNumbers** object represents a collection of [**Extension**](extension.md) objects.</span></span> <span data-ttu-id="e4aa1-107">Каждый объект [**расширения**](extension.md) представляет номер уведомления пользователя.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-107">Each [**Extension**](extension.md) object represents a user notice number.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e4aa1-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="e4aa1-108">When to use</span></span>

<span data-ttu-id="e4aa1-109">Объект **нотиценумберс** используется для выполнения следующих задач:</span><span class="sxs-lookup"><span data-stu-id="e4aa1-109">The **NoticeNumbers** object is used to perform the following tasks:</span></span>

-   <span data-ttu-id="e4aa1-110">Получение числа объектов [**расширения**](extension.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-110">Retrieve the number of [**Extension**](extension.md) objects in the collection.</span></span>
-   <span data-ttu-id="e4aa1-111">Извлечение указанного объекта [**расширения**](extension.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-111">Retrieve a specific [**Extension**](extension.md) object from the collection.</span></span>
-   <span data-ttu-id="e4aa1-112">Выполните итерацию по коллекции.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-112">Iterate through the collection.</span></span>

## <a name="members"></a><span data-ttu-id="e4aa1-113">Элементы</span><span class="sxs-lookup"><span data-stu-id="e4aa1-113">Members</span></span>

<span data-ttu-id="e4aa1-114">Объект **нотиценумберс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e4aa1-114">The **NoticeNumbers** object has these types of members:</span></span>

-   [<span data-ttu-id="e4aa1-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="e4aa1-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e4aa1-116">Свойства</span><span class="sxs-lookup"><span data-stu-id="e4aa1-116">Properties</span></span>

<span data-ttu-id="e4aa1-117">Объект **нотиценумберс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-117">The **NoticeNumbers** object has these properties.</span></span>



| <span data-ttu-id="e4aa1-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="e4aa1-118">Property</span></span>                                              | <span data-ttu-id="e4aa1-119">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="e4aa1-119">Access type</span></span>          | <span data-ttu-id="e4aa1-120">Описание</span><span class="sxs-lookup"><span data-stu-id="e4aa1-120">Description</span></span>                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4aa1-121">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="e4aa1-121">**\_NewEnum**</span></span>](noticenumbers-newenum.md)<br/> | <span data-ttu-id="e4aa1-122">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e4aa1-122">Read-only</span></span><br/> | <span data-ttu-id="e4aa1-123">Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который может быть использован для перечисления коллекции.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-123">Retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e4aa1-124">Это свойство скрыто в Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="e4aa1-124">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span><br/> |
| [<span data-ttu-id="e4aa1-125">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="e4aa1-125">**Count**</span></span>](noticenumbers-count.md)<br/>       | <span data-ttu-id="e4aa1-126">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e4aa1-126">Read-only</span></span><br/> | <span data-ttu-id="e4aa1-127">Возвращает число объектов [**расширения**](extension.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-127">Retrieves the number of [**Extension**](extension.md) objects in the collection.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="e4aa1-128">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="e4aa1-128">**Item**</span></span>](noticenumbers-item.md)<br/>         | <span data-ttu-id="e4aa1-129">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="e4aa1-129">Read-only</span></span><br/> | <span data-ttu-id="e4aa1-130">Извлекает объект [**расширения**](extension.md) , который представляет номер индексированного уведомления коллекции.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-130">Retrieves the [**Extension**](extension.md) object that represents the indexed notice number of the collection.</span></span><br/> <span data-ttu-id="e4aa1-131">Это свойство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e4aa1-131">This is the default property.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="e4aa1-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e4aa1-132">Remarks</span></span>

<span data-ttu-id="e4aa1-133">Не удается создать объект **нотиценумберс** .</span><span class="sxs-lookup"><span data-stu-id="e4aa1-133">The **NoticeNumbers** object cannot be created.</span></span>

<span data-ttu-id="e4aa1-134">Объект Нотиценумберс используется в свойстве [**квалификатора. нотиценумберс**](qualifier-noticenumbers.md) .</span><span class="sxs-lookup"><span data-stu-id="e4aa1-134">The NoticeNumbers object is used in the [**Qualifier.NoticeNumbers**](qualifier-noticenumbers.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4aa1-135">Требования</span><span class="sxs-lookup"><span data-stu-id="e4aa1-135">Requirements</span></span>



| <span data-ttu-id="e4aa1-136">Требование</span><span class="sxs-lookup"><span data-stu-id="e4aa1-136">Requirement</span></span> | <span data-ttu-id="e4aa1-137">Значение</span><span class="sxs-lookup"><span data-stu-id="e4aa1-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4aa1-138">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="e4aa1-138">Redistributable</span></span><br/> | <span data-ttu-id="e4aa1-139">CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP</span><span class="sxs-lookup"><span data-stu-id="e4aa1-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e4aa1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e4aa1-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="e4aa1-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4aa1-141"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
