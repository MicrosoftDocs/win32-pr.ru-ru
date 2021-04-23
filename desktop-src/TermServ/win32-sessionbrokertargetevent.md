---
title: Класс Win32_SessionBrokerTargetEvent
description: Представляет изменение целевого объекта посредника сеансов.
ms.assetid: ee3ae0ed-eb8b-4777-9b9e-0e50722cf52a
ms.tgt_platform: multiple
keywords:
- Класс Win32_SessionBrokerTargetEvent службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_SessionBrokerTargetEvent, описание
topic_type:
- apiref
api_name:
- Win32_SessionBrokerTargetEvent
- Win32_SessionBrokerTargetEvent.SECURITY_DESCRIPTOR
- Win32_SessionBrokerTargetEvent.TIME_CREATED
- Win32_SessionBrokerTargetEvent.ChangeType
- Win32_SessionBrokerTargetEvent.PluginName
- Win32_SessionBrokerTargetEvent.TargetName
- Win32_SessionBrokerTargetEvent.FarmName
- Win32_SessionBrokerTargetEvent.Guid
- Win32_SessionBrokerTargetEvent.Environment
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d7f1cf6aab1c4497ce85cb93318c9ca79368853
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801678"
---
# <a name="win32_sessionbrokertargetevent-class"></a><span data-ttu-id="d0f65-105">\_Класс Win32 сессионброкертаржетевент</span><span class="sxs-lookup"><span data-stu-id="d0f65-105">Win32\_SessionBrokerTargetEvent class</span></span>

<span data-ttu-id="d0f65-106">Представляет изменение целевого объекта посредника сеансов.</span><span class="sxs-lookup"><span data-stu-id="d0f65-106">Represents a change to a session broker target.</span></span>

