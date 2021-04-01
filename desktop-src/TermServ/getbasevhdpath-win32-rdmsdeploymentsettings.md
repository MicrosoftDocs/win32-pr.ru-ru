---
title: Метод Жетбасевхдпас класса Win32_RDMSDeploymentSettings
description: Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов. | Метод Жетбасевхдпас класса Win32_RDMSDeploymentSettings
ms.assetid: d3629a08-ef16-4aab-b74b-f837a8ba00d0
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетбасевхдпас
- Службы удаленных рабочих столов метода Жетбасевхдпас, класс Win32_RDMSDeploymentSettings
- Класс Win32_RDMSDeploymentSettings службы удаленных рабочих столов, метод Жетбасевхдпас
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings.GetBaseVHDPath
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 595c6459148a0270bed2328c70e15ef74a69acf3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104000161"
---
# <a name="getbasevhdpath-method-of-the-win32_rdmsdeploymentsettings-class"></a>Метод Жетбасевхдпас \_ класса Win32 рдмсдеплойментсеттингс

Извлекает базовый путь к каталогу, в который развертываются виртуальные жесткие диски коллекции виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetBaseVHDPath(
  [out] string DirectoryPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*DirectoryPath* \[ заполняет\]
</dt> <dd>

Получает путь развертывания VHD.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

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

 

 





