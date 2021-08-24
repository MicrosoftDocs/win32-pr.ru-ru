---
title: Метод ID3DX11EffectScalarVariable Жетинтаррай (D3dx11effect. h)
description: Получение массива целочисленных переменных.
ms.assetid: 6db0d5f8-9b15-4149-a80d-1145d5839e93
keywords:
- Метод Жетинтаррай Direct3D 11
- Метод Жетинтаррай Direct3D 11, интерфейс ID3DX11EffectScalarVariable
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, метод Жетинтаррай
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable.GetIntArray
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fe6d774aa553f4748a1918694951541bcc6ee6f5e75a6dede4b7ef173ed2b3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119377594"
---
# <a name="id3dx11effectscalarvariablegetintarray-method"></a>Метод ID3DX11EffectScalarVariable:: Жетинтаррай

Получение массива целочисленных переменных.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetIntArray(
   int  *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pData* 
</dt> <dd>

Тип: **[ **int**](/windows/desktop/WinProg/windows-data-types)\***

Указатель на начало данных, которые необходимо задать.

</dd> <dt>

*Offset* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Необходимо задать значение 0; это зарезервировано для будущего использования.

</dd> <dt>

*Количество* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Число заданных элементов массива.

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

 

