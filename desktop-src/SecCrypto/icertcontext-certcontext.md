---
description: Задает или получает контекст ПКЦЕРТ \_ сертификата.
ms.assetid: aedd219d-43fa-4722-9af4-36172d2c18b0
title: 'Свойство Ицертконтекст:: Цертконтекст'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertContext.CertContext
- ICertContext.get_CertContext
- ICertContext.put_CertContext
- CertContext.CertContext
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5c517384bdffd8723c1e9e0d96683cc4bd4918361acdf19df77286bfbac962b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006372"
---
# <a name="icertcontextcertcontext-property"></a>Свойство Ицертконтекст:: Цертконтекст

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]

Свойство **цертконтекст** задает или получает \_ контекст пкцерт сертификата.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
CertContext.CertContext As Long
```



## <a name="property-value"></a>Значение свойства

Контекст ПКЦЕРТ \_ сертификата.

## <a name="error-codes"></a>Коды ошибок

Если методы доступа к свойству **помещают \_ цертконтекст** и **Get \_ Цертконтекст** , они возвращают S \_ ОК.

Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="remarks"></a>Remarks

Чтобы освободить контекст, необходимо вызвать метод [**фриконтекст**](icertcontext-freecontext.md) или функцию [**цертфрицертификатеконтекст**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext) .

Если задано свойство **цертконтекст** , состояние всего объекта [**сертификата**](certificate.md) сбрасывается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ицертконтекст**](icertcontext.md)
</dt> </dl>

 

 




