---
description: Указывает время окончания презентации.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: Атрибут MF_TOPONODE_MEDIASTOP (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea2abc172151afe404f3acc6cf8c75d03bd0ac495564cb0f322283998677f83b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663874"
---
# <a name="mf_toponode_mediastop-attribute"></a>\_Атрибут MF топоноде \_ медиастоп

Указывает время окончания презентации.

## <a name="data-type"></a>Тип данных

**UINT64**

Рассматривать как значение **лонглонг** .

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).

## <a name="applies-to"></a>Применяется к

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a>Remarks

Этот атрибут задает позицию в источнике, в которой воспроизведение останавливается в единицах с 100-наносекундных относительных загрузок относительно начала источника. Если атрибут не задан, воспроизведение останавливается в конце источника. Например, чтобы прерывать воспроизведение с 5-секундным отметкой, установите для этого атрибута значение 50000000. Задайте атрибут для исходных узлов в топологии (узлы с типом, равным **MF \_ \_ саурцестреам \_ node**). Задайте атрибут перед вызовом [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).

> [!Note]  
> Если вы вручную вставили декодер в топологию, необходимо также задать значение [MF \_ топоноде \_ Маркин \_ здесь](mf-toponode-markin-here-attribute.md) и [MF \_ топоноде \_ отметить \_ здесь](mf-toponode-markout-here-attribute.md) атрибуты в узле декодера.

 

После установки топологии Установка этого атрибута не оказывает никакого влияния.

Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**. Однако отрицательные значения не имеют смысла.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                               |
| Заголовок<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Время представления последовательности](sequence-presentation-times.md)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> <dt>

[**MF \_ топоноде \_ медиастарт**](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




