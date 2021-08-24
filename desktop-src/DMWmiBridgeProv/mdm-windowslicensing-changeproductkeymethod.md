---
title: Метод Чанжепродукткэймесод класса MDM_WindowsLicensing
description: этот метод устанавливает ключ продукта для устройств Windows 10 настольных пк. Точка не перезагружена. См. также Чанжепродукткэй.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Метод Чанжепродукткэймесод
- Метод Чанжепродукткэймесод, класс MDM_WindowsLicensing
- Класс MDM_WindowsLicensing, метод Чанжепродукткэймесод
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c164a97061b5e558a199a7d7e19a6bf26d7efc5d2a82c0a00e3831985c1a1cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693354"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Метод Чанжепродукткэймесод \_ класса MDM виндовслиценсинг

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Корпорация Майкрософт не предоставляет никаких гарантий, явных или подразумеваемых, относительно предоставленной здесь информации.\]

этот метод устанавливает ключ продукта для устройств Windows 10 настольных пк. Точка не перезагружена. См. также [чанжепродукткэй](/windows/client-management/mdm/windowslicensing-csp)

## <a name="syntax"></a>Синтаксис


```mof
uint32 ChangeProductKeyMethod(
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
| Пространство имен<br/>                | Корневой \\ CIMV2 \\ MDM \\ дммап<br/>                                                             |
| MOF<br/>                      | <dl> <dt>Дмвмибриджепров. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_ВИНДОВСЛИЦЕНСИНГ MDM**](mdm-windowslicensing.md)
</dt> </dl>

 

