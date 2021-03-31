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
ms.openlocfilehash: bc50af216eaae1687351d472b7151aaaeae9116f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354230"
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

## <a name="remarks"></a>Комментарии

Объекты верхнего уровня всегда являются объектами данных. Объекты ссылок на данные и двоичные объекты могут быть только дочерними объектами данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Дксфиле. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[идиректксфилинумобжект](idirectxfileenumobject.md)
</dt> </dl>

 

 




