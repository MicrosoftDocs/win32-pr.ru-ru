---
description: Регистрирует пользовательские шаблоны при наличии объекта перечисления ID3DXFileEnumObject.
ms.assetid: 1b0c71db-639b-4836-8a65-7d0a2ed3ba4f
title: 'Метод ID3DXFile:: Регистеренумтемплатес (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterEnumTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 89a8b136bdc0e202fc87ba8fd4d7f013203814eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424446"
---
# <a name="id3dxfileregisterenumtemplates-method"></a>Метод ID3DXFile:: Регистеренумтемплатес

Регистрирует пользовательские шаблоны при наличии объекта перечисления [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterEnumTemplates(
  [in] ID3DXFileEnumObject *pEnum
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пенум* \[ окне\]
</dt> <dd>

Тип: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\***

Указатель на объект перечисления [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , содержащий шаблоны.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ .

Если метод завершается с ошибкой, будет возвращено следующее значение: D3DXFERR \_ бадвалуе.

## <a name="remarks"></a>Комментарии

При вызове этого метода он копирует шаблоны, хранящиеся в ID3DXFileEnumObject, представляющие файл, в локальное хранилище шаблонов объекта [**ID3DXFile**](id3dxfile.md) .

Если указатель [**ID3DXFileEnumObject**](id3dxfileenumobject.md) недоступен, вызовите вместо этого метод [**регистертемплатес**](id3dxfile--registertemplates.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**регистертемплатес**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




