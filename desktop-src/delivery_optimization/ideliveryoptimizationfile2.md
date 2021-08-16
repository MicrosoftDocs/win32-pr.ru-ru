---
title: Интерфейс IDeliveryOptimizationFile2
description: IDeliveryOptimizationFile2 поддерживает настройку и получение необязательных свойств файла.
keywords:
- Интерфейс IDeliveryOptimizationFile2
- Интерфейс IDeliveryOptimizationFile2, описание
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed7409635444885b662688ce94c300aae6e62186dd76bd7278b3e7445ef50c90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542049"
---
# <a name="ideliveryoptimizationfile2-interface"></a>Интерфейс IDeliveryOptimizationFile2

**IDeliveryOptimizationFile2** поддерживает настройку и получение необязательных свойств файла. 

## <a name="members"></a>Элементы

Интерфейс **IDeliveryOptimizationFile2** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IDeliveryOptimizationFile2** также имеет следующие типы членов:

- [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **IDeliveryOptimizationFile2** содержит следующие методы.

| Метод                                                 | Описание                                                  |
|:-------------------------------------------------------|:-------------------------------------------------------------|
| [**GetProperty**](ideliveryoptimizationfile2-getproperty.md)  | Этот метод возвращает одно свойство файла DO. |
| [**SetProperty**](ideliveryoptimizationfile2-setproperty.md)  | Этот метод задает одно свойство для файла DO.    |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------|-----------------------------------------------------------------------------------|
| Минимальная версия клиента      | Windows 10, только для \[ настольных приложений версии 1803\]                                    |
| Минимальная версия сервера      | Windows Server, только для \[ настольных приложений версии 1709\]                                |
| Header                        | Deliveryoptimization. h                                                            |
| IDL                           | DeliveryOptimization. idl                                                          |
| Библиотека                       | Досвк. lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 определен как 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
