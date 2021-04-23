---
description: Узнайте, как работать с высокоскоростными устройствами NVMe из приложения Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Работа с дисками NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662724"
---
# <a name="working-with-nvme-drives"></a><span data-ttu-id="28745-103">Работа с дисками NVMe</span><span class="sxs-lookup"><span data-stu-id="28745-103">Working with NVMe drives</span></span>

<span data-ttu-id="28745-104">**Относится к**</span><span class="sxs-lookup"><span data-stu-id="28745-104">**Applies to:**</span></span>

-   <span data-ttu-id="28745-105">Windows 10</span><span class="sxs-lookup"><span data-stu-id="28745-105">Windows 10</span></span>
-   <span data-ttu-id="28745-106">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="28745-106">Windows Server 2016</span></span>

<span data-ttu-id="28745-107">Узнайте, как работать с высокоскоростными устройствами NVMe из приложения Windows.</span><span class="sxs-lookup"><span data-stu-id="28745-107">Learn how to work with high-speed NVMe devices from your Windows application.</span></span> <span data-ttu-id="28745-108">Доступ к устройству включается через **StorNVMe.sys**, встроенный драйвер впервые появился в Windows Server 2012 R2 и Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="28745-108">Device access is enabled via **StorNVMe.sys**, the in-box driver first introduced in Windows Server 2012 R2 and Windows 8.1.</span></span> <span data-ttu-id="28745-109">Она также доступна для устройств Windows 7 с помощью горячего исправления KB.</span><span class="sxs-lookup"><span data-stu-id="28745-109">It's also available to Windows 7 devices through a KB hot fix.</span></span> <span data-ttu-id="28745-110">В Windows 10 появились некоторые новые функции, включая сквозной механизм для специфичных для поставщика команд NVMe и обновлений существующих IOCTL.</span><span class="sxs-lookup"><span data-stu-id="28745-110">In Windows 10, several new features were introduced, including a pass-through mechanism for vendor-specific NVMe commands and updates to existing IOCTLs.</span></span>

<span data-ttu-id="28745-111">В этом разделе приводятся общие сведения об интерфейсах API общего использования, которые можно использовать для доступа к дискам NVMe в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="28745-111">This topic provides an overview of general-use APIs that you can use to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="28745-112">Он также описывает:</span><span class="sxs-lookup"><span data-stu-id="28745-112">It also describes:</span></span>

