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
ms.openlocfilehash: 2b86434f4be2f7d14ae46f4af92784c1be4fd1aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710475"
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
| Минимальная версия клиента      | \[Только для настольных приложений Windows 10 версии 1709\]                                   |
| Минимальная версия сервера      | \[Только для настольных приложений Windows Server версии 1709\]                               |
| Header                        | Deliveryoptimization. h                                                           |
| IDL                           | DeliveryOptimization. idl                                                         |
| Библиотека                       | Досвк. lib                                                                        |
| DLL                           | Dosvc.dll                                                                        |
| IID                           | IID_IDeliveryOptimizationFile определен как B76B9699-E99E-4101-803F-A20E325D93E2 |
