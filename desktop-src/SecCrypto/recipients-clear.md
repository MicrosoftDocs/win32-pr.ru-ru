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
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685305"
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

## <a name="requirements"></a>Требования



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

 

 
