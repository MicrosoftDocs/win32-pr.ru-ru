---
description: Одноэлементный класс Скриптингстандардконсумерсеттинг предоставляет данные регистрации, общие для всех экземпляров класса-получателя Активескриптевентконсумер Standard.
ms.assetid: d217e058-3529-4173-b896-ebff3d7b05c6
ms.tgt_platform: multiple
title: Класс Скриптингстандардконсумерсеттинг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ScriptingStandardConsumerSetting
- ScriptingStandardConsumerSetting.Caption
- ScriptingStandardConsumerSetting.Description
- ScriptingStandardConsumerSetting.MaximumScripts
- ScriptingStandardConsumerSetting.SettingID
- ScriptingStandardConsumerSetting.Timeout
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 43eae14eea445f546f731605c94b38e770b08691
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263808"
---
# <a name="scriptingstandardconsumersetting-class"></a><span data-ttu-id="4c9e3-103">Класс Скриптингстандардконсумерсеттинг</span><span class="sxs-lookup"><span data-stu-id="4c9e3-103">ScriptingStandardConsumerSetting class</span></span>

<span data-ttu-id="4c9e3-104">Одноэлементный класс **скриптингстандардконсумерсеттинг** предоставляет данные регистрации, общие для всех экземпляров класса-получателя [**активескриптевентконсумер**](activescripteventconsumer.md) Standard.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-104">The singleton **ScriptingStandardConsumerSetting** class provides registration data that is common to all instances of the [**ActiveScriptEventConsumer**](activescripteventconsumer.md) standard consumer class.</span></span> <span data-ttu-id="4c9e3-105">Экземпляр **активескриптевентконсумер** использует свойства **максимумскриптс** и **timeout** .</span><span class="sxs-lookup"><span data-stu-id="4c9e3-105">An **ActiveScriptEventConsumer** instance uses the **MaximumScripts** and **Timeout** properties.</span></span> <span data-ttu-id="4c9e3-106">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="4c9e3-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>

<span data-ttu-id="4c9e3-107">Следующий синтаксис упрощен из кода MOF-файл (MOF) и включает все его унаследованные свойства.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="4c9e3-108">Свойства и методы имеют алфавитный порядок, а не порядок MOF.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-108">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c9e3-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4c9e3-109">Syntax</span></span>

``` syntax
[Singleton, AMENDMENT]
class ScriptingStandardConsumerSetting : CIM_Setting
{
  string Caption = "Scripting Standard Consumer Setting";
  string Description = "Registration data common to all instances of the Scripting Standard Consumer";
  uint32 MaximumScripts = 300;
  string SettingID = "ScriptingStandardConsumerSetting";
  uint32 Timeout = 0;
};
```

## <a name="members"></a><span data-ttu-id="4c9e3-110">Члены</span><span class="sxs-lookup"><span data-stu-id="4c9e3-110">Members</span></span>

<span data-ttu-id="4c9e3-111">Класс **скриптингстандардконсумерсеттинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="4c9e3-111">The **ScriptingStandardConsumerSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="4c9e3-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c9e3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4c9e3-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="4c9e3-113">Properties</span></span>

<span data-ttu-id="4c9e3-114">Класс **скриптингстандардконсумерсеттинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-114">The **ScriptingStandardConsumerSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4c9e3-115">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c9e3-116">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c9e3-117">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c9e3-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c9e3-118">Квалификаторы: [**maxlen**](standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="4c9e3-118">Qualifiers: [**MaxLen**](standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="4c9e3-119">Краткое описание объекта — одна строка строки.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-119">A short description of an object a one line string.</span></span> <span data-ttu-id="4c9e3-120">Содержит строку **скриптингстандардконсумерсеттинг** , так как это одноэлементный класс.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-120">Contains the string **ScriptingStandardConsumerSetting** because this is a singleton class.</span></span>

</dd> <dt>

<span data-ttu-id="4c9e3-121">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c9e3-122">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c9e3-123">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c9e3-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4c9e3-124">Текстовое описание объекта.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-124">A text description of an object.</span></span>

</dd> <dt>

