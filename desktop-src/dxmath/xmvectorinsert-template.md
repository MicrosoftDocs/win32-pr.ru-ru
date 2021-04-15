---
description: Поворачивает вектор влево на заданное число 32-разрядных компонентов и вставляет выбранные элементы этого результата в другой вектор.
ms.assetid: m:microsoft.directx_sdk.template.xmvectorinsert(xmvector,xmvector)
title: Шаблон Ксмвекторинсерт (Директксмас. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3250ad52ab19a127b110b02ecf71543f44708681
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648812"
---
# <a name="xmvectorinsert-template"></a>Шаблон Ксмвекторинсерт

Поворачивает вектор влево на заданное число 32-разрядных компонентов и вставляет выбранные элементы этого результата в другой вектор.

## <a name="syntax"></a>Синтаксис

``` syntax
template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3> XMVECTOR XMVectorInsert(
  [in]  XMVECTOR VD,
  [in]  XMVECTOR VS
);
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="VD"></span><span id="vd"></span>*VD*
</dt> <dd>

\[в \] vector для вставки в.

</dd> <dt>

<span id="VS"></span><span id="vs"></span>*ЛИНЕЙЧАТ*
</dt> <dd>

\[\]для поворота влево в векторе.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает [**ксмвектор**](xmvector-data-type.md) , полученное в результате вращения и вставки.

## <a name="remarks"></a>Комментарии

Эта функция является версией шаблона [**ксмвекторинсерт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) , в которой аргументы *SELECT \** являются значениями шаблона.

Для лучшей производительности результат `XMVectorInsert` должен быть назначен обратно в *VD*.

> [!Note]  
> `XMVectorInsert`Шаблон является новым для директксмас и недоступен для кснамас 2. x.

 

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
</dt> <dt>

[**ксмвекторшифтлефт**](xmvectorshiftleft-template.md)
</dt> </dl>

 

 
