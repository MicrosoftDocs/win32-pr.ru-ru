---
title: Класс Win32_SessionDirectoryVMMPlugin
description: Представляет подключаемый модуль Virtual Machine Manager (VMM), зарегистрированный в посреднике сеансов.
ms.assetid: b5c5deb1-6c1b-4547-a24a-db3ce6654144
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionDirectoryVMMPlugin службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionDirectoryVMMPlugin, описание
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin.sName
- Win32_SessionDirectoryVMMPlugin.sProvider
- Win32_SessionDirectoryVMMPlugin.sClassID
- Win32_SessionDirectoryVMMPlugin.sServiceLocation
- Win32_SessionDirectoryVMMPlugin.Priority
- Win32_SessionDirectoryVMMPlugin.Enabled
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c5fc6b899eaa264357527eb107e11ad5a40ad67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988336"
---
# <a name="win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="7b705-105">\_Класс Win32 сессиондиректоривммплугин</span><span class="sxs-lookup"><span data-stu-id="7b705-105">Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="7b705-106">Представляет подключаемый модуль Virtual Machine Manager (VMM), зарегистрированный в посреднике сеансов.</span><span class="sxs-lookup"><span data-stu-id="7b705-106">Represents a virtual machine manager (VMM) plug-in registered with a session broker.</span></span>

