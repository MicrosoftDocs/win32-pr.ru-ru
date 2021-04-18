---
title: Метод Ивмдрмлиценсе-License (Вмдрмсдк. h)
description: Метод КСМР извлекает лицензию как данные XML или.
ms.assetid: 63317841-fd13-4e83-8b99-e3cab1405050
keywords:
- Формат Windows Media для метода с лицензией
- Метод Ивмдрмлиценсе формат Windows Media, интерфейс
- Интерфейс Ивмдрмлиценсе интерфейса Windows Media Format, метод onlicense
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0692afb2ff127f9456e6da3c7546c67ae22ded
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704474"
---
# <a name="iwmdrmlicensegetlicense-method"></a>Метод Ивмдрмлиценсе:: License

Метод **КСМР извлекает лицензию как** данные XML или.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetLicense(
  [out] BYTE  **ppbLicense,
  [out] DWORD *pcbLicense,
  [out] DWORD *pdwLicenseType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппблиценсе* \[ заполняет\]
</dt> <dd>

Получает лицензию.

</dd> <dt>

*пкблиценсе* \[ заполняет\]
</dt> <dd>

Получает размер лицензии.

</dd> <dt>

*пдвлиценсетипе* \[ заполняет\]
</dt> <dd>

Получает тип возвращенной лицензии. Это значение устанавливается равным одной из констант в следующей таблице.



| Константа                  | Описание                            |
|---------------------------|----------------------------------------|
| \_ \_ XML типа лицензии \_ WMDRM | Полученная лицензия форматируется как XML. |
| \_тип лицензии \_ WMDRM \_ КСМР | Полученная лицензия отформатирована как КСМР. |



 

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Метод возвращает **значение HRESULT**. Допустимые значения включают, но не ограничиваются, значения, приведенные в следующей таблице.



| Код возврата                                                                          | Описание                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl> | Метод выполнен успешно.<br/> |



 

## <a name="remarks"></a>Комментарии

Нет.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вмдрмсдк. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>Вмдрмсдк. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**жетлиценсепроперти**](iwmdrmlicense-getlicenseproperty.md)
</dt> <dt>

[**Интерфейс Ивмдрмлиценсе**](iwmdrmlicense.md)
</dt> </dl>

 

 





