---
description: Сдвигает вектор влево на заданное число 32-разрядных элементов, заполняя освобождаемые элементы элементами из второго вектора.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorshiftleft(xmvector,xmvector)
title: Шаблон Ксмвекторшифтлефт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab92e2fb64a101251a7531ca1d96b8b06f3e9af6e2b7dabe7958673a61bd8c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118499283"
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

## <a name="remarks"></a>Remarks

Эта функция является версией шаблона [**ксмвекторшифтлефт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) , в которой аргумент *Elements* является значением шаблона.

> [!Note]  
> `XMVectorShiftLeft`Шаблон является новым для директксмас и недоступен для кснамас 2. x.

 

**Пространство имен**. Использование DirectX

### <a name="platform-requirements"></a>Требования к платформе

Microsoft Visual Studio 2010 или Microsoft Visual Studio 2012 с Windows SDK для Windows 8. поддерживается для классических приложений Win32, приложений для магазина Windows и Windows Phone 8 приложений.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Директксмас. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Функции шаблона библиотеки Директксмас](ovw-xnamath-templates.md)
</dt> <dt>

[**ксмвекторпермуте**](xmvectorpermute-template.md)
</dt> <dt>

[**ксмвекторротателефт**](xmvectorrotateleft-template.md)
</dt> <dt>

[**ксмвекторротатеригхт**](xmvectorrotateright-template.md)
</dt> </dl>

 

 
