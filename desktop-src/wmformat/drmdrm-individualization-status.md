---
title: Перечисление DRM_INDIVIDUALIZATION_STATUS (Вмдрмсдк. h)
description: '\_Тип перечисления для индивидуальной защиты DRM \_ определяет допустимые состояния для индивидуальной защиты DRM. | Перечисление DRM_INDIVIDUALIZATION_STATUS (Вмдрмсдк. h)'
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- Формат Windows Media DRM_INDIVIDUALIZATION_STATUS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669163"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a>Перечисление DRM_INDIVIDUALIZATION_STATUS (Вмдрмсдк. h)

Тип перечисления для **\_ индивидуальной защиты DRM \_** определяет допустимые состояния для индивидуальной защиты DRM.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**столбец indid не \_ определен**
</dt> <dd>

Это значение зарезервировано для использования в будущем.

</dd> <dt>

<span id="INDI_BEGIN"></span><span id="indi_begin"></span>**\_Начало indid**
</dt> <dd>

Указывает начало процесса индивидуализации.

</dd> <dt>

<span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**столбец indid \_ выполнен**
</dt> <dd>

Указывает, что процесс индивидуализации завершен.

</dd> <dt>

<span id="INDI_FAIL"></span><span id="indi_fail"></span>**\_Ошибка indid**
</dt> <dd>

Указывает, что процесс индивидуализации завершился ошибкой.

</dd> <dt>

<span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**\_Отмена indid**
</dt> <dd>

Указывает, что процесс индивидуализации был отменен приложением.

</dd> <dt>

<span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**\_скачивание indid**
</dt> <dd>

Указывает, что загружается обновление безопасности.

</dd> <dt>

<span id="INDI_INSTALL"></span><span id="indi_install"></span>**\_Установка indid**
</dt> <dd>

Указывает, что устанавливается обновление системы безопасности.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](drmwm-individualize-status.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Типы перечислений**](drm-enumeration-types.md)
</dt> </dl>

 

 





