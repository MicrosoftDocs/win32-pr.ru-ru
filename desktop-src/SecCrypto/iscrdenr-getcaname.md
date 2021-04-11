---
description: Возвращает имя указанного центра сертификации (ЦС) для данного шаблона сертификата.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'Метод Искрденр:: Жетканаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272261"
---
# <a name="iscrdenrgetcaname-method"></a>Метод Искрденр:: Жетканаме

Метод **жетканаме** извлекает имя указанного [*центра сертификации*](../secgloss/c-gly.md) (CA) для данного шаблона сертификата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Значение, определяющее, относится ли имя к имени центра сертификации или имени компьютера ЦС. Если это значение равно бросить \_ Регистрация \_ \_ имени компьютера ЦС \_ (определено как 0x01), то имя будет ссылаться на имя компьютера центра сертификации; в противном случае имя будет ссылаться на имя ЦС.

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

## <a name="remarks"></a>Комментарии

Имя ЦС по умолчанию — это первое имя в списке доступных центров сертификации.

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

[**Искрденр:: Енумканаме**](iscrdenr-enumcaname.md)
</dt> <dt>

[**Искрденр:: Жеткакаунт**](iscrdenr-getcacount.md)
</dt> <dt>

[**Искрденр:: Сетканаме**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
