---
description: Указывает имя шаблона сертификата.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'Метод Искрденр:: Сетцерттемплатенаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 5f757ead06e5d1769e109bcbfc8e3510f4298f32145d60c4c0bc992a01f3ab36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993044"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>Метод Искрденр:: Сетцерттемплатенаме

Метод **сетцерттемплатенаме** задает имя шаблона сертификата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Значение, которое определяет, устанавливается ли реальное имя или отображаемое имя шаблона сертификата. Если для *dwFlags* задано значение \_ \_ \_ \_ Отображаемое имя шаблона сертификата регистрации бросить, то \_ будет задано отображаемое имя шаблона сертификатов. В противном случае задается реальное имя шаблона сертификата.

</dd> <dt>

*бстрцерттемплатенаме* \[ окне\]
</dt> <dd>

Имя шаблона сертификата, который будет использоваться в запросе сертификата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="vb"></a>VB

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

## <a name="remarks"></a>Remarks

Если имя шаблона сертификата не задано путем вызова **искрденр:: сетцерттемплатенаме**, по умолчанию используется имя в списке доступных шаблонов сертификатов.

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

[**Искрденр:: Жетцерттемплатенаме**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




