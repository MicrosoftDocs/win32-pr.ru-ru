---
description: Представляет исправленную обработку проверки компьютера (CMC) для переключения из драйвера прерываний для опроса. Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: c5e99e13-0f65-40bc-8863-b2ca7ea221df
title: Класс MSMCAEvent_SwitchToCMCPolling
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_SwitchToCMCPolling
- MSMCAEvent_SwitchToCMCPolling.Active
- MSMCAEvent_SwitchToCMCPolling.InstanceName
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: f7d0d543dc36054550d4ddf6cc1a77ce80cf1647
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343445"
---
# <a name="msmcaevent_switchtocmcpolling-class"></a><span data-ttu-id="441da-104">\_Класс мсмкаевент свитчтокмкполлинг</span><span class="sxs-lookup"><span data-stu-id="441da-104">MSMCAEvent\_SwitchToCMCPolling class</span></span>

<span data-ttu-id="441da-105">Класс **мсмкаевент \_ свитчтокмкполлинг** представляет исправленную обработку проверки компьютера (CMC), которую необходимо переключить из драйвера прерываний для опроса.</span><span class="sxs-lookup"><span data-stu-id="441da-105">The **MSMCAEvent\_SwitchToCMCPolling** class represents the corrected machine check (CMC) handling to be switched from the interrupt driver to polling.</span></span> <span data-ttu-id="441da-106">В некоторых случаях ядро опрашивает уровень абстракции системы (SAL) на предмет ошибки CMC или исправленной платформы (CPE), произошедшей в течение предыдущего интервала опроса.</span><span class="sxs-lookup"><span data-stu-id="441da-106">In some cases, the kernel polls the system abstraction layer (SAL) for any CMC or corrected platform error (CPE) that occurred within the previous polling interval.</span></span> <span data-ttu-id="441da-107">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="441da-107">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="441da-108">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="441da-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="441da-109">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="441da-109">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="441da-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="441da-110">Syntax</span></span>

``` syntax
class MSMCAEvent_SwitchToCMCPolling : WMIEvent
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="441da-111">Члены</span><span class="sxs-lookup"><span data-stu-id="441da-111">Members</span></span>

<span data-ttu-id="441da-112">Класс **мсмкаевент \_ свитчтокмкполлинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="441da-112">The **MSMCAEvent\_SwitchToCMCPolling** class has these types of members:</span></span>

-   [<span data-ttu-id="441da-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="441da-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="441da-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="441da-114">Properties</span></span>

<span data-ttu-id="441da-115">Класс **мсмкаевент \_ свитчтокмкполлинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="441da-115">The **MSMCAEvent\_SwitchToCMCPolling** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="441da-116">**Активен**</span><span class="sxs-lookup"><span data-stu-id="441da-116">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="441da-117">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="441da-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="441da-118">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="441da-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="441da-119">**Значение true**, если данный экземпляр класса активен; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="441da-119">**TRUE**, if this instance of the class is active; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="441da-120">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="441da-120">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="441da-121">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="441da-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="441da-122">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="441da-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="441da-123">Квалификаторы: [ **ключ**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="441da-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="441da-124">Уникальный идентификатор этого экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="441da-124">Unique identifier of this instance of the class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="441da-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="441da-125">Remarks</span></span>

<span data-ttu-id="441da-126">Класс **мсмкаевент \_ свитчтокмкполлинг** является производным от [**WMIEvent**](wmievent.md).</span><span class="sxs-lookup"><span data-stu-id="441da-126">The **MSMCAEvent\_SwitchToCMCPolling** class is derived from [**WMIEvent**](wmievent.md).</span></span>

<span data-ttu-id="441da-127">Уровень абстрагирования системы (SAL) — это код, записываемый в ПЗУ, который вызывается операционной системой для выполнения операций, зависящих от платформы.</span><span class="sxs-lookup"><span data-stu-id="441da-127">The system abstraction layer (SAL) is code burned onto ROM that the operating system calls to perform platform-dependent operations.</span></span> <span data-ttu-id="441da-128">Он аналогичен BIOS на платформе x86.</span><span class="sxs-lookup"><span data-stu-id="441da-128">It is similar to the BIOS on an x86 platform.</span></span> <span data-ttu-id="441da-129">В случаях, когда платформа не поддерживает прерывания для опроса CMC или CPE, операционная система опрашивает каждую минуту, проверяя, произошла ли ошибка ранее.</span><span class="sxs-lookup"><span data-stu-id="441da-129">In cases where the platform does not support interrupts for CMC or CPE polling, the operating system polls every minute, checking if an error occurred previously.</span></span> <span data-ttu-id="441da-130">Если платформа поддерживает прерывания, а операционная система получает определенный пользователем объем опросов CMC или CPE в течение одной минуты, то отключается прерывание и опрос.</span><span class="sxs-lookup"><span data-stu-id="441da-130">If the platform does support interrupts and the operating system receives a user defined amount of CMC or CPE polls within one minute, then it disables the interrupt and poll.</span></span> <span data-ttu-id="441da-131">Если пользователь не определяет число опросов в течение одной минуты, система устанавливает значение по умолчанию 10 опросов в минуту.</span><span class="sxs-lookup"><span data-stu-id="441da-131">If the user does not define the number of polls within one minute, the system sets a default to 10 polls per minute.</span></span>

## <a name="requirements"></a><span data-ttu-id="441da-132">Требования</span><span class="sxs-lookup"><span data-stu-id="441da-132">Requirements</span></span>



| <span data-ttu-id="441da-133">Требование</span><span class="sxs-lookup"><span data-stu-id="441da-133">Requirement</span></span> | <span data-ttu-id="441da-134">Значение</span><span class="sxs-lookup"><span data-stu-id="441da-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="441da-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="441da-135">Minimum supported client</span></span><br/> | <span data-ttu-id="441da-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="441da-136">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="441da-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="441da-137">Minimum supported server</span></span><br/> | <span data-ttu-id="441da-138">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="441da-138">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="441da-139">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="441da-139">Namespace</span></span><br/>                | <span data-ttu-id="441da-140">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="441da-140">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="441da-141">MOF</span><span class="sxs-lookup"><span data-stu-id="441da-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="441da-142"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="441da-142"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="441da-143">DLL</span><span class="sxs-lookup"><span data-stu-id="441da-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="441da-144"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="441da-144"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="441da-145">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="441da-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="441da-146">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="441da-146">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="441da-147">**WMIEvent**</span><span class="sxs-lookup"><span data-stu-id="441da-147">**WMIEvent**</span></span>](wmievent.md)
</dt> </dl>

 

