---
description: Указывает имя центра сертификации (ЦС).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'Метод Искрденр:: Сетканаме'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 726b1d6d6a31831e5db192b5a71dea9efa32f624333ee7f6d6d2eea432dacae9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960274"
---
# <a name="iscrdenrsetcaname-method"></a>Метод Искрденр:: Сетканаме

Метод **сетканаме** указывает имя [*центра сертификации*](../secgloss/c-gly.md) (ЦС).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*dwFlags* \[ окне\]
</dt> <dd>

Значение, указывающее, относится ли имя к имени центра сертификации или имени компьютера ЦС. Если это значение равно бросить \_ Регистрация \_ \_ имени компьютера ЦС \_ (определено как 0x01), имя будет ССЫЛАТЬСЯ на имя компьютера ЦС. В противном случае имя ссылается на имя ЦС.

</dd> <dt>

*бстрцерттемплатенаме* \[ окне\]
</dt> <dd>

Имя шаблона сертификата.

</dd> <dt>

*бстрканаме* \[ окне\]
</dt> <dd>

Имя ЦС, которое будет использоваться с шаблоном сертификата, указанным параметром *бстрцерттемплатенаме*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="vb"></a>VB

Возвращаемое значение является значением **HRESULT**. Значение S \_ ОК указывает, что вызов выполнен успешно.

## <a name="remarks"></a>Remarks

Используйте этот метод, чтобы указать ЦС для шаблона сертификата.

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

[**Искрденр:: Енумканаме**](iscrdenr-enumcaname.md)
</dt> <dt>

[**Искрденр:: Жетканаме**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
