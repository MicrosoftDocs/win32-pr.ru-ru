---
description: Возвращает число поставщиков криптографических служб (CSP).
ms.assetid: 7e0c1613-85ad-4f25-837e-d7b0f11e654a
title: 'Свойство Искрденр:: Кспкаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPCount
- ISCrdEnr.get_CSPCount
- SCrdEnr.CSPCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b2aea22db3c804ae4808996002b68efdcb6cf9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348515"
---
# <a name="iscrdenrcspcount-property"></a>Свойство Искрденр:: Кспкаунт

Свойство **кспкаунт** Извлекает число [*поставщиков криптографических служб*](../secgloss/c-gly.md) (CSP).

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT get_CSPCount(
   LONG *pVal
);
```



## <a name="property-value"></a>Значение свойства

Число CSP.

## <a name="error-codes"></a>Коды ошибок

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искрденр**](iscrdenr.md)
</dt> <dt>

[**Искрденр:: CSPName**](iscrdenr-cspname.md)
</dt> <dt>

[**Искрденр:: Енумкспнаме**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
