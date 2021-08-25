---
title: Метод Сетсекондариконнектионстринг класса Win32_RDMSDeploymentSettings
description: Задает вторичную строку подключения базы данных уровня развертывания.
ms.assetid: 154c495e-564e-4d90-a4ff-de683d41aa73
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетсекондариконнектионстринг
- Службы удаленных рабочих столов метода Сетсекондариконнектионстринг, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Сетсекондариконнектионстринг
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.SetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeb43f0317f4a31733cf0c0f7b5b578234e14b50dc8976df096e5b9b0b3426d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868254"
---
# <a name="setsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>Метод Сетсекондариконнектионстринг \_ класса Win32 рдмсдеплойментсеттингс

Задает вторичную строку подключения базы данных уровня развертывания.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetSecondaryConnectionString(
  [in] string SecondaryConnectionString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Секондариконнектионстринг* \[ окне\]
</dt> <dd>

Строка подключения для установки

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Рдмсдеплойментсеттингс Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





