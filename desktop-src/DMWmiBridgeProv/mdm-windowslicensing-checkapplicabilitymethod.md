---
title: Метод Чеккаппликабилитимесод класса MDM_WindowsLicensing
description: проверяет, может ли указанный ключ продукта использоваться для обновления выпуска, активации или изменения ключа продукта Windows 10 для устройств настольных систем. См. также Чеккаппликабилити.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Метод Чеккаппликабилитимесод
- Метод Чеккаппликабилитимесод, класс MDM_WindowsLicensing
- Класс MDM_WindowsLicensing, метод Чеккаппликабилитимесод
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db236e05ffe7b5b6273e7cba594266c31720932b43a7df2de751a0fa66cced5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750154"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>Метод Чеккаппликабилитимесод \_ класса MDM виндовслиценсинг

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

проверяет, может ли указанный ключ продукта использоваться для обновления выпуска, активации или изменения ключа продукта Windows 10 для устройств настольных систем. См. также [чеккаппликабилити](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Синтаксис


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*параметр* \[ окне\]
</dt> <dd>

Ключ продукта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

TRUE или FALSE

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

[**\_ВИНДОВСЛИЦЕНСИНГ MDM**](mdm-windowslicensing.md)
</dt> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

