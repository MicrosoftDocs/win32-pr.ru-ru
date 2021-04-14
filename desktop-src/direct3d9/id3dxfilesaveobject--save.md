---
description: Сохраняет объект данных и его дочерние элементы в файл. x на диске.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'Метод ID3DXFileSaveObject:: Save (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424393"
---
# <a name="id3dxfilesaveobjectsave-method"></a>Метод ID3DXFileSaveObject:: Save

Сохраняет объект данных и его дочерние элементы в файл. x на диске.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Save();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть следующим: D3DXFERR \_ бадобжект.

## <a name="remarks"></a>Комментарии

После выполнения этого метода [**ID3DXFileSaveObject:: адддатаобжект**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData:: адддатаобжект**](id3dxfilesavedata--adddataobject.md) и [**ID3DXFileSaveData:: адддатареференце**](id3dxfilesavedata--adddatareference.md) нельзя вызвать, пока не будет создан новый объект [**ID3DXFile**](id3dxfile.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




