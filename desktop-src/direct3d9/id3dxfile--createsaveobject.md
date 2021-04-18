---
description: Создает объект Save, который будет использоваться для сохранения данных в файл. x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'Метод ID3DXFile:: Креатесавеобжект (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713805"
---
# <a name="id3dxfilecreatesaveobject-method"></a>Метод ID3DXFile:: Креатесавеобжект

Создает объект Save, который будет использоваться для сохранения данных в файл. x.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на имя файла, используемого для сохранения данных.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[D3DXF \_ филесавеоптионс](d3dxf.md)**

Значение типа, указывающее имя файла, в который должны быть сохранены данные. Это значение может быть одним из флагов [параметров сохранения файла](d3dxf.md) .

</dd> <dt>

*двфилеформат* \[ окне\]
</dt> <dd>

Тип: **[D3DXF \_ FILEFORMAT](d3dxf.md)**

Указывает формат, используемый при сохранении файла. x. Это значение может быть одним из флагов [формата файла](d3dxf.md) . Дополнительные сведения см. в подразделе "Примечания".

</dd> <dt>

*ппсавеобж* \[ заполняет\]
</dt> <dd>

Тип: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Адрес указателя на интерфейс [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , представляющий созданный объект Save.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DXFERR \_ бадвалуе, D3DXFERR \_ парсиррор.

## <a name="remarks"></a>Комментарии

После использования этого метода используйте методы интерфейса [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) для создания объектов данных и сохранения шаблонов или данных.

Для сохраненного формата файла *двфилеформат* необходимо указать один из двоичных, устаревших двоичных или текстовых флагов в [форматах файлов](d3dxf.md) . Файл можно сжать с помощью необязательного \_ \_ флага сжатия D3DXF FILEFORMAT.

Значения формата файла можно комбинировать в логическом или для создания сжатого текста или сжатых двоичных файлов. Если указать, что формат файла должен быть текстовым и сжатым, файл будет записан первым в виде текста, а затем сжат. Однако сжатые текстовые файлы не так эффективны, как двоичные текстовые файлы; в большинстве случаев необходимо указать двоичные и сжатые данные.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 
