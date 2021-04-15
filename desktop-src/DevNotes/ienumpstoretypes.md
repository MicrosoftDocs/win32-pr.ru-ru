---
description: Предоставляет стандартные методы перечисления COM для интерфейса Ипсторе.
ms.assetid: a90bc5cf-ca42-4007-a57b-be9c59d9552a
title: Интерфейс Иенумпсторетипес (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreTypes
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: 748f6e21701fdd27c2a88d1959b0b29cf56929f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649028"
---
# <a name="ienumpstoretypes-interface"></a>Интерфейс Иенумпсторетипес

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Предоставляет стандартные методы перечисления COM для интерфейса [**ипсторе**](ipstore.md) .

## <a name="members"></a>Элементы

Интерфейс **иенумпсторетипес** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иенумпсторетипес** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иенумпсторетипес** содержит следующие методы.



| Метод                                  | Описание                                                                                        |
|:----------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Клонировать**](ienumpstoretypes-clone.md) | Создает другой перечислитель с тем же состоянием перечисления, что и текущий.<br/> |
| [**Далее**](ienumpstoretypes-next.md)   | Возвращает следующий указанный тип поставщика в последовательности перечисления.<br/>                      |
| [**Перезапуск**](ienumpstoretypes-reset.md) | Выполняет сброс до начала последовательности перечисления.<br/>                                    |
| [**Пропустить**](ienumpstoretypes-skip.md)   | Пропускает указанный тип поставщика в последовательности перечисления.<br/>                          |



 

## <a name="remarks"></a>Комментарии

Объект перечислителя должен быть освобожден, если он больше не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
