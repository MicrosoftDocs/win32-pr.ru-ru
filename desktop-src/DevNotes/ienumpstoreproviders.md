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
ms.openlocfilehash: eb73345dd594f3583b4a6cfbc6e0462848d85de0e9470e6bc8177574a2fff20d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017712"
---
# <a name="ienumpstoreproviders-interface"></a>Интерфейс Иенумпсторепровидерс

\[защищенные служба хранилища (Pstore) доступны для использования в Windows Server 2003 и Windows XP. она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Предоставляет стандартные методы перечисления COM для интерфейса [**ипсторе**](ipstore.md) .

## <a name="members"></a>Элементы

Интерфейс **иенумпсторепровидерс** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **Иенумпсторепровидерс** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иенумпсторепровидерс** содержит следующие методы.



| Метод                                      | Описание                                                                                        |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------|
| [**Клонировать**](ienumpstoreproviders-clone.md) | Создает другой перечислитель с тем же состоянием перечисления, что и текущий.<br/> |
| [**Далее**](ienumpstoreproviders-next.md)   | Возвращает следующий указанный поставщик в последовательности перечисления.<br/>                           |
| [**Перезапуск**](ienumpstoreproviders-reset.md) | Выполняет сброс до начала последовательности перечисления.<br/>                                    |
| [**Сразу**](ienumpstoreproviders-skip.md)   | Пропускает указанный поставщик в последовательности перечисления.<br/>                               |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>PStore. h</dt> </dl>    |
| DLL<br/>    | <dl> <dt>Pstorec.dll</dt> </dl> |



 

 
