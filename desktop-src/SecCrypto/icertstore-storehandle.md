---
description: Задает или получает маркер ХЦЕРТСТОРЕ хранилища сертификатов.
ms.assetid: 3ff8b4c7-4a9a-4cc1-b0ea-da442ebce157
title: 'Свойство Ицертсторе:: Сторехандле'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.StoreHandle
- ICertStore.get_StoreHandle
- ICertStore.put_StoreHandle
- CertStore.StoreHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2858e7484c82663b2ba6866d0f17b5528921619dbfa80cbb76ec0eabbb39a332
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005622"
---
# <a name="icertstorestorehandle-property"></a>Свойство Ицертсторе:: Сторехандле

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]

Свойство **сторехандле** задает или получает маркер хцертсторе хранилища сертификатов.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
CertStore.StoreHandle As Long
```



## <a name="property-value"></a>Значение свойства

ХЦЕРТСТОРЕный обработчик хранилища сертификатов.

## <a name="error-codes"></a>Коды ошибок

Если методы доступа к свойству **помещают \_ сторехандле** и **Get \_ Сторехандле** , они возвращают S \_ ОК.

Любое другое значение **HRESULT** указывает на сбой вызова.

## <a name="remarks"></a>Remarks

Чтобы освободить контекст, необходимо вызвать либо метод [**CloseHandle**](icertstore-closehandle.md) , либо функцию [**цертклосесторе**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore) .

Если задано свойство **сторехандле** , состояние всего объекта [**Store**](store.md) сбрасывается.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ицертсторе**](icertstore.md)
</dt> </dl>

 

 




