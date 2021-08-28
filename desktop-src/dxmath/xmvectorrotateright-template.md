---
description: Поворачивает вектор вправо на заданное число 32-разрядных элементов.
ms.assetid: 7493c1fe-2c3d-4eb6-bec1-02c066a70b9f
title: Шаблон Ксмвекторротатеригхт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47017982af6bb61212129665010d403bd9db898c65056110c4d2f40a5f8a9362
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984494"
---
# <a name="xmvectorrotateright-template"></a>Шаблон Ксмвекторротатеригхт

Поворачивает вектор вправо на заданное число 32-разрядных элементов.

## <a name="syntax"></a>Синтаксис

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateRight(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="V"></span><span id="v"></span>*3,3*
</dt> <dd>

\[\]для поворота в векторе вправо.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает повернутое [**ксмвектор**](xmvector-data-type.md).

## <a name="remarks"></a>Remarks

Эта функция является версией шаблона [**ксмвекторротатеригхт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) , в которой аргумент *Elements* является значением шаблона.

> [!Note]  
> `XMVectorRotateRight`Шаблон является новым для директксмас и недоступен для кснамас 2. x.

 

**Пространство имен**. Использование DirectX

### <a name="platform-requirements"></a>Требования к платформе

Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8. поддерживается для классических приложений Win32, приложений для магазина Windows и Windows Phone 8 приложений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Директксмас. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции шаблона библиотеки Директксмас](ovw-xnamath-templates.md)
</dt> <dt>

[**ксмвекторпермуте**](xmvectorpermute-template.md)
</dt> <dt>

[**ксмвекторротателефт**](xmvectorrotateleft-template.md)
</dt> <dt>

[**ксмвекторшифтлефт**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
