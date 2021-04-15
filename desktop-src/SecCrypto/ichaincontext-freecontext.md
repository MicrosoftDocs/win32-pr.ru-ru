---
description: Освобождает \_ контекст цепочки пкцерт, \_ полученный через свойство чаинконтекст.
ms.assetid: fa9a6171-58ff-400f-bdcc-ba32a0ae0441
title: 'Метод Ичаинконтекст:: Фриконтекст'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.FreeContext
- ChainContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 413b119f250bfbd061301391fee7741362979f65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688943"
---
# <a name="ichaincontextfreecontext-method"></a>Метод Ичаинконтекст:: Фриконтекст

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]

Метод **фриконтекст** освобождает \_ контекст цепочки пкцерт, \_ полученный через свойство [**чаинконтекст**](ichaincontext-chaincontext.md) .

## <a name="syntax"></a>Синтаксис


```VB
ChainContext.FreeContext()
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пчаинконтекст* \[ окне\]
</dt> <dd>

\_Освобождаемый контекст цепочки пкцерт \_ .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT**. Значение S \_ ОК указывает на успешное выполнение. Любое другое значение указывает на сбой операции.

## <a name="remarks"></a>Комментарии

Этот метод не освобождает \_ контекст цепочки пкцерт, \_ содержащийся в объекте [**цепочки**](chain.md) . Он должен использоваться только для освобождения \_ контекста цепочки пкцерт, \_ полученного через свойство [**чаинконтекст**](ichaincontext-chaincontext.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ичаинконтекст**](ichaincontext.md)
</dt> </dl>

 

 




