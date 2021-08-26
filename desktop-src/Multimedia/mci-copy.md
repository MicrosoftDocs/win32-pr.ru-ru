---
title: Команда MCI_COPY (Ммсистем. h)
description: Команда MCI \_ Copy копирует данные в буфер обмена. Устройство Digital-Video распознает эту команду.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- команда MCI_COPY Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 590acf61b352fa9abab00dfd49f3f54b166bfc340eaf12061e3d90b7a3025d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039294"
---
# <a name="mci_copy-command"></a>\_Команда копирования MCI

Команда MCI \_ Copy копирует данные в буфер обмена. Устройство Digital-Video распознает эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
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

<span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*лпкопи*
</dt> <dd>

Указатель на структуру [**\_ \_ \_ пармс копирования ДГВ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Следующие дополнительные флаги применяются к устройствам цифрового видео:

<dl> <dt>

<span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_копирование ДГВ \_ MCI \_ в
</dt> <dd>

Прямоугольник включается в элемент **RC** структуры, идентифицируемой *лпкопи*. Прямоугольник указывает часть каждого копируемого кадра. Если флаг опущен, \_ то при копировании MCI копируется весь кадр.

</dd> <dt>

<span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>\_ \_ копирование \_ звукового \_ потока MCI ДГВ
</dt> <dd>

Номер звукового потока включается в элемент **дваудиостреам** структуры, определяемой *лпкопи*. Если вы используете этот флаг, а также хотите скопировать видео, необходимо также использовать \_ \_ \_ \_ флаг копирования видеопотоков MCI ДГВ. (Если ни один из флагов не указан, копируются данные из всех потоков аудио и видео.)

</dd> <dt>

<span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_ \_ копирование \_ \_ видеопотока MCI ДГВ
</dt> <dd>

Номер видеопотока включается в элемент **дввидеостреам** структуры, определяемой *лпкопи*. Если вы используете этот флаг, а также хотите скопировать аудио, необходимо также использовать \_ \_ флаг копирования звука MCI ДГВ \_ \_ . (Если ни один из флагов не указан, копируются данные из всех потоков аудио и видео.)

</dd> <dt>

<span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ из
</dt> <dd>

Начальное расположение включается в элемент **двфром** структуры, идентифицируемой *лпкопи*. Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ команды [MCI \_ Set](mci-set.md) .

</dd> <dt>

<span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —
</dt> <dd>

Конечное расположение включено в элемент **двто** структуры, идентифицируемой *лпкопи*. Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ \_ команды MCI Set.

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

 

