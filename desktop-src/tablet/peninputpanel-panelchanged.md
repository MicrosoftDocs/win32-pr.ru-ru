---
description: Не рекомендуется. Пенинпутпанел был заменен панелью ввода текста (TIP). Происходит при изменении объекта Пенинпутпанел между макетами.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Событие Пенинпутпанел. Панелчанжед (Мсинкаут. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f722609ae71761a2a2a05c743aba7bfd83b7d4ff8689333bf2093d4dc21345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117856523"
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

## <a name="remarks"></a>Remarks

При создании объекта [**пенинпутпанел**](peninputpanel-class.md) используется [**Рукописный ввод**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) по умолчанию **панелтипе**. Если изменить панель, установив свойство [**куррентпанел**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) до того, как панель ввода пера станет активной в первый раз, происходит событие **панелчанжед** .

Событие **панелчанжед** не возникает, когда пользователь изменяет между линией с текстом и упакованным Pad.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                       |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                           |
| Header<br/>                   | <dl> <dt>Мсинкаут. h (также требуется Мсинкаут \_ i. c)</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>InkObj.dll</dt> </dl>                               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**пенинпутпанел**](peninputpanel-class.md)
</dt> </dl>

 

 
