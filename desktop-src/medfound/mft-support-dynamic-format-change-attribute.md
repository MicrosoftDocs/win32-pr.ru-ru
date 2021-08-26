---
description: Указывает, поддерживает ли преобразование Media Foundation (MFT) динамическое изменение формата.
ms.assetid: 64d32c78-8bee-4d3c-a770-5a097cb71b13
title: Атрибут MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE (Мфапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d9bfd2185006975cf128cc60f2b774eba6ba74229b3e290c743c4cde3930
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012614"
---
# <a name="mft_support_dynamic_format_change-attribute"></a>Основная таблица MFT \_ поддерживает \_ \_ \_ атрибут изменения динамического формата

Указывает, поддерживает ли преобразование Media Foundation (MFT) динамическое изменение формата.

## <a name="data-type"></a>Тип данных

**UINT32**

Рассматривать как логическое значение.

## <a name="remarks"></a>Remarks

Этот атрибут может иметь следующие значения.



| Значение     | Описание                                                            |
|-----------|------------------------------------------------------------------------|
| **TRUE**  | Клиент может изменить входной формат во время потоковой передачи.               |
| **FALSE** | Таблица MFT должна быть остановлена, прежде чем клиент сможет изменить входной формат. |



 

Чтобы получить этот атрибут, сначала вызовите [**имфтрансформ:: InAttribute**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) , чтобы получить глобальное хранилище АТРИБУТОВ для MFT. Затем вызовите [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) , чтобы получить значение атрибута.

Если [**произошел сбой или атрибут не**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) задан, по умолчанию используется значение **false**.

[Асинхронный МФТС](asynchronous-mfts.md) должен возвращать значение **true**.

Дополнительные сведения см. в разделе [Обработка изменений в потоковой передаче](handling-stream-changes.md).

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Приложения UWP для классических приложений Vista \|\]<br/>                              |
| Минимальная версия сервера<br/> | Windows \[Приложения UWP для классических приложений сервера 2008 \|\]<br/>                        |
| Заголовок<br/>                   | <dl> <dt>Мфапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Асинхронный МФТС](asynchronous-mfts.md)
</dt> <dt>

[Атрибуты преобразования](transform-attributes.md)
</dt> <dt>

[**Имфаттрибутес:: UINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**Имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
</dt> </dl>

 

 




