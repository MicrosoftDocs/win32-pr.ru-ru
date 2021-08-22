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
ms.openlocfilehash: aaf37f3907bc2b26ca1adbbded7be5ed7897a74ea9664d4353354d5ad9657d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409624"
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

## <a name="remarks"></a>Remarks

Если имя шаблона сертификата не задано путем вызова [**искрденр:: сетцерттемплатенаме**](iscrdenr-setcerttemplatename.md), по умолчанию используется имя в списке доступных шаблонов сертификатов.

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

[**Искрденр:: Сетцерттемплатенаме**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
