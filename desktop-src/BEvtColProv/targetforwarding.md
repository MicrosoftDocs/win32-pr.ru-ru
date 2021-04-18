---
description: Извлекает данные пересылки с конечного компьютера.
ms.assetid: e9ed210d-09ad-4689-b6a0-f84c5cce86f5
ms.tgt_platform: multiple
title: Класс Таржетфорвардинг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TargetForwarding
- TargetForwarding.TargetEndpoint
- TargetForwarding.TargetMac
- TargetForwarding.TargetGuid
- TargetForwarding.CollectorEndpoint
- TargetForwarding.Computer
- TargetForwarding.ForwarderType
- TargetForwarding.Destination
- TargetForwarding.DestinationPattern
- TargetForwarding.Error
- TargetForwarding.ConnectedSince
api_type:
- DllExport
api_location:
- BEvtCol.exe
ms.openlocfilehash: aba0a40ccd5611cecfe7450e518620d4d41ec1e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538333"
---
# <a name="targetforwarding-class"></a><span data-ttu-id="74194-103">Класс Таржетфорвардинг</span><span class="sxs-lookup"><span data-stu-id="74194-103">TargetForwarding class</span></span>

<span data-ttu-id="74194-104">Извлекает данные пересылки с конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="74194-104">Retrieves forwarding data from a target computer.</span></span>

> [!Note]  
> <span data-ttu-id="74194-105">На целевом компьютере может быть настроено несколько серверов пересылки.</span><span class="sxs-lookup"><span data-stu-id="74194-105">A target computer may have multiple forwarders configured.</span></span>

 

<span data-ttu-id="74194-106">Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.</span><span class="sxs-lookup"><span data-stu-id="74194-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="74194-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74194-107">Syntax</span></span>

``` syntax
[Provider("BootEventCollectorWmiProvider"), Dynamic, AMENDMENT]
class TargetForwarding
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
};
```

## <a name="members"></a><span data-ttu-id="74194-108">Члены</span><span class="sxs-lookup"><span data-stu-id="74194-108">Members</span></span>

<span data-ttu-id="74194-109">Класс **таржетфорвардинг** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="74194-109">The **TargetForwarding** class has these types of members:</span></span>

