---
description: Запускает предопределенный скрипт на произвольном языке скриптов при доставке события в него.
ms.assetid: 2c0aa216-4255-49ff-9bbd-d6c62b5b9139
ms.tgt_platform: multiple
title: Класс Активескриптевентконсумер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActiveScriptEventConsumer
- ActiveScriptEventConsumer.CreatorSID
- ActiveScriptEventConsumer.KillTimeout
- ActiveScriptEventConsumer.MachineName
- ActiveScriptEventConsumer.MaximumQueueSize
- ActiveScriptEventConsumer.Name
- ActiveScriptEventConsumer.ScriptingEngine
- ActiveScriptEventConsumer.ScriptFileName
- ActiveScriptEventConsumer.ScriptText
api_type:
- DllExport
api_location:
- Scrcons.exe
ms.openlocfilehash: 11e2886fd5d0804946433e102e24617df768dcec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712609"
---
# <a name="activescripteventconsumer-class"></a><span data-ttu-id="ca49b-103">Класс Активескриптевентконсумер</span><span class="sxs-lookup"><span data-stu-id="ca49b-103">ActiveScriptEventConsumer class</span></span>

<span data-ttu-id="ca49b-104">Класс **активескриптевентконсумер** запускает предопределенный скрипт на произвольном языке сценариев, когда в него доставляется событие.</span><span class="sxs-lookup"><span data-stu-id="ca49b-104">The **ActiveScriptEventConsumer** class runs a predefined script in an arbitrary scripting language when an event is delivered to it.</span></span> <span data-ttu-id="ca49b-105">Этот класс является одним из стандартных потребителей событий, предоставляемых инструментарием WMI.</span><span class="sxs-lookup"><span data-stu-id="ca49b-105">This class is one of the standard event consumers that WMI provides.</span></span> <span data-ttu-id="ca49b-106">Дополнительные сведения см. [в разделе Мониторинг и реагирование на события с помощью стандартных потребителей](monitoring-and-responding-to-events-with-standard-consumers.md).</span><span class="sxs-lookup"><span data-stu-id="ca49b-106">For more information, see [Monitoring and Responding to Events with Standard Consumers](monitoring-and-responding-to-events-with-standard-consumers.md).</span></span>


```cmd
Mofcomp -n:root\<namespace> scrcons.mof
```



<span data-ttu-id="ca49b-107">Можно настроить производительность всех экземпляров **активескриптевентконсумер** в системе, задав значения свойства [**timeout**](scriptingstandardconsumersetting.md) или **Максимумскриптс** в одном экземпляре **скриптингстандардконсумерсеттинг**.</span><span class="sxs-lookup"><span data-stu-id="ca49b-107">You can configure the performance of all instances of **ActiveScriptEventConsumer** on a system by setting the values of either the [**Timeout**](scriptingstandardconsumersetting.md) or **MaximumScripts** property in the single instance of **ScriptingStandardConsumerSetting**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca49b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ca49b-108">Syntax</span></span>

``` syntax
[AMENDMENT]
class ActiveScriptEventConsumer : __EventConsumer
{
  uint8  CreatorSID[] = {1,1,0,0,0,0,0,5,18,0,0,0};
  uint32 KillTimeout = 0;
  string MachineName;
  uint32 MaximumQueueSize;
  string Name;
  string ScriptingEngine;
  string ScriptFileName;
  string ScriptText;
};
```

## <a name="members"></a><span data-ttu-id="ca49b-109">Члены</span><span class="sxs-lookup"><span data-stu-id="ca49b-109">Members</span></span>

<span data-ttu-id="ca49b-110">Класс **активескриптевентконсумер** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="ca49b-110">The **ActiveScriptEventConsumer** class has these types of members:</span></span>

