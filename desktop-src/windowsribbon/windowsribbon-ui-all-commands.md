---
title: UI_ALL_COMMANDS (Уириббон. h)
description: Задает константу, определяющую коллекцию команд, объявленных в файле ресурсов разметки.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24767f2d3839b94ee83c6a9a527b2e80dcf8c1960e877f65a0e7e96fff4e3ec4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705963"
---
# <a name="ui_all_commands"></a>\_все \_ команды пользовательского интерфейса

Задает константу, определяющую коллекцию команд, объявленных в файле ресурсов разметки.

## <a name="remarks"></a>Remarks

**Пользовательский интерфейс \_ ВСЕ \_ команды** полезны, когда необходимо получить доступ к аналогичным свойствам во всех командах. Например, **Пользовательский интерфейс \_ все \_ команды** можно передать в [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) , чтобы сделать недействительными и обновить все команды ленты, запросив ведущее приложение о новых значениях свойств.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы \[ только для настольных приложений Windows Vista\]<br/>                          |
| Минимальная версия сервера<br/> | Windows server 2008 R2, Windows server 2008 с пакетом обновления 2 (SP2) и обновлением платформы для Windows Server 2008 \[ только классические приложения\]<br/> |
| Header<br/>                   | <dl> <dt>Уириббон. h</dt> </dl>                                             |
| IDL<br/>                      | <dl> <dt>Уириббон. idl</dt> </dl>                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы и перечисления](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

