---
description: Команда WPD \_ , \_ \_ \_ полученная при \_ получении \_ описания расширения поставщика \_ , получает строку описания поставщика-расширения. Эта строка определяется набором данных DeviceInfo.
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: Команда WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION (Впдмтпекстенсионс. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1b98d5b8bce699537bc261e915d8233be6082c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708380"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>Команда WPD команда для \_ \_ \_ \_ получения \_ расширения поставщику \_ расширений \_ MTP

Команда **WPD \_ , \_ \_ \_ полученная при \_ получении \_ \_ описания расширения поставщика** , получает строку описания поставщика-расширения. Эта строка определяется набором данных **DeviceInfo** .

## <a name="command-category"></a>Категория команды

**\_операции категории WPD для \_ \_ поставщика MTP ext \_ \_**

## <a name="parameters"></a>Параметры

У этой команды нет параметров.

## <a name="return-value"></a>Возвращаемое значение

Драйвер возвращает следующие результаты.



| Результат                                                      | VarType    | Описание                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **\_Описание свойства WPD для \_ \_ \_ \_ расширения поставщика \_ MTP** | VT \_ LPWSTR | Обязательный. Указывает строку описания поставщика-расширения. |



 

## <a name="calling-methods"></a>Вызов методов

Метод можно вызвать напрямую с помощью [**ипортабледевице:: сендкомманд**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Впдмтпекстенсионс. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Поддержка расширений MTP](supporting-mtp-extensions.md)
</dt> </dl>

 

 




