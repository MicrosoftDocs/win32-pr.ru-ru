---
title: Перечисление DRM_INDIVIDUALIZATION_STATUS (Дрмекстерналс. h)
description: '\_Тип перечисления для индивидуальной защиты DRM \_ определяет допустимые состояния для индивидуальной защиты DRM. | Перечисление DRM_INDIVIDUALIZATION_STATUS (Дрмекстерналс. h)'
ms.assetid: 76748fb3-340e-47e2-969d-5e857bb4e4d8
keywords:
- Формат Windows Media DRM_INDIVIDUALIZATION_STATUS перечисления
- Формат Windows Media для перечисления
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d59a19c58c775ee22d78e17bc09add2825948e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104424293"
---
# <a name="drm_individualization_status-enumeration-drmexternalsh"></a>Перечисление DRM_INDIVIDUALIZATION_STATUS (Дрмекстерналс. h)

Тип перечисления для **\_ индивидуальной защиты DRM \_** определяет допустимые состояния для [*индивидуальной*](wmformat-glossary.md)защиты DRM. Когда приложение инициирует индивидуальную работу с помощью вызова [**ивмдрмреадер:: индивидуализируйте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize), ход выполнения запроса на индивидуальную передачу передается приложению посредством вызовов метода [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Все сообщения о состоянии индивидуальной работы будут использовать \_ член ВМТ индивидуализируйте типа [**перечисления \_ ВМТ**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) в качестве параметра *Status* . Состояние индивидуализации передается в **OnStatus** в параметре *pValue* .

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

Указывает, что процесс индивидуализации был отменен в результате вызова [**ивмдрмреадер:: канцелиндивидуализатион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancelindividualization).

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

Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](wm-individualize-status.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                      |
| Версия<br/>                  | Пакет SDK для Windows Media Format 7 или более поздние версии пакета SDK<br/>                       |
| Header<br/>                   | <dl> <dt>Дрмекстерналс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_состояние HTTP \_ DRM**](drm-http-status.md)
</dt> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





