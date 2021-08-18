---
description: Возвращает версию обработчика обработки WPAD.
ms.assetid: f9e9a867-d491-4d46-bbd8-c0c3d8d5b3d6
title: Функция Жетклиентверсион
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- dnsResolveEx
api_type:
- NA
api_location: ''
ms.openlocfilehash: 33aeb4bd59730c48407220fede0cec0a606614f4a9692cd0e9852d56757a7f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133217"
---
# <a name="getclientversion-function"></a>Функция Жетклиентверсион

Возвращает версию обработчика обработки WPAD.

## <a name="parameters"></a>Параметры

<dl> <dt>

*ипаддресслист* 
</dt> <dd>

Строка, разделенная точкой с запятой, содержащая IP-адреса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Список упорядоченных IP-адресов, разделенных точкой с запятой, или пустая строка, если не удалось отсортировать список IP-адресов.

## <a name="remarks"></a>Remarks

В настоящее время эта функция возвращает версию 1,0.

Корпорация Майкрософт добавила эту функцию, чтобы позволить ИТ-администраторам обновлять свои скрипты WPAD, чтобы использовать разные версии механизма обработки WPAD, не нарушая их существующее развертывание. Например, если корпорация Майкрософт добавила функцию в версию 2,0 модуля WPAD, администраторы смогут проверить версию, прежде чем пытаться вызвать эту функцию. Это позволяет сценарию работать с клиентами, работающими под управлением версий 1,0 и 2,0 модуля WPAD.

## <a name="examples"></a>Примеры

``` syntax
getClientVersion();
    returns the appropriate versions number of the WPAD engine.
```

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Определения API вспомогательных функций прокси-сервера с поддержкой IPv6](ipv6-aware-proxy-helper-api-definitions.md)
</dt> <dt>

[Расширения IPv6 для формата файла автоматической настройки Navigator](ipv6-extensions-to-navigator-auto-config-file-format.md)
</dt> </dl>

 

 



