---
title: IManipulationProcessor Минимумскалеротатерадиус, свойство
description: Указывает, насколько велика дистанция контактов на жесте масштабирования или вращения для запуска манипуляций.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- Сенсорный ввод окон свойств Минимумскалеротатерадиус
- Минимумскалеротатерадиус свойств Windows Touch, интерфейс IManipulationProcessor
- IManipulationProcessor интерфейса Windows, свойство Минимумскалеротатерадиус
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784155"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a>Свойство IManipulationProcessor:: Минимумскалеротатерадиус

Указывает, насколько велика дистанция контактов на жесте масштабирования или вращения для запуска манипуляций.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a>Значение свойства

Указывает минимальное расстояние между контактами для триггеров масштабирования или вращения.

## <a name="error-codes"></a>Коды ошибок

## <a name="remarks"></a>Комментарии

> [!Note]  
> Это свойство задается в центипикселс (100ths пикселей).

 

При задании этого значения процессор манипуляции будет игнорировать жесты, которые имеют слишком маленький радиус. Это полезно, если вы хотите запретить пользователю манипулировать объектом слишком маленьким радиусом. Например, если вы используете процессор манипуляции с кругом и хотите обеспечить поддержку радиуса, превышающего 100 пикселей, это значение можно задать равным 10000.

## <a name="examples"></a>Примеры


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




