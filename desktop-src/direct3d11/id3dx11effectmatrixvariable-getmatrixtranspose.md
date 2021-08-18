---
title: Метод ID3DX11EffectMatrixVariable Жетматрикстранспосе (D3dx11effect. h)
description: Переставить и получить матрицу с плавающей точкой.
ms.assetid: a261128c-d1f9-4864-b562-5fe9a69c9969
keywords:
- Метод Жетматрикстранспосе Direct3D 11
- Метод Жетматрикстранспосе Direct3D 11, интерфейс ID3DX11EffectMatrixVariable
- Интерфейс ID3DX11EffectMatrixVariable Direct3D 11, метод Жетматрикстранспосе
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTranspose
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d2f04057dac5bc432cc3c6a9a3060654d8f6d181836823aa29f0a02f82f667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046182"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtranspose-method"></a>Метод ID3DX11EffectMatrixVariable:: Жетматрикстранспосе

Переставить и получить матрицу с плавающей точкой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMatrixTranspose(
   float *pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* 
</dt> <dd>

Тип: **float \***

Указатель на первый элемент трансобъектной матрицы.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

При перестановке матрицы порядок данных переупорядочивается из порядка строк в столбец в порядке строк (или наоборот).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

 





