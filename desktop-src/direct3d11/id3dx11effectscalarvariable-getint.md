---
title: Метод ID3DX11EffectScalarVariable GetInt (D3dx11effect. h)
description: Получение целочисленной переменной.
ms.assetid: 82a5a7a5-17cb-4e5e-ae4e-57c0ff9757c5
keywords:
- Метод GetInt Direct3D 11
- Метод GetInt Direct3D 11, интерфейс ID3DX11EffectScalarVariable
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, метод GetInt
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetInt
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7619fe4e0fd668e280efa094cc8b8d8d91b2b99f559612bfc6a7af09e08dab1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118534180"
---
# <a name="id3dx11effectscalarvariablegetint-method"></a>Метод ID3DX11EffectScalarVariable:: GetInt

Получение целочисленной переменной.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetInt(
   int *pValue
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pValue* 
</dt> <dd>

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

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

 

