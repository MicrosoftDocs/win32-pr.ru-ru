---
title: Метод Ибаккграундкопифиле метода Progress (Deliveryoptimization. h)
description: Получает сведения о ходе перемещения файла.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Метод Progress
- Метод Progress, интерфейс Ибаккграундкопифиле
- Интерфейс Ибаккграундкопифиле, метод Progress
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490266"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a>Метод Ибаккграундкопифиле:: Progress

Получает сведения о ходе перемещения файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппрогресс* \[ заполняет\]
</dt> <dd>

Структура, члены которой указывают ход выполнения операции перемещения файла. Дополнительные сведения о типе доступных сведений о ходе выполнения см. в разделе Структура [**BG_FILE_PROGRESS**](bg-file-progress.md) .

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
| IID<br/>                      | IID_IBackgroundCopyFile определен как 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**ибаккграундкопифиле**](ibackgroundcopyfile.md)
</dt> <dt>

[**Использованием метода ibackgroundcopyjob:: Progress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