-   <span data-ttu-id="28745-113">Отправка команды NVMe, относящейся к поставщику, с [передаваемым](#pass-through-mechanism)</span><span class="sxs-lookup"><span data-stu-id="28745-113">How to send a vendor-specific NVMe command with [pass-through](#pass-through-mechanism)</span></span>
-   <span data-ttu-id="28745-114">[Отправка команды "найти", "получить компоненты" или "получение страниц журнала](#protocol-specific-queries) " на диск NVMe</span><span class="sxs-lookup"><span data-stu-id="28745-114">How to [send an Identify, Get Features, or Get Log Pages command](#protocol-specific-queries) to the NVMe drive</span></span>
-   <span data-ttu-id="28745-115">[Получение сведений о температуре](#temperature-queries) с диска NVMe</span><span class="sxs-lookup"><span data-stu-id="28745-115">How to [obtain temperature information](#temperature-queries) from an NVMe drive</span></span>
-   <span data-ttu-id="28745-116">Как выполнить изменение параметров поведения, например [задать пороговые значения температуры](#behavior-changing-commands)</span><span class="sxs-lookup"><span data-stu-id="28745-116">How to perform behavior changing commands, such as [setting temperature thresholds](#behavior-changing-commands)</span></span>

## <a name="apis-for-working-with-nvme-drives"></a><span data-ttu-id="28745-117">Интерфейсы API для работы с дисками NVMe</span><span class="sxs-lookup"><span data-stu-id="28745-117">APIs for working with NVMe drives</span></span>

<span data-ttu-id="28745-118">Для доступа к дискам NVMe в Windows 10 можно использовать следующие интерфейсы API общего пользования.</span><span class="sxs-lookup"><span data-stu-id="28745-118">You can use the following general-use APIs to access NVMe drives in Windows 10.</span></span> <span data-ttu-id="28745-119">Эти API-интерфейсы можно найти в **виниоктл. h** для приложений пользовательского режима и **нтддстор. h** для драйверов режима ядра.</span><span class="sxs-lookup"><span data-stu-id="28745-119">These APIs can be found in **winioctl.h** for user mode applications, and **ntddstor.h** for kernel mode drivers.</span></span> <span data-ttu-id="28745-120">Дополнительные сведения о файлах заголовков см. в разделе [заголовочные файлы](#header-files).</span><span class="sxs-lookup"><span data-stu-id="28745-120">For more information about header files, see [Header files](#header-files).</span></span>

-   <span data-ttu-id="28745-121">Запрос [**ioctl \_ \_ \_ Команда протокола хранилища**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) . Используйте этот запрос IOCTL в **структуре \_ \_ команд протокола хранилища** для выпусков команд NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-121">[**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use this IOCTL with the **STORAGE\_PROTOCOL\_COMMAND** structure to issue NVMe commands.</span></span> <span data-ttu-id="28745-122">Этот запрос IOCTL обеспечивает сквозную передачу NVMe и поддерживает журнал командных эффектов в NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-122">This IOCTL enables NVMe pass-through and supports the Command Effects log in NVMe.</span></span> <span data-ttu-id="28745-123">Его можно использовать с командами, зависящими от поставщика.</span><span class="sxs-lookup"><span data-stu-id="28745-123">You can use it with vendor-specific commands.</span></span> <span data-ttu-id="28745-124">Дополнительные сведения см. в разделе [сквозной механизм](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="28745-124">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

-   <span data-ttu-id="28745-125">[**Хранилище \_ \_Команда протокола**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : Эта структура входного буфера включает поле **ReturnStatus** , которое можно использовать для передачи следующих значений состояния.</span><span class="sxs-lookup"><span data-stu-id="28745-125">[**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : This input-buffer structure includes a **ReturnStatus** field that can be used report the following status values.</span></span>
    -   <span data-ttu-id="28745-126">**\_ \_ ожидается состояние протокола \_ хранилища**</span><span class="sxs-lookup"><span data-stu-id="28745-126">**STORAGE\_PROTOCOL\_STATUS\_PENDING**</span></span>
    -   <span data-ttu-id="28745-127">**\_состояние протокола хранилища — \_ \_ успешно**</span><span class="sxs-lookup"><span data-stu-id="28745-127">**STORAGE\_PROTOCOL\_STATUS\_SUCCESS**</span></span>
    -   <span data-ttu-id="28745-128">**\_ \_ Ошибка состояния протокола \_ хранилища**</span><span class="sxs-lookup"><span data-stu-id="28745-128">**STORAGE\_PROTOCOL\_STATUS\_ERROR**</span></span>
    -   <span data-ttu-id="28745-129">**\_ \_ \_ Недопустимый \_ запрос состояния протокола хранилища**</span><span class="sxs-lookup"><span data-stu-id="28745-129">**STORAGE\_PROTOCOL\_STATUS\_INVALID\_REQUEST**</span></span>
    -   <span data-ttu-id="28745-130">**\_состояние протокола \_ хранилища \_ нет \_ устройства**</span><span class="sxs-lookup"><span data-stu-id="28745-130">**STORAGE\_PROTOCOL\_STATUS\_NO\_DEVICE**</span></span>
    -   <span data-ttu-id="28745-131">**\_состояние протокола \_ хранилища \_ занято**</span><span class="sxs-lookup"><span data-stu-id="28745-131">**STORAGE\_PROTOCOL\_STATUS\_BUSY**</span></span>
    -   <span data-ttu-id="28745-132">**\_ \_ \_ переполнение данных о состоянии протокола \_ хранилища**</span><span class="sxs-lookup"><span data-stu-id="28745-132">**STORAGE\_PROTOCOL\_STATUS\_DATA\_OVERRUN**</span></span>
    -   <span data-ttu-id="28745-133">**\_состояние протокола хранилища — \_ \_ недостаточно \_ ресурсов**</span><span class="sxs-lookup"><span data-stu-id="28745-133">**STORAGE\_PROTOCOL\_STATUS\_INSUFFICIENT\_RESOURCES**</span></span>
    -   <span data-ttu-id="28745-134">**\_состояние протокола \_ хранилища \_ не \_ поддерживается**</span><span class="sxs-lookup"><span data-stu-id="28745-134">**STORAGE\_PROTOCOL\_STATUS\_NOT\_SUPPORTED**</span></span>
-   <span data-ttu-id="28745-135">Запрос [**ioctl \_ \_ \_ Свойство "запрос хранилища**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) ". Используйте этот запрос IOCTL со структурой **\_ \_ запроса свойства хранилища** для получения сведений об устройстве.</span><span class="sxs-lookup"><span data-stu-id="28745-135">[**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use this IOCTL with the **STORAGE\_PROPERTY\_QUERY** structure to retrieve device information.</span></span> <span data-ttu-id="28745-136">Дополнительные сведения см. в разделе [запросы, зависящие от протокола](#protocol-specific-queries) , и [запросы на температуру](#temperature-queries).</span><span class="sxs-lookup"><span data-stu-id="28745-136">For more info, see [Protocol-specific queries](#protocol-specific-queries) and [Temperature queries](#temperature-queries).</span></span>

-   <span data-ttu-id="28745-137">[**Хранилище \_ \_Запрос свойства**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) . Эта структура включает в себя поля **PropertyId** и **аддитионалпараметерс** для указания данных для запроса.</span><span class="sxs-lookup"><span data-stu-id="28745-137">[**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : This structure includes the **PropertyId** and **AdditionalParameters** fields to specify the data to be queried.</span></span> <span data-ttu-id="28745-138">В **PropertyId** с помощью перечисления **\_ \_ идентификаторов свойств хранилища** укажите тип данных.</span><span class="sxs-lookup"><span data-stu-id="28745-138">In the **PropertyId** filed, use the **STORAGE\_PROPERTY\_ID** enumeration to specify the type of data.</span></span> <span data-ttu-id="28745-139">Используйте поле **аддитионалпараметерс** для указания дополнительных сведений в зависимости от типа данных.</span><span class="sxs-lookup"><span data-stu-id="28745-139">Use the **AdditionalParameters** field to specify more details, depending on the type of data.</span></span> <span data-ttu-id="28745-140">Для данных, относящихся к протоколу, используйте структуру **данных, \_ \_ относящуюся \_ к протоколу хранилища** , в поле **аддитионалпараметерс** .</span><span class="sxs-lookup"><span data-stu-id="28745-140">For protocol-specific data, use the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure in the **AdditionalParameters** field.</span></span> <span data-ttu-id="28745-141">Для данных температуры используйте структуру **\_ \_ сведений о температуре хранилища** в поле **аддитионалпараметерс** .</span><span class="sxs-lookup"><span data-stu-id="28745-141">For temperature data, use the **STORAGE\_TEMPERATURE\_INFO** structure in the **AdditionalParameters** field.</span></span>
-   <span data-ttu-id="28745-142">[**Хранилище \_ \_Идентификатор свойства**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) . Это перечисление включает новые значения, которые позволяют **\_ \_ \_ свойству запроса на хранение через ioctl** получать сведения об особенностях протокола и температуры.</span><span class="sxs-lookup"><span data-stu-id="28745-142">[**STORAGE\_PROPERTY\_ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : This enumeration includes new values that allow **IOCTL\_STORAGE\_QUERY\_PROPERTY** to retrieve protocol-specific and temperature information.</span></span>

    -   <span data-ttu-id="28745-143">**сторажеадаптерпротоколспеЦификпроперти**</span><span class="sxs-lookup"><span data-stu-id="28745-143">**StorageAdapterProtocolSpecificProperty**</span></span>
    -   <span data-ttu-id="28745-144">**сторажедевицепротоколспеЦификпроперти**</span><span class="sxs-lookup"><span data-stu-id="28745-144">**StorageDeviceProtocolSpecificProperty**</span></span>

    <span data-ttu-id="28745-145">Используйте один из этих идентификаторов свойств для конкретного протокола в сочетании **с \_ \_ \_ данными протокола хранилища** для получения данных, относящихся к протоколу, в структуре [**\_ \_ \_ дескриптора данных протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="28745-145">Use one of these protocol-specific property IDs in combination with **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** to retrieve protocol-specific data in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) structure.</span></span>

    -   <span data-ttu-id="28745-146">**сторажеадаптертемпературепроперти**</span><span class="sxs-lookup"><span data-stu-id="28745-146">**StorageAdapterTemperatureProperty**</span></span>
    -   <span data-ttu-id="28745-147">**сторажедевицетемпературепроперти**</span><span class="sxs-lookup"><span data-stu-id="28745-147">**StorageDeviceTemperatureProperty**</span></span>

    <span data-ttu-id="28745-148">Используйте один из этих идентификаторов свойств температуры для получения данных температуры в [**структуре \_ \_ \_ дескриптора данных температуры хранилища**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .</span><span class="sxs-lookup"><span data-stu-id="28745-148">Use one of these temperature property IDs to retrieve temperature data in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) structure.</span></span>

-   <span data-ttu-id="28745-149">[**Хранилище \_ \_ \_ Данные, относящиеся к протоколу**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : получение данных, относящихся к NVMe, если эта структура используется для поля **аддитионалпараметерс** **\_ \_ запроса свойства хранилища** и указано значение перечисления [**\_ \_ \_ \_ типа данных NVMe протокола хранилища**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) .</span><span class="sxs-lookup"><span data-stu-id="28745-149">[**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Retrieve NVMe-specific data when this structure is used for the **AdditionalParameters** field of **STORAGE\_PROPERTY\_QUERY** and a [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) enum value is specified.</span></span> <span data-ttu-id="28745-150">Используйте одно из следующих значений **\_ \_ \_ \_ типа данных NVME протокола хранилища** в поле **DataType** структуры **\_ \_ \_ данных, характерной для протокола хранилища** :</span><span class="sxs-lookup"><span data-stu-id="28745-150">Use one of the following **STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE** values in the **DataType** field of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** structure:</span></span>

    -   <span data-ttu-id="28745-151">Используйте **нвмедататипеидентифи** , чтобы найти данные контроллера или указать данные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="28745-151">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="28745-152">Используйте **нвмедататипелогпаже** для получения страниц журнала (в том числе интеллектуальных и данных о работоспособности).</span><span class="sxs-lookup"><span data-stu-id="28745-152">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="28745-153">Используйте **нвмедататипефеатуре** для получения компонентов диска NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-153">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

-   <span data-ttu-id="28745-154">[**Хранилище \_ \_Сведения о температуре**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) . Эта структура используется для хранения данных о температуре.</span><span class="sxs-lookup"><span data-stu-id="28745-154">[**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : This structure is used to hold specific temperature data.</span></span> <span data-ttu-id="28745-155">Он используется в **\_ \_ \_ дескрипторе данных темературе хранилища** для возврата результатов запроса температуры.</span><span class="sxs-lookup"><span data-stu-id="28745-155">It's used in the **STORAGE\_TEMERATURE\_DATA\_DESCRIPTOR** to return the results of a temperature query.</span></span>

-   <span data-ttu-id="28745-156">Запрос [**ioctl \_ \_ \_ \_ Порог температуры для набора хранения**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Используйте этот запрос IOCTL **с \_ \_ пороговой структурой температуры хранилища** , чтобы задать пороговые значения температуры.</span><span class="sxs-lookup"><span data-stu-id="28745-156">[**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use this IOCTL with the **STORAGE\_TEMPERATURE\_THRESHOLD** structure to set temperature thresholds.</span></span> <span data-ttu-id="28745-157">Дополнительные сведения см. в разделе [поведение при изменении команд](#behavior-changing-commands).</span><span class="sxs-lookup"><span data-stu-id="28745-157">For more info, see [Behavior changing commands](#behavior-changing-commands).</span></span>

-   <span data-ttu-id="28745-158">[**Хранилище \_ \_Пороговое значение температуры**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) . Эта структура используется в качестве входного буфера для указания порога температуры.</span><span class="sxs-lookup"><span data-stu-id="28745-158">[**STORAGE\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : This structure is used as an input buffer to specify the temperature threshold.</span></span> <span data-ttu-id="28745-159">Поле "превышение **порогового** значения" (логическое значение) указывает, является ли поле **порогового** значения пороговое значение или нет (в противном случае это будет ниже порогового значения).</span><span class="sxs-lookup"><span data-stu-id="28745-159">The **OverThreshold** field (boolean) specifies if the **Threshold** field is the over threshold value or not (otherwise, it's the under threshold value).</span></span>

## <a name="pass-through-mechanism"></a><span data-ttu-id="28745-160">Сквозной механизм</span><span class="sxs-lookup"><span data-stu-id="28745-160">Pass-through mechanism</span></span>

<span data-ttu-id="28745-161">Команды, которые не определены в спецификации NVMe, наиболее сложны для обработки. узел не имеет сведений о влиянии команд на целевое устройство, предоставленной инфраструктуре (пространствах имен/размеров блоков) и его поведении.</span><span class="sxs-lookup"><span data-stu-id="28745-161">Commands which are not defined in the NVMe specification are the most difficult for the host OS to handle – the host has no insight into the effects that the commands may have on the target device, the exposed infrastructure (namespaces/block sizes), and its behavior.</span></span>

<span data-ttu-id="28745-162">Для более эффективного выполнения таких команд конкретного устройства через стек хранилища Windows новый механизм сквозного перебора позволяет передавать команды, относящиеся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="28745-162">To better carry such device specific commands through the Windows storage stack, a new pass-through mechanism allows vendor-specific commands to be piped through.</span></span> <span data-ttu-id="28745-163">Этот транзитный канал также поможет в разработке средств управления и тестирования.</span><span class="sxs-lookup"><span data-stu-id="28745-163">This pass-through pipe will also aid in development of management and testing tools.</span></span> <span data-ttu-id="28745-164">Однако этот механизм передачи данных требует использования журнала командных эффектов.</span><span class="sxs-lookup"><span data-stu-id="28745-164">However, this pass-through mechanism requires use of the Command Effects Log.</span></span> <span data-ttu-id="28745-165">Более того, для StoreNVMe.sys требуются все команды, а не только транзитные команды, которые должны быть описаны в журнале командных эффектов.</span><span class="sxs-lookup"><span data-stu-id="28745-165">Moreover, StoreNVMe.sys requires all commands, not just pass-through commands, to be described in the Command Effects Log.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="28745-166">StorNVMe.sys и Storport.sys будут блокировать любую команду на устройство, если оно не описано в журнале командных эффектов.</span><span class="sxs-lookup"><span data-stu-id="28745-166">StorNVMe.sys and Storport.sys will block any command to a device if it is not described in the Command Effects Log.</span></span>

 

### <a name="supporting-the-command-effects-log"></a><span data-ttu-id="28745-167">Поддержка журнала командных эффектов</span><span class="sxs-lookup"><span data-stu-id="28745-167">Supporting the Command Effects Log</span></span>

<span data-ttu-id="28745-168">Журнал командных эффектов (как описано в разделе Supported and Effects, Section 5.10.1.5 of [NVMe 1,2](https://nvmexpress.org/specifications)) позволяет описать влияние команд, относящихся к поставщику, вместе с командами, определяемыми спецификацией.</span><span class="sxs-lookup"><span data-stu-id="28745-168">The Command Effects Log (as described in Commands Supported and Effects, section 5.10.1.5 of [NVMe Specification 1.2](https://nvmexpress.org/specifications)) allows the description of the effects of vendor-specific commands together with specification-defined commands.</span></span> <span data-ttu-id="28745-169">Это упрощает проверку поддержки команд, а также оптимизацию поведения команд и, следовательно, должна быть реализована для всего набора команд, поддерживаемых устройством.</span><span class="sxs-lookup"><span data-stu-id="28745-169">This facilitates both command support validation as well as command behavior optimization, and therefore should be implemented for the entire set of commands that the device supports.</span></span> <span data-ttu-id="28745-170">Следующие условия описывают результат отправки команды на основе записи журнала командных эффектов.</span><span class="sxs-lookup"><span data-stu-id="28745-170">The following conditions describe the result on how the command is sent based on its Command Effects Log entry.</span></span>

<span data-ttu-id="28745-171">Для любой команды, описанной в журнале командных эффектов...</span><span class="sxs-lookup"><span data-stu-id="28745-171">For any specific command described in the Command Effects Log...</span></span>

<span data-ttu-id="28745-172">**Время**:</span><span class="sxs-lookup"><span data-stu-id="28745-172">**While**:</span></span>

-   <span data-ttu-id="28745-173">Для поддерживаемой команды (КСУПП) задано значение "1", что означает, что команда поддерживается контроллером (бит 01).</span><span class="sxs-lookup"><span data-stu-id="28745-173">Command Supported (CSUPP) is set to ‘1’ signifying that the command is supported by the controller (Bit 01)</span></span>

    > [!Note]  
    > <span data-ttu-id="28745-174">Если для КСУПП задано значение "0" (что означает, что команда не поддерживается), команда будет заблокирована</span><span class="sxs-lookup"><span data-stu-id="28745-174">When CSUPP is set to ‘0’ (signifying that the command is not supported) the command will be blocked</span></span>

     

<span data-ttu-id="28745-175">**Если** заданы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="28745-175">**And if** any of the following is set:</span></span>

-   <span data-ttu-id="28745-176">Для изменения возможностей контроллера (CCC) задано значение "1", что означает, что команда может изменить возможности контроллера (бит 04)</span><span class="sxs-lookup"><span data-stu-id="28745-176">Controller Capability Change (CCC) is set to ‘1’ signifying that the command may change controller capabilities (Bit 04)</span></span>

-   <span data-ttu-id="28745-177">Для изменения описи пространства имен (NIC) задано значение "1", что означает, что команда может изменить число или возможности для нескольких пространств имен (бит 03)</span><span class="sxs-lookup"><span data-stu-id="28745-177">Namespace Inventory Change (NIC) is set to ‘1’ signifying that the command may change the number, or capabilities for multiple namespaces (Bit 03)</span></span>

-   <span data-ttu-id="28745-178">Для изменения возможностей пространства имен (RIPE) задано значение "1", что означает, что команда может изменить возможности одного пространства имен (бит 02)</span><span class="sxs-lookup"><span data-stu-id="28745-178">Namespace Capability Change (NCC) is set to ‘1’ signifying that the command may change the capabilities of a single namespace (Bit 02)</span></span>

-   <span data-ttu-id="28745-179">Для отправки команды и выполнения (CSE) задано значение 001В или 010B, что означает, что команда может быть отправлена при отсутствии других невыполненных команд для одного и того же или любого пространства имен, а другая команда не должна быть отправлена в то же или какое-либо пространство имен, пока эта команда не будет завершена (BITS 18:16).</span><span class="sxs-lookup"><span data-stu-id="28745-179">Command Submission and Execution (CSE) is set to 001b or 010b, signifying that the command may be submitted when there is no other outstanding command to the same or any namespace, and that another command should not be submitted to the same or any namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="28745-180">**Затем** команда будет отправлена в качестве единственной команды, ожидающей адаптеру.</span><span class="sxs-lookup"><span data-stu-id="28745-180">**Then** the command will be sent as the only command outstanding to the adapter.</span></span>

<span data-ttu-id="28745-181">**Else If**:</span><span class="sxs-lookup"><span data-stu-id="28745-181">**Else if**:</span></span>

-   <span data-ttu-id="28745-182">Для отправки команды и выполнения (CSE) задано значение 001В, что означает, что команда может быть отправлена при отсутствии других необработанных команд в том же пространстве имен, а другая команда не должна быть отправлена в то же пространство имен, пока эта команда не будет завершена (BITS 18:16).</span><span class="sxs-lookup"><span data-stu-id="28745-182">Command Submission and Execution (CSE) is set to 001b, signifying that the command may be submitted when there is no other outstanding command to the same namespace, and that another command should not be submitted to the same namespace until this command is complete (Bits 18:16)</span></span>

<span data-ttu-id="28745-183">**Затем** команда будет отправлена как единственная команда, недоступная для объекта логического номера устройства (LUN).</span><span class="sxs-lookup"><span data-stu-id="28745-183">**Then** the command will be sent as the only command outstanding to the Logical Unit Number object (LUN).</span></span>

<span data-ttu-id="28745-184">**В противном случае** команда отправляется с другими командами, выполненными без запрета.</span><span class="sxs-lookup"><span data-stu-id="28745-184">**Otherwise**, the command is sent with other commands outstanding without inhibition.</span></span> <span data-ttu-id="28745-185">Например, если на устройство отправляется команда, зависящая от поставщика, для получения статистических сведений, не определенных спецификацией, не должно быть риска изменять поведение устройства или возможность выполнения команд ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="28745-185">For example, if a vendor-specific command is sent to the device to retrieve statistical information that is not spec-defined, there should be no risk to changing the device’s behavior or capability to execute I/O commands.</span></span> <span data-ttu-id="28745-186">Такие запросы могут обслуживаться параллельно с вводом-выводом, а пауза-возобновление не потребуется.</span><span class="sxs-lookup"><span data-stu-id="28745-186">Such requests could be serviced in parallel to I/O and no pause-resume would be necessary.</span></span>

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a><span data-ttu-id="28745-187">Использование \_ \_ команды протокола хранилища ioctl \_ для отправки команд</span><span class="sxs-lookup"><span data-stu-id="28745-187">Using IOCTL\_STORAGE\_PROTOCOL\_COMMAND to send commands</span></span>

<span data-ttu-id="28745-188">Для передачи данных можно использовать [**\_ \_ \_ команду протокола хранилища ioctl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), представленную в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="28745-188">Pass-through can be conducted using the [**IOCTL\_STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introduced in Windows 10.</span></span> <span data-ttu-id="28745-189">Этот запрос IOCTL был разработан так, чтобы иметь такое же поведение, как и существующие сквозные IOCTL SCSI и ATA, для отправки внедренной команды на целевое устройство.</span><span class="sxs-lookup"><span data-stu-id="28745-189">This IOCTL was designed to have a similar behavior as the existing SCSI and ATA pass-through IOCTLs, to send an embedded command to the target device.</span></span> <span data-ttu-id="28745-190">С помощью этого IOCTL можно отправлять данные на устройство хранения, включая диск NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-190">Via this IOCTL, pass-through can be sent to a storage device, including an NVMe drive.</span></span>

<span data-ttu-id="28745-191">Например, в NVMe запрос IOCTL разрешит отправку следующих кодов команд.</span><span class="sxs-lookup"><span data-stu-id="28745-191">For example, in NVMe, the IOCTL will allow the sending down of the following command codes.</span></span>

-   <span data-ttu-id="28745-192">Команды администрирования для конкретного поставщика (C0h – ФФХ)</span><span class="sxs-lookup"><span data-stu-id="28745-192">Vendor Specific Admin Commands (C0h – FFh)</span></span>
-   <span data-ttu-id="28745-193">Специфические для поставщика команды NVMe (80h – ФФХ)</span><span class="sxs-lookup"><span data-stu-id="28745-193">Vendor Specific NVMe Commands (80h – FFh)</span></span>

<span data-ttu-id="28745-194">Как и в случае со всеми другими IOCTL, используйте [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) для отправки сквозного IOCTL.</span><span class="sxs-lookup"><span data-stu-id="28745-194">As with all other IOCTLs, Use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) to send the pass-through IOCTL down.</span></span> <span data-ttu-id="28745-195">Запрос IOCTL заполняется с помощью структуры входного буфера [**\_ \_ команды протокола хранилища**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , обнаруженной в **нтддстор. h**.</span><span class="sxs-lookup"><span data-stu-id="28745-195">The IOCTL is populated using the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) input-buffer structure found in **ntddstor.h**.</span></span> <span data-ttu-id="28745-196">Заполните поле **команда** командой, зависящей от поставщика.</span><span class="sxs-lookup"><span data-stu-id="28745-196">Populate the **Command** field with the vendor-specific command.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



<span data-ttu-id="28745-197">Указанная выше команда для конкретного поставщика должна быть заполнена в выделенном поле выше.</span><span class="sxs-lookup"><span data-stu-id="28745-197">The vendor specific command desired to be sent should be populated in the highlighted field above.</span></span> <span data-ttu-id="28745-198">Обратите внимание, что журнал командных эффектов должен быть реализован для транзитных команд.</span><span class="sxs-lookup"><span data-stu-id="28745-198">Note again that the Command Effects Log must be implemented for pass-through commands.</span></span> <span data-ttu-id="28745-199">В частности, эти команды необходимо сообщить как поддерживаемые в журнале командных эффектов (Дополнительные сведения см. в предыдущем разделе).</span><span class="sxs-lookup"><span data-stu-id="28745-199">In particular, these commands need to be reported as supported in the Command Effects Log (see previous section for more information).</span></span> <span data-ttu-id="28745-200">Кроме того, обратите внимание, что поля репликации паролей являются специфическими для драйвера, поэтому приложения, отправляющие команды, могут оставить их как 0</span><span class="sxs-lookup"><span data-stu-id="28745-200">Also note that PRP fields are driver specific thus applications sending commands can leave them as 0.</span></span>

<span data-ttu-id="28745-201">Наконец, этот транзитный запрос IOCTL предназначен для отправки команд, относящихся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="28745-201">Finally, this pass-through IOCTL is intended for sending vendor-specific commands.</span></span> <span data-ttu-id="28745-202">Чтобы отправить другим администраторам или не относящимся к поставщику команды NVMe, такие как Identify, не следует использовать этот сквозной запрос IOCTL.</span><span class="sxs-lookup"><span data-stu-id="28745-202">To send other admin or non-vendor specific NVMe commands such as Identify, this pass-through IOCTL should not be used.</span></span> <span data-ttu-id="28745-203">Например, **\_ \_ \_ свойство запроса хранилища ioctl** должно использоваться для поиска и получения страниц журнала.</span><span class="sxs-lookup"><span data-stu-id="28745-203">For example, **IOCTL\_STORAGE\_QUERY\_PROPERTY** should be used for Identify or Get Log Pages.</span></span> <span data-ttu-id="28745-204">Дополнительные сведения см. в следующем разделе запросы, [относящиеся к протоколу](/windows).</span><span class="sxs-lookup"><span data-stu-id="28745-204">For more info, see the next section, [Protocol-specific queries](/windows).</span></span>

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a><span data-ttu-id="28745-205">Не обновляйте встроенное по через сквозной механизм</span><span class="sxs-lookup"><span data-stu-id="28745-205">Don't update firmware through the pass-through mechanism</span></span>

<span data-ttu-id="28745-206">Команды загрузки и активации встроенного по не должны отправляться с помощью сквозной передачи.</span><span class="sxs-lookup"><span data-stu-id="28745-206">Firmware download and activation commands should not be sent using pass-through.</span></span> <span data-ttu-id="28745-207">Запрос **ioctl \_ \_ \_ Команда протокола хранилища** должна использоваться только для специфичных для поставщика команд.</span><span class="sxs-lookup"><span data-stu-id="28745-207">**IOCTL\_STORAGE\_PROTOCOL\_COMMAND** should only be used for vendor-specific commands.</span></span>

<span data-ttu-id="28745-208">Вместо этого используйте следующие общие протоколы IOCTL службы хранилища (появившиеся в Windows 10), чтобы избежать непосредственного использования \_ версии минипорта встроенного по для порта SCSI.</span><span class="sxs-lookup"><span data-stu-id="28745-208">Instead, use the following general storage IOCTLs (introduced in Windows 10) to avoid applications directly using the SCSI\_miniport version of the Firmware IOCTL.</span></span> <span data-ttu-id="28745-209">Драйверы хранилища преобразовывают IOCTL в команду SCSI или \_ версию МИНИПОРТА SCSI для IOCTL на Минипорт.</span><span class="sxs-lookup"><span data-stu-id="28745-209">Storage drivers will translate the IOCTL to either a SCSI command or the SCSI\_miniport version of the IOCTL to the miniport.</span></span>

<span data-ttu-id="28745-210">Эти запросы IOCTL рекомендуются для разработки средств обновления встроенного по в Windows 10 и Windows Server 2016:</span><span class="sxs-lookup"><span data-stu-id="28745-210">These IOCTLs are recommended for developing firmware upgrade tools in Windows 10 and Windows Server 2016:</span></span>

-   [<span data-ttu-id="28745-211">**\_ \_ \_ Получение сведений о встроенном по для хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="28745-211">**IOCTL\_STORAGE\_FIRMWARE\_GET\_INFO**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [<span data-ttu-id="28745-212">**\_ \_ скачивание встроенного по для хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="28745-212">**IOCTL\_STORAGE\_FIRMWARE\_DOWNLOAD**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [<span data-ttu-id="28745-213">**\_ \_ Активация встроенного по службы хранилища ioctl \_**</span><span class="sxs-lookup"><span data-stu-id="28745-213">**IOCTL\_STORAGE\_FIRMWARE\_ACTIVATE**</span></span>](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

<span data-ttu-id="28745-214">Для быстрого получения сведений о хранилище и обновления встроенного по в Windows также поддерживаются командлеты PowerShell:</span><span class="sxs-lookup"><span data-stu-id="28745-214">For getting storage information and updating firmware, Windows also supports PowerShell cmdlets for doing this quickly:</span></span>

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> <span data-ttu-id="28745-215">Для обновления встроенного по в NVMe в Windows 8.1 Используйте \_ \_ \_ подпрограмму ioctl SCSI минипорта.</span><span class="sxs-lookup"><span data-stu-id="28745-215">To update firmware on NVMe in Windows 8.1, use IOCTL\_SCSI\_MINIPORT\_FIRMWARE.</span></span> <span data-ttu-id="28745-216">Этот запрос IOCTL не был перенесен на Windows 7.</span><span class="sxs-lookup"><span data-stu-id="28745-216">This IOCTL was not backported to Windows 7.</span></span> <span data-ttu-id="28745-217">Дополнительные сведения см. [в разделе Обновление встроенного по для устройства NVMe в Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span><span class="sxs-lookup"><span data-stu-id="28745-217">For more information, see [Upgrading Firmware for an NVMe Device in Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).</span></span>

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a><span data-ttu-id="28745-218">Возвращение ошибок через сквозной механизм</span><span class="sxs-lookup"><span data-stu-id="28745-218">Returning errors through the pass-through mechanism</span></span>

<span data-ttu-id="28745-219">При отправке команды или запроса на мини-порт или устройство, как и в случае передачи команд и запросов между SCSI и ATA, функция IOCTL возвращает значение, если он был успешным.</span><span class="sxs-lookup"><span data-stu-id="28745-219">Similar to SCSI and ATA pass-through IOCTLs, when a command/request is sent to the miniport or device, the IOCTL returns if it was successful or not.</span></span> <span data-ttu-id="28745-220">В структуре [**\_ \_ команды протокола хранилища**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) ioctl возвращает состояние через поле **ReturnStatus** .</span><span class="sxs-lookup"><span data-stu-id="28745-220">In the [**STORAGE\_PROTOCOL\_COMMAND**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) structure, the IOCTL returns the status through the **ReturnStatus** field.</span></span>

### <a name="example-sending-a-vendor-specific-command"></a><span data-ttu-id="28745-221">Пример. Отправка команды, относящейся к поставщику</span><span class="sxs-lookup"><span data-stu-id="28745-221">Example: sending a vendor-specific command</span></span>

<span data-ttu-id="28745-222">В этом примере произвольная команда, зависящая от поставщика (0xFF), отправляется через транзитный диск в устройство NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-222">In this example, an arbitrary vendor-specific command (0xFF) is sent via pass-through to an NVMe drive.</span></span> <span data-ttu-id="28745-223">Следующий код выделяет буфер, инициализирует запрос, а затем отправляет команду на устройство через DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="28745-223">The following code allocates a buffer, initializes a query, and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



<span data-ttu-id="28745-224">В этом примере мы предполагаем, что `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` команда была успешной на устройстве.</span><span class="sxs-lookup"><span data-stu-id="28745-224">In this example, we expect `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` if the command succeeded to the device.</span></span>

## <a name="protocol-specific-queries"></a><span data-ttu-id="28745-225">Запросы для конкретного протокола</span><span class="sxs-lookup"><span data-stu-id="28745-225">Protocol-specific queries</span></span>

<span data-ttu-id="28745-226">Windows 8.1 представил [**\_ \_ \_ свойство запроса хранилища ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) для получения данных.</span><span class="sxs-lookup"><span data-stu-id="28745-226">Windows 8.1 introduced [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) for data retrieval.</span></span> <span data-ttu-id="28745-227">В Windows 10 функция IOCTL была улучшена для поддержки часто запрашиваемых функций NVMe, таких как **получение страниц журнала**, **Получение функций** и **Обнаружение**.</span><span class="sxs-lookup"><span data-stu-id="28745-227">In Windows 10, the IOCTL was enhanced to support commonly requested NVMe features such as **Get Log Pages**, **Get Features**, and **Identify**.</span></span> <span data-ttu-id="28745-228">Это позволяет получить сведения о конкретном NVMe для мониторинга и инвентаризации.</span><span class="sxs-lookup"><span data-stu-id="28745-228">This allows for the retrieval of NVMe specific information for monitoring and inventory purposes.</span></span>

<span data-ttu-id="28745-229">Здесь показан входной буфер для запроса IOCTL [**, \_ свойства \_ хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (из Windows 10).</span><span class="sxs-lookup"><span data-stu-id="28745-229">The input buffer for the IOCTL, [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



<span data-ttu-id="28745-230">При использовании [**\_ \_ \_ Свойства запроса хранилища ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) для получения сведений о конкретном протоколе NVMe [**в \_ \_ \_ дескрипторе данных протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)настройте [**структуру \_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28745-230">When using [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) to retrieve NVMe protocol-specific information in the [**STORAGE\_PROTOCOL\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="28745-231">Выделите буфер, который может содержать как [**\_ \_ запрос свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) , так и структуру [**\_ \_ \_ данных, специфичную для протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) .</span><span class="sxs-lookup"><span data-stu-id="28745-231">Allocate a buffer that can contains both a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) and a [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure.</span></span>

-   <span data-ttu-id="28745-232">Задайте для поля **PropertyID** значение **сторажеадаптерпротоколспеЦификпроперти** или **сторажедевицепротоколспеЦификпроперти** для запроса контроллера или устройства/пространства имен соответственно.</span><span class="sxs-lookup"><span data-stu-id="28745-232">Set the **PropertyID** field to **StorageAdapterProtocolSpecificProperty** or **StorageDeviceProtocolSpecificProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="28745-233">Задайте для поля **QueryType** значение **пропертистандардкуери**.</span><span class="sxs-lookup"><span data-stu-id="28745-233">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

-   <span data-ttu-id="28745-234">Заполните структуру [**\_ данных, \_ относящуюся \_ к протоколу хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) , с нужными значениями.</span><span class="sxs-lookup"><span data-stu-id="28745-234">Fill the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure with the desired values.</span></span> <span data-ttu-id="28745-235">В начале **\_ \_ \_ данных протокола хранилища** задается поле **аддитионалпараметерс** [**\_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span><span class="sxs-lookup"><span data-stu-id="28745-235">The start of the **STORAGE\_PROTOCOL\_SPECIFIC\_DATA** is the **AdditionalParameters** field of [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).</span></span>

<span data-ttu-id="28745-236">Здесь показана структура [**\_ \_ \_ данных, специфичная для протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (из Windows 10).</span><span class="sxs-lookup"><span data-stu-id="28745-236">The [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



<span data-ttu-id="28745-237">Чтобы указать тип сведений, относящихся к протоколу NVMe, настройте структуру [**\_ \_ \_ данных, специфичную для протокола хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) , следующим образом.</span><span class="sxs-lookup"><span data-stu-id="28745-237">To specify a type of NVMe protocol-specific information, configure the [**STORAGE\_PROTOCOL\_SPECIFIC\_DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) structure as follows:</span></span>

-   <span data-ttu-id="28745-238">Задайте для поля **ProtocolType** значение **протоколтипенвме**.</span><span class="sxs-lookup"><span data-stu-id="28745-238">Set the **ProtocolType** field to **ProtocolTypeNVMe**.</span></span>

-   <span data-ttu-id="28745-239">Задайте для поля **DataType** значение перечисления, определенное [**\_ \_ \_ \_ типом данных NVME протоколом хранилища**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span><span class="sxs-lookup"><span data-stu-id="28745-239">Set the **DataType** field to an enumeration value defined by [**STORAGE\_PROTOCOL\_NVME\_DATA\_TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):</span></span>

    -   <span data-ttu-id="28745-240">Используйте **нвмедататипеидентифи** , чтобы найти данные контроллера или указать данные пространства имен.</span><span class="sxs-lookup"><span data-stu-id="28745-240">Use **NVMeDataTypeIdentify** to get Identify Controller data or Identify Namespace data.</span></span>
    -   <span data-ttu-id="28745-241">Используйте **нвмедататипелогпаже** для получения страниц журнала (в том числе интеллектуальных и данных о работоспособности).</span><span class="sxs-lookup"><span data-stu-id="28745-241">Use **NVMeDataTypeLogPage** to get log pages (including SMART/health data).</span></span>
    -   <span data-ttu-id="28745-242">Используйте **нвмедататипефеатуре** для получения компонентов диска NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-242">Use **NVMeDataTypeFeature** to get features of the NVMe drive.</span></span>

<span data-ttu-id="28745-243">Если в качестве **ProtocolType** используется **протоколтипенвме** , запросы сведений, относящихся к протоколу, можно получить параллельно с другими операциями ввода-вывода на диске NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-243">When **ProtocolTypeNVMe** is used as the **ProtocolType**, queries for protocol-specific information can be retrieved in parallel with other I/O on the NVMe drive.</span></span>

<span data-ttu-id="28745-244">В следующих примерах демонстрируются запросы, зависящие от протокола NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-244">The following examples demonstrate NVMe protocol-specific queries.</span></span>

### <a name="example-nvme-identify-query"></a><span data-ttu-id="28745-245">Пример: NVMe Identify, запрос</span><span class="sxs-lookup"><span data-stu-id="28745-245">Example: NVMe Identify query</span></span>

<span data-ttu-id="28745-246">В этом примере запрос **Identify** отправляется на диск NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-246">In this example, the **Identify** request is sent to an NVMe drive.</span></span> <span data-ttu-id="28745-247">Следующий код инициализирует структуру данных запроса, а затем отправляет команду на устройство через DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="28745-247">The following code initializes the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



<span data-ttu-id="28745-248">Обратите внимание, что вызывающему объекту необходимо выделить один буфер, содержащий \_ запрос свойства хранилища \_ , и \_ размер \_ данных, характерных для протокола хранилища \_ .</span><span class="sxs-lookup"><span data-stu-id="28745-248">Note that the caller needs to allocate a single buffer containing STORAGE\_PROPERTY\_QUERY and the size of STORAGE\_PROTOCOL\_SPECIFIC\_DATA.</span></span> <span data-ttu-id="28745-249">В этом примере для ввода и вывода запроса свойства используется один и тот же буфер.</span><span class="sxs-lookup"><span data-stu-id="28745-249">In this example, it’s using the same buffer for input and output from the property query.</span></span> <span data-ttu-id="28745-250">Вот почему выделенный буфер имеет размер " \_ смещение поля ( \_ запрос свойства хранилища \_ , аддитионалпараметерс) + sizeof ( \_ данные протокола хранилища \_ \_ ) + \_ \_ " максимальный размер журнала NVME \_ ".</span><span class="sxs-lookup"><span data-stu-id="28745-250">That’s why the buffer that was allocated has a size of “FIELD\_OFFSET(STORAGE\_PROPERTY\_QUERY, AdditionalParameters) + sizeof(STORAGE\_PROTOCOL\_SPECIFIC\_DATA) + NVME\_MAX\_LOG\_SIZE”.</span></span> <span data-ttu-id="28745-251">Несмотря на то, что отдельные буферы можно выделить для ввода и вывода, мы рекомендуем использовать один буфер для запроса связанных данных NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-251">Although separate buffers could be allocated for both input and output, we recommend using a single buffer to query NVMe related-information.</span></span>

### <a name="example-nvme-get-log-pages-query"></a><span data-ttu-id="28745-252">Пример: запрос на получение страниц журнала NVMe</span><span class="sxs-lookup"><span data-stu-id="28745-252">Example: NVMe Get Log Pages query</span></span>

<span data-ttu-id="28745-253">В этом примере, основанном на предыдущем, запрос _ *Get log Pages*\* отправляется на диск NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-253">In this example, based off of the previous one, the _ *Get Log Pages*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="28745-254">Следующий код подготавливает структуру данных запроса, а затем отправляет команду на устройство через DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="28745-254">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a><span data-ttu-id="28745-255">Пример: запрос на получение функций NVMe</span><span class="sxs-lookup"><span data-stu-id="28745-255">Example: NVMe Get Features query</span></span>

<span data-ttu-id="28745-256">В этом примере, основанном на предыдущем, запрос _ *Get Features*\* отправляется на диск NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-256">In this example, based off of the previous one, the _ *Get Features*\* request is sent to an NVMe drive.</span></span> <span data-ttu-id="28745-257">Следующий код подготавливает структуру данных запроса, а затем отправляет команду на устройство через DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="28745-257">The following code prepares the query data structure and then sends the command down to the device via DeviceIoControl.</span></span>


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a><span data-ttu-id="28745-258">Набор, зависящий от протокола</span><span class="sxs-lookup"><span data-stu-id="28745-258">Protocol-specific set</span></span>

<span data-ttu-id="28745-259">Начиная с Windows 10 19H1, IOCTL_STORAGE_SET_PROPERTY был усовершенствован для поддержки функций набора NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-259">From Windows 10 19H1, the IOCTL_STORAGE_SET_PROPERTY was enhanced to support NVMe Set Features.</span></span>

<span data-ttu-id="28745-260">Входной буфер для IOCTL_STORAGE_SET_PROPERTY показан ниже:</span><span class="sxs-lookup"><span data-stu-id="28745-260">The input buffer for the IOCTL_STORAGE_SET_PROPERTY is shown here:</span></span>

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

<span data-ttu-id="28745-261">При использовании IOCTL_STORAGE_SET_PROPERTY для установки функции NVMe Настройте структуру STORAGE_PROPERTY_SET следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28745-261">When using IOCTL_STORAGE_SET_PROPERTY to set NVMe feature, configure the STORAGE_PROPERTY_SET structure as follows:</span></span>

-   <span data-ttu-id="28745-262">Выделите буфер, который может содержать как STORAGE_PROPERTY_SET, так и STORAGE_PROTOCOL_SPECIFIC_DATA_EXT структуру.</span><span class="sxs-lookup"><span data-stu-id="28745-262">Allocate a buffer that can contains both a STORAGE_PROPERTY_SET and a STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure;</span></span>
-   <span data-ttu-id="28745-263">Задайте для поля PropertyID значение СторажеадаптерпротоколспеЦификпроперти или СторажедевицепротоколспеЦификпроперти для запроса контроллера или устройства/пространства имен соответственно.</span><span class="sxs-lookup"><span data-stu-id="28745-263">Set the PropertyID field to StorageAdapterProtocolSpecificProperty or StorageDeviceProtocolSpecificProperty for a controller or device/namespace request, respectively.</span></span>
-   <span data-ttu-id="28745-264">Заполните структуру STORAGE_PROTOCOL_SPECIFIC_DATA_EXT нужными значениями.</span><span class="sxs-lookup"><span data-stu-id="28745-264">Fill the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure with the desired values.</span></span> <span data-ttu-id="28745-265">Началом STORAGE_PROTOCOL_SPECIFIC_DATA_EXT является поле Аддитионалпараметерс STORAGE_PROPERTY_SET.</span><span class="sxs-lookup"><span data-stu-id="28745-265">The start of the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT is the AdditionalParameters field of STORAGE_PROPERTY_SET.</span></span>

<span data-ttu-id="28745-266">Структура STORAGE_PROTOCOL_SPECIFIC_DATA_EXT показана здесь.</span><span class="sxs-lookup"><span data-stu-id="28745-266">The STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure is shown here.</span></span>

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

<span data-ttu-id="28745-267">Чтобы указать тип устанавливаемой функции NVMe, настройте структуру STORAGE_PROTOCOL_SPECIFIC_DATA_EXT следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28745-267">To specify a type of NVMe feature to set, configure the STORAGE_PROTOCOL_SPECIFIC_DATA_EXT structure as follows:</span></span>
-   <span data-ttu-id="28745-268">Задайте для поля ProtocolType значение Протоколтипенвме.</span><span class="sxs-lookup"><span data-stu-id="28745-268">Set the ProtocolType field to ProtocolTypeNvme;</span></span>
-   <span data-ttu-id="28745-269">Задайте в поле DataType значение перечисления Нвмедататипефеатуре, определенное STORAGE_PROTOCOL_NVME_DATA_TYPE.</span><span class="sxs-lookup"><span data-stu-id="28745-269">Set the DataType field to the enumeration value NVMeDataTypeFeature defined by STORAGE_PROTOCOL_NVME_DATA_TYPE;</span></span>

<span data-ttu-id="28745-270">В следующих примерах демонстрируется набор функций NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-270">The following examples demonstrate NVMe feature set.</span></span>

### <a name="example-nvme-set-features"></a><span data-ttu-id="28745-271">Пример: параметры SET NVMe</span><span class="sxs-lookup"><span data-stu-id="28745-271">Example: NVMe Set Features</span></span>

<span data-ttu-id="28745-272">В этом примере запрос Set Features отправляется на диск NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-272">In this example, the Set Features request is sent to an NVMe drive.</span></span> <span data-ttu-id="28745-273">Следующий код подготавливает структуру данных SET, а затем отправляет команду на устройство через DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="28745-273">The following code prepares the set data structure and then sends the command down to the device via DeviceIoControl.</span></span>

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a><span data-ttu-id="28745-274">Запросы температуры</span><span class="sxs-lookup"><span data-stu-id="28745-274">Temperature queries</span></span>

<span data-ttu-id="28745-275">В Windows 10 [**\_ \_ \_ свойство запроса хранилища ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) можно также использовать для запроса данных о температуре с устройств NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-275">In Windows 10, [**IOCTL\_STORAGE\_QUERY\_PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) can also be used to query temperature data from NVMe devices.</span></span>

<span data-ttu-id="28745-276">Чтобы получить сведения о температуре с диска NVMe в [**\_ \_ \_ дескрипторе данных температуры хранилища**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), настройте структуру [**\_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="28745-276">To retrieve temperature information from an NVMe drive in the [**STORAGE\_TEMPERATURE\_DATA\_DESCRIPTOR**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure the [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure as follows:</span></span>

-   <span data-ttu-id="28745-277">Выделение буфера, который может содержать структуру [**\_ \_ запроса свойства хранилища**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .</span><span class="sxs-lookup"><span data-stu-id="28745-277">Allocate a buffer that can contains a [**STORAGE\_PROPERTY\_QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) structure.</span></span>

-   <span data-ttu-id="28745-278">Задайте для поля **PropertyID** значение **сторажеадаптертемпературепроперти** или **сторажедевицетемпературепроперти** для запроса контроллера или устройства/пространства имен соответственно.</span><span class="sxs-lookup"><span data-stu-id="28745-278">Set the **PropertyID** field to **StorageAdapterTemperatureProperty** or **StorageDeviceTemperatureProperty** for a controller or device/namespace request, respectively.</span></span>

-   <span data-ttu-id="28745-279">Задайте для поля **QueryType** значение **пропертистандардкуери**.</span><span class="sxs-lookup"><span data-stu-id="28745-279">Set the **QueryType** field to **PropertyStandardQuery**.</span></span>

<span data-ttu-id="28745-280">Здесь показана структура [**\_ \_ сведений о температуре хранилища**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (из Windows 10).</span><span class="sxs-lookup"><span data-stu-id="28745-280">The [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure (from Windows 10) is shown here.</span></span>


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a><span data-ttu-id="28745-281">Изменение поведения команд</span><span class="sxs-lookup"><span data-stu-id="28745-281">Behavior changing commands</span></span>

<span data-ttu-id="28745-282">Команды, которые управляют атрибутами устройства или потенциально влияют на поведение устройства, сложнее для работы с операционной системой.</span><span class="sxs-lookup"><span data-stu-id="28745-282">Commands that manipulate device attributes or potentially impact device behavior are more difficult for the operating system to deal with.</span></span> <span data-ttu-id="28745-283">Если при обработке операций ввода-вывода атрибуты устройств изменяются во время выполнения, в случае неправильной обработки могут возникнуть проблемы с синхронизацией или целостностью данных.</span><span class="sxs-lookup"><span data-stu-id="28745-283">If device attributes change at run-time while I/O is being processed, synchronization or data integrity issues can arise if not properly handled.</span></span>

<span data-ttu-id="28745-284">Команда NVMe **Set-Features** — хороший пример команды изменения поведения.</span><span class="sxs-lookup"><span data-stu-id="28745-284">The NVMe **Set-Features** command is a good example of a behavior changing command.</span></span> <span data-ttu-id="28745-285">Он позволяет изменять механизм арбитража и устанавливать пороговые значения температуры.</span><span class="sxs-lookup"><span data-stu-id="28745-285">It allows for the changing of the arbitration mechanism and the setting of temperature thresholds.</span></span> <span data-ttu-id="28745-286">Чтобы гарантировать, что данные на лету не подвергаются риску при отправке команд Set, влияющих на поведение, Windows будет приостанавливать все операции ввода-вывода на устройстве NVMe, сбрасывать очереди и очищать буфер.</span><span class="sxs-lookup"><span data-stu-id="28745-286">To ensure that in-flight data is not at risk when behavior-affecting set commands are sent down, Windows will pause all I/O to the NVMe device, drain queues, and flush buffers.</span></span> <span data-ttu-id="28745-287">После успешного выполнения команды Set операции ввода-вывода возобновляются (если это возможно).</span><span class="sxs-lookup"><span data-stu-id="28745-287">Once the set command has executed successfully, I/O is resumed (if possible).</span></span> <span data-ttu-id="28745-288">Если операция ввода-вывода не может быть возобновлена, может потребоваться сброс устройства.</span><span class="sxs-lookup"><span data-stu-id="28745-288">If I/O cannot be resumed, a device reset may be required.</span></span>

### <a name="setting-temperature-thresholds"></a><span data-ttu-id="28745-289">Установка пороговых значений температуры</span><span class="sxs-lookup"><span data-stu-id="28745-289">Setting temperature thresholds</span></span>

<span data-ttu-id="28745-290">В Windows 10 введено [**\_ \_ \_ \_ пороговое значение температуры для набора хранения ioctl**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), IOCTL для получения и установки порогов температуры.</span><span class="sxs-lookup"><span data-stu-id="28745-290">Windows 10 introduced [**IOCTL\_STORAGE\_SET\_TEMPERATURE\_THRESHOLD**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), an IOCTL for getting and setting temperature thresholds.</span></span> <span data-ttu-id="28745-291">Его также можно использовать для получения текущей температуры устройства.</span><span class="sxs-lookup"><span data-stu-id="28745-291">You can also use it to get the current temperature of the device.</span></span> <span data-ttu-id="28745-292">Буфер ввода-вывода для этого IOCTL является структурой [**\_ \_ сведений о температуре хранилища**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) из предыдущего раздела кода.</span><span class="sxs-lookup"><span data-stu-id="28745-292">The input/output buffer for this IOCTL is the [**STORAGE\_TEMPERATURE\_INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) structure, from the previous code section.</span></span>

### <a name="example-setting-over-threshold-temperature"></a><span data-ttu-id="28745-293">Пример. Настройка температуры с чрезмерным пороговым значением</span><span class="sxs-lookup"><span data-stu-id="28745-293">Example: Setting over-threshold temperature</span></span>

<span data-ttu-id="28745-294">В этом примере задается пороговое значение температуры диска NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-294">In this example, an NVMe drive's over-threshold temperature is set.</span></span> <span data-ttu-id="28745-295">Следующий код подготавливает команду, а затем отправляет ее на устройство через DeviceIoControl.</span><span class="sxs-lookup"><span data-stu-id="28745-295">The following code prepares the command and then sends it down to the device via DeviceIoControl.</span></span>


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a><span data-ttu-id="28745-296">Настройка функций для конкретного поставщика</span><span class="sxs-lookup"><span data-stu-id="28745-296">Setting vendor-specific features</span></span>

<span data-ttu-id="28745-297">Без журнала командных эффектов драйвер не знает о последствиях выполнения команды.</span><span class="sxs-lookup"><span data-stu-id="28745-297">Without the Command Effects Log, the driver has no knowledge of the ramifications of the command.</span></span> <span data-ttu-id="28745-298">Именно поэтому требуется журнал командных эффектов.</span><span class="sxs-lookup"><span data-stu-id="28745-298">This is why the Command Effects Log is required.</span></span> <span data-ttu-id="28745-299">Она помогает операционной системе определить, является ли команда высокой, и может ли она параллельно отправляться с другими командами на диск.</span><span class="sxs-lookup"><span data-stu-id="28745-299">It helps the operating system determine if a command is high impact and if it can be sent in parallel with other commands to the drive.</span></span>

<span data-ttu-id="28745-300">Журнал командных эффектов еще не является достаточно детализированным, чтобы охватывать команды **набора функций** , зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="28745-300">The Command Effects Log is not yet granular enough to encompass vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="28745-301">По этой причине невозможно отправить команды **набора функций** , зависящие от поставщика.</span><span class="sxs-lookup"><span data-stu-id="28745-301">For this reason, it is not yet possible to send vendor-specific **Set-Features** commands.</span></span> <span data-ttu-id="28745-302">Однако можно использовать сквозной механизм, рассмотренный ранее, для отправки команд, относящихся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="28745-302">However, it is possible to use the pass-through mechanism, discussed earlier, to send vendor-specific commands.</span></span> <span data-ttu-id="28745-303">Дополнительные сведения см. в разделе [сквозной механизм](#pass-through-mechanism).</span><span class="sxs-lookup"><span data-stu-id="28745-303">For more info, see [Pass-through mechanism](#pass-through-mechanism).</span></span>

## <a name="header-files"></a><span data-ttu-id="28745-304">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="28745-304">Header files</span></span>

<span data-ttu-id="28745-305">Следующие файлы относятся к разработке NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-305">The following files are relevant to NVMe development.</span></span> <span data-ttu-id="28745-306">Эти файлы входят в состав [пакета средств разработки программного обеспечения (SDK) для Microsoft Windows](https://developer.microsoft.com/windows/downloads).</span><span class="sxs-lookup"><span data-stu-id="28745-306">These files are included with the [Microsoft Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads).</span></span>



| <span data-ttu-id="28745-307">Файл заголовка</span><span class="sxs-lookup"><span data-stu-id="28745-307">Header file</span></span>    | <span data-ttu-id="28745-308">Описание</span><span class="sxs-lookup"><span data-stu-id="28745-308">Description</span></span>                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="28745-309">**нтддстор. h**</span><span class="sxs-lookup"><span data-stu-id="28745-309">**ntddstor.h**</span></span> | <span data-ttu-id="28745-310">Определяет константы и типы для доступа к драйверам класса хранилища из режима ядра.</span><span class="sxs-lookup"><span data-stu-id="28745-310">Defines constants and types for accessing the storage class drivers from kernel mode.</span></span>   |
| <span data-ttu-id="28745-311">**nvme. h**</span><span class="sxs-lookup"><span data-stu-id="28745-311">**nvme.h**</span></span>     | <span data-ttu-id="28745-312">Для других структур данных, связанных с NVMe.</span><span class="sxs-lookup"><span data-stu-id="28745-312">For other NVMe-related data-structures.</span></span>                                                 |
| <span data-ttu-id="28745-313">**виниоктл. h**</span><span class="sxs-lookup"><span data-stu-id="28745-313">**winioctl.h**</span></span> | <span data-ttu-id="28745-314">Для общих определений Win32 IOCTL, включая API хранилища для приложений пользовательского режима.</span><span class="sxs-lookup"><span data-stu-id="28745-314">For overall Win32 IOCTL definitions, including storage APIs for user mode applications.</span></span> |



 

 

 
