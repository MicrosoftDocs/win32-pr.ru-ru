---
title: Команда MCI_MONITOR (Ммсистем. h)
description: '\_Команда монитора MCI указывает источник представления. Устройство Digital-Video распознает эту команду.'
ms.assetid: b6c476ef-d1a4-477d-a104-dda10be60915
keywords:
- MCI_MONITOR команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_MONITOR
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aa2f36b0e486143dc348d2e150422b2b082ecf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988963"
---
# <a name="mci_monitor-command"></a>\_Команда монитора MCI

\_Команда монитора MCI указывает источник представления. Устройство Digital-Video распознает эту команду.

Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MONITOR, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_MONITOR_PARMS) lpMonitor
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

<span id="lpMonitor"></span><span id="lpmonitor"></span><span id="LPMONITOR"></span>*лпмонитор*
</dt> <dd>

Указатель на структуру [**\_ \_ \_ пармс монитора MCI ДГВ**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_monitor_parms) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает нуль в случае успеха или ошибку в противном случае.

## <a name="remarks"></a>Комментарии

Следующие дополнительные флаги применяются к устройствам цифрового видео:

<dl> <dt>

<span id="MCI_DGV_MONITOR_METHOD"></span><span id="mci_dgv_monitor_method"></span>\_ \_ метод монитора MCI \_ ДГВ
</dt> <dd>

Константа, указывающая метод мониторинга, включается в элемент **двмесод** структуры, идентифицируемой *лпмонитор*.

Если в элементе \_ \_ \_ **ДВСАУРЦЕ** используется флаг ввода MCI ДГВ, выбирается метод мониторинга. Как правило, различные методы мониторинга имеют различные последствия использования оборудования. На устройстве выбирается метод мониторинга по умолчанию.

</dd> <dt>

<span id="MCI_DGV_MONITOR_SOURCE"></span><span id="mci_dgv_monitor_source"></span>\_ \_ источник монитора MCI \_ ДГВ
</dt> <dd>

Константа, указывающая, что источник монитора включен в элемент **двсаурце** структуры, идентифицируемой *лпмонитор*.

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

 

