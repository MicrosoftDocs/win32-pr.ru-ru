---
description: Поворачивает вектор влево на заданное число 32-разрядных элементов.
ms.assetid: ba3698ed-212d-4ef0-846a-4099d0e1abec
title: Шаблон Ксмвекторротателефт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb3d2a06f775e99b275d7333816307f494c5b2a4a7cc0183eaddc4ee4cd8950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499407"
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

## <a name="remarks"></a>Remarks

Эта функция является версией шаблона [**ксмвекторротателефт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft) , в которой аргумент *Elements* является значением шаблона.

> [!Note]  
> `XMVectorRotateLeft`Шаблон является новым для директксмас и недоступен для кснамас 2. x.

 

**Пространство имен**. Использование DirectX

### <a name="platform-requirements"></a>Требования к платформе

Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8. поддерживается для классических приложений Win32, приложений для магазина Windows и Windows Phone 8 приложений.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Директксмас. h</dt> </dl> |



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

 

 
