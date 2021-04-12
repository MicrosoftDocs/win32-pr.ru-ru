---
description: Освобождает ресурсы, используемые интерфейсом Иеаксисервице.
ms.assetid: 11f5cfdc-dcdd-4b41-b02c-b19b9452509e
title: 'Метод Иеаксисервице:: Cleanup'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IeAxiService.Cleanup
api_type:
- COM
api_location: ''
ms.openlocfilehash: b29784ae360ec78b9f7e01d2045617615333a5c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265643"
---
# <a name="ieaxiservicecleanup-method"></a>Метод Иеаксисервице:: Cleanup

Метод **Cleanup** освобождает ресурсы, используемые интерфейсом [**иеаксисервице**](ieaxiservice.md) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Cleanup();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](/windows/desktop/SecCrypto/common-hresult-values).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista Business, Windows Vista Корпоративная, только для \[ настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |
| IID<br/>                      | IID \_ иеаксисервице определен как E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**иеаксисервице**](ieaxiservice.md)
</dt> </dl>

 

