---
title: Метод Ивмдвддрививентс Онмедиаежект (Впккоминтерфацес. h)
description: Получает уведомление о том, что носитель был извлечен с диска. | Метод Ивмдвддрививентс Онмедиаежект (Впккоминтерфацес. h)
ms.assetid: ec90fbce-7123-4bfa-abab-300e916fa089
keywords:
- Метод Онмедиаежект Virtual PC
- Метод Онмедиаежект Virtual PC, интерфейс Ивмдвддрививентс
- Ивмдвддрививентс интерфейс Virtual PC, метод Онмедиаежект
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaEject
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b66091dcc6cc5ee28ab6e0cb3d58e3e647e41cb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914352"
---
# <a name="ivmdvddriveeventsonmediaeject-method"></a>Метод Ивмдвддрививентс:: Онмедиаежект

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает уведомление о том, что носитель был извлечен с диска.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnMediaEject(
  [in] BSTR mediaPath
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*mediaPath* \[ окне\]
</dt> <dd>

Буква диска узла или путь к ISO-образу.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Этот метод вызывается при извлечении носителя (ISO-образ или диск на диске узла). Клиентская программа должна реализовать этот метод интерфейса, чтобы получить уведомление о \_ событии вмдвддрививент oneject, созданном из [**ивмдвддриве**](ivmdvddrive.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмдвддрививентс определяется как c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмдвддрививентс**](ivmdvddriveevents.md)
</dt> </dl>

 