<span data-ttu-id="4c9e3-125">**максимумскриптс**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-125">**MaximumScripts**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c9e3-126">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-126">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c9e3-127">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4c9e3-127">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4c9e3-128">Максимальное количество скриптов, выполняемых до того, как потребитель запустит новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-128">Maximum number of scripts that are run before a consumer starts a new instance.</span></span> <span data-ttu-id="4c9e3-129">Чтобы очистить утечки памяти из скриптов, регулярно выполняйте очистку потребителя.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-129">To clear out memory leaks from scripts, shut down the consumer regularly.</span></span> <span data-ttu-id="4c9e3-130">Значение по умолчанию — 300.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-130">The default value is 300.</span></span>

</dd> <dt>

<span data-ttu-id="4c9e3-131">**SettingID**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-131">**SettingID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c9e3-132">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4c9e3-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="4c9e3-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4c9e3-134">Квалификаторы: [**maxlen**](standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="4c9e3-134">Qualifiers: [**MaxLen**](standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="4c9e3-135">Идентификатор объекта параметра.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-135">Identifier for the setting object.</span></span>

</dd> <dt>

<span data-ttu-id="4c9e3-136">**Timeout**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-136">**Timeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4c9e3-137">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4c9e3-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="4c9e3-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4c9e3-139">Квалификаторы: [**единицы**](standard-qualifiers.md) ("минуты")</span><span class="sxs-lookup"><span data-stu-id="4c9e3-139">Qualifiers: [**units**](standard-qualifiers.md) ("Minutes")</span></span>
</dt> </dl>

<span data-ttu-id="4c9e3-140">Максимальное число минут, по истечении которого потребитель запускает новый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-140">Maximum number of minutes before a consumer starts a new instance.</span></span> <span data-ttu-id="4c9e3-141">Если значение равно 0 (ноль), свойство **максимумскриптс** управляет жизненным циклом потребителя.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-141">If 0 (zero), the **MaximumScripts** property controls the consumer lifetime.</span></span> <span data-ttu-id="4c9e3-142">Допустимый диапазон значений для **времени ожидания** — от 0 до 71 000, а значение по умолчанию — 0 (ноль).</span><span class="sxs-lookup"><span data-stu-id="4c9e3-142">The valid range for **Timeout** is 0 through 71,000 and the default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c9e3-143">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4c9e3-143">Remarks</span></span>

<span data-ttu-id="4c9e3-144">Единственный экземпляр класса **скриптингстандардконсумерсеттинг** находится в корневом \\ пространстве имен CIMV2.</span><span class="sxs-lookup"><span data-stu-id="4c9e3-144">The single instance of the **ScriptingStandardConsumerSetting** class resides in the root\\cimv2 namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c9e3-145">Требования</span><span class="sxs-lookup"><span data-stu-id="4c9e3-145">Requirements</span></span>



| <span data-ttu-id="4c9e3-146">Требование</span><span class="sxs-lookup"><span data-stu-id="4c9e3-146">Requirement</span></span> | <span data-ttu-id="4c9e3-147">Значение</span><span class="sxs-lookup"><span data-stu-id="4c9e3-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9e3-148">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4c9e3-148">Minimum supported client</span></span><br/> | <span data-ttu-id="4c9e3-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c9e3-149">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4c9e3-150">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4c9e3-150">Minimum supported server</span></span><br/> | <span data-ttu-id="4c9e3-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c9e3-151">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4c9e3-152">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="4c9e3-152">Namespace</span></span><br/>                | <span data-ttu-id="4c9e3-153">Корневая \\ Подписка</span><span class="sxs-lookup"><span data-stu-id="4c9e3-153">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="4c9e3-154">MOF</span><span class="sxs-lookup"><span data-stu-id="4c9e3-154">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c9e3-155"><dt>Скрконс. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c9e3-155"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c9e3-156">DLL</span><span class="sxs-lookup"><span data-stu-id="4c9e3-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c9e3-157"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4c9e3-157"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c9e3-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4c9e3-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c9e3-159">**\_Параметр CIM**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-159">**CIM\_Setting**</span></span>](/windows/desktop/CIMWin32Prov/cim-setting)
</dt> <dt>

[<span data-ttu-id="4c9e3-160">Классы стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="4c9e3-160">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="4c9e3-161">Выполнение скрипта на основе события</span><span class="sxs-lookup"><span data-stu-id="4c9e3-161">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="4c9e3-162">Создание логического потребителя</span><span class="sxs-lookup"><span data-stu-id="4c9e3-162">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="4c9e3-163">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="4c9e3-163">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="4c9e3-164">**\_\_евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="4c9e3-164">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> </dl>

 

