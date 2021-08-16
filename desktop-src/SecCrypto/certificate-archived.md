---
description: Задает или получает логическое значение, указывающее, архивируется ли сертификат.
ms.assetid: a6526b0e-e76b-4f03-a6ba-9e380e362364
title: Заархивированное Свойство Certificate.
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Archived
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2e3ab848caa24cb77a8cb45e992eeac7365af0de743fa148b07b484239fa658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771953"
---
# <a name="certificatearchived-property"></a>Заархивированное Свойство Certificate.

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

**Заархивированное** свойство задает или получает логическое значение, указывающее, архивируется ли сертификат.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
Certificate.Archived As Boolean
```



## <a name="property-value"></a>Значение свойства

Логическое значение, указывающее, архивируется ли сертификат. Если **значение — true**, сертификат архивируется. Обратите внимание, что изменение значения с **false** на **true** архивирует сертификат.

## <a name="remarks"></a>Remarks

Это свойство вызывает CAPICOM \_ E \_ не \_ разрешено при создании скрипта из веб-приложения.

> [!Note]  
> Архивный сертификат не отображается в пользовательском интерфейсе управления сертификатами. Кроме того, архивные сертификаты не будут включены в метод [**Store. Open**](store-open.md) , если не \_ задано поле Открыть хранилище CAPICOM с \_ \_ \_ параметром archiveed.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
