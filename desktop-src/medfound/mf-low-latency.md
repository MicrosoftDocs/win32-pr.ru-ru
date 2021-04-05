---
description: Включает обработку с низкой задержкой в конвейере Microsoft Media Foundation.
ms.assetid: 4D11B4D6-8CFF-4850-BF8F-9019A1F79153
title: Атрибут MF_LOW_LATENCY (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d1b0a89452256f01fc893ced7dc191fd064bbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815512"
---
# <a name="mf_low_latency-attribute"></a>\_Атрибут низкой \_ задержки MF

Включает обработку с низкой задержкой в конвейере Microsoft Media Foundation.

## <a name="data-type"></a>Тип данных

**Bool** , сохраненный как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Низкая задержка определяется как наименьшая возможная задержка от момента создания (или получения) данных мультимедиа до их подготовки к просмотру. Низкая задержка желательно для сценариев связи в режиме реального времени. В других сценариях, таких как локальное воспроизведение или перекодирование, обычно не следует включать режим с низкой задержкой, так как он может повлиять на качество.

> [!Note]  
> Значение GUID этого атрибута идентично свойству [кодекапи \_ авловлатенцимоде](codecapi-avlowlatencymode.md) , определенному для интерфейса [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) .

 

Установите этот атрибут в компонентах конвейера следующим образом:

-   Источник мультимедиа: используйте метод [**имфмедиасаурцеекс:: жетсаурцеаттрибутес**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getsourceattributes) .
-   Преобразование Media Foundation (MFT): используйте метод [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Для кодировщиков кодировщик может поддерживать низкую задержку через интерфейс [**икодекапи**](/windows/win32/api/strmif/nn-strmif-icodecapi) .
-   Приемник мультимедиа. запросите приемник мультимедиа для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Обычно приложения не задают этот атрибут непосредственно в компонентах конвейера, а устанавливают атрибут для одного из следующих объектов:

-   [Сеанс мультимедиа](media-session.md): используйте параметр *пконфигуатион* функции [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) или задайте атрибут в топологии.
-   [Модуль чтения исходного кода](source-reader.md): Задайте атрибут в свойствах конфигурации при создании модуля чтения исходного кода. Дополнительные сведения см. в разделе [атрибуты модуля чтения исходного кода](source-reader-attributes.md).
-   [Модуль записи приемника](sink-writer.md): Задайте атрибут в свойствах конфигурации при создании модуля записи приемника. Дополнительные сведения см. в разделе [атрибуты модуля записи приемника](sink-writer-attributes.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты модуля записи приемника](sink-writer-attributes.md)
</dt> <dt>

[Атрибуты модуля чтения исходного кода](source-reader-attributes.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> </dl>

 

 
