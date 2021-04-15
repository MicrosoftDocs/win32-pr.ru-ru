---
description: Представляет отдельный атрибут, прошедший проверку подлинности.
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute, объект
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669301"
---
# <a name="attribute-object"></a>Attribute, объект

\[CAPICOM — это 32-разрядный компонент, доступный для использования в следующих операционных системах: Windows Server 2008, Windows Vista, Windows XP. Вместо этого используйте [**класс криптографикаттрибутеобжект**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) в пространстве имен [**System. Security. Cryptography**](/previous-versions/windows/) .\]

Объект **атрибута** представляет один атрибут, прошедший проверку подлинности.

## <a name="when-to-use"></a>Назначение

Объект **атрибута** используется для выполнения следующих задач:

-   Задайте или извлеките имя элемента CAPICOM атрибута.
-   Задайте или получите значение атрибута, например время подписи, имя подписанного документа или описание документа, подписанного.

## <a name="members"></a>Элементы

Объект **атрибута** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Объект **атрибута** имеет следующие свойства.



| Свойство                                    | Тип доступа           | Описание                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Имя**](attribute-name.md)<br/>   | Чтение/запись<br/> | Задает или получает имя элемента CAPICOM атрибута. Это свойство по умолчанию.<br/> |
| [**Значение**](attribute-value.md)<br/> | Чтение/запись<br/> | Задает или получает значение атрибута.<br/>                                      |



 

## <a name="remarks"></a>Комментарии

Объект **атрибута** может быть создан и защищен для создания скриптов. ProgID для объекта **атрибута** — CAPICOM. Атрибут. 1.

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

 

 
