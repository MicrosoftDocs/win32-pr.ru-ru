---
title: Команда MCI_REALIZE (Ммсистем. h)
description: Команда MCI \_ понимает, что графическое устройство реализует свою палитру в контексте устройства (DC). Устройство Digital-Video распознает эту команду.
ms.assetid: cbc9e6ef-a372-4ddb-b7f3-ea99ac14ec95
keywords:
- команда MCI_REALIZE Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_REALIZE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81204fe679d543438a0d0dcc7ec333462cb6a3d0c30212706969dc22a143df1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689834"
---
# <a name="mci_realize-command"></a>\_Команда MCI

Команда MCI \_ понимает, что графическое устройство реализует свою палитру в контексте устройства (DC). Устройство Digital-Video распознает эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_REALIZE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpRealize
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

**MCI \_ УВЕДОМЛЕНИЕ**, **\_ Ожидание MCI** или, для устройств с цифровыми видео, **\_ тест MCI**. Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRealize"></span><span id="lprealize"></span><span id="LPREALIZE"></span>*лпреализе*
</dt> <dd>

Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) . (Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Эту команду следует использовать, когда приложение получает сообщение [**WM \_ куериневпалетте**](/windows/desktop/gdi/wm-querynewpalette) .

С типом устройства "дигиталвидео" используются следующие дополнительные флаги:

<dl> <dt>

<span id="MCI_DGV_REALIZE_BKGD"></span><span id="mci_dgv_realize_bkgd"></span>MCI \_ ДГВ \_ \_ бкгд
</dt> <dd>

Реализует палитру в виде палитры фона.

</dd> <dt>

<span id="MCI_DGV_REALIZE_NORM"></span><span id="mci_dgv_realize_norm"></span>\_ \_ норма реализации MCI ДГВ \_
</dt> <dd>

Реализует палитру в обычном режиме. Это значение по умолчанию.

</dd> </dl>

Для устройств с цифровыми видео параметр *лпреализе* указывает на структуру **MCI \_ \_ пармс** . Дополнительные сведения см. в разделе комментарии в структуре [**MCI \_ Generic \_ пармс**](mci-generic-parms.md) .

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

 

