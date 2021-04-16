---
description: Указывает, использует ли приемник выборочного захвата часы презентации для планирования образцов.
ms.assetid: 780ec4a6-8e14-4b81-9d50-82b2850c70ae
title: Атрибут MF_SAMPLEGRABBERSINK_IGNORE_CLOCK (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57ad5476779d958bdbf94af554d889dd8d174ca3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712252"
---
# <a name="mf_samplegrabbersink_ignore_clock-attribute"></a>\_ \_ Атрибут часов пропуска MF самплеграбберсинк \_

Указывает, использует ли приемник выборочного захвата часы презентации для планирования образцов.

## <a name="data-type"></a>Тип данных

**UINT32**

## <a name="getset"></a>Get/Set

Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Комментарии

Этот атрибут можно задать для объекта активации, созданного функцией [**мфкреатесамплеграбберсинкактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesamplegrabbersinkactivate) . Задайте атрибут перед вызовом метода [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) для объекта активации.

По умолчанию, когда приемник выборки получает пример, он ждет, пока время презентации примера не вызовет обратный вызов приложения. Если атрибут MF \_ самплеграбберсинк \_ Ignore \_ не равен нулю, приемник выборки игнорирует часы презентации и вызывает обратный вызов, как только он получает каждый пример.

Рекомендуемое использование:

-   Если требуется как можно быстрее обрабатывать примеры, установите для этого атрибута **значение true**.
-   Если нужно, чтобы вызовы метода обратного вызова синхронизировались с часами, не устанавливайте этот атрибут или присвойте ему значение **false**. Вы можете получить образцы несколько раз в часы, сохраняя их синхронизацию, установив атрибут [**\_ \_ \_ \_ смещения Самплеграбберсинк выборки**](mf-samplegrabbersink-sample-time-offset-attribute.md) в формате MF.

Константа GUID для этого атрибута экспортируется из мфууид. lib.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                         |
| Минимальная версия сервера<br/> | Только классические приложения Windows Server 2008 R2 \[\]<br/>                            |
| Header<br/>                   | <dl> <dt>Мфидл. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Алфавитный список атрибутов Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Атрибуты Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 