-   [<span data-ttu-id="ca49b-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca49b-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ca49b-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="ca49b-112">Properties</span></span>

<span data-ttu-id="ca49b-113">Класс **активескриптевентконсумер** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ca49b-113">The **ActiveScriptEventConsumer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ca49b-114">**креаторсид**</span><span class="sxs-lookup"><span data-stu-id="ca49b-114">**CreatorSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49b-115">Тип данных: массив **Uint8**</span><span class="sxs-lookup"><span data-stu-id="ca49b-115">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ca49b-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca49b-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49b-117">Массив, представляющий идентификатор безопасности (SID), который уникальным образом идентифицирует создателя потребителя событий активного скрипта.</span><span class="sxs-lookup"><span data-stu-id="ca49b-117">Array that represents the security identifier (SID), which uniquely identifies the creator of the Active Script Event consumer.</span></span> <span data-ttu-id="ca49b-118">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="ca49b-118">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca49b-119">**киллтимеаут**</span><span class="sxs-lookup"><span data-stu-id="ca49b-119">**KillTimeout**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49b-120">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca49b-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca49b-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca49b-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49b-122">Число (в секундах), в течение которого разрешено выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="ca49b-122">Number, in seconds, that the script is allowed to run.</span></span> <span data-ttu-id="ca49b-123">Если 0 (нуль), то есть значение по умолчанию, скрипт не будет завершен.</span><span class="sxs-lookup"><span data-stu-id="ca49b-123">If 0 (zero), which is the default, the script is not terminated.</span></span>

</dd> <dt>

<span data-ttu-id="ca49b-124">**MachineName**</span><span class="sxs-lookup"><span data-stu-id="ca49b-124">**MachineName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49b-125">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca49b-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49b-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca49b-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49b-127">Имя компьютера, на который WMI отправляет события.</span><span class="sxs-lookup"><span data-stu-id="ca49b-127">Name of the computer to which WMI sends events.</span></span> <span data-ttu-id="ca49b-128">По соглашению для потребителей Microsoft Standard, потребитель скриптов не может быть запущен удаленно.</span><span class="sxs-lookup"><span data-stu-id="ca49b-128">By convention of Microsoft standard consumers, the script consumer cannot be run remotely.</span></span> <span data-ttu-id="ca49b-129">Сторонние потребители также могут использовать это свойство.</span><span class="sxs-lookup"><span data-stu-id="ca49b-129">Third-party consumers can also use this property.</span></span> <span data-ttu-id="ca49b-130">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="ca49b-130">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca49b-131">**максимумкуеуесизе**</span><span class="sxs-lookup"><span data-stu-id="ca49b-131">**MaximumQueueSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49b-132">Тип данных: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ca49b-132">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ca49b-133">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca49b-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49b-134">Максимальная очередь в байтах для потребителя событий активного скрипта.</span><span class="sxs-lookup"><span data-stu-id="ca49b-134">Maximum queue, in bytes, for the Active Script Event consumer.</span></span> <span data-ttu-id="ca49b-135">Это свойство наследуется от [**\_ \_ евентконсумер**](--eventconsumer.md).</span><span class="sxs-lookup"><span data-stu-id="ca49b-135">This property is inherited from [**\_\_EventConsumer**](--eventconsumer.md).</span></span>

</dd> <dt>

<span data-ttu-id="ca49b-136">**Name**</span><span class="sxs-lookup"><span data-stu-id="ca49b-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49b-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca49b-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49b-138">Тип доступа: чтение и запись</span><span class="sxs-lookup"><span data-stu-id="ca49b-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ca49b-139">Квалификаторы: [ **ключ**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="ca49b-139">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="ca49b-140">Уникальный идентификатор потребителя событий.</span><span class="sxs-lookup"><span data-stu-id="ca49b-140">Unique identifier for the event consumer.</span></span> <span data-ttu-id="ca49b-141">При переименовании потребителя результатом будет два одинаковых потребителей с разными именами.</span><span class="sxs-lookup"><span data-stu-id="ca49b-141">If you rename the consumer, the result is two equal consumers that have different names.</span></span>

</dd> <dt>

<span data-ttu-id="ca49b-142">**скриптфиленаме**</span><span class="sxs-lookup"><span data-stu-id="ca49b-142">**ScriptFileName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49b-143">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca49b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49b-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca49b-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49b-145">Имя файла, из которого считывается текст скрипта, предназначенное в качестве альтернативы указанию текста скрипта в свойстве **скрипттекст** .</span><span class="sxs-lookup"><span data-stu-id="ca49b-145">Name of the file from which the script text is read, intended as an alternative to specifying the text of the script in the **ScriptText** property.</span></span> <span data-ttu-id="ca49b-146">Это свойство должно иметь **значение NULL** , если свойство **Скрипттекст** не равно **null**.</span><span class="sxs-lookup"><span data-stu-id="ca49b-146">This property must be **NULL** if the **ScriptText** property is not **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="ca49b-147">При указании **скриптфиленаме** важно защитить исполняемый файл, который вы запускаете.</span><span class="sxs-lookup"><span data-stu-id="ca49b-147">When you specify the **ScriptFileName**, it is important to secure the executable that you are launching.</span></span> <span data-ttu-id="ca49b-148">Если исполняемый файл не находится в безопасном месте или защищен с помощью строгого списка управления доступом (ACL), любой пользователь может заменить исполняемый файл другим.</span><span class="sxs-lookup"><span data-stu-id="ca49b-148">If the executable is not in a secure location or secured with a strong access control list (ACL), anyone can replace the executable with a different one.</span></span> <span data-ttu-id="ca49b-149">Дополнительные сведения об ACL см. [в разделе Создание дескриптора безопасности (SD) для нового объекта в C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="ca49b-149">For more information about ACLs, see [Creating a Security Descriptor (SD) for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

 

</dd> <dt>

<span data-ttu-id="ca49b-150">**скриптинженгине**</span><span class="sxs-lookup"><span data-stu-id="ca49b-150">**ScriptingEngine**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49b-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca49b-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49b-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca49b-152">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49b-153">Имя используемого обработчика скриптов, например "VBScript".</span><span class="sxs-lookup"><span data-stu-id="ca49b-153">Name of the scripting engine to use, for example, "VBScript".</span></span> <span data-ttu-id="ca49b-154">Это свойство не может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="ca49b-154">This property cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ca49b-155">**скрипттекст**</span><span class="sxs-lookup"><span data-stu-id="ca49b-155">**ScriptText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ca49b-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="ca49b-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ca49b-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="ca49b-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ca49b-158">Текст скрипта, выраженный в языке, известном обработчику скриптов.</span><span class="sxs-lookup"><span data-stu-id="ca49b-158">Text of the script that is expressed in a language known to the scripting engine.</span></span> <span data-ttu-id="ca49b-159">Это свойство должно иметь **значение NULL** , если свойство **Скриптфиленаме** не равно **null**.</span><span class="sxs-lookup"><span data-stu-id="ca49b-159">This property must be **NULL** if the **ScriptFileName** property is not **NULL**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca49b-160">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ca49b-160">Remarks</span></span>

<span data-ttu-id="ca49b-161">Этот класс является производным от абстрактного класса [**\_ \_ евентконсумер**](--eventconsumer.md) .</span><span class="sxs-lookup"><span data-stu-id="ca49b-161">This class is derived from the [**\_\_EventConsumer**](--eventconsumer.md) abstract class.</span></span> <span data-ttu-id="ca49b-162">Он находится в \\ пространстве имен корневой подписки.</span><span class="sxs-lookup"><span data-stu-id="ca49b-162">It is located in the root\\subscription namespace.</span></span>

<span data-ttu-id="ca49b-163">Если текст скрипта указан в экземпляре потребителя события, он имеет доступ к экземпляру события в переменной среды скрипта **таржетевент**.</span><span class="sxs-lookup"><span data-stu-id="ca49b-163">When the text of a script is specified in the event consumer instance, the script has access to the event instance in the script environment variable **TargetEvent**.</span></span>

<span data-ttu-id="ca49b-164">Скрипты выполняются в контексте безопасности LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="ca49b-164">The scripts run in the LocalSystem security context.</span></span> <span data-ttu-id="ca49b-165">В качестве меры безопасности только администратор локальной системы или администратор домена может настроить потребитель сценариев.</span><span class="sxs-lookup"><span data-stu-id="ca49b-165">As a security measure, only a local system administrator or a domain administrator can configure the scripting consumer.</span></span> <span data-ttu-id="ca49b-166">Права доступа не проверяются до времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="ca49b-166">Access rights are not checked until run time.</span></span> <span data-ttu-id="ca49b-167">После настройки потребителя любой пользователь может запустить событие, вызывающее выполнение скрипта.</span><span class="sxs-lookup"><span data-stu-id="ca49b-167">After the consumer is configured, any user can trigger the event that causes the script to .</span></span>

<span data-ttu-id="ca49b-168">Сбой загрузки обработчика скриптов или синтаксического анализа и проверки сценария считается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="ca49b-168">Failure to load the scripting engine or parse and validate the script is considered a failure.</span></span> <span data-ttu-id="ca49b-169">Коды возврата из скрипта и завершение скрипта с использованием времени ожидания также считаются ошибками.</span><span class="sxs-lookup"><span data-stu-id="ca49b-169">Error return codes from the script and terminating the script by using a time-out are also considered failures.</span></span>

<span data-ttu-id="ca49b-170">Значение **скрипттекст** или **скриптфиленаме** должно быть не **null**.</span><span class="sxs-lookup"><span data-stu-id="ca49b-170">Either **ScriptText** or **ScriptFileName** must be not **NULL**.</span></span> <span data-ttu-id="ca49b-171">Если оба свойства имеют **значение NULL** или не **равны NULL**, создается ошибка.</span><span class="sxs-lookup"><span data-stu-id="ca49b-171">If both properties are **NULL** or not **NULL**, an error is generated.</span></span>

<span data-ttu-id="ca49b-172">Когда WMI запускается как служба, скрипты, запускаемые **активескриптевентконсумер** , не создают выходные данные экрана.</span><span class="sxs-lookup"><span data-stu-id="ca49b-172">When WMI is run as a service, scripts run by **ActiveScriptEventConsumer** do not generate screen output.</span></span> <span data-ttu-id="ca49b-173">Скрипты, использующие **MsgBox** , запускаются, но не отображают сведения на экране.</span><span class="sxs-lookup"><span data-stu-id="ca49b-173">Scripts that use **MsgBox** do run, but they do not display information on the screen.</span></span> <span data-ttu-id="ca49b-174">Запуск службы WMI в качестве исполняемого файла не поддерживается, но Инструментарий WMI позволяет сценариям, использующим функцию **MsgBox** , отображать выходные данные или принимать вводимые пользователем данные.</span><span class="sxs-lookup"><span data-stu-id="ca49b-174">Running the WMI service as an executable file is not supported, but WMI allows scripts that use the **MsgBox** function to display output or accept user input.</span></span> <span data-ttu-id="ca49b-175">Ни один из методов, предоставляемых объектом [Wscript](/previous-versions//at5ydy31(v=vs.85)) , не может использоваться, так как **Активескриптевентконсумер** не использует сервер сценариев Windows (WSH).</span><span class="sxs-lookup"><span data-stu-id="ca49b-175">None of the methods provided by the [WScript](/previous-versions//at5ydy31(v=vs.85)) object can be used because **ActiveScriptEventConsumer** does not use Windows Script Host (WSH).</span></span>

## <a name="examples"></a><span data-ttu-id="ca49b-176">Примеры</span><span class="sxs-lookup"><span data-stu-id="ca49b-176">Examples</span></span>

<span data-ttu-id="ca49b-177">[Процедура создания постоянной регистрации событий WMI для мониторинга файлов](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) в коллекции TechNet использует **активескриптевентконсумер** в составе сложного сценария для настройки постоянной регистрации событий WMI.</span><span class="sxs-lookup"><span data-stu-id="ca49b-177">The [Create Permanent WMI Event registration to monitor files](https://Gallery.TechNet.Microsoft.Com/Create-Permenant-WMI-Event-f67ce5c2) PowerShell example on TechNet Gallery uses **ActiveScriptEventConsumer** as part of a complex script to set up a permanent WMI event registration.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca49b-178">Требования</span><span class="sxs-lookup"><span data-stu-id="ca49b-178">Requirements</span></span>



| <span data-ttu-id="ca49b-179">Требование</span><span class="sxs-lookup"><span data-stu-id="ca49b-179">Requirement</span></span> | <span data-ttu-id="ca49b-180">Значение</span><span class="sxs-lookup"><span data-stu-id="ca49b-180">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca49b-181">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ca49b-181">Minimum supported client</span></span><br/> | <span data-ttu-id="ca49b-182">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ca49b-182">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ca49b-183">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ca49b-183">Minimum supported server</span></span><br/> | <span data-ttu-id="ca49b-184">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ca49b-184">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ca49b-185">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ca49b-185">Namespace</span></span><br/>                | <span data-ttu-id="ca49b-186">Корневая \\ Подписка</span><span class="sxs-lookup"><span data-stu-id="ca49b-186">Root\\subscription</span></span><br/>                                                          |
| <span data-ttu-id="ca49b-187">MOF</span><span class="sxs-lookup"><span data-stu-id="ca49b-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca49b-188"><dt>Скрконс. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ca49b-188"><dt>Scrcons.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca49b-189">DLL</span><span class="sxs-lookup"><span data-stu-id="ca49b-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca49b-190"><dt>Scrcons.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca49b-190"><dt>Scrcons.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca49b-191">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ca49b-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca49b-192">Классы стандартных потребителей</span><span class="sxs-lookup"><span data-stu-id="ca49b-192">Standard Consumer Classes</span></span>](standard-consumer-classes.md)
</dt> <dt>

[<span data-ttu-id="ca49b-193">Выполнение скрипта на основе события</span><span class="sxs-lookup"><span data-stu-id="ca49b-193">Running a Script Based on an Event</span></span>](running-a-script-based-on-an-event.md)
</dt> <dt>

[<span data-ttu-id="ca49b-194">Получение событий в любое время</span><span class="sxs-lookup"><span data-stu-id="ca49b-194">Receiving Events At All Times</span></span>](receiving-events-at-all-times.md)
</dt> <dt>

[<span data-ttu-id="ca49b-195">Создание логического потребителя</span><span class="sxs-lookup"><span data-stu-id="ca49b-195">Creating a Logical Consumer</span></span>](creating-a-logical-consumer.md)
</dt> <dt>

[<span data-ttu-id="ca49b-196">**\_\_евентконсумер**</span><span class="sxs-lookup"><span data-stu-id="ca49b-196">**\_\_EventConsumer**</span></span>](--eventconsumer.md)
</dt> <dt>

[<span data-ttu-id="ca49b-197">**скриптингстандардконсумерсеттинг**</span><span class="sxs-lookup"><span data-stu-id="ca49b-197">**ScriptingStandardConsumerSetting**</span></span>](scriptingstandardconsumersetting.md)
</dt> </dl>

 

