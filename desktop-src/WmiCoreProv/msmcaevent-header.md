---
description: Представляет общий заголовок, используемый всеми классами Мсмкаевент. Этот класс доступен только в 64-разрядных системах Windows.
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: Класс MSMCAEvent_Header
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693380"
---
# <a name="msmcaevent_header-class"></a><span data-ttu-id="45925-104">\_Класс заголовка мсмкаевент</span><span class="sxs-lookup"><span data-stu-id="45925-104">MSMCAEvent\_Header class</span></span>

<span data-ttu-id="45925-105">Класс **\_ заголовка мсмкаевент** представляет общий заголовок, используемый всеми [классами мсмка](msmca-classes.md) .</span><span class="sxs-lookup"><span data-stu-id="45925-105">The **MSMCAEvent\_Header** class represents the common header that all [MSMCA classes](msmca-classes.md) use.</span></span> <span data-ttu-id="45925-106">Файлы заголовков используются таким образом, чтобы код C и C++ мог иметь структуру данных, описывающую общий заголовок для всех событий.</span><span class="sxs-lookup"><span data-stu-id="45925-106">The header files are used so that C and C++ code can have a data structure that describes the common header for all events.</span></span> <span data-ttu-id="45925-107">Этот класс зарезервирован для внутреннего использования.</span><span class="sxs-lookup"><span data-stu-id="45925-107">This class is reserved for internal use.</span></span> <span data-ttu-id="45925-108">Этот класс доступен только в 64-разрядных системах Windows.</span><span class="sxs-lookup"><span data-stu-id="45925-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="45925-109">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="45925-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="45925-110">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="45925-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="45925-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="45925-111">Syntax</span></span>

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="45925-112">Члены</span><span class="sxs-lookup"><span data-stu-id="45925-112">Members</span></span>

<span data-ttu-id="45925-113">Класс **\_ заголовка мсмкаевент** содержит следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="45925-113">The **MSMCAEvent\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="45925-114">Свойства</span><span class="sxs-lookup"><span data-stu-id="45925-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="45925-115">Свойства</span><span class="sxs-lookup"><span data-stu-id="45925-115">Properties</span></span>

<span data-ttu-id="45925-116">Класс **\_ заголовка мсмкаевент** содержит следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="45925-116">The **MSMCAEvent\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45925-117">**аддитионалеррорс**</span><span class="sxs-lookup"><span data-stu-id="45925-117">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45925-118">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45925-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45925-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45925-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45925-120">Число дополнительных ошибок в записи MCA.</span><span class="sxs-lookup"><span data-stu-id="45925-120">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="45925-121">**Загрузки**</span><span class="sxs-lookup"><span data-stu-id="45925-121">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45925-122">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45925-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45925-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45925-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45925-124">ЦП, который сообщает об ошибке.</span><span class="sxs-lookup"><span data-stu-id="45925-124">CPU that reports the error.</span></span> <span data-ttu-id="45925-125">Это свойство применяется только к многопроцессорной системе, в которой первый процессор назначается с номером 0, второму процессору присваивается номер 1 и т. д.</span><span class="sxs-lookup"><span data-stu-id="45925-125">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="45925-126">**еррорсеверити**</span><span class="sxs-lookup"><span data-stu-id="45925-126">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45925-127">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="45925-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="45925-128">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45925-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45925-129">Степень серьезности ошибки, о которой сообщается.</span><span class="sxs-lookup"><span data-stu-id="45925-129">Severity level of the error reported.</span></span>



| <span data-ttu-id="45925-130">Значение</span><span class="sxs-lookup"><span data-stu-id="45925-130">Value</span></span>                                                                                                | <span data-ttu-id="45925-131">Значение</span><span class="sxs-lookup"><span data-stu-id="45925-131">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="45925-132"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="45925-132"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="45925-133">Восстанавливаемых</span><span class="sxs-lookup"><span data-stu-id="45925-133">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="45925-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="45925-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="45925-135">Аварий</span><span class="sxs-lookup"><span data-stu-id="45925-135">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="45925-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="45925-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="45925-137">Исправимая</span><span class="sxs-lookup"><span data-stu-id="45925-137">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="45925-138">**логтоевентлог**</span><span class="sxs-lookup"><span data-stu-id="45925-138">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45925-139">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45925-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45925-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45925-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45925-141">Если значение равно 0 (ноль), это событие не заносится в журнал системных событий.</span><span class="sxs-lookup"><span data-stu-id="45925-141">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="45925-142">**RecordId**</span><span class="sxs-lookup"><span data-stu-id="45925-142">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45925-143">Тип данных: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45925-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45925-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45925-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45925-145">Идентификатор записи записи об ошибке для этой ошибки.</span><span class="sxs-lookup"><span data-stu-id="45925-145">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="45925-146">Дополнительные сведения об использовании значений **UInt64** в скриптах см. [в разделе Создание сценариев в WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45925-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45925-147">**Тип**</span><span class="sxs-lookup"><span data-stu-id="45925-147">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45925-148">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45925-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45925-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="45925-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45925-150">Тип сообщения журнала событий.</span><span class="sxs-lookup"><span data-stu-id="45925-150">Type of event log message.</span></span> <span data-ttu-id="45925-151">Эти сообщения соответствуют кодам сообщений журнала событий, используемым для вставки сообщений журнала событий поставщиком потребителей журнала событий Windows при получении одного из событий.</span><span class="sxs-lookup"><span data-stu-id="45925-151">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45925-152">Требования</span><span class="sxs-lookup"><span data-stu-id="45925-152">Requirements</span></span>



| <span data-ttu-id="45925-153">Требование</span><span class="sxs-lookup"><span data-stu-id="45925-153">Requirement</span></span> | <span data-ttu-id="45925-154">Значение</span><span class="sxs-lookup"><span data-stu-id="45925-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="45925-155">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45925-155">Minimum supported client</span></span><br/> | <span data-ttu-id="45925-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="45925-156">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="45925-157">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45925-157">Minimum supported server</span></span><br/> | <span data-ttu-id="45925-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="45925-158">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="45925-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="45925-159">Namespace</span></span><br/>                | <span data-ttu-id="45925-160">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="45925-160">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="45925-161">MOF</span><span class="sxs-lookup"><span data-stu-id="45925-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45925-162"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45925-162"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="45925-163">DLL</span><span class="sxs-lookup"><span data-stu-id="45925-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45925-164"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45925-164"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45925-165">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="45925-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45925-166">Классы МСМКА</span><span class="sxs-lookup"><span data-stu-id="45925-166">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="45925-167">Классы C++ для WMI</span><span class="sxs-lookup"><span data-stu-id="45925-167">WMI C++ Classes</span></span>](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

