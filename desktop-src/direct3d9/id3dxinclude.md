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
ms.openlocfilehash: d4b0a34eb5b4c3ab20a57a5089de1d6d1ebbdf51
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703985"
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



 

## <a name="remarks"></a>Комментарии

Пользователь создает интерфейс ID3DXInclude, реализуя класс, производный от этого интерфейса, и реализуя все методы интерфейса.

Тип LPD3DXINCLUDE определяется как указатель на этот интерфейс.


```
typedef interface ID3DXInclude ID3DXInclude;
typedef interface ID3DXInclude *LPD3DXINCLUDE;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы эффектов](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
