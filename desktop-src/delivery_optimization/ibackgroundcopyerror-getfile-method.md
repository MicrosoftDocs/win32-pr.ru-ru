---
title: Метод Ибаккграундкоперрор-File (Deliveryoptimization. h)
description: Извлекает указатель интерфейса на объект File, связанный с ошибкой.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- Метод onfile
- Метод onfile, интерфейс Ибаккграундкоперрор
- Интерфейс Ибаккграундкоперрор, метод onfile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fbed5497bcebb3518c7f6a56646976cc01fbfebc501af4a08e861139311f4bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096714"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a>Метод Ибаккграундкоперрор:: onfile

Извлекает указатель интерфейса на объект File, связанный с ошибкой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппфиле* \[ заполняет\]
</dt> <dd>

Указатель интерфейса [**ибаккграундкопифиле**](ibackgroundcopyfile.md) , методы которого используются для определения локальных и удаленных имен файлов, связанных с ошибкой. Параметр *ппфиле* имеет значение **null** , если ошибка не связана с локальным или удаленным файлом. По завершении выпустите *ппфиле*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие значения **HRESULT** .



| Код возврата                                                                                                | Описание                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                   | Указатель интерфейса на объект файла успешно получен.<br/>                                     |
| <dl> <dt>**DO_E_FILE_NOT_AVAILABLE**</dt> </dl> | Ошибка не связана с локальным или удаленным файлом. Параметр *ппфиле* имеет значение **null**.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError определен как 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ибаккграундкоперрор**](ibackgroundcopyerror.md)
</dt> <dt>

[**Ибаккграундкоперрор:: возникла ошибка**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





