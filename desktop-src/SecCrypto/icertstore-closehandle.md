---
description: Закрывает обработчик ХЦЕРТСТОРЕ, полученный через свойство Сторехандле.
ms.assetid: 1b0d3d9b-09e0-4035-88ac-2887b3ab60c9
title: 'Метод Ицертсторе:: CloseHandle'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ICertStore.CloseHandle
- CertStore.CloseHandle
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bb1e9ab032b76b8ef02de786d1fc39af0b0d54b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669519"
---
# <a name="icertstoreclosehandle-method"></a>Метод Ицертсторе:: CloseHandle

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP.\]

Метод **CloseHandle** закрывает обработчик хцертсторе, полученный через свойство [**сторехандле**](icertstore-storehandle.md) .

## <a name="syntax"></a>Синтаксис


```VB
CertStore.CloseHandle( _
  ByVal hCertStore _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хцертсторе* \[ окне\]
</dt> <dd>

Закрываемый обработчик ХЦЕРТСТОРЕ.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращаемое значение является значением **HRESULT**. Значение **S \_ ОК** указывает на успешное выполнение. Любое другое значение указывает на сбой операции.

## <a name="remarks"></a>Комментарии

Этот метод не освобождает обработчик ХЦЕРТСТОРЕ, содержащийся в объекте [**Store**](store.md) . Он должен использоваться только для освобождения обработчика ХЦЕРТСТОРЕ, полученного через свойство [**сторехандле**](icertstore-storehandle.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ицертсторе**](icertstore.md)
</dt> </dl>

 

 




