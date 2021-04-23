---
description: Представляет входные параметры аналогового видео для монитора компьютера.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: Класс Вмимонитораналогвидеоинпутпарамс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998860"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a><span data-ttu-id="438d8-103">Класс Вмимонитораналогвидеоинпутпарамс</span><span class="sxs-lookup"><span data-stu-id="438d8-103">WmiMonitorAnalogVideoInputParams class</span></span>

<span data-ttu-id="438d8-104">Класс WMI **вмимонитораналогвидеоинпутпарамс** представляет аналоговые входные параметры видео монитора компьютера.</span><span class="sxs-lookup"><span data-stu-id="438d8-104">The **WmiMonitorAnalogVideoInputParams** WMI class represents the analog video input parameters of a computer monitor.</span></span> <span data-ttu-id="438d8-105">Данные в этом классе соответствуют данным в определении видеовходного видео по стандарту (E-EDID) расширенному расширенному отображению данных.</span><span class="sxs-lookup"><span data-stu-id="438d8-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="438d8-106">Экземпляр этого класса доступен, только если свойство **видеоинпуттипе** класса [**вмимониторбасикдисплайпарамс**](wmimonitorbasicdisplayparams.md) имеет значение "аналоговый".</span><span class="sxs-lookup"><span data-stu-id="438d8-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Analog".</span></span>

## <a name="syntax"></a><span data-ttu-id="438d8-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="438d8-107">Syntax</span></span>

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a><span data-ttu-id="438d8-108">Члены</span><span class="sxs-lookup"><span data-stu-id="438d8-108">Members</span></span>

<span data-ttu-id="438d8-109">Класс **вмимонитораналогвидеоинпутпарамс** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="438d8-109">The **WmiMonitorAnalogVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="438d8-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="438d8-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="438d8-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="438d8-111">Properties</span></span>

<span data-ttu-id="438d8-112">Класс **вмимонитораналогвидеоинпутпарамс** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="438d8-112">The **WmiMonitorAnalogVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="438d8-113">**Активен**</span><span class="sxs-lookup"><span data-stu-id="438d8-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="438d8-114">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="438d8-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="438d8-115">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="438d8-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="438d8-116">Указывает активный монитор.</span><span class="sxs-lookup"><span data-stu-id="438d8-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="438d8-117">**компоситесинксуппортед**</span><span class="sxs-lookup"><span data-stu-id="438d8-117">**CompositeSyncSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="438d8-118">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="438d8-118">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="438d8-119">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="438d8-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="438d8-120">Указывает, поддерживается ли составная синхронизация.</span><span class="sxs-lookup"><span data-stu-id="438d8-120">Indicates whether composite sync is supported.</span></span>



| <span data-ttu-id="438d8-121">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-121">Value</span></span>                                                                              | <span data-ttu-id="438d8-122">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-122">Meaning</span></span>                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="438d8-123"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-123"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="438d8-124">Поддерживается составная синхронизация по горизонтальной линии синхронизации.</span><span class="sxs-lookup"><span data-stu-id="438d8-124">Composite sync on horizontal sync line is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="438d8-125"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-125"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="438d8-126">Составная синхронизация по горизонтальной линии синхронизации не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="438d8-126">Composite sync on horizontal sync line is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="438d8-127">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="438d8-127">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="438d8-128">Тип данных: **строка**</span><span class="sxs-lookup"><span data-stu-id="438d8-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="438d8-129">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="438d8-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="438d8-130">Квалификаторы: **ключ**</span><span class="sxs-lookup"><span data-stu-id="438d8-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="438d8-131">Имя конкретного экземпляра монитора.</span><span class="sxs-lookup"><span data-stu-id="438d8-131">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="438d8-132">**сепаратесинкссуппортед**</span><span class="sxs-lookup"><span data-stu-id="438d8-132">**SeparateSyncsSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="438d8-133">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="438d8-133">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="438d8-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="438d8-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="438d8-135">Указывает, поддерживаются ли отдельные синхронизации.</span><span class="sxs-lookup"><span data-stu-id="438d8-135">Indicates whether separate syncs are supported.</span></span>



| <span data-ttu-id="438d8-136">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-136">Value</span></span>                                                                              | <span data-ttu-id="438d8-137">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-137">Meaning</span></span>                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="438d8-138"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-138"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="438d8-139">Поддерживаются отдельные синхронизации.</span><span class="sxs-lookup"><span data-stu-id="438d8-139">Separate syncs are supported.</span></span><br/>     |
| <dl> <span data-ttu-id="438d8-140"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-140"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="438d8-141">Отдельные синхронизации не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="438d8-141">Separate syncs are not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="438d8-142">**серратионофвсинкрекуиред**</span><span class="sxs-lookup"><span data-stu-id="438d8-142">**SerrationOfVsyncRequired**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="438d8-143">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="438d8-143">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="438d8-144">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="438d8-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="438d8-145">Указывает, требуется ли вертикальная синхронизация Pulse серратион.</span><span class="sxs-lookup"><span data-stu-id="438d8-145">Indicates whether vertical sync pulse serration is required.</span></span>



