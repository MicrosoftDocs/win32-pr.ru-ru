---
title: Метод Упградидитионвиспродукткэймесод класса MDM_WindowsLicensing
description: Вводит ключ продукта для обновления выпусков устройств Windows 10 Desktop. См. также Упградидитионвиспродукткэй.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Метод Упградидитионвиспродукткэймесод
- Метод Упградидитионвиспродукткэймесод, класс MDM_WindowsLicensing
- Класс MDM_WindowsLicensing, метод Упградидитионвиспродукткэймесод
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85824fc6fac9e5a15bf2bc890215afcbd0958680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491934"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Метод Упградидитионвиспродукткэймесод \_ класса MDM виндовслиценсинг

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Вводит ключ продукта для обновления выпусков устройств Windows 10 Desktop. См. также [упградидитионвиспродукткэй](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Синтаксис


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*параметр* \[ окне\]
</dt> <dd>

Ключ продукта.

</dd> </dl>

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

[**\_ВИНДОВСЛИЦЕНСИНГ MDM**](mdm-windowslicensing.md)
</dt> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

