---
description: ID3DXInclude — это реализованный пользователем интерфейс, обеспечивающий обратные вызовы для \# директив include во время компиляции шейдера.
ms.assetid: 8e0bfff1-8d6d-4381-b9fd-f5f64f854712
title: Интерфейс ID3DXInclude (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e48ab32894ad1bf4c2f992ab4fff5953b3d98de4afd5e044de0119e056ee8133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118295184"
---
# <a name="id3dxinclude-interface"></a>Интерфейс ID3DXInclude

ID3DXInclude — это реализованный пользователем интерфейс, обеспечивающий обратные вызовы для \# директив include во время компиляции шейдера. Каждый из методов этого интерфейса должен быть реализован пользователем, который затем будет использоваться в качестве обратных вызовов приложения при возникновении одного из следующих условий:

-   Шейдер HLSL, содержащий \# include, компилируется путем вызова одной из \* \* \* функций D3DXCompileShader.
-   Включение шейдера сборки \# осуществляется путем вызова любой из \* \* \* функций D3DXAssembleShader.
-   Результат, содержащий include, \# компилируется путем вызова любой из \* \* \* функций D3DXCreateEffect или D3DXCreateEffectCompiler \* \* \* .

## <a name="members"></a>Элементы

Интерфейс **ID3DXInclude** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXInclude** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXInclude** содержит следующие методы.



| Метод                               | Описание                                                                                           |
|:-------------------------------------|:------------------------------------------------------------------------------------------------------|
| [**Закрыть**](id3dxinclude--close.md) | Реализованный пользователем метод для закрытия файла включения шейдера \# .<br/>                             |
| [**Открыт**](id3dxinclude--open.md)   | Реализованный пользователем метод для открытия и чтения содержимого \# включаемого файла шейдера.<br/> |



 

## <a name="remarks"></a>Remarks

Пользователь создает интерфейс ID3DXInclude, реализуя класс, производный от этого интерфейса, и реализуя все методы интерфейса.

Тип LPD3DXINCLUDE определяется как указатель на этот интерфейс.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы эффектов](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
