---
title: Метод ID3DX11EffectVariable Жетмембербисемантик (D3dx11effect. h)
description: Получение члена структуры по семантике.
ms.assetid: e4ae1f6a-43d2-45df-9dba-833d4f767818
keywords:
- Метод Жетмембербисемантик Direct3D 11
- Метод Жетмембербисемантик Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Жетмембербисемантик
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberBySemantic
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46155fc961836b187e0a12ab3571a4edcb67740c7e4dd26fb92350009b95edef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045822"
---
# <a name="id3dx11effectvariablegetmemberbysemantic-method"></a>Метод ID3DX11EffectVariable:: Жетмембербисемантик

Получение члена структуры по семантике.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectVariable* GetMemberBySemantic(
   LPCSTR Semantic
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Семантическ* 
</dt> <dd>

Тип: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

Семантика.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Указатель на [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Remarks

Если переменная действия является структурой, используйте этот метод для поиска члена по присоединенной семантике.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

