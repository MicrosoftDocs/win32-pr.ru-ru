---
description: Модуль подготовки видео был уничтожен или удален из графа.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675033"
---
# <a name="ec_window_destroyed"></a>\_окно EC \_ уничтожено

Модуль подготовки видео был уничтожен или удален из графа.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**IUnknown** \* ) Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) модуля подготовки видео.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Ноль.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Диспетчер графов фильтров освобождает это окно в качестве фокуса через интерфейс [**метод IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . Он не отправляет уведомление о событии в приложение.

## <a name="remarks"></a>Комментарии

Модуль подготовки видео отправляет это событие, когда оно покидает граф фильтра в своем методе [**ибасефилтер:: жоинфилтерграф**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) . (Отправка события при уничтожении фильтра может быть слишком поздно, так как в этом случае диспетчер графов фильтров также может быть уничтожен.)

Это событие позволяет другим фильтрам получать ресурсы, зависящие от фокуса окна, например звуковыми устройствами.

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

 

 




