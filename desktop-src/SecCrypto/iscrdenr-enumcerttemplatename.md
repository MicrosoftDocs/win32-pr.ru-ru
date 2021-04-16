---
description: Перечисляет имена шаблонов сертификатов.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'Метод Искрденр:: Енумцерттемплатенаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664400"
---
# <a name="iscrdenrenumcerttemplatename-method"></a>Метод Искрденр:: Енумцерттемплатенаме

Метод **енумцерттемплатенаме** перечисляет имена шаблонов сертификатов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*двиндекс* \[ окне\]
</dt> <dd>

Отсчитываемый от нуля индекс последовательности перечисления.

</dd> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Значение, определяющее, применяется ли перечисленный шаблон сертификата к сертификатам пользователя или компьютера. Если это значение равно бросить \_ зарегистрировать \_ \_ шаблон сертификата пользователя \_ (определяется как 1), то перечисление применяется к шаблонам сертификатов пользователей. Если это значение равно бросить \_ зарегистрировать \_ \_ шаблон сертификата компьютера \_ (определяется как 2), то перечисление применяется к шаблонам сертификатов компьютера.

</dd> <dt>

*пбстрцерттемплатенаме* \[ заполняет\]
</dt> <dd>

Указатель на строку, которая возвращает имя перечисленного шаблона сертификата.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="c"></a>C++

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Строка, содержащая имя перечисленного шаблона сертификата.

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

[**Искрденр:: Жетцерттемплатекаунт**](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[**Искрденр:: Жетцерттемплатенаме**](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[**Искрденр:: Сетцерттемплатенаме**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




