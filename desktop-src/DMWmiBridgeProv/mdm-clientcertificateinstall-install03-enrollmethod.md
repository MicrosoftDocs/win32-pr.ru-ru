---
title: Метод Енроллмесод класса MDM_ClientCertificateInstall_Install03
description: Активирует устройство для запуска регистрации сертификата.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Метод Енроллмесод
- Метод Енроллмесод, класс MDM_ClientCertificateInstall_Install03
- Класс MDM_ClientCertificateInstall_Install03, метод Енроллмесод
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803130"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>Метод Енроллмесод \_ класса MDM клиентцертификатеинсталл \_ Install03

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Активирует устройство для запуска регистрации сертификата. Устройство не будет уведомлять сервер MDM после того, как будет выполнена регистрация сертификата. Сервер MDM может позже запросить устройство, чтобы узнать, добавлен ли новый сертификат. См. также [**Регистрация**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Синтаксис


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Обязательный. Активирует устройство для запуска регистрации сертификата. Устройство не будет уведомлять сервер MDM после того, как будет выполнена регистрация сертификата. Сервер MDM может позже запросить устройство, чтобы узнать, добавлен ли новый сертификат.

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

[**MDM \_ клиентцертификатеинсталл \_ Install03**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

