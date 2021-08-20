---
title: Команда MCI_SETTUNER (Ммсистем. h)
description: Команда MCI \_ сеттунер устанавливает текущий канал на тюнере. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- команда MCI_SETTUNER Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc0e4d812a89c8b7ca5a8e65b322e19dcb4f7d4e7e2ef8c49745ebb16e22af65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138110"
---
# <a name="mci_settuner-command"></a>\_Команда MCI сеттунер

Команда MCI \_ сеттунер устанавливает текущий канал на тюнере. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
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

<span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*лпсеттунер*
</dt> <dd>

Указатель на структуру [**\_ \_ \_ пармс сеттунер видеомагнитофона MCI**](mci-vcr-settuner-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Следующие дополнительные флаги применяются к устройствам ВИДЕОМАГНИТОФОНА:

<dl> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>\_ \_ канал СЕТТУНЕР видеомагнитофона \_ MCI
</dt> <dd>

Элемент **двчаннел** структуры, идентифицируемой *лпсеттунер* , содержит новый номер канала.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>\_ \_ канал СЕТТУНЕР видеомагнитофона \_ MCI \_
</dt> <dd>

Уменьшает канал тюнера.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>\_ \_ \_ Поиск канала сеттунер \_ видеомагнитофона \_ MCI
</dt> <dd>

Выполняет поиск допустимого канала в обратном направлении.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>\_ \_ \_ Поиск канала сеттунер \_ видеомагнитофона \_ MCI
</dt> <dd>

Выполняет поиск допустимого канала в прямом направлении.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>\_канал MCI \_ сеттунер \_ Channel \_ up
</dt> <dd>

Увеличивает канал тюнера.

</dd> <dt>

<span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>\_ \_ номер СЕТТУНЕР видеомагнитофона \_ MCI
</dt> <dd>

Элемент **двнумбер** структуры, определяемой параметром *лпсеттунер* , указывает, какой логический тюнер будет влиять на эту команду.

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

 

