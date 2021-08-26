---
title: метод Довипемесод класса MDM_RemoteWipe
description: Запускает устройство для запуска удаленной очистки.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- метод Довипемесод
- метод Довипемесод, класс MDM_RemoteWipe
- Класс MDM_RemoteWipe, метод Довипемесод
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cff9cb831931c96fa8df1b376f96ea4c20b05bafdb12a85dec00b4f505af4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045644"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a>метод Довипемесод \_ класса MDM ремотевипе

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

Запускает устройство для запуска удаленной очистки. См. также [doWipe](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Синтаксис


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*параметр* \[ окне\]
</dt> <dd></dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                      |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_РЕМОТЕВИПЕ MDM**](mdm-remotewipe.md)
</dt> <dt>

[Использование сценариев PowerShell с WMI Bridge Provider](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

