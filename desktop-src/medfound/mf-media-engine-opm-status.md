---
description: Определяет состояние диспетчера выходной защиты (ОПМ).
ms.assetid: 7C4D88F6-369B-4364-90C4-6D0F8DD1523B
title: Перечисление MF_MEDIA_ENGINE_OPM_STATUS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MEDIA_ENGINE_OPM_STATUS
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: 98efb0054402f8bf019e91d639f16322a1378a23dfeee76cd31daea9d12bf6fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013044"
---
# <a name="mf_media_engine_opm_status-enumeration"></a>\_ \_ \_ Перечисление состояния ОПМ для подсистемы передачи мультимедиа MF \_

Определяет состояние [диспетчера выходной защиты](output-protection-manager.md) (ОПМ).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum _MF_MEDIA_ENGINE_OPM_STATUS { 
  MF_MEDIA_ENGINE_OPM_NOT_REQUESTED           =  0,
  MF_MEDIA_ENGINE_OPM_ESTABLISHED             = 1,
  MF_MEDIA_ENGINE_OPM_FAILED_VM               = 2,
  MF_MEDIA_ENGINE_OPM_FAILED_BDA              = 3,
  MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER  = 4,
  MF_MEDIA_ENGINE_OPM_FAILED                  = 5
} MF_MEDIA_ENGINE_OPM_STATUS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MF_MEDIA_ENGINE_OPM_NOT_REQUESTED"></span><span id="mf_media_engine_opm_not_requested"></span>**\_ \_ ОПМ подсистема мультимедиа MF \_ \_ не \_ запрошена**
</dt> <dd>

Состояние по умолчанию. Используется для возврата правильного состояния, когда содержимое не защищено.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_ESTABLISHED"></span><span id="mf_media_engine_opm_established"></span>**\_ \_ опмная система мультимедиа MF \_ \_ установлена**
</dt> <dd>

ОПМ успешно установлен.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_VM"></span><span id="mf_media_engine_opm_failed_vm"></span>**\_ \_ \_ \_ сбой \_ виртуальной машины ОПМ в MF Media Engine**
</dt> <dd>

Сбой ОПМ из-за запуска в виртуальной машине (ВМ).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_BDA"></span><span id="mf_media_engine_opm_failed_bda"></span>**\_BDA Media \_ Engine \_ ОПМ \_ Failed \_**
</dt> <dd>

Сбой ОПМ из-за отсутствия графического драйвера, и система использует базовый видеоадаптер (BDA).

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED_UNSIGNED_DRIVER"></span><span id="mf_media_engine_opm_failed_unsigned_driver"></span>**\_ \_ \_ \_ \_ неподписанный драйвер ОПМ для подсистемы передачи мультимедиа MF \_**
</dt> <dd>

Сбой ОПМ из-за того, что графический драйвер не подписан PE, вернемся к ИСКРИВЛЕНию.

</dd> <dt>

<span id="MF_MEDIA_ENGINE_OPM_FAILED"></span><span id="mf_media_engine_opm_failed"></span>**\_ \_ сбой ОПМ для механизма передачи мультимедиа \_ MF \_**
</dt> <dd>

Не удалось выполнить ОПМ по другим причинам.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                      |
| IDL<br/>                      | <dl> <dt>Мфмедиаенгине. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления Media Foundation](media-foundation-enumerations.md)
</dt> </dl>

 

 




