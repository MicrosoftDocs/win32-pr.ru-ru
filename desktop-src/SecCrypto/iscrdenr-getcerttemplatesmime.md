---
description: Используется для определения того, содержит ли шаблон сертификата \_ \_ \_ Использование ключа защиты электронной почты сзоид пкикс \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'Метод Искрденр:: Жетцерттемплатесмиме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8da8c9c3202c0955a001a63e77f85858fc6237d7476c0fc5222ae8f85e94a7c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515964"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>Метод Искрденр:: Жетцерттемплатесмиме

Метод **жетцерттемплатесмиме** используется для определения того, содержит ли шаблон сертификата \_ \_ \_ Использование ключа защиты электронной почты сзоид пкикс \_ .

Если это использование ключа является частью шаблона сертификата, шаблон сертификата поддерживает операции с [*безопасными и многоцелевыми расширениями электронной почты Интернета*](../secgloss/s-gly.md) (S/MIME).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрцерттемплатенаме* \[ окне\]
</dt> <dd>

Имя сертификата, для которого запрашивается использование ключа S/MIME.

</dd> <dt>

*пдвцерттемплатесмиме* \[ заполняет\]
</dt> <dd>

Указатель на **DWORD** , возвращающий значение, равное 1, если *бстрцерттемплатенаме* поддерживает S/MIME; в противном случае возвращается ноль.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="c"></a>C++

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Значение **типа Long** , равное единице, если *бстрцерттемплатенаме* поддерживает S/MIME; в противном случае — ноль.

## <a name="remarks"></a>Remarks

Константа для \_ \_ защиты электронной почты сзоид пкикс-ключевого средства \_ \_ определяется в винкрипт. h.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                    |
| DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ искрденр определен как 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>См. также

<dl> <dt>

[**искрденр**](iscrdenr.md)
</dt> <dt>

[**Искрденр:: регистрация**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
