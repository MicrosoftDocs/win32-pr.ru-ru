---
description: 'Метод ID3DXFileEnumObject:: Child — получает дочерний объект в этом объекте данных файла.'
ms.assetid: d8f367dd-8858-48ae-9de5-17de1538aadf
title: Метод ID3DXFileEnumObject::-Child (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 20075c0e30985ab4f5c7c691b40caf302db98d6b5c8cf863fd9c57fca895ee40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802797"
---
# <a name="id3dxfileenumobjectgetchild-method"></a>Метод ID3DXFileEnumObject:: Child

Извлекает дочерний объект в этом объекте данных файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetChild(
  [in]  SIZE_T        id,
  [out] ID3DXFileData **ppObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*идентификатор* \[ в\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)**

ИДЕНТИФИКАТОР получаемого дочернего объекта.

</dd> <dt>

*ппобж* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Адрес указателя для получения указателя интерфейса дочернего объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ номореобжектс.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileEnumObject](id3dxfileenumobject.md)
</dt> </dl>

 

 
