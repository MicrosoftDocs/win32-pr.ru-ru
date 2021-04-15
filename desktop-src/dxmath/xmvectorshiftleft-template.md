---
description: Сдвигает вектор влево на заданное число 32-разрядных элементов, заполняя освобождаемые элементы элементами из второго вектора.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Шаблон Ксмвекторшифтлефт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 115604871d9e8402157a82bf3c420e5762b3a424
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648806"
---
# <a name="xmvectorshiftleft-template"></a>Шаблон Ксмвекторшифтлефт

Сдвигает вектор влево на заданное число 32-разрядных элементов, заполняя освобождаемые элементы элементами из второго вектора.

## <a name="syntax"></a>Синтаксис

``` syntax
template<uint32_t Elements> XMVECTOR XMVectorShiftLeft(
  [in]  XMVECTOR V1,
  [in]  XMVECTOR V2
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="V1"></span><span id="v1"></span>*ADO.NET*
</dt> <dd>

\[\]для сдвига влево в векторе.

</dd> <dt>

<span id="V2"></span><span id="v2"></span>*Шаблон*
</dt> <dd>

\[\]вектор, используемый для заполнения освобожденных компонентов v1 после сдвига влево.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает перемещенный и заполненный [**ксмвектор**](xmvector-data-type.md).

## <a name="remarks"></a>Комментарии

Эта функция является версией шаблона [**ксмвекторшифтлефт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) , в которой аргумент *Elements* является значением шаблона.

> [!Note]  
> `XMVectorShiftLeft`Шаблон является новым для директксмас и недоступен для кснамас 2. x.

 

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

[**ксмвекторротателефт**](xmvectorrotateleft-template.md)
</dt> <dt>

[**ксмвекторротатеригхт**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
