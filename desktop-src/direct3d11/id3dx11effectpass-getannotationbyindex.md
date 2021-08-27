---
title: Метод ID3DX11EffectPass Жетаннотатионбиндекс (D3dx11effect. h)
description: Получение заметки по индексу. | Метод ID3DX11EffectPass Жетаннотатионбиндекс (D3dx11effect. h)
ms.assetid: 734eeeca-58c2-4f0c-84d1-2898394a03d6
keywords:
- Метод Жетаннотатионбиндекс Direct3D 11
- Метод Жетаннотатионбиндекс Direct3D 11, интерфейс ID3DX11EffectPass
- Интерфейс ID3DX11EffectPass Direct3D 11, метод Жетаннотатионбиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.GetAnnotationByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50cb2f1df512f8726874896b7cb7c2948b6dd33b672a66f7670b75d5520cb6af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046042"
---
# <a name="id3dx11effectpassgetannotationbyindex-method"></a>Метод ID3DX11EffectPass:: Жетаннотатионбиндекс

Получение заметки по индексу.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectVariable* GetAnnotationByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Отсчитываемый с нуля индекс.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Remarks

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectPass](id3dx11effectpass.md)
</dt> </dl>

 

