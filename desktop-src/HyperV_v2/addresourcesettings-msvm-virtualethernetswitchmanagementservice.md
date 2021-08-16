---
description: Добавляет ресурсы в конфигурацию виртуального коммутатора.
ms.assetid: aad5fac1-3884-4a95-abe3-bf192f23ea41
title: Метод Аддресаурцесеттингс класса Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e13b9a9738b830f5b9dfcce5f37efa23c1014c735a5cb0a9cc0e09afa7b0038
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914154"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Метод Аддресаурцесеттингс \_ класса Виртуалесернетсвитчманажементсервице мсвм

Добавляет ресурсы в конфигурацию виртуального коммутатора. При применении к конфигурации виртуальной машины "State" в качестве ресурсов побочных эффектов добавляются к активной виртуальной машине.

## <a name="syntax"></a>Синтаксис


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Аффектедконфигуратион* \[ окне\]
</dt> <dd>

Ссылка на объект [**CIM \_ виртуалсистемсеттингдата**](/previous-versions//cc136954(v=vs.85)) , представляющий затронутую конфигурацию виртуального коммутатора.

</dd> <dt>

*Ресаурцесеттингс* \[ окне\]
</dt> <dd>

Массив строк, содержащий один внедренный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , который описывает виртуальные аспекты виртуального ресурса, добавляемого к виртуальному коммутатору.

</dd> <dt>

*Ресултингресаурцесеттингс* \[ заполняет\]
</dt> <dd>

Массив ссылок на экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) , представляющий виртуальные аспекты добавленных виртуальных ресурсов.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

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

[**модифиресаурцесеттингс**](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**ремовересаурцесеттингс**](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**Мсвм \_ виртуалесернетсвитчманажементсервице**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

