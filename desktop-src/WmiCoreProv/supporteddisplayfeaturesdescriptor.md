---
description: Представляет поддерживаемые функции отображения монитора.
ms.assetid: 28eeead3-8fb9-4720-8d93-1c6757dfb31b
title: Класс Суппортеддисплайфеатуресдескриптор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SupportedDisplayFeaturesDescriptor
- SupportedDisplayFeaturesDescriptor.ActiveOffSupported
- SupportedDisplayFeaturesDescriptor.DisplayType
- SupportedDisplayFeaturesDescriptor.GTFSupported
- SupportedDisplayFeaturesDescriptor.HasPreferredTimingMode
- SupportedDisplayFeaturesDescriptor.sRGBSupported
- SupportedDisplayFeaturesDescriptor.StandbySupported
- SupportedDisplayFeaturesDescriptor.SuspendSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 30350d477533b7e51ba8b3130c5a24d81c12f10e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701789"
---
# <a name="supporteddisplayfeaturesdescriptor-class"></a><span data-ttu-id="8ab21-103">Класс Суппортеддисплайфеатуресдескриптор</span><span class="sxs-lookup"><span data-stu-id="8ab21-103">SupportedDisplayFeaturesDescriptor class</span></span>

<span data-ttu-id="8ab21-104">**Суппортеддисплайфеатуресдескриптор** представляет поддерживаемые функции отображения монитора.</span><span class="sxs-lookup"><span data-stu-id="8ab21-104">The **SupportedDisplayFeaturesDescriptor** represents the supported display features of the monitor.</span></span> <span data-ttu-id="8ab21-105">Сведения в этом классе соответствуют данным в определении входного видео для расширенного расширенного представления идентификационных данных по стандарту (E-EDID).</span><span class="sxs-lookup"><span data-stu-id="8ab21-105">The information in this class corresponds to data in the Video Input Definition of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ab21-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ab21-106">Syntax</span></span>

``` syntax
class SupportedDisplayFeaturesDescriptor
{
  boolean ActiveOffSupported;
  uint8   DisplayType;
  boolean GTFSupported;
  boolean HasPreferredTimingMode;
  boolean sRGBSupported;
  boolean StandbySupported;
  boolean SuspendSupported;
};
```

## <a name="members"></a><span data-ttu-id="8ab21-107">Члены</span><span class="sxs-lookup"><span data-stu-id="8ab21-107">Members</span></span>

<span data-ttu-id="8ab21-108">Класс **суппортеддисплайфеатуресдескриптор** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8ab21-108">The **SupportedDisplayFeaturesDescriptor** class has these types of members:</span></span>

