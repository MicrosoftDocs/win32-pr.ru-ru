---
description: Перечисляет имена центров сертификации (ЦС) для заданного имени шаблона сертификата.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'Метод Искрденр:: Енумканаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 11742525d616aecc8d83871ae2a59025d1034513ae99d8a7253d16d9e0f64dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005222"
---
# <a name="iscrdenrenumcaname-method"></a>Метод Искрденр:: Енумканаме

Метод **енумканаме** перечисляет имена [*центров сертификации*](../secgloss/c-gly.md) (CAS) для заданного имени шаблона сертификата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
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

Значение, определяющее, относится ли имя к имени центра сертификации или имени компьютера ЦС. Если это значение равно бросить \_ Регистрация \_ \_ имени компьютера ЦС \_ (определено как 0x01), имя будет ССЫЛАТЬСЯ на имя компьютера ЦС. В противном случае имя ссылается на имя ЦС.

</dd> <dt>

*бстрцерттемплатенаме* \[ окне\]
</dt> <dd>

Имя шаблона сертификата.

</dd> <dt>

*пбстрканаме* \[ заполняет\]
</dt> <dd>

Указатель на строку, которая возвращает имя центра сертификации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="c"></a>C++

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Строка, представляющая имя центра сертификации.

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

[**Искрденр:: Жеткакаунт**](iscrdenr-getcacount.md)
</dt> <dt>

[**Искрденр:: Жетканаме**](iscrdenr-getcaname.md)
</dt> <dt>

[**Искрденр:: Сетканаме**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
