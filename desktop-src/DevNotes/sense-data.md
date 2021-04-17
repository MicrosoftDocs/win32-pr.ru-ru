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
# <a name="sense_data-structure"></a>Структура данных с ОСМЫСЛЕНными \_ данными

Используется для передачи сведений о состоянии или ошибке в ответ на команду **датчика запросов** SCSI.

## <a name="syntax"></a>Синтаксис


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



## <a name="members"></a>Члены

<dl> <dt>

**ErrorCode**
</dt> <dd>

Тип отчета.



| Значение                                                                           | Значение                     |
|---------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0x70</dt> </dl> | Текущие ошибки.<br/>  |
| <dl> <dt>0x71</dt> </dl> | Отложенные ошибки.<br/> |



 

</dd> <dt>

**Допустимо**
</dt> <dd>

1, если **информационное** поле определено в стандарте; в противном случае **информационное** поле зависит от поставщика и не определяется стандартом.

</dd> <dt>

**сегментнумбер**
</dt> <dd>

Является устаревшей.

</dd> <dt>

**сенсекэй**
</dt> <dd>

Указывает категорию ошибки.

<dl> <dt>

<span id="No_Sense"></span><span id="no_sense"></span><span id="NO_SENSE"></span>**Нет смысла** (0x0)
</dt> <dt>

<span id="Recovered_Error"></span><span id="recovered_error"></span><span id="RECOVERED_ERROR"></span>**Восстановленная ошибка** (0x1)
</dt> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Не готово** (0x2)
</dt> <dt>

<span id="Medium_Error"></span><span id="medium_error"></span><span id="MEDIUM_ERROR"></span>**Средняя ошибка** (0x3)
</dt> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Аппаратная ошибка** (0x4)
</dt> <dt>

<span id="Illegal_Request"></span><span id="illegal_request"></span><span id="ILLEGAL_REQUEST"></span>**Недопустимый запрос** (0x5)
</dt> <dt>

<span id="Unit_Attention"></span><span id="unit_attention"></span><span id="UNIT_ATTENTION"></span>**Внимание к единицам** (0x6)
</dt> <dt>

<span id="Data_Protect"></span><span id="data_protect"></span><span id="DATA_PROTECT"></span>**Защита данных** (0x7)
</dt> <dt>

<span id="Firmware_Error"></span><span id="firmware_error"></span><span id="FIRMWARE_ERROR"></span>**Ошибка встроенного по** (0x9)
</dt> <dt>

<span id="Aborted_Command"></span><span id="aborted_command"></span><span id="ABORTED_COMMAND"></span>**Прерванная Команда** (0xB)
</dt> <dt>

<span id="Equal"></span><span id="equal"></span><span id="EQUAL"></span>**Равно** (0xC)
</dt> <dt>

<span id="Volume_Overflow"></span><span id="volume_overflow"></span><span id="VOLUME_OVERFLOW"></span>**Переполнение тома** (0xD)
</dt> <dt>

<span id="Miscompare"></span><span id="miscompare"></span><span id="MISCOMPARE"></span>**Неравенство** (0xE)
</dt> </dl> </dd> <dt>

**Reserved**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**инкорректленгс**
</dt> <dd>

1, если запрошенная Длина логического блока не совпадает с длиной логического блока данных на носителе.

</dd> <dt>

**ендофмедиа**
</dt> <dd>

1, если устройство с последовательным доступом достиг конца носителя или в принтере нет бумаги.

</dd> <dt>

**Метка файла**
</dt> <dd>

1, если текущая команда достигла метка файла или сетмарк. Допустимо только для последовательных устройств доступа.

</dd> <dt>

**Информация**
</dt> <dd>

Данные типа устройства или команды.

</dd> <dt>

**аддитионалсенселенгс**
</dt> <dd>

Длина оставшейся части структуры в байтах. Общая длина минус 7.

</dd> <dt>

**коммандспеЦифиЦинформатион**
</dt> <dd>

Данные, относящиеся к команде. Значения определяются в соответствующей стандартной команде.

</dd> <dt>

**аддитионалсенсекоде**
</dt> <dd>

Специфичный для устройства код, описывающий ошибку, обнаруженную в поле **сенсекэй** .

</dd> <dt>

**аддитионалсенсекодекуалифиер**
</dt> <dd>

Может содержать дополнительные сведения о поле **аддитионалсенсекоде** .

</dd> <dt>

**фиелдреплацеаблеуниткоде**
</dt> <dd>

Сведения о компоненте, связанном с этими данными, зависит от поставщика.

</dd> <dt>

**сенсекэйспеЦифик**
</dt> <dd>

Содержимое и формат сведений об основном ключе определяются значением поля **сенсекэй** .

</dd> </dl>

## <a name="remarks"></a>Комментарии

Дополнительные сведения о формате осмысленных данных см. в разделе [команда датчика запросов SCSI](https://wikipedia.org/wiki/SCSI_command) ( https://wikipedia.org/wiki/SCSI_command) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows XP\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                              |
| Header<br/>                   | <dl> <dt>SCSI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Передача цели iSCSI](/powershell/module/iscsi)
</dt> <dt>

[\_прямой проход \_ через \_ SCSI](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_pass_through_direct)
</dt> </dl>

 

 




