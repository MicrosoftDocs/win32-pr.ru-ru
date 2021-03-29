---
title: Сопоставление синтаксиса Active Directory синтаксису ADSI
description: Следующая таблица сопоставляет синтаксисы Active Directory с соответствующими синтаксисами ADSI.
ms.assetid: ffb40eff-e137-4d6a-81e7-24d2cbbdbfbf
ms.tgt_platform: multiple
keywords:
- атрибуты ADSI, сопоставление синтаксиса Active Directory синтаксису ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ba332a39a5d2452925f1a8f1cc8c8ca766ca10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105654119"
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
| 2.5.5.8<br/>  | Логический<br/>                       | Логический<br/>                                                  |
| 2.5.5.9<br/>  | Целочисленный тип<br/>                       | Целочисленный тип<br/>                                                  |
| 2.5.5.10<br/> | Строка октета<br/>                  | Строка октета<br/>                                             |
| 2.5.5.11<br/> | Время<br/>                          | Время в формате UTC<br/>                                                 |
| 2.5.5.12<br/> | Юникод<br/>                       | Пропустить строку без учета регистра<br/>                                       |
| 2.5.5.13<br/> | Адрес<br/>                       | Не поддерживается<br/>                                            |
| 2.5.5.14<br/> | Distname-Address<br/>              |                                                                     |
| 2.5.5.15<br/> | Дескриптор безопасности NT<br/>        | [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)<br/> |
| 2.5.5.16<br/> | Большое целое число<br/>                 | [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)<br/>             |
| 2.5.5.17<br/> | SID<br/>                           | Строка октета<br/>                                             |



 

 

 





