---
title: Команда MCI_RESTORE (Ммсистем. h)
description: Команда MCI \_ RESTORE Копирует растровое изображение из файла в буфер кадров. Устройство Digital-Video распознает эту команду. Эта команда выполняет обратное действие \_ команды захвата MCI.
ms.assetid: ed309cc6-72a3-4abb-aef2-40a55381d8b6
keywords:
- MCI_RESTORE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_RESTORE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b0c82db597a0e347f382c7cda55ce507f4e6dcc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803257"
---
# <a name="mci_restore-command"></a>\_Команда восстановления MCI

Команда MCI \_ RESTORE Копирует растровое изображение из файла в буфер кадров. Устройство Digital-Video распознает эту команду. Эта команда выполняет обратное действие команды [ \_ захвата MCI](mci-capture.md) .

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESTORE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_RESTORE_PARMS) lpRestore
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

\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI. Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpRestore"></span><span id="lprestore"></span><span id="LPRESTORE"></span>*лпресторе*
</dt> <dd>

Указатель на структуру [**\_ \_ \_ пармс восстановления MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_restore_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Реализация может распознать различные форматы изображений, но всегда принимается независимый от устройства точечный рисунок Windows (DIB).

Следующие дополнительные флаги применяются к устройствам цифрового видео:

<dl> <dt>

<span id="MCI_DGV_RESTORE_FROM"></span><span id="mci_dgv_restore_from"></span>\_Восстановление MCI \_ ДГВ \_ из
</dt> <dd>

Элемент **лпстрфиленаме** структуры, идентифицируемой *лпресторе* , содержит адрес буфера, содержащего имя исходного файла. Требуется указать имя файла.

</dd> <dt>

<span id="MCI_DGV_RESTORE_AT"></span><span id="mci_dgv_restore_at"></span>\_Восстановление ДГВ \_ MCI \_ в
</dt> <dd>

Элемент **RC** структуры, идентифицируемой *лпресторе* , содержит допустимый прямоугольник. Прямоугольник задает область буфера фрейма относительно ее начала. Первая пара координат задает верхний левый угол прямоугольника. Вторая пара указывает ширину и высоту. Если этот флаг не указан, изображение копируется в левый верхний угол буфера кадров.

</dd> </dl>

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

 

