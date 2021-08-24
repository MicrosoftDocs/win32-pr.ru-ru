---
description: Размер собственного видео изменился.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da9fc430b8d36a61b90f567f082c7224765a702549d050f11555c8e55c387a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792384"
---
# <a name="ec_video_size_changed"></a>\_Размер видео \_ EC \_ изменен

Размер собственного видео изменился.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**DWORD**) СЛОВО низкого порядка задает новую ширину в пикселях; в высоком порядке слово указывает новую высоту (в пикселях).

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Модули подготовки видео могут отправить это событие, если они обнаруживают изменение в собственном размере видео.

Модуль [подготовки видео 7](video-mixing-renderer-filter-7.md) (VMR-7) и [устройство микширования видео 9](video-mixing-renderer-filter-9.md) (VMR-9) отправляют это событие в оконном режиме, но не в режиме без окон или режиме отображения. Дополнительные сведения о режиме окон в фильтре VMR см. в разделе [визуализация видео](video-rendering.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




