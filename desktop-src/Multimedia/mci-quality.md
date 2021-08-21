---
title: Команда MCI_QUALITY (Ммсистем. h)
description: '\_Команда качества MCI определяет пользовательский уровень качества для сжатия данных в аудио, видео или по-прежнему. Устройство Digital-Video распознает эту команду.'
ms.assetid: 91ad9704-0089-4b1f-b0f6-919ab5fd84e0
keywords:
- команда MCI_QUALITY Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_QUALITY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1237d9b70c9f06782342c404c19dd23cf6f0848f8c7b33523bce35990287fa27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138225"
---
# <a name="mci_quality-command"></a>\_Команда качества MCI

\_Команда качества MCI определяет пользовательский уровень качества для сжатия данных в аудио, видео или по-прежнему. Устройство Digital-Video распознает эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_QUALITY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_QUALITY_PARMS) lpQuality
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

<span id="lpQuality"></span><span id="lpquality"></span><span id="LPQUALITY"></span>*лпкуалити*
</dt> <dd>

Указатель на структуру [**\_ \_ \_ пармс качества MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_quality_parmsa) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Имя, определенное для этого уровня качества, можно использовать при настройке звука, видео или по-прежнему качества с помощью команд [MCI \_ Сетаудио](mci-setaudio.md) и [MCI \_ сетвидео](mci-setvideo.md) .

Следующие дополнительные флаги применяются к устройствам цифрового видео:

<dl> <dt>

<span id="MCI_QUALITY_ALG"></span><span id="mci_quality_alg"></span>\_алгоритм качества \_ MCI
</dt> <dd>

Элемент **лпстралгорисм** структуры, идентифицируемой *лпкуалити* , содержит адрес буфера, содержащего имя алгоритма. Этот алгоритм должен поддерживаться драйвером устройства и должен быть совместим с используемым аудио-или видеодескриптором. Если этот флаг опущен, используется текущий алгоритм.

</dd> <dt>

<span id="MCI_QUALITY_DIALOG"></span><span id="mci_quality_dialog"></span>\_ \_ диалоговое окно качества MCI
</dt> <dd>

Драйвер устройства должен отображать диалоговое окно для указания уровня качества. Диалоговое окно содержит внутренние поля, используемые драйвером устройства для создания структуры, описывающей конкретный уровень качества.

</dd> <dt>

<span id="MCI_QUALITY_HANDLE"></span><span id="mci_quality_handle"></span>\_маркер качества \_ MCI
</dt> <dd>

Элемент **двхандле** структуры, идентифицируемой *лпкуалити* , содержит маркер для структуры. Структура содержит зависящие от алгоритма данные, описывающие конкретный уровень качества. Формат структур для алгоритмов зависит от устройства.

</dd> <dt>

<span id="MCI_QUALITY_ITEM"></span><span id="mci_quality_item"></span>\_элемент качества \_ MCI
</dt> <dd>

Константа, указывающая тип алгоритма, включенный в элемент **двитем** структуры, идентифицируемой *лпкуалити*.

</dd> <dt>

<span id="MCI_QUALITY_NAME"></span><span id="mci_quality_name"></span>\_имя качества \_ MCI
</dt> <dd>

Элемент **лпстрнаме** структуры, идентифицируемой *лпкуалити* , содержит адрес буфера, содержащего дескриптор качества.

</dd> </dl>

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

 

