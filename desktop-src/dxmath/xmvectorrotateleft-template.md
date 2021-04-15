---
description: Поворачивает вектор влево на заданное число 32-разрядных элементов.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Шаблон Ксмвекторротателефт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e5b52fccebeb93803fdc33346fa4ee5e873c1d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648810"
---
# <a name="xmvectorrotateleft-template"></a>Шаблон Ксмвекторротателефт

Поворачивает вектор влево на заданное число 32-разрядных элементов.

## <a name="syntax"></a>Синтаксис

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorRotateLeft(
  [in]  XMVECTOR V
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="V"></span><span id="v"></span>*3,3*
</dt> <dd>

\[\]для поворота влево в векторе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает повернутое [**ксмвектор**](xmvector-data-type.md).

## <a name="remarks"></a>Комментарии

Эта функция является версией шаблона [**ксмвекторротателефт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) , в которой аргумент *Elements* является значением шаблона.

> [!Note]  
> `XMVectorRotateLeft`Шаблон является новым для директксмас и недоступен для кснамас 2. x.

 

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
</dt> <dt>

[**ксмвекторротатеригхт**](xmvectorrotateright-template.md)
</dt> <dt>

[**ксмвекторшифтлефт**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