<span data-ttu-id="d0f65-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="d0f65-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0f65-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0f65-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class Win32_SessionBrokerTargetEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  uint32 ChangeType;
  string PluginName;
  string TargetName;
  string FarmName;
  string Guid;
  string Environment;
};
```

## <a name="members"></a><span data-ttu-id="d0f65-109">Члены</span><span class="sxs-lookup"><span data-stu-id="d0f65-109">Members</span></span>

<span data-ttu-id="d0f65-110">Класс **Win32 \_ сессионброкертаржетевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="d0f65-110">The **Win32\_SessionBrokerTargetEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="d0f65-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="d0f65-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0f65-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="d0f65-112">Properties</span></span>

<span data-ttu-id="d0f65-113">Класс **Win32 \_ сессионброкертаржетевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="d0f65-113">The **Win32\_SessionBrokerTargetEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d0f65-114">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="d0f65-114">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0f65-115">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0f65-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d0f65-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0f65-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0f65-117">Указывает произошедшее изменение.</span><span class="sxs-lookup"><span data-stu-id="d0f65-117">Specifies the change that occurred.</span></span> <span data-ttu-id="d0f65-118">Это может быть одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="d0f65-118">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="d0f65-119">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d0f65-119">1 (0x1)</span></span>
</dt> <dd>

<span data-ttu-id="d0f65-120">Тип изменения не указан.</span><span class="sxs-lookup"><span data-stu-id="d0f65-120">The type of change is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-121">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="d0f65-121">2 (0x2)</span></span>
</dt> <dd>

<span data-ttu-id="d0f65-122">Внешний IP-адрес изменился.</span><span class="sxs-lookup"><span data-stu-id="d0f65-122">The external IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-123">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d0f65-123">4 (0x4)</span></span>
</dt> <dd>

<span data-ttu-id="d0f65-124">Внутренний IP-адрес изменился.</span><span class="sxs-lookup"><span data-stu-id="d0f65-124">The internal IP address has changed.</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-125">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d0f65-125">8 (0x8)</span></span>
</dt> <dd>

<span data-ttu-id="d0f65-126">Цель была присоединена.</span><span class="sxs-lookup"><span data-stu-id="d0f65-126">The target was joined.</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-127">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="d0f65-127">16 (0x10)</span></span>
</dt> <dd>

<span data-ttu-id="d0f65-128">Цель удалена.</span><span class="sxs-lookup"><span data-stu-id="d0f65-128">The target was removed.</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-129">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="d0f65-129">32 (0x20)</span></span>
</dt> <dd>

<span data-ttu-id="d0f65-130">Состояние целевого объекта изменилось.</span><span class="sxs-lookup"><span data-stu-id="d0f65-130">The state of the target has changed.</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-131">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="d0f65-131">64 (0x40)</span></span>
</dt> <dd>

<span data-ttu-id="d0f65-132">Целевой объект бездействует.</span><span class="sxs-lookup"><span data-stu-id="d0f65-132">The target is idle.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d0f65-133">**Среда**</span><span class="sxs-lookup"><span data-stu-id="d0f65-133">**Environment**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0f65-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0f65-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0f65-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0f65-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0f65-136">Имя среды.</span><span class="sxs-lookup"><span data-stu-id="d0f65-136">The environment name.</span></span> <span data-ttu-id="d0f65-137">В случае целевого объекта виртуальной машины это может быть имя узла виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d0f65-137">In the case of a virtual machine (VM) target, this could be the VM host name.</span></span>

<span data-ttu-id="d0f65-138">**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0f65-138">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-139">**фармнаме**</span><span class="sxs-lookup"><span data-stu-id="d0f65-139">**FarmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0f65-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0f65-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0f65-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0f65-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0f65-142">Имя фермы, которой принадлежит целевой объект.</span><span class="sxs-lookup"><span data-stu-id="d0f65-142">The name of the farm the target belongs to.</span></span>

<span data-ttu-id="d0f65-143">**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0f65-143">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-144">**Устройства**</span><span class="sxs-lookup"><span data-stu-id="d0f65-144">**Guid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0f65-145">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0f65-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0f65-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0f65-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0f65-147">Идентификатор GUID целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="d0f65-147">The GUID of the target.</span></span>

<span data-ttu-id="d0f65-148">**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0f65-148">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-149">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="d0f65-149">**PluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0f65-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0f65-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0f65-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0f65-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0f65-152">Имя подключаемого модуля.</span><span class="sxs-lookup"><span data-stu-id="d0f65-152">The name of the plug-in.</span></span>

<span data-ttu-id="d0f65-153">**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0f65-153">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-154">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="d0f65-154">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0f65-155">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="d0f65-155">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="d0f65-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0f65-156">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0f65-157">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="d0f65-157">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="d0f65-158">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="d0f65-158">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="d0f65-159">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="d0f65-159">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-160">**TargetName**</span><span class="sxs-lookup"><span data-stu-id="d0f65-160">**TargetName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0f65-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="d0f65-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d0f65-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0f65-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0f65-163">Имя целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="d0f65-163">The name of the target.</span></span>

<span data-ttu-id="d0f65-164">**Windows Server 2008 R2:** Это свойство недоступно до Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d0f65-164">**Windows Server 2008 R2:** This property is unavailable prior to Windows Server 2012</span></span>

</dd> <dt>

<span data-ttu-id="d0f65-165">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="d0f65-165">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d0f65-166">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d0f65-166">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d0f65-167">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="d0f65-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d0f65-168">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="d0f65-168">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="d0f65-169">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="d0f65-169">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="d0f65-170">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="d0f65-170">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="d0f65-171">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="d0f65-171">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="d0f65-172">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="d0f65-172">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d0f65-173">Требования</span><span class="sxs-lookup"><span data-stu-id="d0f65-173">Requirements</span></span>



| <span data-ttu-id="d0f65-174">Требование</span><span class="sxs-lookup"><span data-stu-id="d0f65-174">Requirement</span></span> | <span data-ttu-id="d0f65-175">Значение</span><span class="sxs-lookup"><span data-stu-id="d0f65-175">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d0f65-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d0f65-176">Minimum supported client</span></span><br/> | <span data-ttu-id="d0f65-177">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d0f65-177">None supported</span></span><br/>                                                              |
| <span data-ttu-id="d0f65-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d0f65-178">Minimum supported server</span></span><br/> | <span data-ttu-id="d0f65-179">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d0f65-179">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="d0f65-180">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d0f65-180">Namespace</span></span><br/>                | <span data-ttu-id="d0f65-181">Корневой \\ CIMv2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="d0f65-181">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="d0f65-182">MOF</span><span class="sxs-lookup"><span data-stu-id="d0f65-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d0f65-183"><dt>Тссдвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d0f65-183"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d0f65-184">DLL</span><span class="sxs-lookup"><span data-stu-id="d0f65-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0f65-185"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0f65-185"><dt>TssdWmi.dll</dt></span></span> </dl> |



 

