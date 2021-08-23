---
description: Задает или получает имя поставщика служб шифрования (CSP).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'Свойство Искрденр:: CSPName'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 7a1b5b443807dfe7fa737cdfc5eb4da678845e53b555ffe6eebf1529583fdb35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005232"
---
# <a name="iscrdenrcspname-property"></a>Свойство Искрденр:: CSPName

Свойство **CSPName** задает или получает имя [*поставщика служб шифрования*](../secgloss/c-gly.md) (CSP).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a>Значение свойства

Имя CSP.

## <a name="error-codes"></a>Коды ошибок

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

## <a name="remarks"></a>Remarks

Задайте это свойство, чтобы указать имя CSP, используемого для управления регистрацией смарт-карты. Получите это свойство, чтобы получить имя указанного CSP. Если значение для этого свойства не указано, свойство **CSPName** по умолчанию имеет имя, указанное в списке доступных CSP.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**искрденр**](iscrdenr.md)
</dt> <dt>

[**Искрденр:: Кспкаунт**](iscrdenr-cspcount.md)
</dt> <dt>

[**Искрденр:: Енумкспнаме**](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
