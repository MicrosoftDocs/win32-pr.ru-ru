---
title: Команда MCI_STEP (Ммсистем. h)
description: Команда MCI \_ Step пошаговое описание одного или нескольких кадров в проигрывателе. Это команда распознает устройства Digital-Video, ВИДЕОМАГНИТОФОН и Кав-Format видеодиск.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- команда MCI_STEP Windows мультимедиа
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526d5f69d0b0c02d977cc8fc73cd81a7a1bf06c3e55088f11d53c05cfa72c0c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986172"
---
# <a name="mci_step-command"></a>\_Команда на шаге MCI

Команда MCI \_ Step пошаговое описание одного или нескольких кадров в проигрывателе. Это команда распознает устройства Digital-Video, ВИДЕОМАГНИТОФОН и Кав-Format видеодиск.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
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

\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ . Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*лпстеп*
</dt> <dd>

Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) . (Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Remarks

Эта команда поддерживает устройства, которые возвращают **значение true** параметру MCI \_ жетдевкапс \_ с \_ флагом Video команды [MCI \_ жетдевкапс](mci-getdevcaps.md) .

С типом устройства **дигиталвидео** используются следующие дополнительные флаги:

<dl> <dt>

<span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_ \_ кадры шага MCI \_ ДГВ
</dt> <dd>

Элемент **двфрамес** структуры, идентифицируемой *лпстеп* , задает число кадров, которые должны быть предварительно выведены перед отображением другого изображения.

</dd> <dt>

<span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>\_ \_ обратный шаг ДГВ \_ MCI
</dt> <dd>

Действия в обратную.

</dd> </dl>

Для устройств с цифровыми видео параметр *лпстеп* указывает на структуру [**\_ ДГВ \_ шага \_ пармс MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .

Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги:

<dl> <dt>

<span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>\_кадры для \_ шага \_ видеомагнитофона MCI
</dt> <dd>

Элемент **двфрамес** структуры, идентифицируемой *лпстеп* , задает число кадров, которые должны быть предварительно выведены перед отображением другого изображения.

</dd> <dt>

<span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>\_обратный шаг видеомагнитофона MCI \_ \_
</dt> <dd>

Действия в обратную.

</dd> </dl>

Для устройств ВИДЕОМАГНИТОФОНА параметр *лпстеп* указывает на структуру пармс на [**\_ \_ этапе \_ видеомагнитофона MCI**](mci-vcr-step-parms.md) .

С типом устройства **видеодиск** используются следующие дополнительные флаги:

<dl> <dt>

<span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>\_ \_ кадры шага MCI \_ VD
</dt> <dd>

Элемент **двфрамес** структуры, определяемой параметром *лпстеп* , указывает количество кадров для шага.

</dd> <dt>

<span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>\_ \_ обратный шаг VD \_ MCI
</dt> <dd>

Действия в обратную.

</dd> </dl>

Для устройств видеодиск параметр *лпстеп* указывает на структуру [**\_ VD \_ шага MCI \_ пармс**](mci-vd-step-parms.md) .

## <a name="requirements"></a>Требования



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

 

