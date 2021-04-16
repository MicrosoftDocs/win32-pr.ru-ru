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
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664236"
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

## <a name="remarks"></a>Комментарии

Используйте этот метод, чтобы указать ЦС для шаблона сертификата.

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

[**Искрденр:: Жетканаме**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
