---
title: Функция D3DX11SHProjectCubeMap (D3DX11tex. h)
description: Обратите внимание, что библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows. Примечание. вместо использования этой функции рекомендуется использовать математическую библиотеку "сферические гармонические колебания", Шпрожекткубемап.
ms.assetid: 58c741a3-dd5d-4b18-b257-5e85a9b799fd
keywords:
- D3DX11SHProjectCubeMap функция Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11SHProjectCubeMap
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf773c00a649e6ace065fcf552358fbf5eeb19c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998495"
---
# <a name="d3dx11shprojectcubemap-function"></a>Функция D3DX11SHProjectCubeMap

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8 и не поддерживается для приложений Магазина Windows.

 

> [!Note]  
> Вместо использования этой функции рекомендуется использовать [математическую библиотеку "сферические гармонические колебания](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) ", **шпрожекткубемап**.

 

Проецирует функцию, представленную в сопоставлении кубов, в сферические гармонические колебания.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DX11SHProjectCubeMap(
   ID3D11DeviceContext *pContext,
   UINT                Order,
   ID3D11Texture2D     *pCubeMap,
   FLOAT               *pROut,
   FLOAT               *pGOut,
   FLOAT               *pBOut
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pContext* 
</dt> <dd>

Тип: **[ **ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Указатель на объект [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

</dd> <dt>

*Заказ* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

В порядке вычисления SH формирует коэффициенты в заказе ^ 2, степень которых — Order-1. Допустимый диапазон: от 2 до 6.

</dd> <dt>

*пкубемап* 
</dt> <dd>

Тип: **[ **ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)\***

Указатель на [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) , представляющий кубической карты, который планируется спроецировать на сферические гармонические колебания.

</dd> <dt>

*праут* 
</dt> <dd>

Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Выходной вектор SH для Red.

</dd> <dt>

*пгаут* 
</dt> <dd>

Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Выходной вектор SH для зеленого цвета.

</dd> <dt>

*пбаут* 
</dt> <dd>

Тип: **[ **float**](/windows/desktop/WinProg/windows-data-types)\***

Выходной вектор SH для синего.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращаемое значение является одним из значений, перечисленных в [кодах возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3DX11. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции D3DX](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

