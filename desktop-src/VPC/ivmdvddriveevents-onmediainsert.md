---
title: Метод Ивмдвддрививентс Онмедиаинсерт (Впккоминтерфацес. h)
description: Получает уведомление о том, что носитель вставлен в диск. | Метод Ивмдвддрививентс Онмедиаинсерт (Впккоминтерфацес. h)
ms.assetid: a246e2dd-638e-4d2f-9089-74771cd8bb2b
keywords:
- Метод Онмедиаинсерт Virtual PC
- Метод Онмедиаинсерт Virtual PC, интерфейс Ивмдвддрививентс
- Ивмдвддрививентс интерфейс Virtual PC, метод Онмедиаинсерт
topic_type:
- apiref
api_name:
- IVMDVDDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49b19beabfcc4cab182af850d27d3d45ea565b266e8bcaa8fa2488aa145f43fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595738"
---
# <a name="ivmdvddriveeventsonmediainsert-method"></a>Метод Ивмдвддрививентс:: Онмедиаинсерт

\[Windows Virtual PC больше не доступен для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Получает уведомление о том, что носитель вставлен в диск.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT OnMediaInsert(
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

## <a name="remarks"></a>Remarks

Этот метод вызывается при вставке носителя (ISO-образ или диск на диске узла). Клиентская программа должна реализовать этот метод интерфейса, чтобы получить уведомление о \_ событии Вмдвддрививент INSERT, созданном из [**ивмдвддриве**](ivmdvddrive.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмдвддрививентс определяется как c2a7d8e9-e76c-4eb8-94f7-71a5122d249b<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмдвддрививентс**](ivmdvddriveevents.md)
</dt> </dl>

 

