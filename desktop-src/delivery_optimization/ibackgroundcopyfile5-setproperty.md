---
title: Метод SetProperty IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Задает универсальное свойство для передачи файла оптимизации доставки (DO).
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty — метод
- Метод SetProperty, интерфейс IBackgroundCopyFile5
- Интерфейс IBackgroundCopyFile5, метод SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988562"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a>Метод IBackgroundCopyFile5:: SetProperty

Задает универсальное свойство для передачи файла оптимизации доставки (DO).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PropertyId* \[ окне\]
</dt> <dd>

Указывает свойство, которое необходимо задать.

</dd> <dt>

*Проертивалуе* \[ заполняет\]
</dt> <dd>

Указатель на объединение, указывающее значение, которое необходимо задать. Используется элемент объединения, соответствующий ИДЕНТИФИКАТОРу свойства.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается с ошибкой, возвращается **S_OK**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 определен как 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5., свойство**](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





