---
description: '\_ \_ Тип ПЕРЕЧИСЛЕНИЯ параметры удаления объекта описывает параметры, которые поддерживаются устройством при удалении объекта.'
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: Перечисление DELETE_OBJECT_OPTIONS (Портабледевице. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704512"
---
# <a name="delete_object_options-enumeration"></a>\_ \_ Перечисление параметров удаления объекта

Тип **перечисления \_ \_ Параметры удаления объекта** описывает параметры, которые поддерживаются устройством при удалении объекта.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**ПЕРЕНОСное \_ устройство \_ \_ не удаляет \_ рекурсию**
</dt> <dd>

Удалите только объект и завершите его ошибкой, если у него есть дочерние элементы.

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**Удаление ПЕРЕНОСного \_ устройства \_ \_ с \_ рекурсией**
</dt> <dd>

Удалите объект и все его дочерние элементы.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Приложение может получить параметры удаления, которые поддерживает устройство, вызвав [**ипортабледевицекапабилитиес:: жеткоммандоптионс**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) для команды **WPD \_ команда \_ \_ \_ DELETE \_ Objects** . Он должен проверить значение параметра типа WPD, которое **\_ \_ \_ \_ \_ \_ поддерживает рекурсивное удаление** , которое этот метод возвращает в объекте [**ипортабледевицевалуесколлектион**](iportabledevicevaluescollection.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Портабледевице. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры и типы перечислений**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




