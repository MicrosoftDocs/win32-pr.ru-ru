---
title: Метод ID3DX11EffectRasterizerVariable Ундосетрастеризерстате (D3dx11effect. h)
description: Возвращает ранее установленное состояние средства отображения программной прорисовки.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Метод Ундосетрастеризерстате Direct3D 11
- Метод Ундосетрастеризерстате Direct3D 11, интерфейс ID3DX11EffectRasterizerVariable
- Интерфейс ID3DX11EffectRasterizerVariable Direct3D 11, метод Ундосетрастеризерстате
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273979"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a>Метод ID3DX11EffectRasterizerVariable:: Ундосетрастеризерстате

Возвращает ранее установленное состояние средства отображения программной прорисовки.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Index* 
</dt> <dd>

Тип: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Индексировать в массив интерфейсов средства прорисовки. Если имеется только один интерфейс, используйте значение 0.

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

[ID3DX11EffectRasterizerVariable](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

