---
description: Указывает максимальное число кадров длинной ссылки (LTR), управляемых приложением.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: Свойство CODECAPI_AVEncVideoLTRBufferControl (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cca2e24e8295969609ba325a2abf24be76fb07c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481930"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>КОДЕКАПИ \_ авенквидеолтрбуфферконтрол, свойство

Указывает максимальное число кадров длинной ссылки (LTR), управляемых приложением.

## <a name="data-type"></a>Тип данных

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенквидеолтрбуфферконтрол**

## <a name="property-value"></a>Значение свойства

Значение этого элемента управления включает два поля, где каждое поле имеет 16 бит.




| Значение | Значение | 
|-------|---------|
| <span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl><dt><strong>Первое поле</strong></dt><dt>битов [0.. 15]</dt></dl> | Число кадров LTR, управляемых приложением.<br /><strong>Кодировщики H. 264/AVC:</strong><br /> Предполагая, что значение N, а N — ненулевое значение, в каждом кадре IDR кодировщик должен автоматически пометить кадры, следующие за кадром IDR (включая фрейм IDR), как кадры LTR, если все три из следующих условий:<ul><li>Рамка еще не помечена как рамка долгосрочной ссылки.</li><li>Кадр является основным кадром слоя. Например, элемент синтаксиса <strong>temporal_id</strong> равен 0.</li><li>Число кадров, помеченных в настоящий момент как LTR, меньше N.</li></ul><br /> | 
| <span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl><dt><strong>Второе поле</strong></dt><dt>битов [16.. 31]</dt></dl> | Режим доверия для элемента управления LTR.<br /><strong>Кодировщики H. 264/AVC:</strong><br /> 1 (отношение доверия до) означает, что кодировщик может использовать рамку LTR, если только приложение явно не сделает его через элемент управления <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> . <br /> Другие значения являются недопустимыми и зарезервированы для будущего использования.<br /> | 




 

## <a name="remarks"></a>Комментарии

Это статический API.

Значение по умолчанию должно быть равно 0

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ приложения UWP для классических приложений \|\]<br/>                                   |
| Минимальная версия сервера<br/> | Windows Server 2012 Приложения универсального \[ приложения UWP для настольных приложений \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




