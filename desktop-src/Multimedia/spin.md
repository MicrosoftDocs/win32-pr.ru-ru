---
title: Spin, команда
description: Команда Spin запускает вращение диска или останавливает вращение диска. Устройства видеодиск распознают эту команду.
ms.assetid: 1fdf4d09-fafd-4245-ad92-397114d0f473
keywords:
- Команда "вращение" Windows мультимедиа
topic_type:
- apiref
api_name:
- spin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c25e25f5a44ad6e6c9562d05653ab25cb2950b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672703"
---
# <a name="spin-command"></a>Spin, команда

Команда Spin запускает вращение диска или останавливает вращение диска. Устройства видеодиск распознают эту команду.

Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("spin %s %s %s"), 
  lpszDeviceID, 
  lpszUpDown, 
  lpszFlags
); 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*
</dt> <dd>

Идентификатор устройства MCI. Этот идентификатор или псевдоним назначается при открытии устройства.

</dd> <dt>

<span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*лпсзупдовн*
</dt> <dd>

Один из следующих флагов.



| Значение | Значение                       |
|-------|-------------------------------|
| работу  | Останавливает вращение диска. |
| up    | Начинает вращать диск.     |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*
</dt> <dd>

Может иметь значение "Wait", "notify" или и то, и другое. Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="examples"></a>Примеры

Следующая команда запускает вращающееся устройство видеодиск.

``` syntax
spin videodisc up
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

 

