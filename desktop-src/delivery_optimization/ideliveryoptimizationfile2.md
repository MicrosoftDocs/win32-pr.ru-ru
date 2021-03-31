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
ms.openlocfilehash: a45efd821116b24e883ec29d494a1d588559f57a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071393"
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
| Минимальная версия клиента      | \[Только для настольных приложений Windows 10 версии 1803\]                                    |
| Минимальная версия сервера      | \[Только для настольных приложений Windows Server версии 1709\]                                |
| Header                        | Deliveryoptimization. h                                                            |
| IDL                           | DeliveryOptimization. idl                                                          |
| Библиотека                       | Досвк. lib                                                                         |
| DLL                           | Dosvc.dll                                                                         |
| IID                           | IID_IDeliveryOptimizationFile2 определен как 3A87296F-6EC2-4126-AB29-E3F8DC4CC390 |
