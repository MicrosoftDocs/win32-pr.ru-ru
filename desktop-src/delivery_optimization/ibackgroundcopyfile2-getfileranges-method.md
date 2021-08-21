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
ms.openlocfilehash: 156bb2eb1e136593bfec4310599200f2d2800e271defa0e4a3259a4a67acb648
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047082"
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
| <dl> <dt>S_OK * * * *</dt> </dl> | Success<br/>                                                                                                                            |
| <dl> <dt>**S_FALSE**</dt> </dl>  | Не указаны диапазоны или задано задание отправки или отправки-ответа. *Ранжекаунт* имеет нулевое значение, а для *Ranges* задано **значение NULL**.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                       |
| Заголовок<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Досвк. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 определен как 83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>См. также

<dl> <dt>

[**BG_FILE_RANGE**](bg-file-range.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

