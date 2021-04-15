---
description: Получает идентификатор шаблона в этом объекте данных файла.
ms.assetid: abc53dda-d3ed-461b-b3d8-a64845c44c81
title: 'Метод ID3DXFileData:: GetType (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetType
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 566052c06d5f7e55629a26442dd774a2f80fd647
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424457"
---
# <a name="id3dxfiledatagettype-method"></a>Метод ID3DXFileData:: GetType

Получает идентификатор шаблона в этом объекте данных файла.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetType(
  [in] const GUID *pType
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птипе* \[ окне\]
</dt> <dd>

Тип: **константа [**GUID**](guid.md) \***

Указатель на идентификатор GUID, представляющий шаблон в этом объекте данных файла.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileData](id3dxfiledata.md)
</dt> </dl>

 

 




