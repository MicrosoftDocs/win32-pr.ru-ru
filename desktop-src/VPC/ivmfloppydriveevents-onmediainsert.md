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
ms.openlocfilehash: d607a2f63836ca1cb151e602b2d3b2021f4e3913
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694075"
---
# <a name="ivmfloppydriveeventsonmediainsert-method"></a>Метод Ивмфлоппидрививентс:: Онмедиаинсерт

\[Windows Virtual PC больше не доступна для использования в Windows 8. Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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

## <a name="remarks"></a>Комментарии

Этот метод вызывается при вставке носителя (образа гибкого диска или дискеты в дисководе узла). Клиентская программа должна реализовать этот метод интерфейса для получения уведомления о \_ событии вмфлоппидрививент онмедиаинсерт, исходящем от [**ивмфлоппидриве**](ivmfloppydrive.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/>                                                    |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                     |
| Окончание поддержки клиента<br/>    | Windows 7<br/>                                                                          |
| Продукт<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Впккоминтерфацес. h</dt> </dl> |
| IID<br/>                      | ДИИД \_ ивмфлоппидрививентс определяется как a9ed3401-4e09-4177-86ec-a13bf9fa7d4e<br/>      |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ивмфлоппидрививентс**](ivmfloppydriveevents.md)
</dt> </dl>

 

