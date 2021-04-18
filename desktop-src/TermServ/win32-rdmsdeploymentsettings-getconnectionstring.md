---
title: Метод ConnectionString класса Win32_RDMSDeploymentSettings
description: Извлекает строку подключения к базе данных на уровне развертывания.
ms.assetid: 91a90883-9b87-42e5-af52-90226f0344bf
ms.tgt_platform: multiple
keywords:
- Метод ConnectionString службы удаленных рабочих столов
- Метод ConnectionString службы удаленных рабочих столов, Win32_RDMSDeploymentSettings класс
- Win32_RDMSDeploymentSettings класса службы удаленных рабочих столов, метод ConnectionString
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6476c938f62e0cd0e1f9d034c89fded50994946
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490974"
---
# <a name="getconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>Метод ConnectionString \_ класса Win32 рдмсдеплойментсеттингс

Извлекает строку подключения к базе данных на уровне развертывания.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetConnectionString(
  [out] string ConnectionString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Строка* \[ подключения заполняет\]
</dt> <dd>

Строка подключения

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсдеплойментсеттингс Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





