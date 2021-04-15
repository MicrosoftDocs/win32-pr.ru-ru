---
description: Метод Провидеинтежердата объекта Конфигуремодуле вызывается Mergemod.dll для получения целочисленных данных из клиентского средства.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Конфигуремодуле. Провидеинтежердата, метод (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669279"
---
# <a name="configuremoduleprovideintegerdata-method"></a>Конфигуремодуле. Провидеинтежердата, метод

Метод **провидеинтежердата** [**объекта конфигуремодуле**](configuremodule-object.md) вызывается Mergemod.dll для получения целочисленных данных из клиентского средства.

Mergemod.dll предоставляет *имя* из соответствующей записи в [таблице модулеконфигуратион](moduleconfiguration-table.md).

Средство должно вернуть S \_ OK и предоставить соответствующее целое число настройки в *конфигдата*.

Если средство не предоставляет данные конфигурации для этого значения *имени* , функция должна вернуть значение \_ false. В этом случае Mergemod.dll игнорирует значение аргумента *конфигдата* и использует значение по умолчанию из таблицы модулеконфигуратион.

## <a name="syntax"></a>Синтаксис


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Name* 
</dt> <dd>

Имя элемента, для которого извлекаются данные.

</dd> <dt>

*конфигдата* 
</dt> <dd>

Указатель на текст настройки.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

Клиент может быть вызван не более одного раза для каждой записи в [таблице модулеконфигуратион](moduleconfiguration-table.md). Обратите внимание, что Mergemod.dll никогда не выполняет несколько вызовов клиента для одного и того же значения "Name". Если в таблице Модулесубститутион нет записей, использующих свойство, запись в таблице Модулеконфигуратион не вызывает клиент.

### <a name="c"></a>C++

См. раздел [**функция провидеинтежердата**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 2,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