| <span data-ttu-id="438d8-146">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-146">Value</span></span>                                                                              | <span data-ttu-id="438d8-147">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-147">Meaning</span></span>                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="438d8-148"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-148"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="438d8-149">При использовании композитной синхронизации или использования видео на зеленом уровне требуется серратион вертикального пульса синхронизации.</span><span class="sxs-lookup"><span data-stu-id="438d8-149">Serration of the vertical sync pulse is required when composite sync or sync-on-green video is used.</span></span><br/>     |
| <dl> <span data-ttu-id="438d8-150"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-150"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="438d8-151">Серратионный пульс синхронизации не требуется, если используется композитная синхронизация или синхронизация на зеленом видео.</span><span class="sxs-lookup"><span data-stu-id="438d8-151">Serration of the vertical sync pulse is not required when composite sync or sync-on-green video is used.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="438d8-152">**сетупекспектед**</span><span class="sxs-lookup"><span data-stu-id="438d8-152">**SetupExpected**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="438d8-153">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="438d8-153">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="438d8-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="438d8-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="438d8-155">Указывает, ожидается ли программа установки.</span><span class="sxs-lookup"><span data-stu-id="438d8-155">Indicates whether setup is expected.</span></span>



| <span data-ttu-id="438d8-156">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-156">Value</span></span>                                                                              | <span data-ttu-id="438d8-157">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-157">Meaning</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="438d8-158"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-158"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="438d8-159">Монитору требуется установка пустого значения или пьедестал в соответствии со стандартом соответствующего уровня сигнала.</span><span class="sxs-lookup"><span data-stu-id="438d8-159">Monitor expects a blank-to-blank setup or pedestal per appropriate Signal Level Standard.</span></span><br/>                      |
| <dl> <span data-ttu-id="438d8-160"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-160"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="438d8-161">Монитор не ждет установки пустого значения или пьедестал в соответствии со стандартом соответствующего уровня сигнала.</span><span class="sxs-lookup"><span data-stu-id="438d8-161">Monitor does not expect a blank-to-blank setup or pedestal according to the appropriate signal level standard.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="438d8-162">**сигналлевелстандард**</span><span class="sxs-lookup"><span data-stu-id="438d8-162">**SignalLevelStandard**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="438d8-163">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="438d8-163">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="438d8-164">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="438d8-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="438d8-165">Стандарт уровня сигнала для подключений расширенного видео Connector (EVC).</span><span class="sxs-lookup"><span data-stu-id="438d8-165">Signal level standard for Enhanced video connector (EVC) connections.</span></span>



| <span data-ttu-id="438d8-166">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-166">Value</span></span>                                                                              | <span data-ttu-id="438d8-167">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-167">Meaning</span></span>                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="438d8-168"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-168"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="438d8-169">0,7, 0,3 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="438d8-169">0.7,0.3\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="438d8-170"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-170"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="438d8-171">0.714, 0.286 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="438d8-171">0.714,0.286\[V\]</span></span><br/> |
| <dl> <span data-ttu-id="438d8-172"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-172"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="438d8-173">1,0, 0,4. \[ V\]</span><span class="sxs-lookup"><span data-stu-id="438d8-173">1.0,0.4\[V\]</span></span><br/>     |
| <dl> <span data-ttu-id="438d8-174"><dt>3 (0x3)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-174"><dt>3 (0x3)</dt></span></span> </dl> | <span data-ttu-id="438d8-175">0,7, 0.0 \[ V\]</span><span class="sxs-lookup"><span data-stu-id="438d8-175">0.7,0.0\[V\]</span></span><br/>     |



 

</dd> <dt>

<span data-ttu-id="438d8-176">**синконгринвидеосуппортед**</span><span class="sxs-lookup"><span data-stu-id="438d8-176">**SyncOnGreenVideoSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="438d8-177">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="438d8-177">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="438d8-178">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="438d8-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="438d8-179">Указывает, поддерживается ли синхронизация по зеленому цвету.</span><span class="sxs-lookup"><span data-stu-id="438d8-179">Indicates whether sync on green is supported.</span></span>



| <span data-ttu-id="438d8-180">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-180">Value</span></span>                                                                              | <span data-ttu-id="438d8-181">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-181">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="438d8-182"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-182"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="438d8-183">Поддерживается синхронизация на зеленом видео.</span><span class="sxs-lookup"><span data-stu-id="438d8-183">Sync on green video is supported.</span></span><br/>     |
| <dl> <span data-ttu-id="438d8-184"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-184"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="438d8-185">Синхронизация на зеленом видео не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="438d8-185">Sync on green video is not supported.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="438d8-186">Требования</span><span class="sxs-lookup"><span data-stu-id="438d8-186">Requirements</span></span>



| <span data-ttu-id="438d8-187">Требование</span><span class="sxs-lookup"><span data-stu-id="438d8-187">Requirement</span></span> | <span data-ttu-id="438d8-188">Значение</span><span class="sxs-lookup"><span data-stu-id="438d8-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="438d8-189">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="438d8-189">Minimum supported client</span></span><br/> | <span data-ttu-id="438d8-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="438d8-190">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="438d8-191">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="438d8-191">Minimum supported server</span></span><br/> | <span data-ttu-id="438d8-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="438d8-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="438d8-193">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="438d8-193">Namespace</span></span><br/>                | <span data-ttu-id="438d8-194">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="438d8-194">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="438d8-195">MOF</span><span class="sxs-lookup"><span data-stu-id="438d8-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="438d8-196"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-196"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="438d8-197">DLL</span><span class="sxs-lookup"><span data-stu-id="438d8-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="438d8-198"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="438d8-198"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="438d8-199">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="438d8-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="438d8-200">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="438d8-200">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




