---
description: Известные места назначения, содержащие собранные данные. Доступно, только если сборщик работает с включенным журналом состояния.
ms.assetid: ab0d2949-9808-49c3-8a0c-f2ce9c300a2a
ms.tgt_platform: multiple
title: Класс Таржетфорвардингдестинатион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingDestination
- TargetForwardingDestination.TargetEndpoint
- TargetForwardingDestination.TargetMac
- TargetForwardingDestination.TargetGuid
- TargetForwardingDestination.CollectorEndpoint
- TargetForwardingDestination.Computer
- TargetForwardingDestination.ForwarderType
- TargetForwardingDestination.Destination
- TargetForwardingDestination.DestinationPattern
- TargetForwardingDestination.Error
- TargetForwardingDestination.ConnectedSince
- TargetForwardingDestination.DisconnectedSince
- TargetForwardingDestination.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 735b6179fe9d72b5faf0cad976410aeace427f63
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104495849"
---
# <a name="targetforwardingdestination-class"></a><span data-ttu-id="e0853-104">Класс Таржетфорвардингдестинатион</span><span class="sxs-lookup"><span data-stu-id="e0853-104">TargetForwardingDestination class</span></span>

<span data-ttu-id="e0853-105">Известные места назначения, содержащие собранные данные.</span><span class="sxs-lookup"><span data-stu-id="e0853-105">The known destinations containing the collected data.</span></span> <span data-ttu-id="e0853-106">Доступно, только если сборщик работает с включенным журналом состояния.</span><span class="sxs-lookup"><span data-stu-id="e0853-106">Available only if the collector is running with the status log enabled.</span></span>

