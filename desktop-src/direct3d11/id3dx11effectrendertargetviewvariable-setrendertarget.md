---
title: Метод ID3DX11EffectRenderTargetViewVariable Сетрендертаржет (D3dx11effect. h)
description: Задайте целевой объект рендеринга.
ms.assetid: caac7190-4f58-4a8e-9764-b6120ac14856
keywords:
- Метод Сетрендертаржет Direct3D 11
- Метод Сетрендертаржет Direct3D 11, интерфейс ID3DX11EffectRenderTargetViewVariable
- Интерфейс ID3DX11EffectRenderTargetViewVariable Direct3D 11, метод Сетрендертаржет
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable.SetRenderTarget
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb53f0dff19fcd8990575dc9b305b0fb2f7e149b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914827"
---
# <a name="id3dx11effectrendertargetviewvariablesetrendertarget-method"></a>Метод ID3DX11EffectRenderTargetViewVariable:: Сетрендертаржет

Задайте целевой объект рендеринга.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetRenderTarget(
   ID3D11RenderTargetView *pResource
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*исходный код* 
</dt> <dd>

Тип: **[ **ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview)\***

Указатель на интерфейс представления, предназначенный для визуализации. См. [**ID3D11RenderTargetView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11rendertargetview).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Примечания

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectRenderTargetViewVariable](id3dx11effectrendertargetviewvariable.md)
</dt> </dl>

 

 





