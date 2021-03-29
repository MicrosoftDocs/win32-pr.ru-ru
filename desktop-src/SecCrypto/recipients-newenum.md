---
description: '\_Свойство NewEnum получателей Извлекает интерфейс IEnumVARIANT для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).'
ms.assetid: affdc695-b78c-48b5-b66d-5f94e1a86ff2
title: Recipients._NewEnum, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a4a1e7db31ceead23509604edddee05ec64380ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665391"
---
# <a name="recipients_newenum-property"></a>Получатели. \_ Свойство NewEnum

\[Свойство **\_ NewEnum** доступно для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс кмсреЦипиентколлектион**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography. PKCS**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Свойство **\_ NewEnum** Извлекает интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) для объекта, который можно использовать для перечисления коллекции. Это свойство скрыто в Visual Basic Scripting Edition (VBScript).

## <a name="syntax"></a>Синтаксис


```VB
Recipients._NewEnum As IUnknown
```



## <a name="property-value"></a>Значение свойства

Интерфейс [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) объекта, который может использоваться для перечисления коллекции.

## <a name="remarks"></a>Комментарии

Это свойство автоматически используется для внутренних целей при использовании `For Each In` конструкции в Visual Basic Scripting Edition (VBScript).

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Recipients**](recipients.md)
</dt> </dl>

 

 
