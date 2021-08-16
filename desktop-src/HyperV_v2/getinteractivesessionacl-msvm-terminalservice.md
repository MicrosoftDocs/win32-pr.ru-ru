---
description: Извлекает текущий список управления доступом на уровне пользователей (DACL), который управляет доступом к интерактивному сеансу виртуальной машины.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Метод Жетинтерактивесессионакл класса Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 37f33ce16d0b5eb2b998f4f08a37a6e601f82d3aecf49a2e8e68b2a7f571a01e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253724"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a>Метод Жетинтерактивесессионакл \_ класса Терминалсервице мсвм

Извлекает текущий *список управления доступом на уровне пользователей* (DACL), который управляет доступом к интерактивному сеансу виртуальной машины.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ComputerSystem* \[ окне\]
</dt> <dd>

Ссылка на экземпляр класса [**мсвм \_ ComputerSystem**](msvm-computersystem.md) , представляющий виртуальную машину, для которой будет извлечен список DACL.

</dd> <dt>

*Акцессконтроллист* \[ заполняет\]
</dt> <dd>

Массив строк, каждый из которых содержит встроенный экземпляр класса [**мсвм \_ интерактивесессионаце**](msvm-interactivesessionace.md) , представляющий *запись управления доступом* (ACE) в списке DACL интерактивного сеанса виртуальной машины.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Сбой** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Недопустимый параметр** (4)
</dt> <dt>

**Недопустимое состояние** (5)
</dt> <dt>

**Несовместимые параметры** (6)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

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

[**Мсвм \_ терминалсервице**](msvm-terminalservice.md)
</dt> </dl>

 

 




