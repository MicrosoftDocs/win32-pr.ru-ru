---
description: Модуль подготовки видео переключается в полноэкранный режим.
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: EC_FULLSCREEN_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf9384bec15969c904636f37db21ab19674bd2468542c2984ce80aa1773c3c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079134"
---
# <a name="ec_fullscreen_lost"></a>неполноэкранный режим EC \_ \_

Модуль подготовки видео переключается в полноэкранный режим.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Ноль.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) модуля подготовки видео или **значение NULL**.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Нет.

## <a name="remarks"></a>Remarks

Когда модуль [подготовки отчетов к просмотру](full-screen-renderer-filter.md) теряет активацию, он отправляет это событие. Когда модуль подготовки видео переключается из полноэкранного режима, диспетчер графа фильтров отправляет это событие в ответ на событие [**\_ активации EC**](ec-activate.md) из модуля подготовки отчетов.

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

 

 




