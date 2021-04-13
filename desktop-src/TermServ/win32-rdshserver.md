---
title: Класс Win32_RDSHServer
description: Управляет сервером узла сеансов удаленный рабочий стол.
ms.assetid: 2c2840d2-16aa-484a-979b-6dbb1a08bbcf
ms.tgt_platform: multiple
keywords:
- Класс Win32_RDSHServer службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_RDSHServer, описание
topic_type:
- apiref
api_name:
- Win32_RDSHServer
- Win32_RDSHServer.Name
- Win32_RDSHServer.ConnectionBroker
- Win32_RDSHServer.CollectionAlias
- Win32_RDSHServer.ServerState
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6434a4dfe6bc1a79fdaf4576a89ef552cebd5e1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340720"
---
# <a name="win32_rdshserver-class"></a><span data-ttu-id="68284-105">\_Класс Win32 рдшсервер</span><span class="sxs-lookup"><span data-stu-id="68284-105">Win32\_RDSHServer class</span></span>

<span data-ttu-id="68284-106">Управляет сервером узла сеансов удаленный рабочий стол.</span><span class="sxs-lookup"><span data-stu-id="68284-106">Manages a Remote Desktop Session Host (RDSH) server.</span></span>

<span data-ttu-id="68284-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="68284-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="68284-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68284-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDSHServer
{
  string Name;
  string ConnectionBroker;
  string CollectionAlias;
  uint32 ServerState;
};
```

## <a name="members"></a><span data-ttu-id="68284-109">Члены</span><span class="sxs-lookup"><span data-stu-id="68284-109">Members</span></span>

<span data-ttu-id="68284-110">Класс **Win32 \_ рдшсервер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="68284-110">The **Win32\_RDSHServer** class has these types of members:</span></span>

-   [<span data-ttu-id="68284-111">Методы</span><span class="sxs-lookup"><span data-stu-id="68284-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="68284-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="68284-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="68284-113">Методы</span><span class="sxs-lookup"><span data-stu-id="68284-113">Methods</span></span>

<span data-ttu-id="68284-114">Класс **Win32 \_ рдшсервер** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="68284-114">The **Win32\_RDSHServer** class has these methods.</span></span>



| <span data-ttu-id="68284-115">Метод</span><span class="sxs-lookup"><span data-stu-id="68284-115">Method</span></span>                                                                          | <span data-ttu-id="68284-116">Описание</span><span class="sxs-lookup"><span data-stu-id="68284-116">Description</span></span>                                                                                                                                                                       |
|:--------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="68284-117">**GetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="68284-117">**GetInt32Property**</span></span>](getint32property-win32-rdshserver.md)                   | <span data-ttu-id="68284-118">Извлекает значение целочисленного свойства объекта **\_ рдшсервер Win32** .</span><span class="sxs-lookup"><span data-stu-id="68284-118">Retrieves an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                 |
| [<span data-ttu-id="68284-119">**жетпендингстартсерверлист**</span><span class="sxs-lookup"><span data-stu-id="68284-119">**GetPendingStartServerList**</span></span>](win32-rdshserver-getpendingstartserverlist.md) | <span data-ttu-id="68284-120">Возвращает список серверов, ожидающих запуска.</span><span class="sxs-lookup"><span data-stu-id="68284-120">Retrieves a list of server waiting to start.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="68284-121">**жетстрингпроперти**</span><span class="sxs-lookup"><span data-stu-id="68284-121">**GetStringProperty**</span></span>](getstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="68284-122">Извлекает значение свойства строки объекта **Win32 \_ рдшсервер** .</span><span class="sxs-lookup"><span data-stu-id="68284-122">Retrieves a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="68284-123">**SetInt32Property**</span><span class="sxs-lookup"><span data-stu-id="68284-123">**SetInt32Property**</span></span>](setint32property-win32-rdshserver.md)                   | <span data-ttu-id="68284-124">Обновляет значение целочисленного свойства объекта **Win32 \_ рдшсервер** .</span><span class="sxs-lookup"><span data-stu-id="68284-124">Updates an integer property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="68284-125">**сетстрингпроперти**</span><span class="sxs-lookup"><span data-stu-id="68284-125">**SetStringProperty**</span></span>](setstringproperty-win32-rdshserver.md)                 | <span data-ttu-id="68284-126">Обновляет значение свойства строки объекта **Win32 \_ рдшсервер** .</span><span class="sxs-lookup"><span data-stu-id="68284-126">Updates a string property value of a **Win32\_RDSHServer** object.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="68284-127">**тестандсетстате**</span><span class="sxs-lookup"><span data-stu-id="68284-127">**TestAndSetState**</span></span>](win32-rdshserver-testandsetstate.md)                     | <span data-ttu-id="68284-128">Сравнивает текущее состояние с указанным сравниваемый операнд; Если два совпадения, то для состояния задается новое значение.</span><span class="sxs-lookup"><span data-stu-id="68284-128">Compares the current state to the specified comparand; if the two match, the state is set to a new value.</span></span> <span data-ttu-id="68284-129">Независимо от соответствия, также возвращается текущее состояние.</span><span class="sxs-lookup"><span data-stu-id="68284-129">Regardless of the match, the current state is also returned.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="68284-130">Свойства</span><span class="sxs-lookup"><span data-stu-id="68284-130">Properties</span></span>

<span data-ttu-id="68284-131">Класс **Win32 \_ рдшсервер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="68284-131">The **Win32\_RDSHServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="68284-132">**коллектионалиас**</span><span class="sxs-lookup"><span data-stu-id="68284-132">**CollectionAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68284-133">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68284-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68284-134">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="68284-134">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68284-135">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68284-135">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68284-136">Возвращает и задает псевдоним коллекции узлов сеансов удаленных рабочих столов, которой назначен сервер удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="68284-136">Gets and sets the alias to the RDSH collection to which the RDSH server is assigned.</span></span>

</dd> <dt>

<span data-ttu-id="68284-137">**коннектионброкер**</span><span class="sxs-lookup"><span data-stu-id="68284-137">**ConnectionBroker**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68284-138">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68284-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68284-139">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="68284-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="68284-140">Возвращает и задает имя компонента подключение к удаленному рабочему столу Broker (РДКБ), который управляет доступом пользователей к серверу удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="68284-140">Gets and sets the name of the Remote Desktop Connection Broker (RDCB) that manages user access to the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="68284-141">**Name**</span><span class="sxs-lookup"><span data-stu-id="68284-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68284-142">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="68284-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="68284-143">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="68284-143">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="68284-144">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="68284-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="68284-145">Возвращает и задает имя сервера удаленных рабочих столов.</span><span class="sxs-lookup"><span data-stu-id="68284-145">Gets and sets the name of the RDSH server.</span></span>

</dd> <dt>

<span data-ttu-id="68284-146">**ServerState**</span><span class="sxs-lookup"><span data-stu-id="68284-146">**ServerState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="68284-147">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="68284-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="68284-148">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="68284-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="68284-149">Квалификаторы: [ **необязательно**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="68284-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="68284-150">Описывает состояние сервера.</span><span class="sxs-lookup"><span data-stu-id="68284-150">Describes the state of the server.</span></span> <span data-ttu-id="68284-151">Любое значение, отличное **от \_ Targeted** (3), зарезервировано и должно считаться недопустимым состоянием.</span><span class="sxs-lookup"><span data-stu-id="68284-151">Any value other than **TARGET\_RUNNING** (3) is reserved and should be consider an invalid state.</span></span>

<span data-ttu-id="68284-152">Возможные значения:.</span><span class="sxs-lookup"><span data-stu-id="68284-152">The possible values are.</span></span>

<dt>

<span id="TARGET_UNKNOWN"></span><span id="target_unknown"></span>

<span data-ttu-id="68284-153">**Целевой объект \_ НЕИЗВЕСТНО** (1)</span><span class="sxs-lookup"><span data-stu-id="68284-153">**TARGET\_UNKNOWN** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_RUNNING"></span><span id="target_running"></span>

<span data-ttu-id="68284-154">**Целевой объект \_ РАБОТАЕТ** (3)</span><span class="sxs-lookup"><span data-stu-id="68284-154">**TARGET\_RUNNING** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_INVALID"></span><span id="target_invalid"></span>

<span data-ttu-id="68284-155">**Целевой объект \_ НЕДОПУСТИМое** (8)</span><span class="sxs-lookup"><span data-stu-id="68284-155">**TARGET\_INVALID** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STARTING"></span><span id="target_starting"></span>

<span data-ttu-id="68284-156">**Целевой объект \_ Запуск** (9)</span><span class="sxs-lookup"><span data-stu-id="68284-156">**TARGET\_STARTING** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="TARGET_STOPPING"></span><span id="target_stopping"></span>

<span data-ttu-id="68284-157">**Целевой объект \_ ОСТАНОВКА** (10)</span><span class="sxs-lookup"><span data-stu-id="68284-157">**TARGET\_STOPPING** (10)</span></span>


<span data-ttu-id="68284-158"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="68284-158"></dt> <dd></dd> </dl></span></span>

<span data-ttu-id="68284-159">**Windows server 2012 R2 и Windows server 2012:** Это свойство недоступно до Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="68284-159">**Windows Server 2012 R2 and Windows Server 2012:** This property is unavailable prior to Windows Server 2016.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="68284-160">Требования</span><span class="sxs-lookup"><span data-stu-id="68284-160">Requirements</span></span>



| <span data-ttu-id="68284-161">Требование</span><span class="sxs-lookup"><span data-stu-id="68284-161">Requirement</span></span> | <span data-ttu-id="68284-162">Значение</span><span class="sxs-lookup"><span data-stu-id="68284-162">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="68284-163">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="68284-163">Minimum supported client</span></span><br/> | <span data-ttu-id="68284-164">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="68284-164">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="68284-165">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="68284-165">Minimum supported server</span></span><br/> | <span data-ttu-id="68284-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="68284-166">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="68284-167">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="68284-167">Namespace</span></span><br/>                | <span data-ttu-id="68284-168">Корневой \\ \\ rdms CIMV2</span><span class="sxs-lookup"><span data-stu-id="68284-168">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="68284-169">MOF</span><span class="sxs-lookup"><span data-stu-id="68284-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="68284-170"><dt>Рдманажемент. mof</dt></span><span class="sxs-lookup"><span data-stu-id="68284-170"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="68284-171">DLL</span><span class="sxs-lookup"><span data-stu-id="68284-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68284-172"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68284-172"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="68284-173">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="68284-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68284-174">Поставщик служб удаленный рабочий стол Management Services</span><span class="sxs-lookup"><span data-stu-id="68284-174">Remote Desktop Management Services Provider</span></span>](rdms-api-reference.md)
</dt> </dl>

 

