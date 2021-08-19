---
description: Аллловс Расширенный модуль подготовки видео (Евр) для смешивания видео в прямоугольнике, который меньше, чем прямоугольник вывода, а затем масштабирует результат.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: Атрибут EVRConfig_AllowScaling (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83323c42ac81d4cce0bb42733bd4246959cf0fc9a58b5705579a86aee9b2bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879428"
---
# <a name="evrconfig_allowscaling-attribute"></a>Еврконфиг \_ алловскалинг, атрибут

Аллловс Расширенный модуль подготовки видео (Евр) для смешивания видео в прямоугольнике, который меньше, чем прямоугольник вывода, а затем масштабирует результат.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

Этот атрибут можно задать в приемнике носителей Евр. Чтобы задать атрибут, используйте **QueryInterface** , чтобы запросить приемник мультимедиа Евр для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Установка этого атрибута оказывает тот же результат, что и установка флага **мфвидеорендерпрефс \_ АЛЛОВСКАЛИНГ** в Евр. Описание этого флага см. в разделе [**мфвидеорендерпрефс**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .

Константа GUID для этого атрибута экспортируется из стрмиидс. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows \[Только для настольных приложений сервера 2008 R2\]<br/>                            |
| Заголовок<br/>                   | <dl> <dt>UUID. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты Евр](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Управление качеством видео](video-quality-management.md)
</dt> </dl>

 

 




