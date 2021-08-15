---
description: Задает приоритет базового потока для модуля чтения исходного кода или средства записи приемника.
ms.assetid: 9513AE28-2AF4-45EC-AC19-C0718540E26F
title: Атрибут MF_READWRITE_MMCSS_PRIORITY (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56f108b7cce9f1c9d6226803bf2a2cc32b62ac94077f7f84cbc78e632cb25ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118740606"
---
# <a name="mf_readwrite_mmcss_priority-attribute"></a>\_ \_ \_ Атрибут приоритета MMCSS для MF ReadWrite

Задает приоритет базового потока для модуля чтения исходного кода или средства записи приемника.

## <a name="data-type"></a>Тип данных

**Int32** хранится как **UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Remarks

При необходимости задайте этот атрибут при создании экземпляра модуля [чтения источника](source-reader.md) или [средства записи приемника](sink-writer.md). Если этот атрибут задан, также необходимо задать атрибут [ \_ \_ \_ класса MMCSS MF ReadWrite](mf-readwrite-mmcss-class.md) . В противном случае этот атрибут игнорируется.

Когда модуль чтения источника или модуль записи приемника регистрирует потоки с помощью [службы планировщика классов мультимедиа](../procthread/multimedia-class-scheduler-service.md), значение этого атрибута указывает базовый приоритет потока. Если этот атрибут не задан, значение по умолчанию равно нулю.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ приложения UWP для классических приложений \|\]<br/>                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ приложения UWP для классических приложений \|\]<br/>                              |
| Header<br/>                   | <dl> <dt>Мфреадврите. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
