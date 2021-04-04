---
title: Метод Провисионингпрепжоб класса Win32_RDMSVirtualDesktopCollection
description: Создает задание подготовки виртуальных рабочих столов.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Провисионингпрепжоб
- Службы удаленных рабочих столов метода Провисионингпрепжоб, интерфейс Win32_RDMSVirtualDesktopCollection
- Службы удаленных рабочих столов интерфейса Win32_RDMSVirtualDesktopCollection, метод Провисионингпрепжоб
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988570"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Метод Провисионингпрепжоб \_ класса Win32 рдмсвиртуалдесктопколлектион

Создает задание подготовки виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Коллектионалиас* \[ окне\]
</dt> <dd>

Псевдоним коллекции, в которой размещен виртуальный рабочий стол.

</dd> <dt>

*VMHostName* \[ окне\]
</dt> <dd>

Имя узла виртуальной машины.

</dd> <dt>

*VMName* \[ окне\]
</dt> <dd>

Имя виртуальной машины.

</dd> <dt>

*Експорттолокатион* \[ окне\]
</dt> <dd>

Полный путь к расположению для экспорта задания подготовки.

</dd> <dt>

*бсиспреп* \[ окне\]
</dt> <dd>

Указывает, представляет ли задание подготовки развертывание Sysprep.

</dd> <dt>

*MachineName* \[ окне\]
</dt> <dd>

Имя компьютера, на котором размещена виртуальная машина.

</dd> <dt>

*Имя пользователя* \[ окне\]
</dt> <dd>

Имя пользователя администратора виртуальной машины.

</dd> <dt>

*Пароль* \[ окне\]
</dt> <dd>

Пароль администратора виртуальной машины.

</dd> <dt>

*Жобгуид* \[ заполняет\]
</dt> <dd>

**Идентификатор GUID** , однозначно определяющий задание подготовки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсвиртуалдесктопколлектион Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





