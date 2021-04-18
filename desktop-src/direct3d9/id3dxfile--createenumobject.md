---
description: Создает объект перечислителя, который будет считывать x-файл.
ms.assetid: 86d05eab-601c-4beb-9dbe-c23fa524871c
title: 'Метод ID3DXFile:: Креатинумобжект (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateEnumObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a58a3341bacf9b323cc5753f8e9e51c4b703b966
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713806"
---
# <a name="id3dxfilecreateenumobject-method"></a>Метод ID3DXFile:: Креатинумобжект

Создает объект перечислителя, который будет считывать x-файл.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateEnumObject(
  [out] LPCVOID               pvSource,
  [in]  D3DXF_FILELOADOPTIONS loadflags,
  [out] ID3DXFileEnumObject   **ppEnumObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвсаурце* \[ заполняет\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Источник данных. Любое из следующих:

-   Имя файла
-   Структура [**\_ филелоадмемори D3DXF**](d3dxf-fileloadmemory.md)
-   Структура [**\_ филелоадресаурце D3DXF**](d3dxf-fileloadresource.md)

В зависимости от значения лоадфлагс.

</dd> <dt>

*лоадфлагс* \[ окне\]
</dt> <dd>

Тип: **[D3DXF \_ филелоадоптионс](d3dxf.md)**

Значение, указывающее источник данных. Это значение может быть одним из флагов [ \_ филелоадоптионс D3DXF](d3dxf.md) .

</dd> <dt>

*ппенумобж* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DXFileEnumObject**](id3dxfileenumobject.md)\*\***

Адрес указателя на интерфейс [**ID3DXFileEnumObject**](id3dxfileenumobject.md) , представляющий созданный объект перечислителя.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ парсиррор.

## <a name="remarks"></a>Комментарии

После использования этого метода используйте один из методов [**ID3DXFileEnumObject**](id3dxfileenumobject.md) для получения объекта данных.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileEnumObject**](id3dxfileenumobject.md)
</dt> </dl>

 

 
