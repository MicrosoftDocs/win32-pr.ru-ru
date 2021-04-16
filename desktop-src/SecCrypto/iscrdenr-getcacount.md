---
description: Возвращает число центров сертификации (CAs), которые хотят выдать сертификат на основе указанного шаблона сертификата.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'Метод Искрденр:: Жеткакаунт'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664399"
---
# <a name="iscrdenrgetcacount-method"></a>Метод Искрденр:: Жеткакаунт

Метод **жеткакаунт** возвращает число [*центров сертификации*](../secgloss/c-gly.md) (CAS), которые хотят выдать сертификат на основе указанного шаблона сертификата.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a>Параметры

<dl> <dt>

*бстрцерттемплатенаме* \[ окне\]
</dt> <dd>

Строка, представляющая имя шаблона сертификата.

</dd> <dt>

*пдвкакаунт* \[ заполняет\]
</dt> <dd>

Указатель на значение **типа Long** , возвращающее количество доступных центров сертификации, которые выдают сертификат для шаблона сертификата, указанного в *бстрцерттемплатенаме*.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

### <a name="c"></a>C++

Если метод завершается успешно, метод возвращает значение S \_ ОК.

Если метод завершается с ошибкой, возвращается значение **HRESULT** , указывающее на ошибку. Список распространенных кодов ошибок см. в разделе [Общие значения HRESULT](common-hresult-values.md).

### <a name="vb"></a>VB

Значение **типа Long** , представляющее количество доступных центров сертификации, которые будут выдавать сертификат для шаблона сертификата, указанного в *бстрцерттемплатенаме*.

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

 

 
