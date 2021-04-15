---
description: Пермутес компоненты двух векторов для создания нового вектора.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorpermute(xmvector,xmvector)
title: Шаблон Ксмвекторпермуте (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37271cbb165f1e9c1769ef3a55e47f1e07310a81
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649094"
---
# <a name="xmvectorpermute-template"></a>Шаблон Ксмвекторпермуте

Пермутес компоненты двух векторов для создания нового вектора.

## <a name="syntax"></a>Синтаксис

``` syntax
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW> XMVECTOR XMVectorPermute(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*ADO.NET*
</dt> <dd>

\[в \] первом векторе.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*Шаблон*
</dt> <dd>

\[во \] втором векторе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает вектор переставляются, который привел к объединению исходных векторов.

## <a name="remarks"></a>Комментарии

Если все 4 индекса ссылаются только на один вектор (т. е. все они находятся в диапазоне 0-3 или все в диапазоне 4-7), используйте [**ксмвекторсвиззле**](xmvectorswizzle-template.md) вместо этого для повышения производительности.

Обратите внимание, что библиотека использует специализации шаблонов на некоторых платформах для повышения производительности. Не все возможные зеркальные варианты реализованы в этих особых случаях, поэтому предпочтительнее пермутес, где элемент X результирующего вектора берется из параметра v1, а не параметра v2. Например, предпочтительно использовать `XMVectorPermute<0,1,4,5>(A,B);` для `XMVectorPermute(4,5,0,1)(B,A);` .

Эта функция является версией шаблона [**ксмвекторпермуте**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) , где аргументы *переставляют \** являются значениями шаблона.

Константы [ \_ переставляют \_ XM](ovw-xnamath-reference-constants.md) предназначены для использования в качестве входных значений для *пермутекс*,*пермутэй*,*пермутез* и *пермутев*.

> [!Note]  
> `XMVectorPermute`Шаблон является новым для директксмас и недоступен для кснамас 2. x.

 

**Пространство имен**. Использование DirectX

### <a name="platform-requirements"></a>Требования к платформе

Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8. Поддерживается для классических приложений Win32, приложений для Магазина Windows и Windows Phone 8 приложений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Директксмас. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции шаблона библиотеки Директксмас](ovw-xnamath-templates.md)
</dt> <dt>

[**ксмвекторсвиззле**](xmvectorswizzle-template.md)
</dt> </dl>

 

 
