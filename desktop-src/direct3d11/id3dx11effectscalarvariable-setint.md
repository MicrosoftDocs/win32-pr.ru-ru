---
title: Метод ID3DX11EffectScalarVariable SetInt (D3dx11effect. h)
description: Задайте целочисленную переменную.
ms.assetid: 614284be-8f70-4d7e-b797-b67e813615ab
keywords:
- Метод SetInt Direct3D 11
- Метод SetInt Direct3D 11, интерфейс ID3DX11EffectScalarVariable
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, метод SetInt
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.SetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 215083d35bfbdd67cd970bfe31b81a1e19594b2bf849e1c19692fa96af257036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119377544"
---
# <a name="id3dx11effectscalarvariablesetint-method"></a>Метод ID3DX11EffectScalarVariable:: SetInt

Задайте целочисленную переменную.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetInt(
   int Value
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Значение* 
</dt> <dd>

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)**

Указатель на переменную.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

