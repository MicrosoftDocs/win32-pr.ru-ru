---
title: Метод Иделиверйоптимизатионфиле метода stats (Deliveryoptimization. h)
description: Возвращает статистику загрузки и передачи для указанного файла.
ms.assetid: 8A3AD658-F1AD-4EA5-B010-AB7B88126FD6
keywords:
- GetStats - метод
- Метод stats, интерфейс Иделиверйоптимизатионфиле
- Интерфейс Иделиверйоптимизатионфиле, метод метода stats
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile.GetStats
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 08c5cff0672130049c325a00cb63c8dbc5c2e8ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415964"
---
# <a name="ideliveryoptimizationfilegetstats-method"></a>Метод Иделиверйоптимизатионфиле:: stats

Возвращает статистику загрузки и передачи для указанного файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStats(
  [out] DOSwarmStats *swarmStats
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*свармстатс* \[ заполняет\]
</dt> <dd>

Возвращает статистику загрузки и передачи для указанного файла. Дополнительные сведения см. в разделе Структура [**досвармстатс**](doswarmstats.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод должен возвращать **S_OK**.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IDeliveryOptimizationFile определен как B76B9699-E99E-4101-803F-A20E325D93E2<br/>        |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иделиверйоптимизатионфиле**](ideliveryoptimizationfile.md)
</dt> </dl>

 

 





