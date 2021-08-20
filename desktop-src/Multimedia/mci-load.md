---
title: Команда MCI_LOAD (Ммсистем. h)
description: Команда MCI \_ Load загружает файл. Эта команда распознает цифровые видеоролики и устройства наложения видео.
ms.assetid: 0f48afa0-e845-4de5-8433-15bbf4eae683
keywords:
- команда MCI_LOAD Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_LOAD
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e318e79bf24e51fec69f97a0dcb56395cb1a8917a31105deae062a865169b778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138542"
---
# <a name="mci_load-command"></a>\_Команда загрузки MCI

Команда MCI \_ Load загружает файл. Эта команда распознает цифровые видеоролики и устройства наложения видео.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_LOAD, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_LOAD_PARMS) lpLoad
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*
</dt> <dd>

Идентификатор устройства MCI, который должен получить командное сообщение.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

\_Уведомление MCI, \_ Ожидание MCI или, для устройств с цифровыми видео, \_ тест MCI. Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpLoad"></span><span id="lpload"></span><span id="LPLOAD"></span>*лплоад*
</dt> <dd>

Указатель на структуру [**\_ \_ пармс нагрузки MCI**](mci-load-parms.md) . (Устройства с дополнительными параметрами могут заменить эту структуру структурой, зависящей от устройства. Для устройств с цифровыми видео параметр **лплоад** указывает на структуру [**MCI \_ ДГВ \_ Load \_ пармс**](/previous-versions//dd743391(v=vs.85)) .)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Следующий дополнительный флаг применяется ко всем устройствам, поддерживающим \_ загрузку MCI:

<dl> <dt>

<span id="MCI_LOAD_FILE"></span><span id="mci_load_file"></span>\_файл загрузки \_ MCI
</dt> <dd>

Элемент **лпфиленаме** структуры, идентифицируемой *лплоад* , содержит адрес буфера, содержащего имя файла.

</dd> </dl>

Для типа устройства **оверлея** используется следующий дополнительный флаг:

<dl> <dt>

<span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ овли \_ Rect
</dt> <dd>

Элемент **RC** структуры, идентифицируемой *лплоад* , содержит допустимый экранный прямоугольник, определяющий область обновляемого видеобуфера.

</dd> </dl>

Для устройств с наложением параметр *лплоад* указывает на структуру [**MCI \_ овли \_ Load \_ пармс**](mci-ovly-load-parms.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>ммсистем. h (включает Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Команды MCI](mci-commands.md)
</dt> </dl>

 

