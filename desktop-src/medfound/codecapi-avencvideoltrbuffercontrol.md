---
description: Указывает максимальное число кадров длинной ссылки (LTR), управляемых приложением.
ms.assetid: C34AD867-5F94-4414-A282-ECC392678635
title: Свойство CODECAPI_AVEncVideoLTRBufferControl (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33adfc7d0ba2db87c2127489d9496dc5e0bb4158
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539626"
---
# <a name="codecapi_avencvideoltrbuffercontrol-property"></a>КОДЕКАПИ \_ авенквидеолтрбуфферконтрол, свойство

Указывает максимальное число кадров длинной ссылки (LTR), управляемых приложением.

## <a name="data-type"></a>Тип данных

**Ulong** (VT \_ UI4)

## <a name="property-guid"></a>GUID свойства

**КОДЕКАПИ \_ авенквидеолтрбуфферконтрол**

## <a name="property-value"></a>Значение свойства

Значение этого элемента управления включает два поля, где каждое поле имеет 16 бит.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение</th>
<th>Значение</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="The_first_field"></span><span id="the_first_field"></span><span id="THE_FIRST_FIELD"></span><dl> <dt><strong>Первое поле</strong></dt> <dt>битов [0.. 15]</dt> </dl></td>
<td>Число кадров LTR, управляемых приложением.<br/> <strong>Кодировщики H. 264/AVC:</strong><br/> Предполагая, что значение N, а N — ненулевое значение, в каждом кадре IDR кодировщик должен автоматически пометить кадры, следующие за кадром IDR (включая фрейм IDR), как кадры LTR, если все три из следующих условий:
<ul>
<li>Рамка еще не помечена как рамка долгосрочной ссылки.</li>
<li>Кадр является основным кадром слоя. Например, элемент синтаксиса <strong>temporal_id</strong> равен 0.</li>
<li>Число кадров, помеченных в настоящий момент как LTR, меньше N.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span id="The_second_field"></span><span id="the_second_field"></span><span id="THE_SECOND_FIELD"></span><dl> <dt><strong>Второе поле</strong></dt> <dt>битов [16.. 31]</dt> </dl></td>
<td>Режим доверия для элемента управления LTR.<br/> <strong>Кодировщики H. 264/AVC:</strong><br/> 1 (отношение доверия до) означает, что кодировщик может использовать рамку LTR, если только приложение явно не сделает его через элемент управления <a href="codecapi-avencvideouseltrframe.md">CODECAPI_AVEncVideoUseLTRFrame</a> . <br/> Другие значения являются недопустимыми и зарезервированы для будущего использования.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Комментарии

Это статический API.

Значение по умолчанию должно быть равно 0

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                   |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                        |
| Header<br/>                   | <dl> <dt>Кодекапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Свойства Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




