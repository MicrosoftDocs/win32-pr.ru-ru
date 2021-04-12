---
description: Запрашивает сброс объекта типа "логическое".
ms.assetid: f7655825-3de5-421f-a3e9-97d2f605affd
title: Метод Reset класса CIM_LogicalDevice (Управление Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 851332103143e84863762d8cc1183ec3ad841ca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347795"
---
# <a name="reset-method-of-the-cim_logicaldevice-class-hyper-v-management"></a>Метод Reset класса CIM_LogicalDevice (Управление Hyper-V)

Запрашивает сброс объекта типа "логическое". В подклассе можно указать набор возможных кодов возврата, используя квалификатор ValueMap в методе. Строки, в которые содержимое ValueMap является переведенными, могут также быть указаны в подклассе как квалификатор массива Values.

## <a name="syntax"></a>Синтаксис


```mof
uint32 Reset();
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

[**Модель \_ CIM**](cim-logicaldevice.md)
</dt> </dl>

 

 




