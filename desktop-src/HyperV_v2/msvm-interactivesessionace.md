---
description: Представляет запись управления доступом (ACE), определяющую доступ к интерактивному сеансу виртуальной машины.
ms.assetid: dfec83d6-8033-47b5-aa6f-fc7447a29f43
title: Класс Msvm_InteractiveSessionACE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_InteractiveSessionACE
- Msvm_InteractiveSessionACE.Trustee
- Msvm_InteractiveSessionACE.AccessType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c4b63e769b04092323cd2da7362ef6b156886b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682841"
---
# <a name="msvm_interactivesessionace-class"></a>\_Класс мсвм интерактивесессионаце

Представляет *запись управления доступом* (ACE), определяющую доступ к интерактивному сеансу виртуальной машины.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_InteractiveSessionACE
{
  string Trustee;
  uint16 AccessType;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ интерактивесессионаце** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ интерактивесессионаце** имеет следующие свойства.

<dl> <dt>

**акцесстипе**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, предоставляет ли ACE или запрещает доступ к доверенному лицу.

<dt>

<span id="Access_Allowed"></span><span id="access_allowed"></span><span id="ACCESS_ALLOWED"></span>

**Доступ разрешен** (0)


</dt> <dd></dd> <dt>

<span id="Access_Denied"></span><span id="access_denied"></span><span id="ACCESS_DENIED"></span>

**Отказано в доступе** (1)


</dt> <dd></dd> </dl>

</dd> <dt>

**Доверенное лицо**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Определяет субъект безопасности, к которому ACE предоставляет или запрещает доступ. Допустимые форматы для этого свойства включают формат имени пользователя, совместимый с Windows SAM, и формат строки идентификатора безопасности Windows.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетинтерактивесессионакл**](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




