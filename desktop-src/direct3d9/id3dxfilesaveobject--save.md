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
ms.openlocfilehash: a49c4776f9ce590d287869436b329ddf9a378e73f04f0127246fc890944ffee3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563964"
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

## <a name="remarks"></a>Remarks

После выполнения этого метода [**ID3DXFileSaveObject:: адддатаобжект**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData:: адддатаобжект**](id3dxfilesavedata--adddataobject.md) и [**ID3DXFileSaveData:: адддатареференце**](id3dxfilesavedata--adddatareference.md) нельзя вызвать, пока не будет создан новый объект [**ID3DXFile**](id3dxfile.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXFileSaveObject](id3dxfilesaveobject.md)
</dt> </dl>

 

 




