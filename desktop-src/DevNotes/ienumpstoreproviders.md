---
description: Интерфейс Иенумпсторепровидерс — предоставляет стандартные методы перечисления COM для интерфейса Ипсторе.
ms.assetid: d4c0482c-a751-4d41-bcd1-326878fdcf16
title: Интерфейс Иенумпсторепровидерс (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPStoreProviders
api_type:
- COM
api_location:
- Pstorec.dll
ms.openlocfilehash: cf203e0e6de08b6faff3d3b4a040018ec1122975
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089352"
---
# <a name="ienumpstoreproviders-interface"></a>Интерфейс Иенумпсторепровидерс

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Предоставляет стандартные методы перечисления COM для интерфейса [**ипсторе**](ipstore.md) .

## <a name="members"></a>Элементы

Интерфейс **иенумпсторепровидерс** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иенумпсторепровидерс** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иенумпсторепровидерс** содержит следующие методы.



| Метод                                      | Описание                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Clone (Клонировать)**](ienumpstoreproviders-clone.md) | Создает другой перечислитель с тем же состоянием перечисления, что и текущий.<br/> |
| [**Далее**](ienumpstoreproviders-next.md)   | Возвращает следующий указанный поставщик в последовательности перечисления.<br/>                           |
| [**Reset**](ienumpstoreproviders-reset.md) | Выполняет сброс до начала последовательности перечисления.<br/>                                    |
| [**Пропустить**](ienumpstoreproviders-skip.md)   | Пропускает указанный поставщик в последовательности перечисления.<br/>                               |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
