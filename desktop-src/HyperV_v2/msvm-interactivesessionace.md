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
ms.openlocfilehash: ed7dd4c4a3742f43a3de8e919ae2200e76cacc03ba1f7da066f48bac018f0a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148387"
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

### <a name="properties"></a>Элемент Property

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

Определяет субъект безопасности, к которому ACE предоставляет или запрещает доступ. допустимые форматы для этого свойства включают формат имени пользователя, совместимого с Windows SAM, и формат строки идентификатора безопасности Windows.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетинтерактивесессионакл**](getinteractivesessionacl-msvm-terminalservice.md)
</dt> </dl>

 

 




