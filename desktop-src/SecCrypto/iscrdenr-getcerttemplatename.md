---
description: Извлекает имя шаблона сертификата.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'Метод Искрденр:: Жетцерттемплатенаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272259"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>Метод Искрденр:: Жетцерттемплатенаме

Метод **жетцерттемплатенаме** извлекает имя шаблона сертификата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Значение, определяющее, возвращается ли вещественное имя или отображаемое имя шаблона сертификата. Если для *dwFlags* задано значение \_ \_ \_ \_ Отображаемое имя шаблона сертификата регистрации, то выводится \_ Отображаемое имя шаблона сертификатов. в противном случае отображается действительное имя шаблона сертификата.

</dd> <dt>

*пбстрцерттемплатенаме* \[ заполняет\]
</dt> <dd>

Указатель на строку, которая возвращает имя шаблона сертификата, который будет использоваться в [*запросе сертификата*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="c"></a>C++

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Строка, представляющая имя шаблона сертификата, который будет использоваться в [*запросе сертификата*](../secgloss/c-gly.md).

## <a name="remarks"></a>Комментарии

Если имя шаблона сертификата не задано путем вызова [**искрденр:: сетцерттемплатенаме**](iscrdenr-setcerttemplatename.md), по умолчанию используется имя в списке доступных шаблонов сертификатов.

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

[**Искрденр:: Сетцерттемплатенаме**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
