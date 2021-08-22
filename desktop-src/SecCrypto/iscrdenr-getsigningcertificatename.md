---
description: Извлекает имя субъекта из сертификата подписи.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'Метод Искрденр:: Жетсигнингцертификатенаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 29933856eb644e638e9e58c8da0b0e3d6234e4f0175925c8a1fb5b48b126e3ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622404"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a>Метод Искрденр:: Жетсигнингцертификатенаме

Метод **жетсигнингцертификатенаме** извлекает имя субъекта из сертификата подписи.

Этот метод также можно использовать для вывода сертификата в диалоговом окне. Этот метод вызывает функцию [*CryptoAPI*](../secgloss/c-gly.md) [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Значение, определяющее, отображается ли сертификат в диалоговом окне. Если это значение равно бросить \_ Регистрация \_ не \_ отображает сертификат \_ (определенный как 0x01), сертификат подписи не отображается; любые другие значения приводят к тому, что сертификат подписи отображается в диалоговом окне **сертификат** .

</dd> <dt>

*пбстрсигнингцертнаме* \[ заполняет\]
</dt> <dd>

Указатель на строку, которая возвращает имя сертификата подписи. Сертификат для подписи будет использоваться для подписания [*запроса на сертификат*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="c"></a>C++

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Строка, представляющая имя сертификата подписи. Сертификат для подписи будет использоваться для подписания [*запроса на сертификат*](../secgloss/c-gly.md).

## <a name="remarks"></a>Remarks

Метод **жетсигнингцертификатенаме** возвращает имя субъекта сертификата, выбранного вами (или другим администратором) в предыдущем успешном вызове [**Искрденр:: селектсигнингцертификате**](iscrdenr-selectsigningcertificate.md) или [**искрденр:: сетсигнингцертификате**](iscrdenr-setsigningcertificate.md). Этот метод вызывает функцию [**цертжетнаместринг**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) для получения имени субъекта в соответствии с последовательностью, описанной \_ для \_ \_ значения простого отображаемого типа сертификата для \_ параметра *двтипе* **цертжетнаместринг**.

## <a name="requirements"></a>Требования



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

[**Искрденр:: Селектсигнингцертификате**](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
