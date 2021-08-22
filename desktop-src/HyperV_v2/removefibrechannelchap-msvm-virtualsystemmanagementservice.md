---
description: Удаление параметров DH-CHAP (протокол проверки подлинности Диффи-Хелмана) из искусственного Fibre Channel порта виртуальной машины.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Метод Ремовефибречаннелчап класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9b934839f6d908594ee58f0838c884fdedc48f372de061482ddf2147123a351c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147797"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Метод Ремовефибречаннелчап \_ класса Виртуалсистемманажементсервице мсвм

Удаление параметров DH-CHAP (протокол проверки подлинности Диффи-Хелмана) из искусственного Fibre Channel порта виртуальной машины. Этот метод завершится ошибкой, если виртуальная машина запущена.

## <a name="syntax"></a>Синтаксис


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Фкпортсеттингс* \[ окне\]
</dt> <dd>

Массив строк, содержащий встроенный экземпляр класса [**мсвм \_ синсетикфкпортсеттингдата**](msvm-syntheticfcportsettingdata.md) , который определяет искусственные Fibre Channel порты, из которых удаляются параметры DH-CHAP. Свойство **InstanceId** каждого из этих экземпляров определяет изменяемые элементы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Сбой** (32768)
</dt> <dt>

**Отказано в доступе** (32769)
</dt> <dt>

**Не поддерживается** (32770)
</dt> <dt>

**Состояние неизвестно** (32771)
</dt> <dt>

**Время ожидания** (32772)
</dt> <dt>

**Недопустимый параметр** (32773)
</dt> <dt>

**Система используется** (32774)
</dt> <dt>

**Недопустимое состояние для этой операции** (32775)
</dt> <dt>

**Неверный тип данных** (32776)
</dt> <dt>

**Система недоступна** (32777)
</dt> <dt>

**Недостаточно памяти** (32778)
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

[**Мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




