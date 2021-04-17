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
ms.openlocfilehash: cce287d6ee03734ecbb0dd84e020ec542a83f04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710466"
---
# <a name="ui_all_commands"></a>\_все \_ команды пользовательского интерфейса

Задает константу, определяющую коллекцию команд, объявленных в файле ресурсов разметки.

## <a name="remarks"></a>Комментарии

**Пользовательский интерфейс \_ ВСЕ \_ команды** полезны, когда необходимо получить доступ к аналогичным свойствам во всех командах. Например, **Пользовательский интерфейс \_ все \_ команды** можно передать в [**иуифрамеворк:: инвалидатеуикомманд**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) , чтобы сделать недействительными и обновить все команды ленты, запросив ведущее приложение о новых значениях свойств.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 7, Windows Vista с пакетом обновления 2 (SP2) и обновлением платформы \[ только для настольных приложений Windows Vista\]<br/>                          |
| Минимальная версия сервера<br/> | Windows Server 2008 R2, Windows Server 2008 с пакетом обновления 2 (SP2) и обновление платформы для Windows Server 2008 \[ только классические приложения\]<br/> |
| Header<br/>                   | <dl> <dt>Уириббон. h</dt> </dl>                                             |
| IDL<br/>                      | <dl> <dt>Уириббон. idl</dt> </dl>                                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы и перечисления](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

