---
title: WM/Picture
description: Атрибут WM/Picture содержит изображение, связанное с содержимым.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- Формат мультимедиа Windows WM/Picture
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103986954"
---
# <a name="wmpicture"></a>WM/Picture

Атрибут **WM/Picture** содержит изображение, связанное с содержимым.

## <a name="global-constant"></a>Глобальная константа

g \_ всзвмпиктуре

## <a name="data-type"></a>Тип данных

[**WM \_ Рисунок**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**\_ \_ двоичный тип ВМТ**)

## <a name="remarks"></a>Комментарии

Этот атрибут совместим с кадром ID3, APIC. Спецификация ID3 для кадра APIC подразумевает, что, хотя может существовать любое количество кадров APIC, связанных с файлом, только один из них может иметь тип 1, а только один может иметь тип 2. В спецификации также указывается, что описание изображения не может содержать более 64 символов, но может быть пустым.

Атрибуты WM/Picture, добавленные с помощью объектов пакета SDK формата Windows Media, не проверяются автоматически в соответствии со спецификациями ID3. Необходимо добавить код в приложение для выполнения проверок, если требуется обеспечить полную совместимость с ID3.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Список атрибутов**](attribute-list.md)
</dt> <dt>

[**\_изображение WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




