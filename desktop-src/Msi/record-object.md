---
description: Объект Record — это контейнер для хранения и передачи переменного количества значений.
ms.assetid: e832c19f-61a6-4e42-a10a-b7bb1705af59
title: Объект Record
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Record
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c13cb31d628525e529491af1c089555ba2ad8273
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652049"
---
# <a name="record-object"></a><span data-ttu-id="094df-103">Объект Record</span><span class="sxs-lookup"><span data-stu-id="094df-103">Record object</span></span>

<span data-ttu-id="094df-104">Объект **Record** — это контейнер для хранения и передачи переменного количества значений.</span><span class="sxs-lookup"><span data-stu-id="094df-104">The **Record** object is a container for holding and transferring a variable number of values.</span></span> <span data-ttu-id="094df-105">Поля в записи индексируются с числовым индексом и могут содержать строки, целые числа, объекты и значения NULL.</span><span class="sxs-lookup"><span data-stu-id="094df-105">Fields within the record are numerically indexed and can contain strings, integers, objects, and null values.</span></span> <span data-ttu-id="094df-106">Поля, превышающие размер выделенной записи, обрабатываются как непостоянное значение null.</span><span class="sxs-lookup"><span data-stu-id="094df-106">Fields beyond the allocated record size are treated as having permanently null values.</span></span> <span data-ttu-id="094df-107">Поле с номером 0 зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="094df-107">Field number 0 is reserved.</span></span>

## <a name="members"></a><span data-ttu-id="094df-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="094df-108">Members</span></span>

<span data-ttu-id="094df-109">Объект **Record** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="094df-109">The **Record** object has these types of members:</span></span>

-   [<span data-ttu-id="094df-110">Методы</span><span class="sxs-lookup"><span data-stu-id="094df-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="094df-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="094df-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="094df-112">Методы</span><span class="sxs-lookup"><span data-stu-id="094df-112">Methods</span></span>

<span data-ttu-id="094df-113">Объект **Record** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="094df-113">The **Record** object has these methods.</span></span>



| <span data-ttu-id="094df-114">Метод</span><span class="sxs-lookup"><span data-stu-id="094df-114">Method</span></span>                                  | <span data-ttu-id="094df-115">Описание</span><span class="sxs-lookup"><span data-stu-id="094df-115">Description</span></span>                                                                                          |
|:----------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="094df-116">**клеардата**</span><span class="sxs-lookup"><span data-stu-id="094df-116">**ClearData**</span></span>](record-cleardata.md)   | <span data-ttu-id="094df-117">Очищает данные во всех полях, присвоив им значение null.</span><span class="sxs-lookup"><span data-stu-id="094df-117">Clears the data in all fields, setting them to null.</span></span><br/>                                      |
| [<span data-ttu-id="094df-118">**форматтекст**</span><span class="sxs-lookup"><span data-stu-id="094df-118">**FormatText**</span></span>](record-formattext.md) | <span data-ttu-id="094df-119">Форматирует поля в соответствии с шаблоном в поле 0.</span><span class="sxs-lookup"><span data-stu-id="094df-119">Formats fields according to the template in field 0.</span></span><br/>                                      |
| [<span data-ttu-id="094df-120">**реадстреам**</span><span class="sxs-lookup"><span data-stu-id="094df-120">**ReadStream**</span></span>](record-readstream.md) | <span data-ttu-id="094df-121">Считывает указанное число байтов из поля записи, содержащего потоковые данные.</span><span class="sxs-lookup"><span data-stu-id="094df-121">Reads a specified number of bytes from a record field holding stream data.</span></span><br/>                |
| [<span data-ttu-id="094df-122">**сетстреам**</span><span class="sxs-lookup"><span data-stu-id="094df-122">**SetStream**</span></span>](record-setstream.md)   | <span data-ttu-id="094df-123">Копирует содержимое указанного файла в указанное поле записи в виде потоковых данных.</span><span class="sxs-lookup"><span data-stu-id="094df-123">Copies the content of the specified file into the designated record field as stream data.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="094df-124">Свойства</span><span class="sxs-lookup"><span data-stu-id="094df-124">Properties</span></span>

<span data-ttu-id="094df-125">Объект **Record** имеет эти свойства.</span><span class="sxs-lookup"><span data-stu-id="094df-125">The **Record** object has these properties.</span></span>



