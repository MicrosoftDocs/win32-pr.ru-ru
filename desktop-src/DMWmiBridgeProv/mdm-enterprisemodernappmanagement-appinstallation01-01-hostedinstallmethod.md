---
title: Метод Хостединсталлмесод класса MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Метод для выполнения установки пакета приложения из размещенного расположения, такого как локальный диск, UNC-источник данных или HTTPS. См. также Хостединсталл.
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Метод Хостединсталлмесод
- Метод Хостединсталлмесод, класс MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Класс MDM_EnterpriseModernAppManagement_AppInstallation01_01, метод Хостединсталлмесод
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60cd27419dce09b2a0e4aa7304bb53ac63e7d205b93cbaacbf832aa4a3501338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750634"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Метод Хостединсталлмесод \_ класса MDM ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Метод для выполнения установки пакета приложения из размещенного расположения, такого как локальный диск, UNC-источник данных или HTTPS. См. также [хостединсталл](/windows/client-management/mdm/enterprisemodernappmanagement-csp).

## <a name="syntax"></a>Синтаксис


```mof
uint32 HostedInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*параметр* \[ окне\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**MDM \_ ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01**](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

