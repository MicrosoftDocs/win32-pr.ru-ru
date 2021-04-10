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
ms.openlocfilehash: 0e753974f93539f051465f13a1ea92d7e0e3bfa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141824"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>          |
| Минимальная версия сервера<br/> | Только для настольных приложений Windows Server 2003 с пакетом обновления 1 \[\]<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иконтексттрансактионинфо**](icontexttransactioninfo.md)
</dt> </dl>

 

 




