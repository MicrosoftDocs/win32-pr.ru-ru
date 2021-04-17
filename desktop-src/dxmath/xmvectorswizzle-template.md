---
description: Свиззлес вектор.
ms.assetid: 75608e80-5911-45a8-beca-ceac1f4d2c1c
title: Шаблон Ксмвекторсвиззле (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8e872d76f3251eccc8616c143c645b388e2dca4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708590"
---
# <a name="xmvectorswizzle-template"></a>Шаблон Ксмвекторсвиззле

Свиззлес вектор.

## <a name="syntax"></a>Синтаксис

``` syntax
template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW> XMVECTOR XMVectorSwizzle(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="V"></span><span id="v"></span>*3,3*
</dt> <dd>

\[в \] vector to свиззле.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает свиззлед [**ксмвектор**](xmvector-data-type.md).

## <a name="remarks"></a>Комментарии

Эта функция является версией шаблона [**ксмвекторсвиззле**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) , где аргументы *свиззле \** являются значениями шаблона.

`XM_SWIZZLE_X`, `XM_SWIZZLE_Y` , `XM_SWIZZLE_Z` и `XM_SWIZZLE_W` — константы, которые возвращают 0, 1, 2 и 3 соответственно для использования с `XMVectorSwizzle` . Это идентично `XM_PERMUTE_0X` , `XM_PERMUTE_0Y` , `XM_PERMUTE_0Z` и `XM_PERMUTE_0W` .

> [!Note]  
> `XMVectorSwizzle`Шаблон является новым для директксмас и недоступен для кснамас 2. x.

 

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

[**ксмвекторпермуте**](xmvectorpermute-template.md)
</dt> </dl>

 

 
