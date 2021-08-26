---
description: Окно видео активируется или деактивируется.
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: EC_ACTIVATE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14d9b0ad192045f179d9f0f366eed6a32efb0e6cc6f61b47255f118b7f55258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966064"
---
# <a name="ec_activate"></a>\_Активация EC

Окно видео активируется или деактивируется.

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

(**Bool**) **Значение true** , если окно активируется, или **значение false** , если окно деактивировано.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

(**IUnknown** \* ) Указатель на интерфейс [**ибасефилтер**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) визуализатора.

</dd> </dl>

## <a name="default-action"></a>Действие по умолчанию

Диспетчер графов фильтров устанавливает фокус с помощью интерфейса [**метод IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) . Он не отправляет уведомление о событии в приложение.

## <a name="remarks"></a>Remarks

Модуль обработки видео отправляет это событие всякий раз, когда окно активируется или деактивируется (то есть при получении сообщения WM \_ активатеапп). Активация или деактивация окна может быть вызвана тем, что окно получило или потеряло фокус, либо поскольку модуль подготовки отчетов переключен между полноэкранным режимом и оконным режимом.

Это событие позволяет диспетчеру фильтров графа выделять ресурсы, зависящие от фокуса окна, например звуковыми устройствами.

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

 

 




