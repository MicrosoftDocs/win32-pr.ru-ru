---
title: Команда MCI_UPDATE (Ммсистем. h)
description: '\_Команда обновления MCI обновляет прямоугольник экрана. Устройство Digital-Video распознает эту команду.'
ms.assetid: 90a8c10f-61b9-49a1-bbcc-e0729aa8c454
keywords:
- MCI_UPDATE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_UPDATE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 423186096c88a8f1ff74987ff57c6b49dc6c3131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137386"
---
# <a name="mci_update-command"></a>\_Команда обновления MCI

\_Команда обновления MCI обновляет прямоугольник экрана. Устройство Digital-Video распознает эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UPDATE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
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

<span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*лпдест*
</dt> <dd>

Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) . (Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

С типом устройства "дигиталвидео" используются следующие дополнительные флаги:

<dl> <dt>

<span id="MCI_DGV_UPDATE_HDC"></span><span id="mci_dgv_update_hdc"></span>ДГВ MCI, \_ \_ Обновление \_ HDC
</dt> <dd>

Элемент **HDC** структуры, идентифицируемой *лпдест* , содержит допустимое окно контроллера домена для рисования. Этот флаг является обязательным.

</dd> <dt>

<span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ ДГВ \_ Rect
</dt> <dd>

Элемент **RC** структуры, идентифицируемой *лпунфризе* , содержит допустимый отображаемый прямоугольник. Прямоугольник задает прямоугольник обрезки относительно прямоугольника клиента.

</dd> <dt>

<span id="MCI_DGV_UPDATE_PAINT"></span><span id="mci_dgv_update_paint"></span>\_прорисовка ДГВ MCI с \_ обновлением \_
</dt> <dd>

Приложение использует этот флаг при получении сообщения [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) , предназначенного для экрана контроллера домена. Устройство буфера кадров обычно окрашивает ключевой цвет. Если устройство вывода не имеет буфера кадров, команда MCI может игнорироваться \_ при использовании флага **\_ рисования MCI ДГВ \_ Update \_ Paint** , так как во время операции воспроизведения экран будет перерисовываться.

</dd> </dl>

Для устройств с цифровыми видео параметр *лпдест* указывает на структуру [**MCI \_ ДГВ \_ Update \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_update_parms) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 2000 Professional \[только классические приложения\]<br/>                                                |
| Минимальная версия сервера<br/> | Windows 2000 Server \[только классические приложения\]<br/>                                                      |
| Заголовок<br/>                   | <dl> <dt>Ммсистем. h (включение Windows. h)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Команды MCI](mci-commands.md)
</dt> </dl>

 

