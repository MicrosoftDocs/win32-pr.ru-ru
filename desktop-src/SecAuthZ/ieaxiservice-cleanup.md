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
ms.openlocfilehash: de0413c39a4abf47a24913f347ceed0158d0b51aa4e1da0b3005cace1326b53f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119908384"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows vista Business, Windows vista Enterprise, \[ только для настольных приложений Windows Vista Ultimate\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                 |
| IID<br/>                      | IID \_ иеаксисервице определен как E9E92380-9ECD-4982-A0EB-6815A56CCF27<br/>                           |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иеаксисервице**](ieaxiservice.md)
</dt> </dl>

 

