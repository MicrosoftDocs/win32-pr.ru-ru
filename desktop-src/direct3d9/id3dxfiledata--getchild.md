---
description: 'Метод ID3DXFileData:: Child — получает дочерний объект в этом объекте данных файла.'
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: Метод ID3DXFileData::-Child (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7fe6c0393e5cfb9ed8aeaf5808d33175e7f9bfe5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090382"
---
# <a name="id3dxfiledatagetchild-method"></a>Метод ID3DXFileData:: Child

Извлекает дочерний объект в этом объекте данных файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*уичилд* \[ окне\]
</dt> <dd>

Type: **[ **size \_ T**](../winprog/windows-data-types.md)**

ИДЕНТИФИКАТОР получаемого дочернего объекта.

</dd> <dt>

*ппчилд* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***

Адрес указателя для получения указателя интерфейса дочернего объекта.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ номореобжектс.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 
