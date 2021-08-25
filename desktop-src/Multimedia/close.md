---
title: Команда "Закрыть" (Корекрт \_ IO. h)
description: Команда Close закрывает устройство или файл и все связанные с ним ресурсы. MCI выгружает устройство, когда все экземпляры устройства или все файлы закрываются. Все устройства MCI распознают эту команду.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- команда close Windows мультимедиа
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02acd3ebe3d45a402ae565c6fcac121f712df4374924bcb0e02c3dcadf9ceeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807963"
---
# <a name="close-command"></a>Команда "Закрыть"

Команда Close закрывает устройство или файл и все связанные с ним ресурсы. MCI выгружает устройство, когда все экземпляры устройства или все файлы закрываются. Все устройства MCI распознают эту команду.

Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*
</dt> <dd>

Идентификатор устройства MCI. Этот идентификатор или псевдоним назначается при открытии устройства.

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*
</dt> <dd>

Может иметь значение "Wait", "notify" или и то, и другое. Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Чтобы закрыть все устройства, открытые в приложении, укажите идентификатор устройства "ALL" для параметра *лпсздевицеид* .

Закрытие устройства **кдаудио** останавливает воспроизведение звука.

**Windows 2000/XP:** Если устройство **кдаудио** воспроизводится, закрытие устройства **кдаудио** не приводит к прекращению воспроизведения звука. Сначала отправьте команду " [закончить](stop.md) ".

## <a name="examples"></a>Примеры

Следующая команда закрывает устройство "мисаунд".

``` syntax
close mysound
```

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                               |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                     |
| Заголовок<br/>                   | <dl> <dt>Корекрт \_ IO. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Строки команд MCI](mci-command-strings.md)
</dt> </dl>

 