-   [<span data-ttu-id="8ab21-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="8ab21-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8ab21-110">Свойства</span><span class="sxs-lookup"><span data-stu-id="8ab21-110">Properties</span></span>

<span data-ttu-id="8ab21-111">Класс **суппортеддисплайфеатуресдескриптор** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="8ab21-111">The **SupportedDisplayFeaturesDescriptor** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8ab21-112">**активеоффсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8ab21-112">**ActiveOffSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ab21-113">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8ab21-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ab21-114">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ab21-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ab21-115">Поддержка активных и очень низких возможностей.</span><span class="sxs-lookup"><span data-stu-id="8ab21-115">Support for active off and very low power.</span></span> <span data-ttu-id="8ab21-116">При получении сигнала о времени, который находится за пределами объявленного активного диапазона, экран потребляет меньше энергии.</span><span class="sxs-lookup"><span data-stu-id="8ab21-116">The display consumes less power when it receives a timing signal that is outside the declared active operating range.</span></span> <span data-ttu-id="8ab21-117">Если сигнал времени возвращается к нормальному диапазону работы, отображение будет отменено до обычной операции.</span><span class="sxs-lookup"><span data-stu-id="8ab21-117">The display will revert to normal operation if the timing signal returns to the normal operating range.</span></span> <span data-ttu-id="8ab21-118">Примеры повременных сигналов за пределами обычного диапазона работы не являются сигналами синхронизации или отсутствием сигнала "DE".</span><span class="sxs-lookup"><span data-stu-id="8ab21-118">Examples of timing signals outside the normal operating range are no sync signals or no DE signal.</span></span>

</dd> <dt>

<span data-ttu-id="8ab21-119">**дисплайтипе**</span><span class="sxs-lookup"><span data-stu-id="8ab21-119">**DisplayType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ab21-120">Тип данных: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="8ab21-120">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="8ab21-121">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ab21-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ab21-122">Тип отображения для монитора.</span><span class="sxs-lookup"><span data-stu-id="8ab21-122">Type of display for the monitor.</span></span> <span data-ttu-id="8ab21-123">В следующей таблице перечислены возможные значения.</span><span class="sxs-lookup"><span data-stu-id="8ab21-123">The following table lists possible values.</span></span>



| <span data-ttu-id="8ab21-124">Значение</span><span class="sxs-lookup"><span data-stu-id="8ab21-124">Value</span></span>                                                                              | <span data-ttu-id="8ab21-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8ab21-125">Meaning</span></span>                                 |
|------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="8ab21-126"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="8ab21-126"><dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="8ab21-127">Монохромный/черно-белый экран</span><span class="sxs-lookup"><span data-stu-id="8ab21-127">Monochrome/grayscale display</span></span><br/> |
| <dl> <span data-ttu-id="8ab21-128"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="8ab21-128"><dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="8ab21-129">Отображение цвета RGB</span><span class="sxs-lookup"><span data-stu-id="8ab21-129">RGB color display</span></span><br/>            |
| <dl> <span data-ttu-id="8ab21-130"><dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="8ab21-130"><dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="8ab21-131">Цветовой дисплей не RGB</span><span class="sxs-lookup"><span data-stu-id="8ab21-131">Non-RGB multicolor display</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="8ab21-132">**гтфсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8ab21-132">**GTFSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ab21-133">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8ab21-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ab21-134">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ab21-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ab21-135">Указывает, имеет ли дисплей ГТФ поддержку.</span><span class="sxs-lookup"><span data-stu-id="8ab21-135">Indicates whether the display has GTF support.</span></span> <span data-ttu-id="8ab21-136">Если **значение — true**, отображение поддерживает время на основе стандарта ГТФ, использующего значения параметров ГТФ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8ab21-136">If **True**, the display supports timings based on the GTF standard using default GTF parameter values.</span></span>

</dd> <dt>

<span data-ttu-id="8ab21-137">**хаспреферредтимингмоде**</span><span class="sxs-lookup"><span data-stu-id="8ab21-137">**HasPreferredTimingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ab21-138">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8ab21-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ab21-139">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ab21-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ab21-140">Указывает, имеет ли дисплей предпочтительный режим времени.</span><span class="sxs-lookup"><span data-stu-id="8ab21-140">Indicates whether the display has has a preferred timing mode.</span></span> <span data-ttu-id="8ab21-141">Если **значение — true**, первый подробный блок времени содержит предпочтительный режим времени для монитора.</span><span class="sxs-lookup"><span data-stu-id="8ab21-141">If **True**, the first detailed timing block contains the preferred timing mode of the monitor.</span></span> <span data-ttu-id="8ab21-142">Использование предпочтительного режима времени требуется для EDID v. 1.3 и более поздних версий.</span><span class="sxs-lookup"><span data-stu-id="8ab21-142">Use of preferred timing mode is required by EDID v.1.3 and higher.</span></span>

</dd> <dt>

<span data-ttu-id="8ab21-143">**сргбсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8ab21-143">**sRGBSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ab21-144">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8ab21-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ab21-145">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ab21-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ab21-146">Если **значение — true**, экран поддерживает sRGB.</span><span class="sxs-lookup"><span data-stu-id="8ab21-146">If **True**, the display supports sRGB.</span></span>

</dd> <dt>

<span data-ttu-id="8ab21-147">**стандбисуппортед**</span><span class="sxs-lookup"><span data-stu-id="8ab21-147">**StandbySupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ab21-148">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8ab21-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ab21-149">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ab21-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ab21-150">Указывает, поддерживает ли дисплей сигнал дисплея VESA для управления питанием (ДПМС) в режиме ожидания.</span><span class="sxs-lookup"><span data-stu-id="8ab21-150">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) standby.</span></span> <span data-ttu-id="8ab21-151">Если задано **значение true**, ДПМС Standby поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8ab21-151">If **True**, DPMS standby is supported.</span></span>

</dd> <dt>

<span data-ttu-id="8ab21-152">**суспендсуппортед**</span><span class="sxs-lookup"><span data-stu-id="8ab21-152">**SuspendSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8ab21-153">Тип данных: **логический**</span><span class="sxs-lookup"><span data-stu-id="8ab21-153">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="8ab21-154">Тип доступа: только для чтения</span><span class="sxs-lookup"><span data-stu-id="8ab21-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8ab21-155">Указывает, поддерживает ли дисплей приостановку сигнала управления питанием VESA дисплея (ДПМС).</span><span class="sxs-lookup"><span data-stu-id="8ab21-155">Indicates whether the display supports VESA Display Power Management Signaling (DPMS) suspend.</span></span> <span data-ttu-id="8ab21-156">Если **значение — true**, ДПМС Suspend поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8ab21-156">If **True**, DPMS suspend is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ab21-157">Требования</span><span class="sxs-lookup"><span data-stu-id="8ab21-157">Requirements</span></span>



| <span data-ttu-id="8ab21-158">Требование</span><span class="sxs-lookup"><span data-stu-id="8ab21-158">Requirement</span></span> | <span data-ttu-id="8ab21-159">Значение</span><span class="sxs-lookup"><span data-stu-id="8ab21-159">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ab21-160">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8ab21-160">Minimum supported client</span></span><br/> | <span data-ttu-id="8ab21-161">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ab21-161">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8ab21-162">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8ab21-162">Minimum supported server</span></span><br/> | <span data-ttu-id="8ab21-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ab21-163">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8ab21-164">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="8ab21-164">Namespace</span></span><br/>                | <span data-ttu-id="8ab21-165">Корневой \\ инструментарий WMI</span><span class="sxs-lookup"><span data-stu-id="8ab21-165">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="8ab21-166">MOF</span><span class="sxs-lookup"><span data-stu-id="8ab21-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ab21-167"><dt>Вмикоре. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ab21-167"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ab21-168">DLL</span><span class="sxs-lookup"><span data-stu-id="8ab21-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ab21-169"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ab21-169"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ab21-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8ab21-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ab21-171">**мсмониторкласс**</span><span class="sxs-lookup"><span data-stu-id="8ab21-171">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




