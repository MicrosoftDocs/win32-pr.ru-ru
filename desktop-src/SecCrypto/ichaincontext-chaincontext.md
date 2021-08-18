---
description: Задает или получает \_ контекст цепочки пкцерт \_ сертификата.
ms.assetid: 1b33ecd5-88c9-4654-9d2d-95a0be4283c6
title: 'Свойство Ичаинконтекст:: Чаинконтекст'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChainContext.ChainContext
- IChainContext.get_ChainContext
- IChainContext.put_ChainContext
- ChainContext.ChainContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d5e7bc92aa798766538af19cae440542705a859040aed7fc8d9510e3724051f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005502"
---
# <a name="ichaincontextchaincontext-property"></a>Свойство Ичаинконтекст:: Чаинконтекст

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]

Свойство **чаинконтекст** задает или получает \_ контекст цепочки пкцерт \_ сертификата.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
' Data type: Long

ChainContext.ChainContext As Long
```



## <a name="property-value"></a>Значение свойства

\_Контекст цепочки пкцерт \_ сертификата.

## <a name="error-codes"></a>Коды ошибок

Если методы доступа к свойству **помещают \_ чаинконтекст** и **Get \_ Чаинконтекст** , они возвращают S \_ ОК.

Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="remarks"></a>Remarks

Чтобы освободить контекст, необходимо вызвать метод [**фриконтекст**](ichaincontext-freecontext.md) или функцию [**цертфрицертификатечаин**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain) .

Если задано свойство **чаинконтекст** , то состояние всего объекта [**цепочки**](chain.md) сбрасывается.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ичаинконтекст**](ichaincontext.md)
</dt> </dl>

 

 




