---
title: Метод Ивмфлоппидрививентс Онмедиаинсерт (Впккоминтерфацес. h)
description: Получает уведомление о том, что носитель вставлен в диск. | Метод Ивмфлоппидрививентс Онмедиаинсерт (Впккоминтерфацес. h)
ms.assetid: 922fca14-8ef6-4d3d-b1b6-72d2ea83e8ef
keywords:
- Метод Онмедиаинсерт Virtual PC
- Метод Онмедиаинсерт Virtual PC, интерфейс Ивмфлоппидрививентс
- Ивмфлоппидрививентс интерфейс Virtual PC, метод Онмедиаинсерт
topic_type:
- apiref
api_name:
- IVMFloppyDriveEvents.OnMediaInsert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30eb00222304168b30f6512b51f9d381fc4fbd61e7c5d254e0d53c3eb931a819
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594783"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a>Метод Ивмфлоппидрививентс:: Онмедиаинсерт

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

Буква диска узла или путь к образу дискеты.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Этот метод вызывается при вставке носителя (образа гибкого диска или дискеты в дисководе узла). Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии вмфлоппидрививент онмедиаинсерт, исходящем от [**ивмфлоппидриве**](ivmfloppydrive.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Заголовок<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмфлоппидрививентс определяется как a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмфлоппидрививентс**](ivmfloppydriveevents.md)
</dt> </dl>

 

