---
description: Аллловс Расширенный модуль подготовки видео (Евр) для смешивания видео в прямоугольнике, который меньше, чем прямоугольник вывода, а затем масштабирует результат.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: Атрибут EVRConfig_AllowScaling (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1d0662c7145d9f5c5484df81c2483305402850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896565"
---
# <a name="evrconfig_allowscaling-attribute"></a>Еврконфиг \_ алловскалинг, атрибут

Аллловс Расширенный модуль подготовки видео (Евр) для смешивания видео в прямоугольнике, который меньше, чем прямоугольник вывода, а затем масштабирует результат.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Этот атрибут можно задать в приемнике носителей Евр. Чтобы задать атрибут, используйте **QueryInterface** , чтобы запросить приемник мультимедиа Евр для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Установка этого атрибута оказывает тот же результат, что и установка флага **мфвидеорендерпрефс \_ АЛЛОВСКАЛИНГ** в Евр. Описание этого флага см. в разделе [**мфвидеорендерпрефс**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .

Константа GUID для этого атрибута экспортируется из стрмиидс. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>UUID. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты Евр](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Управление качеством видео](video-quality-management.md)
</dt> </dl>

 

 




