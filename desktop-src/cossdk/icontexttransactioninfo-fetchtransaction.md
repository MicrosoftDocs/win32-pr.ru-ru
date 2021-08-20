---
description: Возвращает учетную запись-посредник транзакции или транзакции, связанную с текущим контекстом, если таковая имеется.
ms.assetid: 2f85f395-3ec5-4c5a-a6db-c902cb8f8486
title: 'Метод Иконтексттрансактионинфо:: Фетчтрансактион'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextTransactionInfo.FetchTransaction
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6d673483118feb02ec2f1172640b9972d883505f48bc1fd8d8803844b963b02b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991064"
---
# <a name="icontexttransactioninfofetchtransaction-method"></a>Метод Иконтексттрансактионинфо:: Фетчтрансактион

Возвращает учетную запись-посредник транзакции или транзакции, связанную с текущим контекстом, если таковая имеется.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT FetchTransaction(
  [out, retval] IUnknown **pUnk
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Punk* \[ out, retval\]
</dt> <dd>

Транзакция или прокси транзакции, связанные с текущим контекстом; в противном случае **значение NULL**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод может возвращать стандартные возвращаемые значения E \_ INVALIDARG, e \_ OUTOFMEMORY, e \_ непредвиденные и S \_ ОК.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>          |
| Минимальная версия сервера<br/> | Windows Только для настольных приложений сервера 2003 с пакетом обновления 1 \[\]<br/> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтексттрансактионинфо**](icontexttransactioninfo.md)
</dt> </dl>

 

 




