---
description: Представляет идентификатор объекта (OID), используемый несколькими свойствами CAPICOM.
ms.assetid: d9dc2a9a-920b-41e1-91fb-da1628df577d
title: OID, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a524bfd8d2eb2edcf3c97919129dd694414d5ace
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669456"
---
# <a name="oid-object"></a>OID, объект

\[Объект **OID** доступен для использования в операционных системах, указанных в разделе требования. Вместо этого используйте [**класс Oid**](/dotnet/api/system.security.cryptography.oid?view=netcore-3.1) в пространстве имен [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

Объект **OID** представляет [*идентификатор объекта*](../secgloss/o-gly.md) (OID), используемый несколькими свойствами CAPICOM.

## <a name="when-to-use"></a>Назначение

Объект **OID** используется для выполнения следующих задач:

-   Задайте или извлеките имя элемента CAPICOM и отображаемое имя для OID.
-   Задайте или извлеките числовое значение OID.

## <a name="members"></a>Элементы

Объект **OID** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **OID** имеет эти свойства.



| Свойство                                            | Тип доступа           | Описание                                                                                      |
|:----------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------|
| [**FriendlyName**](oid-friendlyname.md)<br/> | Чтение/запись<br/> | Задает или получает отображаемое имя для OID.<br/>                                       |
| [**Имя**](oid-name.md)<br/>                 | Чтение/запись<br/> | Задает или получает имя объекта, определенное с помощью элемента CAPICOM. Это свойство по умолчанию.<br/> |
| [**Значение**](oid-value.md)<br/>               | Чтение/запись<br/> | Задает или получает значение номера OID, разделенного OID.<br/>                      |



 

## <a name="remarks"></a>Комментарии

Объект **OID** может быть создан и защищен для создания скриптов. ProgID для объекта **OID** — CAPICOM. OID. 1.

Следующие свойства элемента CAPICOM возвращают объект **OID** :

-   [**Полициинформатион. OID**](policyinformation-oid.md)
-   [**Квалификатор. OID**](qualifier-oid.md)
-   [**Extension. OID**](extension-oid.md)
-   [**Template. OID**](template-oid.md)

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
