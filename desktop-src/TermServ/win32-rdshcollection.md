---
title: Класс Win32_RDSHCollection
description: Управляет коллекцией узлов сеансов удаленный рабочий стол.
ms.assetid: 7800bf2e-9497-4e41-aed9-b318748dd83f
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDSHCollection службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDSHCollection, описание
topic_type:
- apiref
api_name:
- Win32_RDSHCollection
- Win32_RDSHCollection.Alias
- Win32_RDSHCollection.Name
- Win32_RDSHCollection.Description
- Win32_RDSHCollection.Type
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8196747714337890d0b27ef6db8d488eedc32fc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490971"
---
# <a name="win32_rdshcollection-class"></a><span data-ttu-id="ced81-105">\_Класс Win32 рдшколлектион</span><span class="sxs-lookup"><span data-stu-id="ced81-105">Win32\_RDSHCollection class</span></span>

<span data-ttu-id="ced81-106">Управляет коллекцией узлов сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="ced81-106">Manages a collection of Remote Desktop Session Hosts.</span></span>

<span data-ttu-id="ced81-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="ced81-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ced81-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ced81-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHCollection
{
  string Alias;
  string Name;
  string Description;
  uint32 Type;
};
```

## <a name="members"></a><span data-ttu-id="ced81-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ced81-109">Members</span></span>

<span data-ttu-id="ced81-110">Класс **Win32 \_ рдшколлектион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ced81-110">The **Win32\_RDSHCollection** class has these types of members:</span></span>

-   [<span data-ttu-id="ced81-111">Методы</span><span class="sxs-lookup"><span data-stu-id="ced81-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ced81-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ced81-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ced81-113">Методы</span><span class="sxs-lookup"><span data-stu-id="ced81-113">Methods</span></span>

<span data-ttu-id="ced81-114">Класс **Win32 \_ рдшколлектион** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="ced81-114">The **Win32\_RDSHCollection** class has these methods.</span></span>



| <span data-ttu-id="ced81-115">Метод</span><span class="sxs-lookup"><span data-stu-id="ced81-115">Method</span></span>                                                                      | <span data-ttu-id="ced81-116">Описание</span><span class="sxs-lookup"><span data-stu-id="ced81-116">Description</span></span>                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ced81-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="ced81-117">**GetInt32Property**</span></span>](getint32property-win32-rdshcollection.md)           | <span data-ttu-id="ced81-118">Извлекает значение целочисленного свойства объекта **\_ рдшколлектион Win32** .</span><span class="sxs-lookup"><span data-stu-id="ced81-118">Retrieves an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                  |
| [<span data-ttu-id="ced81-119">**жетстрингпроперти**</span><span class="sxs-lookup"><span data-stu-id="ced81-119">**GetStringProperty**</span></span>](getstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="ced81-120">Извлекает значение свойства строки объекта **Win32 \_ рдшколлектион** .</span><span class="sxs-lookup"><span data-stu-id="ced81-120">Retrieves a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="ced81-121">**кэйвалуекомпареандсет**</span><span class="sxs-lookup"><span data-stu-id="ced81-121">**KeyValueCompareAndSet**</span></span>](win32-rdshcollection-keyvaluecompareandset.md) | <span data-ttu-id="ced81-122">Сравнивает указанный ключ в коллекции с сравниваемый операнд; Если они совпадают, для ключа задается новое значение.</span><span class="sxs-lookup"><span data-stu-id="ced81-122">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="ced81-123">Если ключ не существует, метод вставит ключ в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="ced81-123">If the key does not exist, the method will insert the key into the collection.</span></span><br/> |
| [<span data-ttu-id="ced81-124">**кэйвалуеделете**</span><span class="sxs-lookup"><span data-stu-id="ced81-124">**KeyValueDelete**</span></span>](win32-rdshcollection-keyvaluedelete.md)               | <span data-ttu-id="ced81-125">Удаляет из коллекции указанный ключ (и связанное значение).</span><span class="sxs-lookup"><span data-stu-id="ced81-125">Deletes the specified key (and associated value) from the collection.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="ced81-126">**кэйвалуежет**</span><span class="sxs-lookup"><span data-stu-id="ced81-126">**KeyValueGet**</span></span>](win32-rdshcollection-keyvalueget.md)                     | <span data-ttu-id="ced81-127">Извлекает значение, связанное с указанным ключом в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ced81-127">Retrieves the value associated with the specified key in the collection.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="ced81-128">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="ced81-128">**SetInt32Property**</span></span>](setint32property-win32-rdshcollection.md)           | <span data-ttu-id="ced81-129">Обновляет значение целочисленного свойства объекта **Win32 \_ рдшколлектион** .</span><span class="sxs-lookup"><span data-stu-id="ced81-129">Updates an integer property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="ced81-130">**сетстрингпроперти**</span><span class="sxs-lookup"><span data-stu-id="ced81-130">**SetStringProperty**</span></span>](setstringproperty-win32-rdshcollection.md)         | <span data-ttu-id="ced81-131">Обновляет значение свойства строки объекта **Win32 \_ рдшколлектион** .</span><span class="sxs-lookup"><span data-stu-id="ced81-131">Updates a string property value of a **Win32\_RDSHCollection** object.</span></span><br/>                                                                                                                      |



 

### <a name="properties"></a><span data-ttu-id="ced81-132">Свойства</span><span class="sxs-lookup"><span data-stu-id="ced81-132">Properties</span></span>

<span data-ttu-id="ced81-133">Класс **Win32 \_ рдшколлектион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ced81-133">The **Win32\_RDSHCollection** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ced81-134">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="ced81-134">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ced81-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ced81-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ced81-136">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ced81-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ced81-137">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ced81-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ced81-138">Возвращает и задает псевдоним коллекции.</span><span class="sxs-lookup"><span data-stu-id="ced81-138">Gets and sets the alias of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="ced81-139">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ced81-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ced81-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ced81-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ced81-141">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ced81-141">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ced81-142">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="ced81-142">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="ced81-143">Возвращает и задает описание коллекции.</span><span class="sxs-lookup"><span data-stu-id="ced81-143">Gets and sets the description of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="ced81-144">**Name**</span><span class="sxs-lookup"><span data-stu-id="ced81-144">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ced81-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ced81-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ced81-146">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ced81-146">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ced81-147">Возвращает и задает имя коллекции.</span><span class="sxs-lookup"><span data-stu-id="ced81-147">Gets and sets the name of the collection.</span></span>

</dd> <dt>

<span data-ttu-id="ced81-148">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ced81-148">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ced81-149">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ced81-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ced81-150">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ced81-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="ced81-151">**Windows server 2012 R2 и Windows server 2012:** Это свойство недоступно до Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ced81-151">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

<span data-ttu-id="ced81-152">Тип коллекции.</span><span class="sxs-lookup"><span data-stu-id="ced81-152">The type of collection.</span></span>

<dt>

<span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>

<span data-ttu-id="ced81-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Обычный** (0)</span><span class="sxs-lookup"><span data-stu-id="ced81-153"><span id="Regular"></span><span id="regular"></span><span id="REGULAR"></span>**Regular** (0)</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="ced81-154">(2)</span><span class="sxs-lookup"><span data-stu-id="ced81-154">(2)</span></span>


</dt> <dd>

<span data-ttu-id="ced81-155">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="ced81-155">Reserved</span></span>

</dd> <dt>



 <span data-ttu-id="ced81-156">(3)</span><span class="sxs-lookup"><span data-stu-id="ced81-156">(3)</span></span>


</dt> <dd>

<span data-ttu-id="ced81-157">Зарезервировано</span><span class="sxs-lookup"><span data-stu-id="ced81-157">Reserved</span></span>

</dd> <dt>

<span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>

<span data-ttu-id="ced81-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**Мануалперсонал** (4)</span><span class="sxs-lookup"><span data-stu-id="ced81-158"><span id="ManualPersonal"></span><span id="manualpersonal"></span><span id="MANUALPERSONAL"></span>**ManualPersonal** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>

<span data-ttu-id="ced81-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**Автопользователь** (5)</span><span class="sxs-lookup"><span data-stu-id="ced81-159"><span id="AutoPersonal"></span><span id="autopersonal"></span><span id="AUTOPERSONAL"></span>**AutoPersonal** (5)</span></span>


<span data-ttu-id="ced81-160"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ced81-160"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ced81-161">Требования</span><span class="sxs-lookup"><span data-stu-id="ced81-161">Requirements</span></span>



| <span data-ttu-id="ced81-162">Требование</span><span class="sxs-lookup"><span data-stu-id="ced81-162">Requirement</span></span> | <span data-ttu-id="ced81-163">Значение</span><span class="sxs-lookup"><span data-stu-id="ced81-163">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ced81-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ced81-164">Minimum supported client</span></span><br/> | <span data-ttu-id="ced81-165">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ced81-165">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="ced81-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ced81-166">Minimum supported server</span></span><br/> | <span data-ttu-id="ced81-167">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="ced81-167">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="ced81-168">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ced81-168">Namespace</span></span><br/>                | <span data-ttu-id="ced81-169">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="ced81-169">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="ced81-170">MOF</span><span class="sxs-lookup"><span data-stu-id="ced81-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ced81-171"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ced81-171"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="ced81-172">DLL</span><span class="sxs-lookup"><span data-stu-id="ced81-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ced81-173"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ced81-173"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="ced81-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ced81-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ced81-175">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="ced81-175">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

