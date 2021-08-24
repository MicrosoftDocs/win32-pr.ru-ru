---
title: ID3DX11EffectScalarVariable-метод с плавающей запятой (D3dx11effect. h)
description: Получение переменной с плавающей запятой.
ms.assetid: 0416db40-5e70-44e4-905f-86f49a9b58b8
keywords:
- Метод с + + Direct3D 11
- Метод с плавающей запятой Direct3D 11, интерфейс ID3DX11EffectScalarVariable
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, метод с плавающей запятой
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetFloat
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f00e5f4863b54a208b1b9f9b32e4292c274575271e447c3ac20e7b09a686ace
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952724"
---
# <a name="id3dx11effectscalarvariablegetfloat-method"></a>Метод ID3DX11EffectScalarVariable:: с плавающей запятой

Получение переменной с плавающей запятой.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetFloat(
   float *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pValue* 
</dt> <dd>

Тип: **float \***

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



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectScalarVariable](id3dx11effectscalarvariable.md)
</dt> </dl>

 

 





