---
description: TAPI отправляет \_ сообщение о состоянии телефона приложению при каждом изменении состояния телефонного устройства.
ms.assetid: 74e74b62-8387-4056-83e6-2350b3da4077
title: Сообщение PHONE_STATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db52f16d6c377087fd6ccadc5e70b5bb2865da2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674811"
---
# <a name="phone_state-message"></a>\_Сообщение о состоянии телефона

TAPI отправляет сообщение **о \_ состоянии телефона** приложению при каждом изменении состояния телефонного устройства.


```C++
            
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хфоне* 
</dt> <dd>

Маркер телефонного устройства.

</dd> <dt>

*двкаллбаккинстанце* 
</dt> <dd>

Экземпляр обратного вызова приложения, предоставленный при открытии телефонного устройства.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Состояние телефона, которое было изменено. Этот параметр использует одну из [**\_ констант фонестате**](phonestate--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Сведения об изменении состояния, зависящие от состояния телефона. Этот параметр не используется, если в *dwParam1* задано несколько флагов, так как изменилось несколько элементов состояния. Приложение должно вызвать [**фонежетстатус**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) для получения полного набора сведений.

Если *dwParam1* является фонестате \_ owner, *dwParam2* содержит новое число владельцев.

Если *dwParam1* — \_ мониторы фонестате *, dwParam2* содержит новое число мониторов.

Если *dwParam1* — фонестате \_ лампа, *dwParam2* содержит идентификатор кнопки или лампы измененной лампы.

Если *dwParam1* имеет значение фонестате \_ рингмоде, *dwParam2* содержит новый режим кольца.

Если *dwParam1* — фонестатеная \_ трубка, докладчик или гарнитура, *dwParam2* содержит новый режим хуксвитч для устройства хуксвитч. Этот параметр использует одну из [**\_ констант фонехуксвитчмоде**](phonehookswitchmode--constants.md).

</dd> <dt>

*dwParam3* 
</dt> <dd>

Не используется.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="remarks"></a>Комментарии

Отправка сообщения **о \_ состоянии телефона** приложению можно контролировать и запрашивать с помощью [**фонесетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) и [**фонежетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages). По умолчанию это сообщение отключено для всех изменений состояния, за исключением ФОНЕСТАТЕ \_ reinit, который нельзя отключить. Это сообщение отправляется во все приложения, имеющие маркер для телефона, включая те, которые вызвали [**фонеопен**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) с параметром *двпривилежес* , настроенным на фонепривилеже \_ owner или фонепривилеже \_ Monitor.

Сообщение **о \_ состоянии телефона** с указанием владельцев и (или) мониторов отправляется в приложения, у которых уже есть маркер для телефона. Это может быть результатом другого приложения, изменяющего владение или мониторингом телефонного устройства с помощью [**фонеопен**](/windows/desktop/api/Tapi/nf-tapi-phoneopen), [**фонеклосе**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) или [**фонешутдовн**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_закрытие телефона**](phone-close.md)
</dt> <dt>

[**фонекапс**](/windows/desktop/api/Tapi/ns-tapi-phonecaps)
</dt> <dt>

[**фонеклосе**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)
</dt> <dt>

[**фонежетдевкапс**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)
</dt> <dt>

[**фонежетстатус**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus)
</dt> <dt>

[**фонежетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages)
</dt> <dt>

[**фонеинитиализе**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[**фонеинитиализикс**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[**фонеопен**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[**фонесетстатусмессажес**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages)
</dt> <dt>

[**фонешутдовн**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




