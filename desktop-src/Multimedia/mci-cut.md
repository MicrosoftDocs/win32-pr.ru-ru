---
title: Команда MCI_CUT (Ммсистем. h)
description: Команда MCI \_ Cut удаляет данные из файла и копирует их в буфер обмена. Устройство Digital-Video распознает эту команду.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- MCI_CUT команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988965"
---
# <a name="mci_cut-command"></a>\_Команда MCI Cut

Команда MCI \_ Cut удаляет данные из файла и копирует их в буфер обмена. Устройство Digital-Video распознает эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
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

<span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*лпкут*
</dt> <dd>

Указатель на [**\_ ДГВ \_ Вырезать \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) структуру.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Следующие дополнительные флаги применяются к устройствам цифрового видео:

<dl> <dt>

<span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>\_ДГВ MCI \_ Вырезать \_ в
</dt> <dd>

Прямоугольник включается в элемент **RC** структуры, идентифицируемой *лпкут*. Прямоугольник указывает часть каждого кадра для вырезания. Если этот флаг опущен, MCI \_ вырезает весь фрейм целиком.

</dd> <dt>

<span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>\_вырезанный АУДИОПОТОК MCI ДГВ \_ \_ \_
</dt> <dd>

Номер звукового потока включается в элемент **дваудиостреам** структуры, определяемой *лпкут*. Если вы используете этот флаг, а также хотите вырезать видео, необходимо также использовать \_ \_ \_ \_ флаг воспроизведения видеопотока MCI ДГВ. (Если ни один из флагов не указан, данные из всех потоков аудио и видео обрезаются.)

</dd> <dt>

<span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_ \_ \_ \_ потоковая передача видео MCI ДГВ
</dt> <dd>

Номер видеопотока включается в элемент **дввидеостреам** структуры, определяемой *лпкут*. Если вы используете этот флаг, а также хотите вырезать звук, необходимо также использовать \_ \_ флаг «вырезать \_ аудио поток» MCI ДГВ \_ . (Если ни один из флагов не указан, данные из всех потоков аудио и видео обрезаются.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ из
</dt> <dd>

Начальное расположение включается в элемент **двфром** структуры, идентифицируемой *лпкут*. Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ команды [MCI \_ Set](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —
</dt> <dd>

Конечное расположение включено в элемент **двто** структуры, идентифицируемой *лпкут*. Единицы, назначенные значениям позиций, задаются \_ \_ \_ флагом формата MCI Set Time \_ .

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

 

