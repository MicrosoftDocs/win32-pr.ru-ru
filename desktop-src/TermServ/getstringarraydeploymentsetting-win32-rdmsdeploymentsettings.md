---
title: Метод Жетстрингаррайдеплойментсеттинг класса Win32_RDMSDeploymentSettings
description: Извлекает параметры развертывания для коллекции виртуальных рабочих столов.
ms.assetid: ab380618-560e-425b-9bf0-a7de6b30d01a
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетстрингаррайдеплойментсеттинг
- Службы удаленных рабочих столов метода Жетстрингаррайдеплойментсеттинг, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетстрингаррайдеплойментсеттинг
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetStringArrayDeploymentSetting
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ac0b82441abef8af1b4f6c8e3bd48b89a8cb6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135403"
---
# <a name="getstringarraydeploymentsetting-method-of-the-win32_rdmsdeploymentsettings-class"></a>Метод Жетстрингаррайдеплойментсеттинг \_ класса Win32 рдмсдеплойментсеттингс

Извлекает параметры развертывания для коллекции виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetStringArrayDeploymentSetting(
  [in]  string Key,
  [out] string Value[]
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

Получает массив строк, содержащий параметры развертывания.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсдеплойментсеттингс Win32**](win32-rdmsdeploymentsettings.md)
</dt> </dl>

 

 





