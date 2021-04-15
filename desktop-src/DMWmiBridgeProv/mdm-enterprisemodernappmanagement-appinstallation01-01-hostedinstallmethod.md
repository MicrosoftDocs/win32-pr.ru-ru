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
ms.openlocfilehash: 9597f748a2b5695fd2703f187cfe50db7ad0aa85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105654592"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a>Метод Хостединсталлмесод \_ класса MDM ентерприсемодернаппманажемент \_ AppInstallation01 \_ 01

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

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
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                    |
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

 

