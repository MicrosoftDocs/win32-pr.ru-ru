---
title: Класс Win32_CentralPublishingChangeEvent
description: Событие, представляющее изменение центральных параметров RDV.
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Класс Win32_CentralPublishingChangeEvent службы удаленных рабочих столов
- Службы удаленных рабочих столов класса Win32_CentralPublishingChangeEvent, описание
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4695479eb33301bda51b558375a18186fa08161e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491313"
---
# <a name="win32_centralpublishingchangeevent-class"></a><span data-ttu-id="98b5b-105">\_Класс Win32 централпублишингчанжеевент</span><span class="sxs-lookup"><span data-stu-id="98b5b-105">Win32\_CentralPublishingChangeEvent class</span></span>

<span data-ttu-id="98b5b-106">Событие, представляющее изменение центральных параметров RDV.</span><span class="sxs-lookup"><span data-stu-id="98b5b-106">An event that represents a change to the central RDV settings.</span></span>

<span data-ttu-id="98b5b-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="98b5b-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="98b5b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98b5b-108">Syntax</span></span>

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a><span data-ttu-id="98b5b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="98b5b-109">Members</span></span>

<span data-ttu-id="98b5b-110">Класс **Win32 \_ централпублишингчанжеевент** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="98b5b-110">The **Win32\_CentralPublishingChangeEvent** class has these types of members:</span></span>

-   [<span data-ttu-id="98b5b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="98b5b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98b5b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="98b5b-112">Properties</span></span>

<span data-ttu-id="98b5b-113">Класс **Win32 \_ централпублишингчанжеевент** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="98b5b-113">The **Win32\_CentralPublishingChangeEvent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98b5b-114">**OperationType**</span><span class="sxs-lookup"><span data-stu-id="98b5b-114">**OperationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b5b-115">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98b5b-115">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="98b5b-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b5b-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b5b-117">Тип операции, соответствующий событию.</span><span class="sxs-lookup"><span data-stu-id="98b5b-117">The type of operation corresponding to the event.</span></span>

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

<span data-ttu-id="98b5b-118">**CREATE** (0)</span><span class="sxs-lookup"><span data-stu-id="98b5b-118">**Create** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

<span data-ttu-id="98b5b-119">**Изменить** (1)</span><span class="sxs-lookup"><span data-stu-id="98b5b-119">**Modify** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

<span data-ttu-id="98b5b-120">**Delete** (2)</span><span class="sxs-lookup"><span data-stu-id="98b5b-120">**Delete** (2)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="98b5b-121">**\_дескриптор безопасности**</span><span class="sxs-lookup"><span data-stu-id="98b5b-121">**SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b5b-122">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="98b5b-122">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="98b5b-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b5b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b5b-124">Дескриптор, используемый поставщиком событий для определения того, какие пользователи могут получить событие.</span><span class="sxs-lookup"><span data-stu-id="98b5b-124">Descriptor used by the event provider to determine which users can receive the event.</span></span> <span data-ttu-id="98b5b-125">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="98b5b-125">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span> <span data-ttu-id="98b5b-126">Дополнительные сведения о константах, используемых для задания этого дескриптора безопасности, см. в разделе [константы безопасности WMI](/windows/desktop/WmiSdk/wmi-security-constants).</span><span class="sxs-lookup"><span data-stu-id="98b5b-126">For more information about constants used to set this security descriptor, see [WMI Security Constants](/windows/desktop/WmiSdk/wmi-security-constants).</span></span>

</dd> <dt>

<span data-ttu-id="98b5b-127">**TargetInstance**</span><span class="sxs-lookup"><span data-stu-id="98b5b-127">**TargetInstance**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b5b-128">Тип данных: **объект**</span><span class="sxs-lookup"><span data-stu-id="98b5b-128">Data type: **object**</span></span>
</dt> <dt>

<span data-ttu-id="98b5b-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b5b-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b5b-130">Объект изменен операцией, соответствующей событию.</span><span class="sxs-lookup"><span data-stu-id="98b5b-130">Object changed by the operation corresponding to the event.</span></span>

</dd> <dt>

<span data-ttu-id="98b5b-131">**ВРЕМЯ \_ создания**</span><span class="sxs-lookup"><span data-stu-id="98b5b-131">**TIME\_CREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98b5b-132">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="98b5b-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="98b5b-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="98b5b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98b5b-134">Уникальное значение, указывающее время создания события.</span><span class="sxs-lookup"><span data-stu-id="98b5b-134">Unique value that indicates the time at which the event was generated.</span></span> <span data-ttu-id="98b5b-135">Это 64-разрядное значение, представляющее число 100-наносекундных интервалов после 1 января 1601 г.</span><span class="sxs-lookup"><span data-stu-id="98b5b-135">This is a 64-bit value that represents the number of 100-nanosecond intervals after January 1, 1601.</span></span> <span data-ttu-id="98b5b-136">Эти сведения находятся в формате всеобщего скоординированного времени (UTC).</span><span class="sxs-lookup"><span data-stu-id="98b5b-136">The information is in the Coordinated Universal Times (UTC) format.</span></span> <span data-ttu-id="98b5b-137">Это свойство наследуется от [**\_ \_ события**](/windows/desktop/WmiSdk/--event).</span><span class="sxs-lookup"><span data-stu-id="98b5b-137">This property is inherited from [**\_\_Event**](/windows/desktop/WmiSdk/--event).</span></span>

<span data-ttu-id="98b5b-138">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="98b5b-138">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98b5b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="98b5b-139">Requirements</span></span>



| <span data-ttu-id="98b5b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="98b5b-140">Requirement</span></span> | <span data-ttu-id="98b5b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="98b5b-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="98b5b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="98b5b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="98b5b-143">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="98b5b-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="98b5b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="98b5b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="98b5b-145">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="98b5b-145">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="98b5b-146">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="98b5b-146">Namespace</span></span><br/>                | <span data-ttu-id="98b5b-147">Корневой \\ CIMV2 \\ терминалсервицес</span><span class="sxs-lookup"><span data-stu-id="98b5b-147">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="98b5b-148">MOF</span><span class="sxs-lookup"><span data-stu-id="98b5b-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98b5b-149"><dt>Тскпуб. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98b5b-149"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="98b5b-150">DLL</span><span class="sxs-lookup"><span data-stu-id="98b5b-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98b5b-151"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98b5b-151"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

