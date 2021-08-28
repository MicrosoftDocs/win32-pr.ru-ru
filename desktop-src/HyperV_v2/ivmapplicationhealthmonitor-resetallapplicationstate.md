---
description: Сбрасывает состояние работоспособности для всех приложений в виртуальной машине.
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: 'Метод Ивмаппликатионхеалсмонитор:: Ресеталлаппликатионстате'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4e97d5d16200501d77acf8b0b02cc5562d51706fcc46298421ad7f7e8fc0dfac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694354"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a>Метод Ивмаппликатионхеалсмонитор:: Ресеталлаппликатионстате

Сбрасывает состояние работоспособности для всех приложений в виртуальной машине. В случае успеха состояние работоспособности всех наблюдаемых приложений будет равно **аппликатионстатехеалси**.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

чтобы использовать этот программный элемент, на виртуальной машине, в которой выполняется приложение, должны быть установлены компоненты интеграции Windows 8.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                      |
| Версия<br/>                  | Интеграционные компоненты для Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>Вмаппликатионхеалсмонитор. idl</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ивмаппликатионхеалсмонитор**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




