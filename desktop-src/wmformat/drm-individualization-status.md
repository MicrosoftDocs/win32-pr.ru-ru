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
ms.openlocfilehash: 081a8714d29cb48236bdb9191c15e92db96b18a9f8c1d9c2388c5baee7783296
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119705654"
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

## <a name="remarks"></a>Remarks

Это перечисление используется структурой [**\_ \_ состояния WM индивидуализируйте**](wm-individualize-status.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                      |
| Версия<br/>                  | Windows Пакет SDK для формата мультимедиа 7 или более поздние версии пакета SDK<br/>                       |
| Заголовок<br/>                   | <dl> <dt>Дрмекстерналс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_состояние HTTP \_ DRM**](drm-http-status.md)
</dt> <dt>

[**Типы перечислений**](enumeration-types.md)
</dt> </dl>

 

 





