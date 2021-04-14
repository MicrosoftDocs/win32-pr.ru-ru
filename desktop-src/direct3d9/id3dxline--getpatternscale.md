---
description: Возвращает значение масштаба стиппле-pattern.
ms.assetid: cf80ae8c-493d-4f35-b4f9-5981e64cc842
title: 'Метод ID3DXLine:: Жетпаттернскале (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.GetPatternScale
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 14a9919ede81eb64b844e1882725e37359ad6738
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424530"
---
# <a name="id3dxlinegetpatternscale-method"></a>Метод ID3DXLine:: Жетпаттернскале

Возвращает значение масштаба стиппле-pattern.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT GetPatternScale();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Возвращает значение, используемое для масштабирования шаблона стиппле. 1.0 f является значением по умолчанию и не представляет масштабирование. Значение меньше 1,0 f сжимает шаблон, а значение, превышающее 1,0, растягивает шаблон.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> <dt>

[**ID3DXLine:: Сетпаттернскале**](id3dxline--setpatternscale.md)
</dt> </dl>

 

 
