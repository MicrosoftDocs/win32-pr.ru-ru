---
title: Метод ID3DX11EffectVariable Жетмембербиндекс (D3dx11effect. h)
description: Получение члена структуры по индексу.
ms.assetid: 256f65aa-5f49-4b83-8dde-ddb6b31c581a
keywords:
- Метод Жетмембербиндекс Direct3D 11
- Метод Жетмембербиндекс Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Жетмембербиндекс
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5176eb220dc928a98ec0f579afaeab1c81b1a7ff9ef3555736ed471bf15b9117
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124499"
---
# <a name="id3dx11effectvariablegetmemberbyindex-method"></a>Метод ID3DX11EffectVariable:: Жетмембербиндекс

Получение члена структуры по индексу.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectVariable* GetMemberByIndex(
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

Если переменная действия является структурой, используйте этот метод для поиска элемента по индексу.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

