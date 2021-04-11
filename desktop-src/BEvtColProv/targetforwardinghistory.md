---
description: Журнал последних изменений пересылаемых данных для конечного компьютера.
ms.assetid: 621e2734-fc75-4e7a-9fae-de3d1b0272ae
ms.tgt_platform: multiple
title: Класс Таржетфорвардингхистори
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwardingHistory
- TargetForwardingHistory.TargetEndpoint
- TargetForwardingHistory.TargetMac
- TargetForwardingHistory.TargetGuid
- TargetForwardingHistory.CollectorEndpoint
- TargetForwardingHistory.Computer
- TargetForwardingHistory.ForwarderType
- TargetForwardingHistory.Destination
- TargetForwardingHistory.DestinationPattern
- TargetForwardingHistory.Error
- TargetForwardingHistory.ConnectedSince
- TargetForwardingHistory.DisconnectedSince
- TargetForwardingHistory.WmiDateTime
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: 7fb713f98709f65de5fa32424f8a3484edaac758
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104142934"
---
# <a name="targetforwardinghistory-class"></a><span data-ttu-id="c3f98-103">Класс Таржетфорвардингхистори</span><span class="sxs-lookup"><span data-stu-id="c3f98-103">TargetForwardingHistory class</span></span>

<span data-ttu-id="c3f98-104">Журнал последних изменений пересылаемых данных для конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="c3f98-104">The recent history of changes to the forwarding data for a target computer.</span></span>

<span data-ttu-id="c3f98-105">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="c3f98-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f98-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c3f98-106">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwardingHistory
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

## <a name="members"></a><span data-ttu-id="c3f98-107">Члены</span><span class="sxs-lookup"><span data-stu-id="c3f98-107">Members</span></span>

<span data-ttu-id="c3f98-108">Класс **таржетфорвардингхистори** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c3f98-108">The **TargetForwardingHistory** class has these types of members:</span></span>

-   [<span data-ttu-id="c3f98-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="c3f98-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c3f98-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="c3f98-110">Properties</span></span>

<span data-ttu-id="c3f98-111">Класс **таржетфорвардингхистори** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c3f98-111">The **TargetForwardingHistory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c3f98-112">**коллекторендпоинт**</span><span class="sxs-lookup"><span data-stu-id="c3f98-112">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-113">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-115">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-115">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-116">Сведения о конечной точке сервера сборщика.</span><span class="sxs-lookup"><span data-stu-id="c3f98-116">The endpoint information of the collector server.</span></span> <span data-ttu-id="c3f98-117">Это свойство имеет формат "строка *узла*:*порт* ".</span><span class="sxs-lookup"><span data-stu-id="c3f98-117">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-118">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="c3f98-118">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-119">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-120">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-121">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-121">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-122">Имя компьютера конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="c3f98-122">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-123">**коннектедсинце**</span><span class="sxs-lookup"><span data-stu-id="c3f98-123">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-124">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3f98-124">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-125">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-126">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-126">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-127">Отметка времени, указывающая, когда было установлено соединение для пересылаемых данных.</span><span class="sxs-lookup"><span data-stu-id="c3f98-127">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-128">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="c3f98-128">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-129">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-130">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-131">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-131">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-132">Назначение пересылаемых данных, например имя файла.</span><span class="sxs-lookup"><span data-stu-id="c3f98-132">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-133">**дестинатионпаттерн**</span><span class="sxs-lookup"><span data-stu-id="c3f98-133">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-134">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-135">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-136">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-136">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-137">Формат, используемый для создания назначения для пересылаемых данных.</span><span class="sxs-lookup"><span data-stu-id="c3f98-137">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-138">**дисконнектедсинце**</span><span class="sxs-lookup"><span data-stu-id="c3f98-138">**DisconnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-139">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3f98-139">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-140">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-141">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-141">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-142">Отметка времени, указывающая, когда соединение было разорвано.</span><span class="sxs-lookup"><span data-stu-id="c3f98-142">The timestamp that indicates when the connection was disconnected.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-143">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-143">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-144">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-146">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-146">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-147">Сообщение об ошибке, описывающее обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="c3f98-147">An error message that describes an encountered error.</span></span> <span data-ttu-id="c3f98-148">Если ошибка не обнаружена, это свойство пусто.</span><span class="sxs-lookup"><span data-stu-id="c3f98-148">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-149">**форвардертипе**</span><span class="sxs-lookup"><span data-stu-id="c3f98-149">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-150">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-151">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-152">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-152">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-153">Тип файла, который содержит данные пересылки, такие как ETL.</span><span class="sxs-lookup"><span data-stu-id="c3f98-153">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-154">**таржетендпоинт**</span><span class="sxs-lookup"><span data-stu-id="c3f98-154">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-155">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-156">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-157">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-157">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-158">Сведения о конечной точке конечного компьютера в удобном для человека формате.</span><span class="sxs-lookup"><span data-stu-id="c3f98-158">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="c3f98-159">Это свойство имеет формат "строка *узла*:*порт* ".</span><span class="sxs-lookup"><span data-stu-id="c3f98-159">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="c3f98-160">Например, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="c3f98-160">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-161">**таржетгуид**</span><span class="sxs-lookup"><span data-stu-id="c3f98-161">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-162">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-163">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-164">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-164">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-165">**Идентификатор GUID** SMBIOS целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="c3f98-165">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-166">**таржетмак**</span><span class="sxs-lookup"><span data-stu-id="c3f98-166">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-167">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="c3f98-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-168">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-168">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-169">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-169">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-170">MAC-адрес конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="c3f98-170">The MAC address of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="c3f98-171">**вмидатетиме**</span><span class="sxs-lookup"><span data-stu-id="c3f98-171">**WmiDateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c3f98-172">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c3f98-172">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-173">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="c3f98-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c3f98-174">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c3f98-174">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c3f98-175">Метка времени записи изменения состояния.</span><span class="sxs-lookup"><span data-stu-id="c3f98-175">Timestamp of when this state change was recorded.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c3f98-176">Требования</span><span class="sxs-lookup"><span data-stu-id="c3f98-176">Requirements</span></span>



| <span data-ttu-id="c3f98-177">Требование</span><span class="sxs-lookup"><span data-stu-id="c3f98-177">Requirement</span></span> | <span data-ttu-id="c3f98-178">Значение</span><span class="sxs-lookup"><span data-stu-id="c3f98-178">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f98-179">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c3f98-179">Minimum supported client</span></span><br/> | <span data-ttu-id="c3f98-180">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c3f98-180">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="c3f98-181">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c3f98-181">Minimum supported server</span></span><br/> | <span data-ttu-id="c3f98-182">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="c3f98-182">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="c3f98-183">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="c3f98-183">Namespace</span></span><br/>                | <span data-ttu-id="c3f98-184">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="c3f98-184">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="c3f98-185">MOF</span><span class="sxs-lookup"><span data-stu-id="c3f98-185">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c3f98-186"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c3f98-186"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="c3f98-187">DLL</span><span class="sxs-lookup"><span data-stu-id="c3f98-187">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c3f98-188"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c3f98-188"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="c3f98-189">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c3f98-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f98-190">Поставщик WMI сборщика событий загрузки</span><span class="sxs-lookup"><span data-stu-id="c3f98-190">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

