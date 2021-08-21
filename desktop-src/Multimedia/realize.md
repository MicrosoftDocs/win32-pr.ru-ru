---
title: Команда "реализовать"
description: Команда "реализовать" указывает устройству выбрать и реализовать его палитру в контексте отображения отображаемого окна. Устройство Digital-Video распознает эту команду.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- команда реализации Windows мультимедиа
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0aba1e610f4636c7dbfb71fbc959d9b4b8496cc23e91a97100ef6edce133b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118371439"
---
# <a name="realize-command"></a>Команда "реализовать"

Команда "реализовать" указывает устройству выбрать и реализовать его палитру в контексте отображения отображаемого окна. Устройство Digital-Video распознает эту команду.

Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*
</dt> <dd>

Идентификатор устройства MCI. Этот идентификатор или псевдоним назначается при открытии устройства.

</dd> <dt>

<span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*лпсзпалетте*
</dt> <dd>

Один из следующих флагов.



| Значение      | Значение                                                                   |
|------------|---------------------------------------------------------------------------|
| background | Реализует палитру в виде палитры фона.                             |
| нормальный     | Реализует палитру для окна верхнего уровня. Это параметр по умолчанию. |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*
</dt> <dd>

Может иметь значение "Wait", "notify" или и то, и другое. Для устройств Digital-Video также можно указать "Test". Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Используйте эту команду, только если приложение использует обработчик окна и получает сообщение **WM \_ Куериневпаллетте** или **WM \_ палеттечанжед** .

## <a name="examples"></a>Примеры

Следующая команда сообщает устройству "мивидео" о своей палитре.

``` syntax
realize myvideo normal
```

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/> |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>       |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Строки команд MCI](mci-command-strings.md)
</dt> </dl>

 

