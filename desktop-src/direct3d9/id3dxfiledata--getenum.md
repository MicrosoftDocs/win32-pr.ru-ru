---
description: Извлекает объект перечисления в этом объекте данных файла.
ms.assetid: 383560e2-1888-4e37-9883-2ddbcb101cf6
title: Метод ID3DXFileData::-Enum (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetEnum
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 79ee6272f6b685c5e80b7c7b76b39925a08bb67cc07ba7af23a5b276b414f194
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748554"
---
# <a name="id3dxfiledatagetenum-method"></a>Метод ID3DXFileData:: Enum

Извлекает объект перечисления в этом объекте данных файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetEnum(
  [in] ID3DXFileEnumObject **ppObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппобж* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Адрес указателя для получения объекта перечисления в этом объекте данных файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