<span data-ttu-id="e0853-107">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="e0853-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0853-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e0853-108">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingDestination
{
  string   TargetEndpoint;
  string   TargetMac;
  string   TargetGuid;
  string   CollectorEndpoint;
  string   Computer;
  string   ForwarderType;
  string   Destination;
  string   DestinationPattern;
  string   Error;
  DATETIME ConnectedSince;
  DATETIME DisconnectedSince;
  DATETIME WmiDateTime;
};
```

## <a name="members"></a><span data-ttu-id="e0853-109">Члены</span><span class="sxs-lookup"><span data-stu-id="e0853-109">Members</span></span>

<span data-ttu-id="e0853-110">Класс **таржетфорвардингдестинатион** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="e0853-110">The **TargetForwardingDestination** class has these types of members:</span></span>

-   [<span data-ttu-id="e0853-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="e0853-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e0853-112">Свойства</span><span class="sxs-lookup"><span data-stu-id="e0853-112">Properties</span></span>

<span data-ttu-id="e0853-113">Класс **таржетфорвардингдестинатион** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="e0853-113">The **TargetForwardingDestination** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e0853-114">**коллекторендпоинт**</span><span class="sxs-lookup"><span data-stu-id="e0853-114">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-115">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0853-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-116">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-117">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-117">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-118">Узел: сведения о порте конечной точки на стороне сборщика.</span><span class="sxs-lookup"><span data-stu-id="e0853-118">The host:port information of the endpoint on the collector side.</span></span>

</dd> <dt>

<span data-ttu-id="e0853-119">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="e0853-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0853-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-122">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-123">Имя целевого компьютера, определенное сборщиком в соответствии с его конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="e0853-123">Target computer name, as determined by the collector according to its configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e0853-124">**коннектедсинце**</span><span class="sxs-lookup"><span data-stu-id="e0853-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-125">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e0853-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-127">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-128">Метка времени установления соединения.</span><span class="sxs-lookup"><span data-stu-id="e0853-128">Timestamp of when the connection was established.</span></span>

</dd> <dt>

<span data-ttu-id="e0853-129">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="e0853-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0853-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-132">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-132">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-133">Назначение данных.</span><span class="sxs-lookup"><span data-stu-id="e0853-133">Destination of the data.</span></span> <span data-ttu-id="e0853-134">Это значение зависит от типа сервера пересылки.</span><span class="sxs-lookup"><span data-stu-id="e0853-134">The meaning depends on the forwarder type.</span></span> <span data-ttu-id="e0853-135">Может быть именем файла или какой-либо другой идентификацией.</span><span class="sxs-lookup"><span data-stu-id="e0853-135">May be a file name or some other identification.</span></span>

</dd> <dt>

<span data-ttu-id="e0853-136">**дестинатионпаттерн**</span><span class="sxs-lookup"><span data-stu-id="e0853-136">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-137">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0853-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-138">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-139">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-139">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-140">Шаблон, используемый для создания назначения данных.</span><span class="sxs-lookup"><span data-stu-id="e0853-140">Pattern used to generate the destination of the data.</span></span> <span data-ttu-id="e0853-141">Это значение зависит от типа и конфигурации сервера пересылки.</span><span class="sxs-lookup"><span data-stu-id="e0853-141">The meaning depends on the forwarder type and configuration.</span></span> <span data-ttu-id="e0853-142">Для фиксированного назначения значение будет таким же, как и у самого места назначения.</span><span class="sxs-lookup"><span data-stu-id="e0853-142">For a fixed destination, would be the same as the destination itself.</span></span> <span data-ttu-id="e0853-143">Для назначения с поворотом файлов будут содержаться символы шаблона, которые будут заменены фактическим индексом в назначении.</span><span class="sxs-lookup"><span data-stu-id="e0853-143">For the destination with rotation of the files would contain the pattern characters that will be replaced with the actual index in the destination.</span></span>

</dd> <dt>

<span data-ttu-id="e0853-144">**дисконнектедсинце**</span><span class="sxs-lookup"><span data-stu-id="e0853-144">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-145">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e0853-145">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-146">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-147">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-147">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-148">Метка времени отклонения соединения.</span><span class="sxs-lookup"><span data-stu-id="e0853-148">Timestamp of when the connection was dropped.</span></span>

</dd> <dt>

<span data-ttu-id="e0853-149">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="e0853-149">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0853-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-152">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-153">Сообщение об ошибке при обнаружении ошибки.</span><span class="sxs-lookup"><span data-stu-id="e0853-153">Error message if an error was encountered.</span></span> <span data-ttu-id="e0853-154">В противном случае будет пустым.</span><span class="sxs-lookup"><span data-stu-id="e0853-154">Otherwise will be empty.</span></span>

</dd> <dt>

<span data-ttu-id="e0853-155">**форвардертипе**</span><span class="sxs-lookup"><span data-stu-id="e0853-155">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-156">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0853-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-157">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-158">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-158">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-159">Тип сервера пересылки (например, "ETL").</span><span class="sxs-lookup"><span data-stu-id="e0853-159">Type of the forwarder (such as 'etl').</span></span>

</dd> <dt>

<span data-ttu-id="e0853-160">**таржетендпоинт**</span><span class="sxs-lookup"><span data-stu-id="e0853-160">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-161">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0853-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-162">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-162">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-163">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-163">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-164">Сведения о конечной точке конечного компьютера в удобном для человека формате.</span><span class="sxs-lookup"><span data-stu-id="e0853-164">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="e0853-165">Это свойство имеет формат "строка *узла*:*порт* ".</span><span class="sxs-lookup"><span data-stu-id="e0853-165">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="e0853-166">Например, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="e0853-166">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="e0853-167">**таржетгуид**</span><span class="sxs-lookup"><span data-stu-id="e0853-167">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-168">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0853-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-169">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-169">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-170">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-170">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-171">GUID SMBIOS целевого компьютера (если он известен).</span><span class="sxs-lookup"><span data-stu-id="e0853-171">The target computer's SMBIOS GUID (if known).</span></span>

</dd> <dt>

<span data-ttu-id="e0853-172">**таржетмак**</span><span class="sxs-lookup"><span data-stu-id="e0853-172">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-173">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="e0853-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-174">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-175">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-175">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-176">MAC-адрес целевого компьютера (если известен).</span><span class="sxs-lookup"><span data-stu-id="e0853-176">The target computer's MAC address (if known).</span></span>

</dd> <dt>

<span data-ttu-id="e0853-177">**вмидатетиме**</span><span class="sxs-lookup"><span data-stu-id="e0853-177">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e0853-178">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="e0853-178">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="e0853-179">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="e0853-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e0853-180">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e0853-180">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e0853-181">Метка времени записи изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="e0853-181">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e0853-182">Требования</span><span class="sxs-lookup"><span data-stu-id="e0853-182">Requirements</span></span>



| <span data-ttu-id="e0853-183">Требование</span><span class="sxs-lookup"><span data-stu-id="e0853-183">Requirement</span></span> | <span data-ttu-id="e0853-184">Значение</span><span class="sxs-lookup"><span data-stu-id="e0853-184">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0853-185">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e0853-185">Minimum supported client</span></span><br/> | <span data-ttu-id="e0853-186">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="e0853-186">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="e0853-187">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e0853-187">Minimum supported server</span></span><br/> | <span data-ttu-id="e0853-188">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e0853-188">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="e0853-189">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e0853-189">Namespace</span></span><br/>                | <span data-ttu-id="e0853-190">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="e0853-190">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="e0853-191">MOF</span><span class="sxs-lookup"><span data-stu-id="e0853-191">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e0853-192"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e0853-192"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="e0853-193">DLL</span><span class="sxs-lookup"><span data-stu-id="e0853-193">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0853-194"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e0853-194"><dt>BEvtCol.exe</dt></span></span> </dl>               |



 

