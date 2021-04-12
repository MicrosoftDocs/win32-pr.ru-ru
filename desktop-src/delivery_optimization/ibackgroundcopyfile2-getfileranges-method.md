---
title: Метод IBackgroundCopyFile2 Жетфилеранжес (Deliveryoptimization. h)
description: Извлекает диапазоны, которые необходимо загрузить из удаленного файла.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Метод Жетфилеранжес
- Метод Жетфилеранжес, интерфейс IBackgroundCopyFile2
- Интерфейс IBackgroundCopyFile2, метод Жетфилеранжес
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415388"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a>Метод IBackgroundCopyFile2:: Жетфилеранжес

Извлекает диапазоны, которые необходимо загрузить из удаленного файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Ранжекаунт* \[ в, out\]
</dt> <dd>

Число элементов в *диапазонах*.

</dd> <dt>

*Диапазоны* \[ заполняет\]
</dt> <dd>

Массив структур [**BG_FILE_RANGE**](bg-file-range.md) , указывающих диапазоны для загрузки. По завершении вызовите функцию [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) для освобождения *диапазонов*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает следующие возвращаемые значения, а также другие.



| Код возврата                                                                              | Описание                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Успешно<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Не указаны диапазоны или задано задание отправки или отправки-ответа. *Ранжекаунт* имеет нулевое значение, а для *Ranges* задано **значение NULL**.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server версии 1709\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 определен как 83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

