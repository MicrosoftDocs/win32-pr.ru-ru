---
description: Размер собственного видео изменился.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675547"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




