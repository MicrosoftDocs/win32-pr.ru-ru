---
description: Извлекает объект ID3DXFile.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: Метод ID3DXFileEnumObject::-File (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b07874cf492bc84207c6ea084df4c8a7506e1a6b3fdf6f94947092ad13cd160d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802736"
---
# <a name="id3dxfileenumobjectgetfile-method"></a>Метод ID3DXFileEnumObject:: onfile

Извлекает объект [**ID3DXFile**](id3dxfile.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппфиле* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DXFile**](id3dxfile.md)\*\***

Адрес указателя на интерфейс [**ID3DXFile**](id3dxfile.md) , представляющий возвращаемый объект.

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

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 




