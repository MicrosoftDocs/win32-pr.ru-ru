---
title: Сопоставление синтаксиса Active Directory синтаксису ADSI
description: Следующая таблица сопоставляет синтаксисы Active Directory с соответствующими синтаксисами ADSI.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- атрибуты ADSI, сопоставление синтаксиса Active Directory синтаксису ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d04682a1e299e14c55c520310bff697ea6664d4dabe71380f7a146fd2dfff053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179282"
---
# <a name="mapping-active-directory-syntax-to-adsi-syntax"></a>Сопоставление синтаксиса Active Directory синтаксису ADSI

Следующая таблица сопоставляет синтаксисы Active Directory с соответствующими синтаксисами ADSI.



| Идентификатор синтаксиса атрибута | Active Directory тип синтаксиса             | Эквивалентный тип синтаксиса ADSI                                         |
|---------------------|------------------------------------------|---------------------------------------------------------------------|
| 2.5.5.1<br/>  | Строка различающегося имени<br/>                     | Строка различающегося имени<br/>                                                |
| 2.5.5.2<br/>  | Идентификатор объекта<br/>                     | Строка Касеигноре<br/>                                        |
| 2.5.5.3<br/>  | Строка с учетом регистра<br/>         | Строка Касиксакт<br/>                                         |
| 2.5.5.4<br/>  | Регистр пропущенных строк<br/>           | Строка Касеигноре<br/>                                        |
| 2.5.5.5<br/>  | Строка варианта печати<br/>             | Печатная строка<br/>                                         |
| 2.5.5.6<br/>  | Числовая строка<br/>                | Числовая строка<br/>                                           |
| 2.5.5.7<br/>  | **Или** Имя Днвисоктетстринг<br/> | Не поддерживается<br/>                                            |
| 2.5.5.8<br/>  | Логический<br/>                       | Логическое<br/>                                                  |
| 2.5.5.9<br/>  | Целочисленный тип<br/>                       | Целое число<br/>                                                  |
| 2.5.5.10<br/> | Строка октета<br/>                  | Строка октета<br/>                                             |
| 2.5.5.11<br/> | Time<br/>                          | Время в формате UTC<br/>                                                 |
| 2.5.5.12<br/> | Юникод<br/>                       | Пропустить строку без учета регистра<br/>                                       |
| 2.5.5.13<br/> | Адрес<br/>                       | Не поддерживается<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | Дескриптор безопасности NT<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Большое целое число<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Строка октета<br/>                                             |



 

 

 





