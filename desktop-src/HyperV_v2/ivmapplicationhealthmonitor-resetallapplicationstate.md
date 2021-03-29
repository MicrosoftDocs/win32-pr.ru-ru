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
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898334"
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

## <a name="remarks"></a>Комментарии

Чтобы использовать этот программный элемент, на виртуальной машине, в которой выполняется приложение, должны быть установлены компоненты интеграции Windows 8.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                                |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                      |
| Версия<br/>                  | Компоненты интеграции для Windows 8<br/>                                                           |
| IDL<br/>                      | <dl> <dt>Вмаппликатионхеалсмонитор. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмаппликатионхеалсмонитор**](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




