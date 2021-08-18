---
description: Освобождает контекст ПКЦЕРТ, \_ полученный через свойство цертконтекст.
ms.assetid: fcb9e885-d26c-4866-a35d-1c940bfe8162
title: 'Метод Ицертконтекст:: Фриконтекст'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.FreeContext
- CertContext.FreeContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06809d8950d62f1136b8efc25c8e5b4499e020dce956d65f9e0d4a0e349567de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006192"
---
# <a name="icertcontextfreecontext-method"></a>Метод Ицертконтекст:: Фриконтекст

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]

Метод **фриконтекст** освобождает контекст пкцерт, \_ полученный через свойство [**цертконтекст**](icertcontext-certcontext.md) .

## <a name="syntax"></a>Синтаксис


```VB
CertContext.FreeContext( _
  ByVal pCertContext _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пцертконтекст* \[ окне\]
</dt> <dd>

Контекст ПКЦЕРТ \_ для освобождения.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT**. Значение S \_ ОК указывает на успешное выполнение. Любое другое значение указывает на сбой операции.

## <a name="remarks"></a>Remarks

Этот метод не освобождает контекст ПКЦЕРТ, \_ содержащийся в объекте [**сертификата**](certificate.md) . Он должен использоваться только для освобождения контекста ПКЦЕРТ, \_ полученного через свойство [**цертконтекст**](icertcontext-certcontext.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ицертконтекст**](icertcontext.md)
</dt> </dl>

 

 




