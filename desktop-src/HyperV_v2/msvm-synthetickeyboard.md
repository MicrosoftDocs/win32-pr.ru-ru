---
description: Представляет устройство виртуальной клавиатуры.
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Класс Msvm_SyntheticKeyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64ac153a2c20815891d8a39fd10f58562ed8d81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650490"
---
# <a name="msvm_synthetickeyboard-class"></a>\_Класс мсвм синсетиккэйбоард

Представляет устройство виртуальной клавиатуры.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ синсетиккэйбоард** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **мсвм \_ синсетиккэйбоард** содержит следующие методы.



| Метод                                                                  | Описание                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [**Равен**](msvm-synthetickeyboard-requeststatechange.md) | Запрашивает изменение состояния.<br/> |
| [**Перезапуск**](msvm-synthetickeyboard-reset.md)                           | выполняет сброс устройства.<br/>       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_УСЕРДЕВИЦЕ CIM**](cim-userdevice.md)
</dt> </dl>

 

 




