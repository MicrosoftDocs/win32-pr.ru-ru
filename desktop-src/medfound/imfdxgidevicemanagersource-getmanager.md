---
description: Возвращает Имфдксгидевицеманажер из приемника отрисовки Microsoft Media Foundation видео.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'Метод Имфдксгидевицеманажерсаурце:: Manage'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692931"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a>Метод Имфдксгидевицеманажерсаурце:: Manage

Возвращает [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) из приемника отрисовки Microsoft Media Foundation видео.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппманажер* \[ заполняет\]
</dt> <dd>

Объект [**имфдксгидевицеманажер**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Приложения UWP для классических приложений Windows 8.1 \|\]<br/>                                  |
| Минимальная версия сервера<br/> | \[Приложения UWP для классических приложений Windows Server 2012 R2 \|\]<br/>                       |
| IDL<br/>                      | <dl> <dt>Мфидл. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имфдксгидевицеманажерсаурце**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




