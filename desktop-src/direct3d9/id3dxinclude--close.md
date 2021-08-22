---
description: Реализованный пользователем метод для закрытия файла включения шейдера \# .
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'Метод ID3DXInclude:: Close (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 32df78aedcf4e7e229eec8c9648c82c86f6fea9f4c7176b8780cee67ccf49fcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987404"
---
# <a name="id3dxincludeclose-method"></a>Метод ID3DXInclude:: Close

Реализованный пользователем метод для закрытия файла включения шейдера \# .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* \[ окне\]
</dt> <dd>

Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**

Указатель на возвращаемый буфер, содержащий директивы include. Это указатель, возвращенный соответствующим вызовом [**ID3DXInclude:: Open**](id3dxinclude--open.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Метод, реализуемый пользователем, должен возвращать значение S \_ ОК. Если при чтении включаемого файла происходит сбой обратного вызова \# , то API-интерфейс, который вызвал вызов функции обратного вызова, завершится ошибкой. Возможны следующие варианты.

-   Шейдер HLSL не сможет выполнить одну из \* \* \* функций D3DXCompileShader.
-   Шейдер сборки завершится ошибкой одной из \* \* \* функций D3DXAssembleShader.
-   Этот результат приведет к сбою одной из \* \* \* функций D3DXCreateEffect или D3DXCreateEffectCompiler \* \* \* .

## <a name="remarks"></a>Remarks

Если [**ID3DXInclude:: Open**](id3dxinclude--open.md) завершился успешно, метод **ID3DXInclude:: Close** гарантированно будет вызываться до того, как интерфейс API, использующий этот интерфейс, возвратит значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: Open**](id3dxinclude--open.md)
</dt> </dl>

 

 
