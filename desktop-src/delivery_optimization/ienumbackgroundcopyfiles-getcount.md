---
title: Метод Иенумбаккграундкопифилес-Count (Deliveryoptimization. h)
description: Извлекает количество файлов в перечислении.
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount - метод
- Метод NOCOUNT, интерфейс Иенумбаккграундкопифилес
- Интерфейс Иенумбаккграундкопифилес, метод NOCOUNT
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05e2672f0cda3c572024a0865b2fb534dddb6598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802254"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a>Метод Иенумбаккграундкопифилес:: NOCOUNT

Извлекает количество файлов в перечислении.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pCount* \[ заполняет\]
</dt> <dd>

Число файлов в перечислении.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает **S_OK** при успешном или одном из стандартных значений **HRESULT** com при ошибке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles определен как CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иенумбаккграундкопифилес**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





