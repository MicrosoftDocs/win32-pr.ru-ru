---
title: Команда MCI_CLOSE (Ммсистем. h)
description: Команда MCI \_ Close освобождает доступ к устройству или файлу. Все устройства распознают эту команду.
ms.assetid: 62dadd90-e8fc-4bdd-9f8c-f9ea9ff5550f
keywords:
- MCI_CLOSE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 417129595405aeb6c9a2345eb9c3f03f1e2731e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135678"
---
# <a name="mci_close-command"></a>\_Команда «закрыть» MCI

Команда MCI \_ Close освобождает доступ к устройству или файлу. Все устройства распознают эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CLOSE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpClose
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

\_Ожидание с уведомлением MCI или MCI \_ . Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).

</dd> <dt>

<span id="lpClose"></span><span id="lpclose"></span><span id="LPCLOSE"></span>*лпклосе*
</dt> <dd>

Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) . (Можно также использовать структуру **пармс для \_ окна \_ MCI** . Дополнительные сведения см. в комментариях для **MCI \_ Generic \_ пармс**.)

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Выход из приложения без закрытия всех открытых устройств MCI может привести к недоступности устройства. Приложение должно явным образом закрыть каждое устройство или файл после его завершения. MCI выгружает устройство при закрытии всех экземпляров устройства или всех связанных с ним файлов.

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

 

