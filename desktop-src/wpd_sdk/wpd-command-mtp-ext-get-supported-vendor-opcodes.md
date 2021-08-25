---
description: Команда WPD с командой \_ \_ MTP \_ \_ Get \_ Supported \_ Vendor \_ код отправляет блок команд MTP. Отсутствует последующий этап данных, связанный с этой командой.
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: Команда WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b0ab00fc3ada963e56dced49f97d3c1dbca578dfc5c1cded4735f9df947ff1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927974"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a>Команда WPD с командой \_ \_ MTP \_ \_ Get \_ поддерживаемые \_ поставщики \_ кодов операций

Команда **WPD с командой \_ \_ MTP \_ \_ Get \_ Supported \_ Vendor \_ код** отправляет блок команд MTP. Отсутствует последующий этап данных, связанный с этой командой.

## <a name="command-category"></a>Категория команды

**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**

## <a name="parameters"></a>Параметры

У этой команды нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Драйвер возвращает следующие результаты.



| Результат                                                | VarType | Описание                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| **\_коды операций для свойства WPD \_ MTP \_ ext \_ поставщика \_ \_** | VT \_ UI4 | Обязательный. **Ипортабледевицепропвариантколлектион** , содержащий все коды расширенных операций, предоставляемые поставщиком. |



 

## <a name="calling-methods"></a>Вызов методов

Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Впдмтпекстенсионс. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Поддержка расширений MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




