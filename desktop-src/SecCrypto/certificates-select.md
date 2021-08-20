---
description: Отображает диалоговое окно для выбора сертификатов и возвращает коллекцию выбранных сертификатов.
ms.assetid: dbf49a4b-6da1-4819-afcd-46db89a00fce
title: 'Метод ICertificates2:: SELECT'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Select
- ICertificates2.Select
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 50e10a9487318c7b89e89afb3d10d5974524c821b76618ca8ffd1f282e844f65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770489"
---
# <a name="icertificates2select-method"></a>Метод ICertificates2:: SELECT

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Метод **SELECT** отображает диалоговое окно для выбора сертификатов и возвращает коллекцию выбранных сертификатов. Этот метод появился в CAPICOM 2,0.

## <a name="syntax"></a>Синтаксис


```VB
Certificates.Select( _
  [ ByVal Title ], _
  [ ByVal DisplayString ], _
  [ ByVal bMultiSelect ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Название* \[ в необязательное\]
</dt> <dd>

Строка, содержащая заголовок для диалогового окна. Значение по умолчанию — пустая строка.

</dd> <dt>

*DisplayString* \[ в необязательное\]
</dt> <dd>

Строка, содержащая текст подсказки, отображаемый в диалоговом окне. Значение по умолчанию — пустая строка.

</dd> <dt>

*бмултиселект* \[ в необязательное\]
</dt> <dd>

Логическое значение, указывающее, может ли пользователь выбрать более одного сертификата. Значение true указывает, что можно выбрать несколько сертификатов с помощью клавиши CTRL или SHIFT. Значением по умолчанию является false.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект [**Certificates**](certificates.md) , который содержит сертификаты, выбранные из диалогового окна.

**CAPICOM 2,1:** Возвращаемый объект [**Certificates**](certificates.md) содержит ссылки на сертификаты в коллекции, из которой был сделан выбор. Все изменения, внесенные в сертификаты в возвращенном объекте **Certificate** , отражаются в этой коллекции.

**Capicom 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 и CAPICOM 2.0.0.3:** Возвращаемый объект [**Certificates**](certificates.md) содержит копии сертификатов в коллекции, из которой был сделан выбор. Любые изменения, внесенные в сертификаты в возвращенном объекте **Certificates** , не отражаются в этой коллекции.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