<span data-ttu-id="7b705-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="7b705-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b705-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7b705-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYVMMPLUGIN_Prov"), AMENDMENT]
class Win32_SessionDirectoryVMMPlugin
{
  string  sName;
  string  sProvider;
  string  sClassID;
  string  sServiceLocation;
  sint32  Priority = 0;
  boolean Enabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="7b705-109">Члены</span><span class="sxs-lookup"><span data-stu-id="7b705-109">Members</span></span>

<span data-ttu-id="7b705-110">Класс **Win32 \_ сессиондиректоривммплугин** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="7b705-110">The **Win32\_SessionDirectoryVMMPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="7b705-111">Методы</span><span class="sxs-lookup"><span data-stu-id="7b705-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="7b705-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b705-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7b705-113">Методы</span><span class="sxs-lookup"><span data-stu-id="7b705-113">Methods</span></span>

<span data-ttu-id="7b705-114">Класс **Win32 \_ сессиондиректоривммплугин** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="7b705-114">The **Win32\_SessionDirectoryVMMPlugin** class has these methods.</span></span>



| <span data-ttu-id="7b705-115">Метод</span><span class="sxs-lookup"><span data-stu-id="7b705-115">Method</span></span>                                                                             | <span data-ttu-id="7b705-116">Описание</span><span class="sxs-lookup"><span data-stu-id="7b705-116">Description</span></span>                                                   |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------|
| [<span data-ttu-id="7b705-117">**жеткуррентвммплугин**</span><span class="sxs-lookup"><span data-stu-id="7b705-117">**GetCurrentVMMPlugin**</span></span>](getcurrentvmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="7b705-118">Возвращает подключаемый модуль наивысшего приоритета, который включен.</span><span class="sxs-lookup"><span data-stu-id="7b705-118">Gets the highest priority plug-in that is enabled.</span></span><br/> |
| [<span data-ttu-id="7b705-119">**регистервммплугин**</span><span class="sxs-lookup"><span data-stu-id="7b705-119">**RegisterVMMPlugin**</span></span>](registervmmplugin-win32-sessiondirectoryvmmplugin.md)     | <span data-ttu-id="7b705-120">Регистрирует новый подключаемый модуль VMM.</span><span class="sxs-lookup"><span data-stu-id="7b705-120">Registers a new VMM plug-in.</span></span><br/>                       |
| [<span data-ttu-id="7b705-121">**сетенаблед**</span><span class="sxs-lookup"><span data-stu-id="7b705-121">**SetEnabled**</span></span>](setenabled-win32-sessiondirectoryvmmplugin.md)                   | <span data-ttu-id="7b705-122">Включает или отключает подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="7b705-122">Enables or disables the plug-in.</span></span><br/>                   |
| [<span data-ttu-id="7b705-123">**SetName**</span><span class="sxs-lookup"><span data-stu-id="7b705-123">**SetName**</span></span>](setname-win32-sessiondirectoryvmmplugin.md)                         | <span data-ttu-id="7b705-124">Задает имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-124">Sets the name of the plug-in.</span></span><br/>                      |
| [<span data-ttu-id="7b705-125">**SetPriority**</span><span class="sxs-lookup"><span data-stu-id="7b705-125">**SetPriority**</span></span>](setpriority-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="7b705-126">Задает приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-126">Sets the priority of the plug-in.</span></span><br/>                  |
| [<span data-ttu-id="7b705-127">**сетпровидер**</span><span class="sxs-lookup"><span data-stu-id="7b705-127">**SetProvider**</span></span>](setprovider-win32-sessiondirectoryvmmplugin.md)                 | <span data-ttu-id="7b705-128">Задает имя поставщика подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-128">Sets the provider name of the plug-in.</span></span><br/>             |
| [<span data-ttu-id="7b705-129">**сетсервицелокатион**</span><span class="sxs-lookup"><span data-stu-id="7b705-129">**SetServiceLocation**</span></span>](setservicelocation-win32-sessiondirectoryvmmplugin.md)   | <span data-ttu-id="7b705-130">Задает расположение службы подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-130">Sets the service location of the plug-in.</span></span><br/>          |
| [<span data-ttu-id="7b705-131">**унрегистервммплугин**</span><span class="sxs-lookup"><span data-stu-id="7b705-131">**UnregisterVMMPlugin**</span></span>](unregistervmmplugin-win32-sessiondirectoryvmmplugin.md) | <span data-ttu-id="7b705-132">Отменяет регистрацию подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-132">Unregisters the plug-in.</span></span><br/>                           |



 

### <a name="properties"></a><span data-ttu-id="7b705-133">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b705-133">Properties</span></span>

<span data-ttu-id="7b705-134">Класс **Win32 \_ сессиондиректоривммплугин** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="7b705-134">The **Win32\_SessionDirectoryVMMPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b705-135">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="7b705-135">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b705-136">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="7b705-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b705-137">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b705-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b705-138">Указывает, включен ли или отключен подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="7b705-138">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="7b705-139">**Значение true** , если подключаемый модуль включен или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7b705-139">**True** if the plug-in is enabled or **false** otherwise.</span></span> <span data-ttu-id="7b705-140">По умолчанию подключаемый модуль отключен.</span><span class="sxs-lookup"><span data-stu-id="7b705-140">The plug-in is disabled by default.</span></span>

</dd> <dt>

<span data-ttu-id="7b705-141">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="7b705-141">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b705-142">Тип данных: **Sint32**</span><span class="sxs-lookup"><span data-stu-id="7b705-142">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b705-143">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b705-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b705-144">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7b705-144">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7b705-145">Приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-145">The priority of the plug-in.</span></span> <span data-ttu-id="7b705-146">Чем выше значение, тем выше приоритет подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-146">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="7b705-147">По умолчанию приоритет равен нулю.</span><span class="sxs-lookup"><span data-stu-id="7b705-147">The priority is zero by default.</span></span>

</dd> <dt>

<span data-ttu-id="7b705-148">**склассид**</span><span class="sxs-lookup"><span data-stu-id="7b705-148">**sClassID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b705-149">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b705-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b705-150">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b705-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b705-151">Идентификатор класса подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-151">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="7b705-152">**sName**</span><span class="sxs-lookup"><span data-stu-id="7b705-152">**sName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b705-153">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b705-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b705-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b705-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b705-155">Имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-155">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="7b705-156">**спровидер**</span><span class="sxs-lookup"><span data-stu-id="7b705-156">**sProvider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b705-157">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b705-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b705-158">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b705-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b705-159">Имя поставщика подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="7b705-159">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="7b705-160">**ссервицелокатион**</span><span class="sxs-lookup"><span data-stu-id="7b705-160">**sServiceLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b705-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="7b705-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b705-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="7b705-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b705-163">Расположение службы, с которой должен связаться подключаемый модуль.</span><span class="sxs-lookup"><span data-stu-id="7b705-163">The service location that the plug-in should contact.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b705-164">Требования</span><span class="sxs-lookup"><span data-stu-id="7b705-164">Requirements</span></span>



| <span data-ttu-id="7b705-165">Требование</span><span class="sxs-lookup"><span data-stu-id="7b705-165">Requirement</span></span> | <span data-ttu-id="7b705-166">Значение</span><span class="sxs-lookup"><span data-stu-id="7b705-166">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b705-167">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7b705-167">Minimum supported client</span></span><br/> | <span data-ttu-id="7b705-168">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="7b705-168">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7b705-169">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7b705-169">Minimum supported server</span></span><br/> | <span data-ttu-id="7b705-170">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7b705-170">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="7b705-171">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="7b705-171">Namespace</span></span><br/>                | <span data-ttu-id="7b705-172">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="7b705-172">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="7b705-173">MOF</span><span class="sxs-lookup"><span data-stu-id="7b705-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b705-174"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b705-174"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b705-175">DLL</span><span class="sxs-lookup"><span data-stu-id="7b705-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b705-176"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b705-176"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

