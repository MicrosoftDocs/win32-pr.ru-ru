---
description: Удаляет все объекты сертификата из коллекции получателей.
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: Метод Recipients. Clear
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c956aacd7b61243fbaeb26ed1a29ed0fee4522d83d8b4ef3ac25b3b1921b42a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900811"
---
# <a name="recipientsclear-method"></a>Метод Recipients. Clear

\[Метод **clear** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс кмсреЦипиентколлектион**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Метод **clear** удаляет все объекты [**сертификата**](certificate.md) из коллекции [**получателей**](recipients.md) .

## <a name="syntax"></a>Синтаксис


```VB
Recipients.Clear()
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение. Приложение, использующее этот метод, должно содержать код, обрабатывающий исключение, вызванное этим методом.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> <dt>

[**Recipients**](recipients.md)
</dt> </dl>

 

 
