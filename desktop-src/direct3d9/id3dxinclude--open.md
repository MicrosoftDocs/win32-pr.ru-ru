---
description: Реализованный пользователем метод для открытия и чтения содержимого \# включаемого файла шейдера.
ms.assetid: ad0105f7-042d-4e96-ad4a-1ece08e519af
title: 'Метод ID3DXInclude:: Open (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Open
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 313b3f4845f9a46f758a40b6b315cc5b5eeecb29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694300"
---
# <a name="id3dxincludeopen-method"></a>Метод ID3DXInclude:: Open

Реализованный пользователем метод для открытия и чтения содержимого \# включаемого файла шейдера.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Open(
  [in]  D3DXINCLUDE_TYPE IncludeType,
  [in]  LPCSTR           pFileName,
  [in]  LPCVOID          pParentData,
  [out] LPCVOID          *ppData,
  [out] UINT             *pBytes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Инклудетипе* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXINCLUDE \_ тип**](./d3dxinclude-type.md)**

Расположение \# включаемого файла. См. раздел [**\_ тип D3DXINCLUDE**](./d3dxinclude-type.md).

</dd> <dt>

*пфиленаме* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Имя \# включаемого файла.

</dd> <dt>

*ппарентдата* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на контейнер, содержащий \# включаемый файл. Компилятор может передать значение NULL в *ппарентдата*. Дополнительные сведения см. в подразделе "Поиск включаемых файлов" статьи [Компиляция влияния (Direct3D 11)](../direct3d11/d3d11-graphics-programming-guide-effects-compile.md).

</dd> <dt>

*ппдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)\***

Указатель на возвращаемый буфер, содержащий директивы include. Этот указатель остается действительным до вызова [**ID3DXInclude:: Close**](id3dxinclude--close.md) .

</dd> <dt>

*пбитес* \[ заполняет\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)\***

Число байтов, возвращенных в Ппдата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Метод, реализуемый пользователем, должен возвращать значение S \_ ОК. Если при чтении включаемого файла происходит сбой обратного вызова \# , то API-интерфейс, который вызвал вызов функции обратного вызова, завершится ошибкой. Возможны следующие варианты.

-   Шейдер HLSL не сможет выполнить одну из \* \* \* функций D3DXCompileShader.
-   Шейдер сборки завершится ошибкой одной из \* \* \* функций D3DXAssembleShader.
-   Этот результат приведет к сбою одной из \* \* \* функций D3DXCreateEffect или D3DXCreateEffectCompiler \* \* \* .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: Close**](id3dxinclude--close.md)
</dt> </dl>

 

 
