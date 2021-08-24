---
title: Интерфейс Иделиверйоптимизатионфиле
description: Реализуйте интерфейс Иделиверйоптимизатионфиле, чтобы узнать состояние определенного файла.
ms.assetid: 4D1D82E1-B39C-4634-A0B7-BC4322796AB2
keywords:
- Интерфейс Иделиверйоптимизатионфиле
- Интерфейс Иделиверйоптимизатионфиле, описание
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 880cc982d32e2a81b4263c3cba55331ea5524643adfc8483ed96465154d47cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635744"
---
# <a name="ideliveryoptimizationfile-interface"></a>Интерфейс Иделиверйоптимизатионфиле

Реализуйте интерфейс **иделиверйоптимизатионфиле** , чтобы узнать состояние определенного файла.

## <a name="members"></a>Элементы

Интерфейс **иделиверйоптимизатионфиле** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иделиверйоптимизатионфиле** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иделиверйоптимизатионфиле** содержит следующие методы.



| Метод                                                 | Описание                                                       |
|:-------------------------------------------------------|:------------------------------------------------------------------|
| [**GetStats**](ideliveryoptimizationfile-getstats.md) | Возвращает статистику загрузки и передачи для указанного файла.<br/> |

## <a name="requirements"></a>Требования

| Требование | Значение |
|-------------------------------|----------------------------------------------------------------------------------|
| Минимальная версия клиента      | Windows 10, только для \[ настольных приложений версии 1709\]                                   |
| Минимальная версия сервера      | Windows Server, только для \[ настольных приложений версии 1709\]                               |
| Заголовок                        | Deliveryoptimization. h                                                           |
| IDL                           | DeliveryOptimization. idl                                                         |
| Библиотека                       | Досвк. lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile определен как B76B9699-E99E-4101-803F-A20E325D93E2 |
