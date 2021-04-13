---
description: Предоставляет стандартные методы COM для управления элементами данных защищенного хранилища.
ms.assetid: 6a4200ed-c3cf-4d6c-8936-22261e670087
title: Интерфейс Ипсторе (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPStore
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 4193e21255445c397bfab6439c4890789b8c5562
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105647946"
---
# <a name="ipstore-interface"></a><span data-ttu-id="f40dd-103">Интерфейс Ипсторе</span><span class="sxs-lookup"><span data-stu-id="f40dd-103">IPStore interface</span></span>

<span data-ttu-id="f40dd-104">\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f40dd-104">\[Protected Storage (Pstore) is available for use in Windows Server 2003 and Windows XP.</span></span> <span data-ttu-id="f40dd-105">Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях.</span><span class="sxs-lookup"><span data-stu-id="f40dd-105">It is only available for read-only operations in Windows Server 2008 and Windows Vista, but may be unavailable in subsequent versions.</span></span> <span data-ttu-id="f40dd-106">PStore использует старую реализацию защиты данных.</span><span class="sxs-lookup"><span data-stu-id="f40dd-106">Pstore uses an older implementation of data protection.</span></span> <span data-ttu-id="f40dd-107">Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]</span><span class="sxs-lookup"><span data-stu-id="f40dd-107">Developers are strongly encouraged to take advantage of the stronger data protection provided by the [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) and [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) functions.\]</span></span>

<span data-ttu-id="f40dd-108">\[Этот интерфейс может быть изменен или недоступен в будущих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f40dd-108">\[This interface may be altered or unavailable in future versions of Windows.\]</span></span>

<span data-ttu-id="f40dd-109">Предоставляет стандартные методы COM для управления элементами данных защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f40dd-109">Provides COM-standard methods to manage protected storage data items.</span></span> <span data-ttu-id="f40dd-110">Метод [**псторекреатеинстанце**](pstorecreateinstance.md) возвращает указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="f40dd-110">The [**PStoreCreateInstance**](pstorecreateinstance.md) method returns a pointer to this interface.</span></span>

## <a name="members"></a><span data-ttu-id="f40dd-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="f40dd-111">Members</span></span>

<span data-ttu-id="f40dd-112">Интерфейс **ипсторе** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f40dd-112">The **IPStore** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f40dd-113">**Ипсторе** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="f40dd-113">**IPStore** also has these types of members:</span></span>

-   [<span data-ttu-id="f40dd-114">Методы</span><span class="sxs-lookup"><span data-stu-id="f40dd-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f40dd-115">Методы</span><span class="sxs-lookup"><span data-stu-id="f40dd-115">Methods</span></span>

<span data-ttu-id="f40dd-116">Интерфейс **ипсторе** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="f40dd-116">The **IPStore** interface has these methods.</span></span>



| <span data-ttu-id="f40dd-117">Метод</span><span class="sxs-lookup"><span data-stu-id="f40dd-117">Method</span></span>                                                   | <span data-ttu-id="f40dd-118">Описание</span><span class="sxs-lookup"><span data-stu-id="f40dd-118">Description</span></span>                                                                                                           |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f40dd-119">**клосеитем**</span><span class="sxs-lookup"><span data-stu-id="f40dd-119">**CloseItem**</span></span>](ipstore-closeitem.md)                   | <span data-ttu-id="f40dd-120">Закрывает указанный элемент данных из защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f40dd-120">Closes a specified data item from protected storage.</span></span><br/>                                                       |
| [<span data-ttu-id="f40dd-121">**креатесубтипе**</span><span class="sxs-lookup"><span data-stu-id="f40dd-121">**CreateSubtype**</span></span>](ipstore-createsubtype.md)           | <span data-ttu-id="f40dd-122">Создает указанный подтип в указанном типе.</span><span class="sxs-lookup"><span data-stu-id="f40dd-122">Creates the specified subtype within the specified type.</span></span><br/>                                                   |
| [<span data-ttu-id="f40dd-123">**CreateType**</span><span class="sxs-lookup"><span data-stu-id="f40dd-123">**CreateType**</span></span>](ipstore-createtype.md)                 | <span data-ttu-id="f40dd-124">Создает указанный тип с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="f40dd-124">Creates the specified type with the specified name.</span></span><br/>                                                        |
| [<span data-ttu-id="f40dd-125">**DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="f40dd-125">**DeleteItem**</span></span>](ipstore-deleteitem.md)                 | <span data-ttu-id="f40dd-126">Удаляет указанный элемент из защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f40dd-126">Deletes the specified item from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="f40dd-127">**делетесубтипе**</span><span class="sxs-lookup"><span data-stu-id="f40dd-127">**DeleteSubtype**</span></span>](ipstore-deletesubtype.md)           | <span data-ttu-id="f40dd-128">Удаляет указанный подтип элемента из защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f40dd-128">Deletes the specified item subtype from the protected storage.</span></span><br/>                                             |
| [<span data-ttu-id="f40dd-129">**делететипе**</span><span class="sxs-lookup"><span data-stu-id="f40dd-129">**DeleteType**</span></span>](ipstore-deletetype.md)                 | <span data-ttu-id="f40dd-130">Удаляет указанный тип из защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f40dd-130">Deletes the specified type from the protected storage.</span></span><br/>                                                     |
| [<span data-ttu-id="f40dd-131">**енумитемс**</span><span class="sxs-lookup"><span data-stu-id="f40dd-131">**EnumItems**</span></span>](ipstore-enumitems.md)                   | <span data-ttu-id="f40dd-132">Возвращает указатель интерфейса подтипа для перечисления элементов в защищенной базе данных хранилища.</span><span class="sxs-lookup"><span data-stu-id="f40dd-132">Returns the interface pointer of a subtype for enumerating items in the protected storage database.</span></span><br/>        |
| [<span data-ttu-id="f40dd-133">**енумсубтипес**</span><span class="sxs-lookup"><span data-stu-id="f40dd-133">**EnumSubtypes**</span></span>](ipstore-enumsubtypes.md)             | <span data-ttu-id="f40dd-134">Возвращает интерфейс для перечисления подтипов типов, зарегистрированных в настоящий момент в защищенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="f40dd-134">Returns an interface for enumerating subtypes of the types currently registered in the protected database.</span></span><br/> |
| [<span data-ttu-id="f40dd-135">**енумтипес**</span><span class="sxs-lookup"><span data-stu-id="f40dd-135">**EnumTypes**</span></span>](ipstore-enumtypes.md)                   | <span data-ttu-id="f40dd-136">Возвращает интерфейс для перечисления типов, зарегистрированных в настоящий момент в защищенной базе данных.</span><span class="sxs-lookup"><span data-stu-id="f40dd-136">Returns an interface for enumerating the types currently registered in the protected database.</span></span><br/>             |
| [<span data-ttu-id="f40dd-137">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="f40dd-137">**GetInfo**</span></span>](ipstore-getinfo.md)                       | <span data-ttu-id="f40dd-138">Извлекает сведения о поставщике хранилища.</span><span class="sxs-lookup"><span data-stu-id="f40dd-138">Retrieves information about the storage provider.</span></span><br/>                                                          |
| [<span data-ttu-id="f40dd-139">**жетпровпарам**</span><span class="sxs-lookup"><span data-stu-id="f40dd-139">**GetProvParam**</span></span>](ipstore-getprovparam.md)             | <span data-ttu-id="f40dd-140">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="f40dd-140">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="f40dd-141">**жетсубтипеинфо**</span><span class="sxs-lookup"><span data-stu-id="f40dd-141">**GetSubtypeInfo**</span></span>](ipstore-getsubtypeinfo.md)         | <span data-ttu-id="f40dd-142">Извлекает сведения, связанные с подтипом.</span><span class="sxs-lookup"><span data-stu-id="f40dd-142">Retrieves information associated with a subtype.</span></span><br/>                                                           |
| [<span data-ttu-id="f40dd-143">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="f40dd-143">**GetTypeInfo**</span></span>](ipstore-gettypeinfo.md)               | <span data-ttu-id="f40dd-144">Извлекает сведения, связанные с типом.</span><span class="sxs-lookup"><span data-stu-id="f40dd-144">Retrieves information associated with a type.</span></span><br/>                                                              |
| [<span data-ttu-id="f40dd-145">**опенитем**</span><span class="sxs-lookup"><span data-stu-id="f40dd-145">**OpenItem**</span></span>](ipstore-openitem.md)                     | <span data-ttu-id="f40dd-146">Открывает элемент для нескольких обращений.</span><span class="sxs-lookup"><span data-stu-id="f40dd-146">Opens an item for multiple accesses.</span></span><br/>                                                                       |
| [<span data-ttu-id="f40dd-147">**реадакцессрулесет**</span><span class="sxs-lookup"><span data-stu-id="f40dd-147">**ReadAccessRuleSet**</span></span>](ipstore-readaccessruleset.md)   | <span data-ttu-id="f40dd-148">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="f40dd-148">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="f40dd-149">**ReadItem**</span><span class="sxs-lookup"><span data-stu-id="f40dd-149">**ReadItem**</span></span>](ipstore-readitem.md)                     | <span data-ttu-id="f40dd-150">Считывает указанный элемент данных из защищенного хранилища.</span><span class="sxs-lookup"><span data-stu-id="f40dd-150">Reads the specified data item from protected storage.</span></span><br/>                                                      |
| [<span data-ttu-id="f40dd-151">**сетпровпарам**</span><span class="sxs-lookup"><span data-stu-id="f40dd-151">**SetProvParam**</span></span>](ipstore-setprovparam.md)             | <span data-ttu-id="f40dd-152">Задает сведения о заданных параметрах.</span><span class="sxs-lookup"><span data-stu-id="f40dd-152">Sets the specified parameter information.</span></span><br/>                                                                  |
| [<span data-ttu-id="f40dd-153">**вритеакцессрулесет**</span><span class="sxs-lookup"><span data-stu-id="f40dd-153">**WriteAccessRuleset**</span></span>](ipstore-writeaccessruleset.md) | <span data-ttu-id="f40dd-154">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="f40dd-154">Not implemented.</span></span><br/>                                                                                           |
| [<span data-ttu-id="f40dd-155">**вритеитем**</span><span class="sxs-lookup"><span data-stu-id="f40dd-155">**WriteItem**</span></span>](ipstore-writeitem.md)                   | <span data-ttu-id="f40dd-156">Записывает элемент данных в защищенное хранилище.</span><span class="sxs-lookup"><span data-stu-id="f40dd-156">Writes a data item to protected storage.</span></span><br/>                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="f40dd-157">Требования</span><span class="sxs-lookup"><span data-stu-id="f40dd-157">Requirements</span></span>



| <span data-ttu-id="f40dd-158">Требование</span><span class="sxs-lookup"><span data-stu-id="f40dd-158">Requirement</span></span> | <span data-ttu-id="f40dd-159">Значение</span><span class="sxs-lookup"><span data-stu-id="f40dd-159">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f40dd-160">Header</span><span class="sxs-lookup"><span data-stu-id="f40dd-160">Header</span></span><br/> | <dl> <span data-ttu-id="f40dd-161"><dt>PStore. h</dt></span><span class="sxs-lookup"><span data-stu-id="f40dd-161"><dt>Pstore.h</dt></span></span> </dl>    |
| <span data-ttu-id="f40dd-162">DLL</span><span class="sxs-lookup"><span data-stu-id="f40dd-162">DLL</span></span><br/>    | <dl> <span data-ttu-id="f40dd-163"><dt>Pstorec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f40dd-163"><dt>Pstorec.dll</dt></span></span> </dl> |



 

 
