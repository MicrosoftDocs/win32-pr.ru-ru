---
description: Метод Нотифйовнермессаже передает в окно видео определенные сообщения.
ms.assetid: 8b27281a-5b8a-46c3-aa66-390d4496f30e
title: Кбасеконтролвиндов. Нотифйовнермессаже, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.NotifyOwnerMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d71057027bd8fbd572dffd714f761ff101ba0de95dd42dcf058009b0cb1b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526854"
---
# <a name="cbasecontrolwindownotifyownermessage-method"></a>Кбасеконтролвиндов. Нотифйовнермессаже, метод

`NotifyOwnerMessage`Метод передает в окно видео определенные сообщения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT NotifyOwnerMessage(
   long     hwnd,
   long     uMsg,
   LONG_PTR wParam,
   LONG_PTR lParam
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*HWND* 
</dt> <dd>

Обработчик для окна видео.

</dd> <dt>

*Uiacp* 
</dt> <dd>

Сведения о сообщении.

</dd> <dt>

*wParam* 
</dt> <dd>

Первый параметр сообщения.

</dd> <dt>

*lParam* 
</dt> <dd>

Второй параметр сообщения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

НЕ возвращает \_ ошибку.

## <a name="remarks"></a>Remarks

Когда окно видео является дочерним по отношению к другому окну, оно не получает определенные сообщения окна верхнего уровня. Эти сообщения могут быть ценными для модуля подготовки отчетов, так как они могут повлиять на его поведение. `NotifyOwnerMessage` передает любое из следующих сообщений в окно видео.

-   WM \_ активатеапп
-   WM \_ девмодечанже
-   WM \_ дисплайчанже
-   WM \_ палеттечанжед
-   WM \_ палеттеисчангинг
-   WM \_ куериневпалетте
-   WM \_ сисколорчанже

Вы можете запросить, чтобы окно с подключаемым модулем [**ивидеовиндов**](/windows/desktop/api/Control/nn-control-ivideowindow) (PID) стало дочерним для другого окна. В этом случае PID будет искать определенные сообщения, которые могут быть отправлены в окно-владелец. Идентификатор процесса пересылает эти сообщения в собственное окно. Обработка сообщений по умолчанию заключается в синхронной отправке их в собственную процедуру окна путем вызова функции Win32 **SendMessage** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасеконтролвиндов**](cbasecontrolwindow.md)
</dt> </dl>

 

 




