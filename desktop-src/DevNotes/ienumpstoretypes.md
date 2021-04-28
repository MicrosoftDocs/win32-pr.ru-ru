---
description: Интерфейс Иенумпсторетипес — предоставляет стандартные методы перечисления COM для интерфейса Ипсторе.
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
ms.openlocfilehash: 7ca2e250864889a5fda465e146287bf59a2b6346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089362"
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
| [**Clone (Клонировать)**](ienumpstoretypes-clone.md) | Создает другой перечислитель с тем же состоянием перечисления, что и текущий.<br/> |
| [**Далее**](ienumpstoretypes-next.md)   | Возвращает следующий указанный тип поставщика в последовательности перечисления.<br/>                      |
| [**Reset**](ienumpstoretypes-reset.md) | Выполняет сброс до начала последовательности перечисления.<br/>                                    |
| [**Пропустить**](ienumpstoretypes-skip.md)   | Пропускает указанный тип поставщика в последовательности перечисления.<br/>                          |



 

## <a name="remarks"></a>Remarks

Объект перечислителя должен быть освобожден, если он больше не используется.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
