---
description: Содержит сведения о кодеках и форматах, которые использовались для кодирования содержимого в формате ASF. Этот атрибут соответствует объекту списка кодеков в заголовке ASF, определенном в спецификации ASF.
ms.assetid: 6dde30d3-dbdc-469c-ad7e-5e670b7e0a64
title: Атрибут MF_PD_ASF_CODECLIST (Вмконтаинер. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 402c53c082ae57fed444168c559f99718322f8a9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693430"
---
# <a name="mf_pd_asf_codeclist-attribute"></a>\_ \_ Атрибут кодеклист MF PD ASF \_

Содержит сведения о кодеках и форматах, которые использовались для кодирования содержимого в формате ASF. Этот атрибут соответствует объекту списка кодеков в заголовке ASF, определенном в спецификации ASF.

## <a name="data-type"></a>Тип данных

массив байтов;

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к дескрипторам представления для содержимого ASF.

Метод [**имфасфконтентинфо:: женератепресентатиондескриптор**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) создает дескриптор представления и создает этот атрибут из объекта списка кодеков в заголовке ASF. Приложение, использующее [источник мультимедиа ASF](asf-media-source.md) , может получить этот атрибут путем вызова [**Имфмедиасаурце:: креатепресентатиондескриптор**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) и получения атрибута из дескриптора представления.

В следующей таблице показана структура большого двоичного объекта атрибута.



| Поле объекта списка кодеков | Тип данных    | Размер    | Описание                           |
|-------------------------|--------------|---------|---------------------------------------|
| Число записей кодека     | **DWORD**    | 4 байта | Число кодеков                      |
| Записи кодека           | **ДВУХБАЙТОВЫХ**\[\] | Различается  | Массив информационных структур кодеков |



 

Поле "записи кода" представляет собой массив структур. В следующей таблице показан формат каждой записи.



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Поле объекта списка кодеков</th>
<th>Тип данных</th>
<th>Размер</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Тип</td>
<td><strong>DWORD</strong></td>
<td>4 байта</td>
<td>Тип кодека. Может иметь одно из следующих значений:<br/>
<ul>
<li>0x0001: аудиокодек</li>
<li>0x0002: видеокодек</li>
<li>0xFFFF: неизвестно</li>
</ul></td>
</tr>
<tr class="even">
<td>Длина имени кодека</td>
<td><strong>DWORD</strong></td>
<td>4 байта</td>
<td>Размер строки имени кодека в байтах, включая символ <strong>null</strong> .</td>
</tr>
<tr class="odd">
<td>Имя кодека</td>
<td><strong>WCHAR</strong>[]</td>
<td>Различается</td>
<td>Строка Юникода, заканчивающаяся нулем, которая содержит имя кодека, например &quot; Windows Media Video 9 &quot; .</td>
</tr>
<tr class="even">
<td>Длина описания кодека</td>
<td><strong>DWORD</strong></td>
<td>4 байта</td>
<td>Размер строки описания кодека в байтах, включая символ <strong>null</strong> .</td>
</tr>
<tr class="odd">
<td>Описание кодека</td>
<td><strong>WCHAR</strong>[]</td>
<td>Различается</td>
<td>Строка в Юникоде, заканчивающаяся нулем и содержащая описание кодека.</td>
</tr>
<tr class="even">
<td>Длина сведений о кодека</td>
<td><strong>DWORD</strong></td>
<td>4 байта</td>
<td>Размер поля сведений кодека в байтах.</td>
</tr>
<tr class="odd">
<td>Сведения о кодека</td>
<td><strong>Byte</strong>[]</td>
<td>Различается</td>
<td>Данные кодека. Значение этих данных зависит от кодека. Как правило, эти данные обозначают формат.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Макет большого двоичного объекта атрибута не точно соответствует макету объекта списка кодеков в заголовке ASF. В частности, длины строк задаются в байтах и включают размер терминатора **null** .

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Вмконтаинер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: BLOB**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**Имфаттрибутес:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**имфпресентатиондескриптор**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[Атрибуты дескриптора представления](presentation-descriptor-attributes.md)
</dt> <dt>

[Объект заголовка ASF](asf-file-structure.md)
</dt> <dt>

[Дескрипторы представления](presentation-descriptors.md)
</dt> </dl>

 

 




