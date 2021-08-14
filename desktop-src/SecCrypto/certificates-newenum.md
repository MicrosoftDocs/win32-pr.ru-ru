---
description: '\_Свойство NewEnum сертификатов Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции. это свойство скрыто в Visual Basic scripting Edition (VBScript).'
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Certificates._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eab4395e24b12b8e9492c6f18f595a91e192a59c53309411433b49881cd4fd4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770516"
---
# <a name="certificates_newenum-property"></a>Сертификаты. \_ Свойство NewEnum

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции. это свойство скрыто в Visual Basic scripting Edition (VBScript).

## <a name="syntax"></a>Синтаксис


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a>Значение свойства

Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.

## <a name="remarks"></a>Remarks

это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic scripting Edition (VBScript).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Сертификаты**](certificates.md)
</dt> </dl>

 

 
