---
description: Создание результата из описания ASCII или двоичного действия. Эта функция является расширенной версией D3DXCreateEffectFromFile, позволяющей приложению контролировать, какие параметры игнорируются системой эффектов.
ms.assetid: 963caa1e-bc1a-4d4b-bdb1-50b17d8b4132
title: Функция D3DXCreateEffectFromFileEx (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateEffectFromFileEx
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b3d97c5aa23dd0711cfb00585e5b8ba7d410fc02
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720935"
---
# <a name="d3dxcreateeffectfromfileex-function"></a>Функция D3DXCreateEffectFromFileEx

Создание результата из описания ASCII или двоичного действия. Эта функция является расширенной версией [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) , позволяющей приложению контролировать, какие параметры игнорируются системой эффектов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateEffectFromFileEx(
  _In_        LPDIRECT3DDEVICE9 pDevice,
  _In_        LPCTSTR           pSrcFile,
  _In_  const D3DXMACRO         *pDefines,
  _In_        LPD3DXINCLUDE     pInclude,
  _In_        LPCSTR            pSkipConstants,
  _In_        DWORD             Flags,
  _In_        LPD3DXEFFECTPOOL  pPool,
  _Out_       LPD3DXEFFECT      *ppEffect,
  _Out_       LPD3DXBUFFER      *ppCompilationErrors
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пдевице* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Указатель на устройство, которое создаст результат. См. [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9).

</dd> <dt>

*псркфиле* \[ окне\]
</dt> <dd>

Тип: **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Указатель на имя файла. Этот параметр поддерживает строки в Юникоде и ANSI. См. заметки.

</dd> <dt>

*пдефинес* \[ окне\]
</dt> <dd>

Тип: **const [**D3DXMACRO**](d3dxmacro.md) \***

Необязательный завершающий нуль массив определений макросов препроцессора. См. [**D3DXMACRO**](d3dxmacro.md).

</dd> <dt>

*пинклуде* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXINCLUDE**](id3dxinclude.md)**

Необязательный указатель интерфейса, [**ID3DXInclude**](id3dxinclude.md), используемый для обработки \# директив include. Если это значение равно **null**, \# включается или учитывается при компиляции из файла или вызывает ошибку при компиляции из ресурса или памяти.

</dd> <dt>

*пскипконстантс* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Строка параметров действия, которая будет игнорироваться системой эффектов. Строка **должна завершаться нулем и** должна содержать имя каждой управляемой приложением константы, разделенной точкой с запятой.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Если *псркфиле* содержит текстовый результат, флаги могут быть сочетанием флагов [D3DXSHADER](d3dxshader-flags.md) и [D3DXFX](d3dxfx.md) . в противном случае *псркфиле* содержит двоичный результат, а только соблюдаются флаги D3DXFX. Компилятор Direct3D 10 HLSL теперь является значением по умолчанию. Дополнительные сведения см. в разделе [средство компилятора Effect](../direct3dtools/fxc.md) .

</dd> <dt>

*ппул* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECTPOOL**](id3dxeffectpool.md)**

Указатель на объект [**ID3DXEffectPool**](id3dxeffectpool.md) , используемый для общих параметров. Если это значение равно **null**, общий доступ к параметрам не предоставляется.

</dd> <dt>

*ппеффект* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***

Возвращает указатель на буфер, содержащий скомпилированный результат. См. [**ID3DXEffect**](id3dxeffect.md).

</dd> <dt>

*ппкомпилатионеррорс* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Возвращает указатель на буфер, содержащий список ошибок компиляции. См. [**ID3DXBuffer**](id3dxbuffer.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Комментарии

Эта функция является расширенной версией [**D3DXCreateEffectFromFile**](d3dxcreateeffectfromfile.md) , позволяющей приложению указывать, какие константы эффектов будут управляться приложением. Константа, управляемая приложением, игнорируется системой эффектов. Это значит, что приложение отвечает за инициализацию константы, а также сохранение и восстановление состояния при необходимости.

Эта функция проверяет каждую константу в Пскипконстантс, чтобы увидеть, что:

-   Он привязан к регистру констант.
-   Он используется только в коде шейдера HLSL.

Если константа имеет имя в строке, которая отсутствует в результате, она игнорируется.

Если для параметров компилятора требуется Юникод, тип данных LPCTSTR разрешается в ЛПКВСТР. В противном случае тип данных LPCTSTR разрешается в LPCSTR.

Параметр компилятора также определяет версию функции. Если определен Юникод, вызов функции разрешается в D3DXCreateEffectFromFileW. В противном случае вызов функции разрешается в D3DXCreateEffectFromFileA, так как используются строки ANSI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции эффектов](dx9-graphics-reference-effects-functions.md)
</dt> <dt>

[**D3DXCreateEffectEx**](d3dxcreateeffectex.md)
</dt> <dt>

[**D3DXCreateEffectFromResourceEx**](d3dxcreateeffectfromresourceex.md)
</dt> </dl>

 

 
