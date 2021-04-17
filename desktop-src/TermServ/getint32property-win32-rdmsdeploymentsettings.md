---
title: Метод GetInt32Property класса Win32_RDMSDeploymentSettings (Microsoft. Diagnostics. аппаналисис. h)
description: Извлекает целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.
ms.assetid: 6b8174bb-ffb7-4699-a3fb-d32ab0b202fc
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода GetInt32Property
- Службы удаленных рабочих столов метода GetInt32Property, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f96374c610084c8ef7973d4ac4db603d9c28cff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681944"
---
# <a name="getint32property-method-of-the-win32_rdmsdeploymentsettings-class"></a>Метод GetInt32Property \_ класса Win32 рдмсдеплойментсеттингс

Извлекает целочисленное свойство для параметров развертывания коллекции виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ключ* \[ окне\]
</dt> <dd>

Псевдоним коллекции виртуальных рабочих столов.

</dd> <dt>

*Значение* \[ заполняет\]
</dt> <dd>

Целое число, получающее полученное значение.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                                 |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                                   |
| Header<br/>                   | <dl> <dt>Microsoft. Diagnostics. аппаналисис. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсдеплойментсеттингс Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





