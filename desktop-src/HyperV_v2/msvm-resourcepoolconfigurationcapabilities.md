---
description: Описывает возможности связанного \_ класса мсвм ресаурцепулконфигуратионсервице.
ms.assetid: 3e6857f9-62a0-420b-8f1d-8aad685a7ff7
title: Класс Msvm_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationCapabilities
- Msvm_ResourcePoolConfigurationCapabilities.InstanceID
- Msvm_ResourcePoolConfigurationCapabilities.Caption
- Msvm_ResourcePoolConfigurationCapabilities.Description
- Msvm_ResourcePoolConfigurationCapabilities.ElementName
- Msvm_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- Msvm_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f49f105af3db5646b32c6aa5d78f28da76bf7b9806174e15f56b4d990de68e8f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535514"
---
# <a name="msvm_resourcepoolconfigurationcapabilities-class"></a>\_Класс мсвм ресаурцепулконфигуратионкапабилитиес

Описывает возможности связанного класса [**мсвм \_ ресаурцепулконфигуратионсервице**](msvm-resourcepoolconfigurationservice.md) . Клиенты могут использовать экземпляры этого класса, чтобы определить, какие методы поддерживаются синхронно или асинхронно. Один и тот же метод не должен находиться в обоих списках. Реализации методов должны быть либо синхронными, либо асинхронными.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider")]
class Msvm_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  string InstanceID;
  string Caption = "Resource Pool Configuration Capabilities";
  string Description = "Microsoft Resource Pool Configuration Capabilities";
  string ElementName = "Resource Pool Configuration Capabilities";
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ ресаурцепулконфигуратионкапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ ресаурцепулконфигуратионкапабилитиес** имеет следующие свойства.

<dl> <dt>

**асинчронаусмесодссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: массив **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив идентификаторов методов, каждый из которых идентифицирует метод класса [**мсвм \_ ресаурцепулконфигуратионсервице**](msvm-resourcepoolconfigurationservice.md) , который поддерживается асинхронно реализацией.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

**CreatePool поддерживается** (32768)


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

**Чанжепулресаурцес поддерживается** (32769)


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

**Чанжепулсеттингс поддерживается** (32770)


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

**DeletePool поддерживается** (32771)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32772.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности конфигурации пула ресурсов".

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности конфигурации пула ресурсов Майкрософт".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности конфигурации пула ресурсов".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**синчронаусмесодссуппортед**
</dt> <dd> <dl> <dt>

Тип данных: массив **UInt32**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Массив идентификаторов методов, каждый из которых идентифицирует метод класса [**мсвм \_ ресаурцепулконфигуратионсервице**](msvm-resourcepoolconfigurationservice.md) , который поддерживается в синхронном режиме реализацией.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="CreatePool_is_supported"></span><span id="createpool_is_supported"></span><span id="CREATEPOOL_IS_SUPPORTED"></span>

**CreatePool поддерживается** (32768)


</dt> <dd></dd> <dt>

<span id="ChangePoolResources_is_supported"></span><span id="changepoolresources_is_supported"></span><span id="CHANGEPOOLRESOURCES_IS_SUPPORTED"></span>

**Чанжепулресаурцес поддерживается** (32769)


</dt> <dd></dd> <dt>

<span id="ChangePoolSettings_is_supported"></span><span id="changepoolsettings_is_supported"></span><span id="CHANGEPOOLSETTINGS_IS_SUPPORTED"></span>

**Чанжепулсеттингс поддерживается** (32770)


</dt> <dd></dd> <dt>

<span id="DeletePool_is_supported"></span><span id="deletepool_is_supported"></span><span id="DELETEPOOL_IS_SUPPORTED"></span>

**DeletePool поддерживается** (32771)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32772.. 65535)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1 \[ только классические приложения\]<br/>                                                            |
| Минимальная версия сервера<br/> | Windows Server 2012 \[Только классические приложения R2\]<br/>                                                 |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

