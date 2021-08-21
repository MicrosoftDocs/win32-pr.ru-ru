---
title: Метод ID3DX11EffectMatrixVariable Жетматрикстранспосеаррай (D3dx11effect. h)
description: Переставить и получить массив матриц с плавающей запятой.
ms.assetid: cfcdbda0-b321-4e94-8d09-bb9d7ddfb4a5
keywords:
- Метод Жетматрикстранспосеаррай Direct3D 11
- Метод Жетматрикстранспосеаррай Direct3D 11, интерфейс ID3DX11EffectMatrixVariable
- Интерфейс ID3DX11EffectMatrixVariable Direct3D 11, метод Жетматрикстранспосеаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable.GetMatrixTransposeArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07ba32807b4acdd4f244b7b4c3cc82b3941cb5a52d899f1e8361c841b58d53ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119046172"
---
# <a name="id3dx11effectmatrixvariablegetmatrixtransposearray-method"></a>Метод ID3DX11EffectMatrixVariable:: Жетматрикстранспосеаррай

Переставить и получить массив матриц с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetMatrixTransposeArray(
   float *pData,
   UINT  Offset,
   UINT  Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* 
</dt> <dd>

Тип: **float \***

Указатель на первый элемент массива матриц транпосед.

</dd> <dt>

*Offset* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Смещение (в количестве матриц) между началом массива и первой матрицей, которую необходимо получить.

</dd> <dt>

*Количество* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число матриц в массиве, которые необходимо получить.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Возвращает один из следующих [кодов возврата Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Remarks

При перестановке матрицы порядок данных переупорядочивается из порядка строк в столбец в порядке строк (или наоборот).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectMatrixVariable](id3dx11effectmatrixvariable.md)
</dt> </dl>

 

