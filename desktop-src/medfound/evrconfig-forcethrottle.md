---
description: Заставляет Расширенный модуль обработки видео (Евр) ограничивать выходные данные в соответствии с пропускной способностью GPU.
ms.assetid: e81e67d6-aa72-44c1-90e9-72ab18bca1c9
title: Атрибут EVRConfig_ForceThrottle (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39cef0bd032eeaf84129e74274b59dbafadbc47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342482"
---
# <a name="evrconfig_forcethrottle-attribute"></a>Еврконфиг \_ форцесроттле, атрибут

Заставляет Расширенный модуль обработки видео (Евр) ограничивать выходные данные в соответствии с пропускной способностью GPU.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Этот атрибут можно задать в приемнике носителей Евр. Чтобы задать атрибут, используйте **IUnknown:: QueryInterface** , чтобы запросить приемник мультимедиа Евр для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Установка этого атрибута оказывает тот же результат, что и установка флага **мфвидеорендерпрефс \_ ФОРЦЕАУТПУТСРОТТЛИНГ** в Евр. Описание этого флага см. в разделе [**мфвидеорендерпрефс**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .

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

 

 




