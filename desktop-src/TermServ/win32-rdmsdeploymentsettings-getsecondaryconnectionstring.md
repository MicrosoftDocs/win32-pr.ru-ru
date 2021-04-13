---
title: Метод Жетсекондариконнектионстринг класса Win32_RDMSDeploymentSettings
description: Извлекает вторичную строку подключения базы данных уровня развертывания, которая может использоваться для поддержки истечения срока действия пароля.
ms.assetid: 0de02752-6cbf-4c21-b752-a57ed58aeef1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетсекондариконнектионстринг
- Службы удаленных рабочих столов метода Жетсекондариконнектионстринг, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетсекондариконнектионстринг
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetSecondaryConnectionString
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2c09f4fcacabbe928fcda00447e252077bd8a51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340640"
---
# <a name="getsecondaryconnectionstring-method-of-the-win32_rdmsdeploymentsettings-class"></a>Метод Жетсекондариконнектионстринг \_ класса Win32 рдмсдеплойментсеттингс

Извлекает вторичную строку подключения базы данных уровня развертывания, которая может использоваться для поддержки истечения срока действия пароля.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetSecondaryConnectionString(
  [out] string SecondaryConnectionString
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Секондариконнектионстринг* \[ заполняет\]
</dt> <dd>

Строка подключения для извлечения

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

 

 





