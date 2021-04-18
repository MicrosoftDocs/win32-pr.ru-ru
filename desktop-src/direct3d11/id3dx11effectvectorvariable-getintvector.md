---
title: Метод ID3DX11EffectVectorVariable Жетинтвектор (D3dx11effect. h)
description: Получение вектора из четырех компонентов, содержащего целочисленные данные.
ms.assetid: 27c75cfb-7c6f-43f4-9489-186006a60203
keywords:
- Метод Жетинтвектор Direct3D 11
- Метод Жетинтвектор Direct3D 11, интерфейс ID3DX11EffectVectorVariable
- Интерфейс ID3DX11EffectVectorVariable Direct3D 11, метод Жетинтвектор
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable.GetIntVector
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e661ecce642cae4cf94a1bc35f92dc1afad16a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104548039"
---
# <a name="id3dx11effectvectorvariablegetintvector-method"></a>Метод ID3DX11EffectVectorVariable:: Жетинтвектор

Получение вектора из четырех компонентов, содержащего целочисленные данные.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIntVector(
   int *pData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* 
</dt> <dd>

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

Указатель на первый компонент.

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

[ID3DX11EffectVectorVariable](id3dx11effectvectorvariable.md)
</dt> </dl>

 

