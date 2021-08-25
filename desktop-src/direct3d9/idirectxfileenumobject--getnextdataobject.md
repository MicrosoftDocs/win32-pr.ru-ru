---
description: Извлекает следующий объект верхнего уровня в файле DirectX. Не рекомендуется.
ms.assetid: 91cd3205-5603-4a62-aab2-7ef4adb9e6d1
title: 'Метод Идиректксфилинумобжект:: Жетнекстдатаобжект (Дксфиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject.GetNextDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 42d95fcee1b431f5121389d7bb6595e5c53ca56298c75ed6010ee86733c310e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985134"
---
# <a name="idirectxfileenumobjectgetnextdataobject-method"></a>Метод Идиректксфилинумобжект:: Жетнекстдатаобжект

Извлекает следующий объект верхнего уровня в файле DirectX. Не рекомендуется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetNextDataObject(
  [out] LPDIRECTXFILEDATA *ppDataObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппдатаобж* \[ заполняет\]
</dt> <dd>

Тип: **[ **лпдиректксфиледата**](idirectxfiledata.md)\***

Адрес указателя на интерфейс [**идиректксфиледата**](idirectxfiledata.md) , представляющий возвращаемый объект данных файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение ДКСФИЛЕ \_ ОК. Если метод завершается ошибкой, возвращаемое значение может быть одним из следующих: ДКСФИЛИРР \_ бадвалуе, дксфилирр \_ номореобжектс

## <a name="remarks"></a>Remarks

Объекты верхнего уровня всегда являются объектами данных. Объекты ссылок на данные и двоичные объекты могут быть только дочерними объектами данных.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[идиректксфилинумобжект](idirectxfileenumobject.md)
</dt> </dl>

 

 




