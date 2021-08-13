---
description: Добавляет ресурсы в конфигурацию виртуальной системы.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Метод Аддресаурцесеттингс класса CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0387d3d46723aede1d0858d647a555db57b3de28e6c1fb5fbb68b6d56342fcb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646472"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Метод Аддресаурцесеттингс \_ класса CIM виртуалсистемманажементсервице

Добавляет ресурсы в конфигурацию виртуальной системы.

При применении к конфигурации виртуальной системы "State" ресурсы побочных эффектов добавляются в активную виртуальную систему.

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

Ссылка [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) на затронутую конфигурацию виртуальной системы.

</dd> <dt>

*Ресаурцесеттингс* \[ окне\]
</dt> <dd>

Массив строк, каждый из которых содержит один внедренный экземпляр класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , описывающий виртуальные аспекты виртуального ресурса, добавляемого в виртуальную систему.

</dd> <dt>

*Ресултингресаурцесеттингс* \[ заполняет\]
</dt> <dd>

Массив ссылок на экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющие виртуальные аспекты добавленных виртуальных ресурсов.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется долго, при необходимости может быть возвращено задание. В этом случае экземпляры класса [**CIM \_ ресаурцеаллокатионсеттингдата**](cim-resourceallocationsettingdata.md) , представляющие добавленные параметры ресурсов, доступны через ассоциацию **CIM \_ конретекомпонент** от экземпляра класса [**CIM \_ виртуалсистемсеттингдата**](cim-virtualsystemsettingdata.md) , представляющего затронутую конфигурацию виртуальной системы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_ВИРТУАЛСИСТЕММАНАЖЕМЕНТСЕРВИЦЕ CIM**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




