---
description: Представляет одно свойство расширенного использования ключа (EKU) сертификата.
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: Объект EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: bd887204abc31583e596e94c25b64addcfe8109e6432845d25d939fd8e79e2d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875144"
---
# <a name="eku-object"></a>Объект EKU

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Объект **EKU** представляет одно свойство расширенного использования ключа (EKU) сертификата.

## <a name="members"></a>Элементы

Объект **EKU** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Объект **EKU** имеет следующие свойства.



| Свойство                            | Тип доступа           | Описание                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Имя**](eku-name.md)<br/> | Чтение/запись<br/> | Задает или получает значение перечисления, которое указывает CAPICOM имя EKU. Это свойство по умолчанию.<br/>                                                                                   |
| [**КОДА**](eku-oid.md)<br/>   | Чтение/запись<br/> | Задает или получает строку, содержащую значение строки [*идентификатора объекта*](../secgloss/o-gly.md) EKU (OID), определенное в винкрипт. h.<br/> |



 

## <a name="remarks"></a>Remarks

Объект **EKU** используется следующей коллекцией и свойством:

-   Коллекция [**EKU**](ekus.md)
-   [**Цертификатестатус. EKU,**](certificatestatus-eku.md) свойство

Не удается создать объект **EKU** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
