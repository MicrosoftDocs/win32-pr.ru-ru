---
title: Метод использованием метода ibackgroundcopyjob Енумфилес (Deliveryoptimization. h)
description: Извлекает указатель интерфейса Иенумбаккграундкопифилес, используемый для перечисления файлов в задании.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- Метод Енумфилес
- Метод Енумфилес, интерфейс использованием метода ibackgroundcopyjob
- Интерфейс использованием метода ibackgroundcopyjob, метод Енумфилес
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136162"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>Метод использованием метода ibackgroundcopyjob:: Енумфилес

Извлекает указатель интерфейса [**иенумбаккграундкопифилес**](ienumbackgroundcopyfiles-.md) , используемый для перечисления файлов в задании.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппенумфилес* \[ заполняет\]
</dt> <dd>

Указатель интерфейса [**иенумбаккграундкопифилес**](ienumbackgroundcopyfiles-.md) , который используется для перечисления файлов в задании. Выпустите *ппенумфилес* по завершении.

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
| IID<br/>                      | IID_IBackgroundCopyJob определен как 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Использованием метода ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**иенумбаккграундкопифилес**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





