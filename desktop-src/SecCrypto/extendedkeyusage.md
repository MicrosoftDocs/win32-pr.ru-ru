---
description: Предоставляет доступ только для чтения к свойствам расширенного использования ключа (EKU) сертификата.
ms.assetid: 636d7f65-d286-4800-a576-a23e6e9811b2
title: Объект Екстендедкэйусаже
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 927e219e22bd0e87c444b1ca3cb63b09a5ddc2fb9ac74e63ebb8f66c6ed75437
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007322"
---
# <a name="extendedkeyusage-object"></a>Объект Екстендедкэйусаже

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista и Windows XP. Вместо этого используйте [**класс X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Объект **екстендедкэйусаже** предоставляет доступ только для чтения к свойствам расширенного использования ключа (EKU) сертификата.

## <a name="members"></a>Элементы

Объект **екстендедкэйусаже** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Объект **екстендедкэйусаже** имеет следующие свойства.



| Свойство                                                     | Тип доступа          | Описание                                                                                                                             |
|:-------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [**EKU**](extendedkeyusage-ekus.md)<br/>             | Только для чтения<br/> | Коллекция [**EKU**](ekus.md) , содержащая объекты [**EKU**](eku.md) для сертификата.<br/>                            |
| [**Критическое**](extendedkeyusage-iscritical.md)<br/> | Только для чтения<br/> | Получает **логическое** значение, указывающее, помечено ли расширение EKU как критическое.<br/>                                   |
| [**IsPresent**](extendedkeyusage-ispresent.md)<br/>   | Только для чтения<br/> | Получает **логическое** значение, указывающее, имеется ли расширение EKU.<br/> Это свойство по умолчанию. <br/> |



 

## <a name="remarks"></a>Remarks

Не удается создать объект **екстендедкэйусаже** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------------|----------------------------------------------------------------------------------------|
| Окончание поддержки клиента<br/> | Windows Vista<br/>                                                               |
| Поддержка конца сервера<br/> | Windows Server 2008<br/>                                                         |
| Распространяемые компоненты<br/>       | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Криптографические объекты**](cryptography-objects.md)
</dt> </dl>

 

 
