---
description: Указывает, как сеанс мультимедиа завершает работу объекта в топологии.
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: Атрибут MF_TOPONODE_NOSHUTDOWN_ON_REMOVE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701701"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a>MF \_ ТОПОНОДЕ \_ отключение \_ при \_ удалении атрибута

Указывает, как сеанс мультимедиа завершает работу объекта в топологии.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Комментарии

Этот атрибут применяется к следующим типам узлов топологии:

-   Выходные узлы
-   Любой узел преобразования, содержащий *асинхронное* преобразование Media Foundation (MFT).

Атрибут может иметь следующие значения:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Значение</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>TRUE</strong></td>
<td>Когда сеанс мультимедиа переключается на новую топологию или очищает текущую топологию, он не завершает работу объекта, принадлежащего этому узлу топологии.</td>
</tr>
<tr class="even">
<td><strong>FALSE</strong></td>
<td>Когда сеанс мультимедиа переключается на новую топологию или очищает текущую топологию, он завершает работу объекта node следующим образом:
<ul>
<li>Выходные узлы. сеанс вызывает <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>имфмедиасинк:: Shutdown</strong></a> в приемнике носителя.</li>
<li>Узлы преобразования. сеанс вызывает <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>имфшутдовн:: Shutdown</strong></a> в MFT.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Значение по умолчанию — **true**.

Если приложение помещает в очередь несколько топологий, рекомендуется присвоить этому атрибуту значение **false**. В противном случае объекты в топологии могут быть неправильно закрыты.

Этот атрибут не применяется, когда приложение завершает сеанс мультимедиа путем вызова [**имфмедиасессион:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Когда сеанс мультимедиа завершает работу, он всегда завершает работу приемников носителей и асинхронных МФТС в текущей топологии.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                     |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                               |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Асинхронный МФТС](asynchronous-mfts.md)
</dt> <dt>

[Атрибуты узла топологии](topology-node-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфтопологиноде**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




