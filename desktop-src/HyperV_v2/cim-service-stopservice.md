---
description: Скорость службы в остановленном состоянии.
ms.assetid: d7469643-bccc-4f55-b2fc-d2bc2e392d84
title: Метод работы класса CIM_Service (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f4eb354a48b074bad8adac4d5635e204844c31b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103897630"
---
# <a name="stopservice-method-of-the-cim_service-class-hyper-v-management"></a>Метод работы класса CIM_Service (Управление Hyper-V)

Скорость службы в остановленном состоянии.

> [!Note]
>
> Семантика этого метода пересекается с методом **RequestStateChange** , унаследованным от [**CIM \_ енабледлогикалелемент**](cim-enabledlogicalelement.md). Этот метод поддерживается, так как он широко реализован, а его простая семантика "остановлена" удобна для использования.

 

## <a name="syntax"></a>Синтаксис


```mof
uint32 StopService();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