| <span data-ttu-id="094df-126">Свойство</span><span class="sxs-lookup"><span data-stu-id="094df-126">Property</span></span>                                             | <span data-ttu-id="094df-127">Тип доступа</span><span class="sxs-lookup"><span data-stu-id="094df-127">Access type</span></span>           | <span data-ttu-id="094df-128">Описание</span><span class="sxs-lookup"><span data-stu-id="094df-128">Description</span></span>                                                                                   |
|:-----------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="094df-129">**DataSize**</span><span class="sxs-lookup"><span data-stu-id="094df-129">**DataSize**</span></span>](record-datasize.md)<br/>       |                       | <span data-ttu-id="094df-130">Возвращает размер данных для указанного поля.</span><span class="sxs-lookup"><span data-stu-id="094df-130">Returns the size of the data for the designated field.</span></span><br/>                             |
| [<span data-ttu-id="094df-131">**FieldCount**</span><span class="sxs-lookup"><span data-stu-id="094df-131">**FieldCount**</span></span>](record-fieldcount.md)<br/>   |                       | <span data-ttu-id="094df-132">Возвращает число полей в записи.</span><span class="sxs-lookup"><span data-stu-id="094df-132">Returns the number of fields in the record.</span></span><br/>                                        |
| [<span data-ttu-id="094df-133">**IntegerData**</span><span class="sxs-lookup"><span data-stu-id="094df-133">**IntegerData**</span></span>](record-integerdata.md)<br/> | <span data-ttu-id="094df-134">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="094df-134">Read/write</span></span><br/> | <span data-ttu-id="094df-135">Передает 32-разрядные целочисленные данные в указанное поле в записи или из него.</span><span class="sxs-lookup"><span data-stu-id="094df-135">Transfers 32-bit integer data in to or out of a specified field within the record.</span></span><br/> |
| [<span data-ttu-id="094df-136">**IsNull**</span><span class="sxs-lookup"><span data-stu-id="094df-136">**IsNull**</span></span>](record-isnull.md)<br/>           |                       | <span data-ttu-id="094df-137">Возвращает значение true, если указанное поле имеет значение null, и false, если поле содержит данные.</span><span class="sxs-lookup"><span data-stu-id="094df-137">Returns True if the indicated field is null and False if the field contains data.</span></span><br/>  |
| [<span data-ttu-id="094df-138">**StringData**</span><span class="sxs-lookup"><span data-stu-id="094df-138">**StringData**</span></span>](record-stringdata.md)<br/>   | <span data-ttu-id="094df-139">Чтение/запись</span><span class="sxs-lookup"><span data-stu-id="094df-139">Read/write</span></span><br/> | <span data-ttu-id="094df-140">Передает строковые данные в указанное поле в записи или из него.</span><span class="sxs-lookup"><span data-stu-id="094df-140">Transfers string data in to or out of a specified field within the record.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="094df-141">Требования</span><span class="sxs-lookup"><span data-stu-id="094df-141">Requirements</span></span>



| <span data-ttu-id="094df-142">Требование</span><span class="sxs-lookup"><span data-stu-id="094df-142">Requirement</span></span> | <span data-ttu-id="094df-143">Значение</span><span class="sxs-lookup"><span data-stu-id="094df-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="094df-144">Версия</span><span class="sxs-lookup"><span data-stu-id="094df-144">Version</span></span><br/> | <span data-ttu-id="094df-145">Установщик Windows 5,0 в Windows Server 2012, Windows 8, Windows Server 2008 R2 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="094df-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="094df-146">Установщик Windows 4,0 или установщик Windows 4,5 на Windows Server 2008 или Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="094df-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="094df-147">установщик Windows в Windows Server 2003 или Windows XP</span><span class="sxs-lookup"><span data-stu-id="094df-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="094df-148">DLL</span><span class="sxs-lookup"><span data-stu-id="094df-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="094df-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="094df-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="094df-150">IID</span><span class="sxs-lookup"><span data-stu-id="094df-150">IID</span></span><br/>     | <span data-ttu-id="094df-151">IID \_ ирекорд определен как 000C1093-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="094df-151">IID\_IRecord is defined as 000C1093-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="094df-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="094df-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="094df-153">**СоздатьЗапись, метод**</span><span class="sxs-lookup"><span data-stu-id="094df-153">**CreateRecord Method**</span></span>](installer-createrecord.md)
</dt> <dt>

[<span data-ttu-id="094df-154">Примеры сценариев установщик Windows</span><span class="sxs-lookup"><span data-stu-id="094df-154">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




