---
description: Не рекомендуется. Пенинпутпанел был заменен панелью ввода текста (TIP). Происходит при изменении объекта Пенинпутпанел между макетами.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Событие Пенинпутпанел. Панелчанжед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347872"
---
# <a name="peninputpanelpanelchanged-event"></a>Пенинпутпанел. Панелчанжед, событие

Не рекомендуется. [**Пенинпутпанел**](peninputpanel-class.md) был заменен [панелью ввода текста (TIP)](text-input-panel-reference.md).

Происходит при изменении объекта [**пенинпутпанел**](peninputpanel-class.md) между макетами.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Невпанелтипе* \[ окне\]
</dt> <dd>

Новый тип панели, используемый для входных данных в объекте [**пенинпутпанел**](peninputpanel-class.md) после срабатывания события **панелчанжед** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если это событие завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

При создании объекта [**пенинпутпанел**](peninputpanel-class.md) используется [**Рукописный ввод**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) по умолчанию **панелтипе**. Если изменить панель, установив свойство [**куррентпанел**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) до того, как панель ввода пера станет активной в первый раз, происходит событие **панелчанжед** .

Событие **панелчанжед** не возникает, когда пользователь изменяет между линией с текстом и упакованным Pad.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только классические приложения Windows XP Tablet PC Edition \[\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**пенинпутпанел**](peninputpanel-class.md)
</dt> </dl>

 

 