-   [<span data-ttu-id="74194-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="74194-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="74194-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="74194-111">Properties</span></span>

<span data-ttu-id="74194-112">Класс **таржетфорвардинг** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="74194-112">The **TargetForwarding** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="74194-113">**коллекторендпоинт**</span><span class="sxs-lookup"><span data-stu-id="74194-113">**CollectorEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-114">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74194-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74194-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-116">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-116">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-117">Сведения о конечной точке сервера сборщика.</span><span class="sxs-lookup"><span data-stu-id="74194-117">The endpoint information of the collector server.</span></span> <span data-ttu-id="74194-118">Это свойство имеет формат "строка *узла*:*порт* ".</span><span class="sxs-lookup"><span data-stu-id="74194-118">This property is formatted as a *host*:*port* string.</span></span>

</dd> <dt>

<span data-ttu-id="74194-119">**Компьютер**</span><span class="sxs-lookup"><span data-stu-id="74194-119">**Computer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-120">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74194-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74194-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-122">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-122">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-123">Имя компьютера конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="74194-123">The computer name of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="74194-124">**коннектедсинце**</span><span class="sxs-lookup"><span data-stu-id="74194-124">**ConnectedSince**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-125">Тип данных: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="74194-125">Data type: **DATETIME**</span></span>
</dt> <dt>

<span data-ttu-id="74194-126">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-127">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-127">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-128">Отметка времени, указывающая, когда было установлено соединение для пересылаемых данных.</span><span class="sxs-lookup"><span data-stu-id="74194-128">The timestamp that indicates when the connection was established for the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="74194-129">**Назначение**</span><span class="sxs-lookup"><span data-stu-id="74194-129">**Destination**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-130">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74194-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74194-131">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-132">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-132">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-133">Назначение пересылаемых данных, например имя файла.</span><span class="sxs-lookup"><span data-stu-id="74194-133">The destination of the forwarding data, such as a file name.</span></span>

</dd> <dt>

<span data-ttu-id="74194-134">**дестинатионпаттерн**</span><span class="sxs-lookup"><span data-stu-id="74194-134">**DestinationPattern**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-135">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74194-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74194-136">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-137">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-137">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-138">Формат, используемый для создания назначения для пересылаемых данных.</span><span class="sxs-lookup"><span data-stu-id="74194-138">The format used to generate the destination of the forwarding data.</span></span>

</dd> <dt>

<span data-ttu-id="74194-139">**Ошибка**</span><span class="sxs-lookup"><span data-stu-id="74194-139">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-140">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74194-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74194-141">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-142">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-142">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-143">Сообщение об ошибке, описывающее обнаруженную ошибку.</span><span class="sxs-lookup"><span data-stu-id="74194-143">An error message that describes an encountered error.</span></span> <span data-ttu-id="74194-144">Если ошибка не обнаружена, это свойство пусто.</span><span class="sxs-lookup"><span data-stu-id="74194-144">This property is empty if no error was encountered.</span></span>

</dd> <dt>

<span data-ttu-id="74194-145">**форвардертипе**</span><span class="sxs-lookup"><span data-stu-id="74194-145">**ForwarderType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-146">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74194-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74194-147">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-148">Квалификаторы: [ **fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-148">Qualifiers: [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-149">Тип файла, который содержит данные пересылки, такие как ETL.</span><span class="sxs-lookup"><span data-stu-id="74194-149">The file type that contains the forwarding data, such as ETL.</span></span>

</dd> <dt>

<span data-ttu-id="74194-150">**таржетендпоинт**</span><span class="sxs-lookup"><span data-stu-id="74194-150">**TargetEndpoint**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-151">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74194-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74194-152">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-153">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-153">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-154">Сведения о конечной точке конечного компьютера в удобном для человека формате.</span><span class="sxs-lookup"><span data-stu-id="74194-154">The endpoint information of the target computer, in human-readable format.</span></span> <span data-ttu-id="74194-155">Это свойство имеет формат "строка *узла*:*порт* ".</span><span class="sxs-lookup"><span data-stu-id="74194-155">This property is formatted as a *host*:*port* string.</span></span> <span data-ttu-id="74194-156">Например, "127.0.0.1:50000".</span><span class="sxs-lookup"><span data-stu-id="74194-156">For example, "127.0.0.1:50000".</span></span>

</dd> <dt>

<span data-ttu-id="74194-157">**таржетгуид**</span><span class="sxs-lookup"><span data-stu-id="74194-157">**TargetGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-158">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74194-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74194-159">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-160">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-160">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-161">**Идентификатор GUID** SMBIOS целевого компьютера.</span><span class="sxs-lookup"><span data-stu-id="74194-161">The SMBIOS **GUID** of the target computer.</span></span>

</dd> <dt>

<span data-ttu-id="74194-162">**таржетмак**</span><span class="sxs-lookup"><span data-stu-id="74194-162">**TargetMac**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="74194-163">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="74194-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="74194-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="74194-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="74194-165">Квалификаторы: [**ключ**](/windows/desktop/WmiSdk/key-qualifier), [**фиксированный**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="74194-165">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Fixed**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="74194-166">MAC-адрес конечного компьютера.</span><span class="sxs-lookup"><span data-stu-id="74194-166">The MAC address of the target computer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74194-167">Требования</span><span class="sxs-lookup"><span data-stu-id="74194-167">Requirements</span></span>



| <span data-ttu-id="74194-168">Требование</span><span class="sxs-lookup"><span data-stu-id="74194-168">Requirement</span></span> | <span data-ttu-id="74194-169">Значение</span><span class="sxs-lookup"><span data-stu-id="74194-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74194-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74194-170">Minimum supported client</span></span><br/> | <span data-ttu-id="74194-171">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="74194-171">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="74194-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74194-172">Minimum supported server</span></span><br/> | <span data-ttu-id="74194-173">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="74194-173">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="74194-174">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="74194-174">Namespace</span></span><br/>                | <span data-ttu-id="74194-175">Корневой \\ узел Microsoft \\ Windows \\ бутевентколлектор</span><span class="sxs-lookup"><span data-stu-id="74194-175">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="74194-176">MOF</span><span class="sxs-lookup"><span data-stu-id="74194-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="74194-177"><dt>Бутевентколлекторвми. mof</dt></span><span class="sxs-lookup"><span data-stu-id="74194-177"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="74194-178">DLL</span><span class="sxs-lookup"><span data-stu-id="74194-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74194-179"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="74194-179"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="74194-180">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74194-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74194-181">Поставщик WMI сборщика событий загрузки</span><span class="sxs-lookup"><span data-stu-id="74194-181">Boot Event Collector WMI Provider</span></span>](boot-event-collector-wmi-provider-portal.md)
</dt> </dl>

 

