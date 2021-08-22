---
description: Помещает службу в запущенное состояние.
ms.assetid: 8977b806-150c-4ddc-a471-3fdafdcb4a55
title: Метод StartService класса CIM_Service (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c0e30adbece838cb913f215abedc4aa86a2762d00f046a54bf2717eaeecdb56e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119561814"
---
# <a name="startservice-method-of-the-cim_service-class-hyper-v-management"></a>Метод StartService класса CIM_Service (Управление Hyper-V)

Помещает службу в запущенное состояние.

> [!Note]
>
> Семантика этого метода пересекается с методом **RequestStateChange** , унаследованным от [**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md). Этот метод поддерживается, так как он широко реализован, и его простая семантика "Start" удобна для использования.

 

## <a name="syntax"></a>Синтаксис


```mof
uint32 StartService();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




