---
description: Извлекает URI, указывающий на заявление о сертификации (CPS), опубликованное центром сертификации (ЦС).
ms.assetid: fd030c1c-137c-4036-bf13-ae989a9703cc
title: Свойство квалификатора. Кпспоинтер
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.CPSPointer
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: db16e8faa25fc929e884358fcd885943adc17e32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648947"
---
# <a name="qualifiercpspointer-property"></a>Свойство квалификатора. Кпспоинтер

\[Свойство **кпспоинтер** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) , вызвав конструктор, принимающий OID в качестве параметра, а затем использовать OID для политик сертификатов для обработки квалификаторов, которые являются частью сведений о политике в расширении политик сертификатов.\]

Свойство **кпспоинтер** Извлекает URI, указывающий на заявление о сертификации (CPS), опубликованное центром сертификации (ЦС).

## <a name="syntax"></a>Синтаксис


```VB
Qualifier.CPSPointer As String
```



## <a name="property-value"></a>Значение свойства

Универсальный код ресурса (URI), указывающий на сервер публикаций Contribute, опубликованный центром сертификации.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Квалификатор**](qualifier.md)
</dt> </dl>

 

 
