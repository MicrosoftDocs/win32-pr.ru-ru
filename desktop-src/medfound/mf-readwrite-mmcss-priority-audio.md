---
description: Задает базовый приоритет для потоков обработки звука, созданных модулем чтения источника или модулем записи приемника.
ms.assetid: C0E3A472-959F-4F74-8906-03630DE4CB8C
title: Атрибут MF_READWRITE_MMCSS_PRIORITY_AUDIO (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c33f3e4cab26a448c3b5a28c6f3cfe631a7c1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701704"
---
# <a name="mf_readwrite_mmcss_priority_audio-attribute"></a>\_ \_ \_ Звуковой атрибут MMCSS с приоритетом MF ReadWrite \_

Задает базовый приоритет для потоков обработки звука, созданных модулем чтения источника или модулем записи приемника.

## <a name="data-type"></a>Тип данных

**Int32** хранится как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

При необходимости задайте этот атрибут при создании экземпляра модуля [чтения источника](source-reader.md) или [средства записи приемника](sink-writer.md). Если этот атрибут задан, также следует установить атрибут [ \_ \_ \_ Audio класса MMCSS для \_ записи на MF](mf-readwrite-mmcss-class-audio.md) . В противном случае этот атрибут игнорируется.

Когда модуль чтения исходного кода или модуль записи приемника регистрирует потоки обработки звука с помощью [службы планировщика классов мультимедиа](../procthread/multimedia-class-scheduler-service.md), значение этого атрибута указывает базовый приоритет потока. Если этот атрибут не задан, значение по умолчанию равно нулю.

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

 

 
