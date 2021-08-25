---
description: Указывает количество времени, которое компонент принимает для обработки каждого образца.
ms.assetid: 84f81ee1-76d8-46fb-86ef-2500f8f4ef36
title: EC_PROCESSING_LATENCY (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb107dd4c895f9819d268e6112c22c0c514e480bf778692f28bc87853aee9bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792624"
---
# <a name="ec_processing_latency"></a>\_Задержка обработки \_ EC

Указывает количество времени, которое компонент принимает для обработки каждого образца.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**\_ время ссылки на константу** \* ) количество времени для обработки каждого образца в единицах с 100 до единицы.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Выступающий для [**расширенного фильтра модуля подготовки видео**](enhanced-video-renderer-filter.md) (Евр) может отправить это сообщение в евр, чтобы уведомить Евр о задержке обработки в выступающем.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Коды уведомлений о событиях](event-notification-codes.md)
</dt> <dt>

[Уведомление о событии в DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




