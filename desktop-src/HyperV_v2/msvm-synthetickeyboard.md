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
ms.openlocfilehash: 86ee3a7835349ab47082627f98020f84084b4b86e9c6b4ce4a37ba2f455497cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582224"
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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_УСЕРДЕВИЦЕ CIM**](cim-userdevice.md)
</dt> </dl>

 

 




