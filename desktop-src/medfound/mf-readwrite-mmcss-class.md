---
description: Указывает класс мультимедиа класса службы планировщика классов (MMCSS) для модуля чтения источника или приемника.
ms.assetid: A3A295E8-AC9C-4641-ADDA-B97D5AB13A9A
title: Атрибут MF_READWRITE_MMCSS_CLASS (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d2088ba09bf4f8ad9516d9b2117ab54161d7ac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103817128"
---
# <a name="mf_readwrite_mmcss_class-attribute"></a>\_ \_ Атрибут класса MMCSS MF ReadWrite \_

Указывает класс [мультимедиа класса службы планировщика классов](../procthread/multimedia-class-scheduler-service.md) (MMCSS) для модуля чтения источника или приемника.

## <a name="data-type"></a>Тип данных

**LPWSTR**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Комментарии

При необходимости задайте этот атрибут при создании экземпляра модуля [чтения источника](source-reader.md) или [средства записи приемника](sink-writer.md). Значение атрибута должно быть допустимым именем класса MMCSS.

Если этот атрибут задан, модуль чтения источника или модуль записи приемника регистрирует все свои потоки с помощью указанного класса MMCSS. Служба MMCSS гарантирует, что обработка данных в модуле чтения источника или в модуле записи приемника имеет приоритет над другими системными задачами.

Чтобы указать базовый приоритет, установите атрибут [ \_ \_ \_ приоритета MMCSS в MF ReadWrite](mf-readwrite-mmcss-priority.md) . Если этот атрибут не задан, базовый приоритет равен нулю.

Для потоков обработки звука атрибут [ \_ \_ \_ \_ Audio класса MMCSS ReadWrite](mf-readwrite-mmcss-class-audio.md) (если он задан) переопределяет этот атрибут.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8 \|\]<br/>                                        |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфреадврите. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
