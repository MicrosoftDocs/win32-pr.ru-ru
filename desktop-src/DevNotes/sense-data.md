---
description: Используется для передачи сведений о состоянии или ошибке в ответ на команду датчика запросов SCSI.
ms.assetid: 43B2FE98-1468-4457-AB7D-3038C16E20B6
title: Структура SENSE_DATA (SCSI. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SENSE_DATA
api_type:
- HeaderDef
api_location:
- Scsi.h
ms.openlocfilehash: b5eacf9bee8c2cebf93b27c97a88c691852a3841
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/06/2021
ms.locfileid: "105647773"
---
# <a name="sense_data-structure"></a><span data-ttu-id="5a8a4-103">Структура данных с ОСМЫСЛЕНными \_ данными</span><span class="sxs-lookup"><span data-stu-id="5a8a4-103">SENSE\_DATA structure</span></span>

<span data-ttu-id="5a8a4-104">Используется для передачи сведений о состоянии или ошибке в ответ на команду **датчика запросов** SCSI.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-104">Used to report status or error information in response to a SCSI **Request Sense** command.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a8a4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5a8a4-105">Syntax</span></span>


```C++
typedef struct _SENSE_DATA {
  UCHAR  ErrorCode  :7;
  UCHAR  Valid  :1;
  UCHAR  SegmentNumber;
  UCHAR  SenseKey  :4;
  UCHAR  Reserved  :1;
  UCHAR  IncorrectLength  :1;
  UCHAR  EndOfMedia  :1;
  UCHAR  FileMark  :1;
  UCHAR  Information[4];
  UCHAR  AdditionalSenseLength;
  UCHAR  CommandSpecificInformation[4];
  UCHAR  AdditionalSenseCode;
  UCHAR  AdditionalSenseCodeQualifier;
  UCHAR  FieldReplaceableUnitCode;
  UCHAR  SenseKeySpecific[3];
} SENSE_DATA, *PSENSE_DATA;
```



## <a name="members"></a><span data-ttu-id="5a8a4-106">Члены</span><span class="sxs-lookup"><span data-stu-id="5a8a4-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5a8a4-107">**ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-107">**ErrorCode**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-108">Тип отчета.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-108">The report type.</span></span>



| <span data-ttu-id="5a8a4-109">Значение</span><span class="sxs-lookup"><span data-stu-id="5a8a4-109">Value</span></span>                                                                           | <span data-ttu-id="5a8a4-110">Значение</span><span class="sxs-lookup"><span data-stu-id="5a8a4-110">Meaning</span></span>                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <span data-ttu-id="5a8a4-111"><dt>0x70</dt></span><span class="sxs-lookup"><span data-stu-id="5a8a4-111"><dt>0x70</dt></span></span> </dl> | <span data-ttu-id="5a8a4-112">Текущие ошибки.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-112">Current errors.</span></span><br/>  |
| <dl> <span data-ttu-id="5a8a4-113"><dt>0x71</dt></span><span class="sxs-lookup"><span data-stu-id="5a8a4-113"><dt>0x71</dt></span></span> </dl> | <span data-ttu-id="5a8a4-114">Отложенные ошибки.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-114">Deferred errors.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5a8a4-115">**Допустимо**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-115">**Valid**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-116">1, если **информационное** поле определено в стандарте; в противном случае **информационное** поле зависит от поставщика и не определяется стандартом.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-116">1 if the **Information** field is defined in a standard; otherwise the **Information** field is vendor-specific and not defined by a standard.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-117">**сегментнумбер**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-117">**SegmentNumber**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-118">Является устаревшей.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-118">Obsolete.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-119">**сенсекэй**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-119">**SenseKey**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-120">Указывает категорию ошибки.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-120">Indicates the category of error.</span></span>

<dl> <dt>

<span data-ttu-id="5a8a4-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Нет смысла** (0x0)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-121"><span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**No Sense** (0x0)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Восстановленная ошибка** (0x1)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-122"><span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Recovered Error** (0x1)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (0x2)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-123"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (0x2)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Средняя ошибка** (0x3)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-124"><span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Medium Error** (0x3)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Аппаратная ошибка** (0x4)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-125"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (0x4)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Недопустимый запрос** (0x5)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-126"><span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Illegal Request** (0x5)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Внимание к единицам** (0x6)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-127"><span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Unit Attention** (0x6)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Защита данных** (0x7)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-128"><span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Data Protect** (0x7)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Ошибка встроенного по** (0x9)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-129"><span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Firmware Error** (0x9)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Прерванная Команда** (0xB)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-130"><span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Aborted Command** (0xB)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Равно** (0xC)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-131"><span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Equal** (0xC)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Переполнение тома** (0xD)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-132"><span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Volume Overflow** (0xD)</span></span>
</dt> <dt>

<span data-ttu-id="5a8a4-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Неравенство** (0xE)</span><span class="sxs-lookup"><span data-stu-id="5a8a4-133"><span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Miscompare** (0xE)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="5a8a4-134">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-134">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-135">Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-135">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-136">**инкорректленгс**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-136">**IncorrectLength**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-137">1, если запрошенная Длина логического блока не совпадает с длиной логического блока данных на носителе.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-137">1 if the requested logical block length does not match the logical block length of the data on the media.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-138">**ендофмедиа**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-138">**EndOfMedia**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-139">1, если устройство с последовательным доступом достиг конца носителя или в принтере нет бумаги.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-139">1 if a sequential-access device has reached end-of-media, or a printer is out of paper.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-140">**Метка файла**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-140">**FileMark**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-141">1, если текущая команда достигла метка файла или сетмарк.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-141">1 if the current command has reached a filemark or setmark.</span></span> <span data-ttu-id="5a8a4-142">Допустимо только для последовательных устройств доступа.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-142">Only valid for sequential-access devices.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-143">**Информация**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-143">**Information**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-144">Данные типа устройства или команды.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-144">Device-type or command specific data.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-145">**аддитионалсенселенгс**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-145">**AdditionalSenseLength**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-146">Длина оставшейся части структуры в байтах.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-146">The length in bytes of the remainder of the structure.</span></span> <span data-ttu-id="5a8a4-147">Общая длина минус 7.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-147">The total length minus 7.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-148">**коммандспеЦифиЦинформатион**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-148">**CommandSpecificInformation**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-149">Данные, относящиеся к команде.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-149">Command-specific data.</span></span> <span data-ttu-id="5a8a4-150">Значения определяются в соответствующей стандартной команде.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-150">Values are defined in the appropriate command standard.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-151">**аддитионалсенсекоде**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-151">**AdditionalSenseCode**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-152">Специфичный для устройства код, описывающий ошибку, обнаруженную в поле **сенсекэй** .</span><span class="sxs-lookup"><span data-stu-id="5a8a4-152">Device specific code that describes the error reported in the **SenseKey** field.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-153">**аддитионалсенсекодекуалифиер**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-153">**AdditionalSenseCodeQualifier**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-154">Может содержать дополнительные сведения о поле **аддитионалсенсекоде** .</span><span class="sxs-lookup"><span data-stu-id="5a8a4-154">Can contain additional detail about the **AdditionalSenseCode** field.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-155">**фиелдреплацеаблеуниткоде**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-155">**FieldReplaceableUnitCode**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-156">Сведения о компоненте, связанном с этими данными, зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="5a8a4-156">Vender-specific information about the component associated with this sense data.</span></span>

</dd> <dt>

<span data-ttu-id="5a8a4-157">**сенсекэйспеЦифик**</span><span class="sxs-lookup"><span data-stu-id="5a8a4-157">**SenseKeySpecific**</span></span>
</dt> <dd>

<span data-ttu-id="5a8a4-158">Содержимое и формат сведений об основном ключе определяются значением поля **сенсекэй** .</span><span class="sxs-lookup"><span data-stu-id="5a8a4-158">The content and format of the sense key specific information is determined by the value of the **SenseKey** field.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5a8a4-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5a8a4-159">Remarks</span></span>

<span data-ttu-id="5a8a4-160">Дополнительные сведения о формате осмысленных данных см. в разделе [команда датчика запросов SCSI](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .</span><span class="sxs-lookup"><span data-stu-id="5a8a4-160">For more information about the sense data format, see [SCSI Request Sense Command](https://wikipedia.org/wiki/SCSI_command) (https://wikipedia.org/wiki/SCSI_command).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a8a4-161">Требования</span><span class="sxs-lookup"><span data-stu-id="5a8a4-161">Requirements</span></span>



| <span data-ttu-id="5a8a4-162">Требование</span><span class="sxs-lookup"><span data-stu-id="5a8a4-162">Requirement</span></span> | <span data-ttu-id="5a8a4-163">Значение</span><span class="sxs-lookup"><span data-stu-id="5a8a4-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5a8a4-164">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5a8a4-164">Minimum supported client</span></span><br/> | <span data-ttu-id="5a8a4-165">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5a8a4-165">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5a8a4-166">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5a8a4-166">Minimum supported server</span></span><br/> | <span data-ttu-id="5a8a4-167">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5a8a4-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5a8a4-168">Header</span><span class="sxs-lookup"><span data-stu-id="5a8a4-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a8a4-169"><dt>SCSI. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a8a4-169"><dt>Scsi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a8a4-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5a8a4-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a8a4-171">Передача цели iSCSI</span><span class="sxs-lookup"><span data-stu-id="5a8a4-171">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="5a8a4-172">\_прямой проход \_ через \_ SCSI</span><span class="sxs-lookup"><span data-stu-id="5a8a4-172">SCSI\_PASS\_THROUGH\_DIRECT</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




