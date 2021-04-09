---
title: Дескриптор безопасности по умолчанию
description: С помощью домен Active Directory Services можно также указать безопасность по умолчанию для каждого типа объектов.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Дескриптор безопасности по умолчанию AD
- AD дескрипторов безопасности, по умолчанию
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069789"
---
# <a name="default-security-descriptor"></a>Дескриптор безопасности по умолчанию

С помощью домен Active Directory Services можно также указать безопасность по умолчанию для каждого типа объектов. Это указывается в атрибуте [**дефаултсекуритидескриптор**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) в определении объекта [**classSchema**](/windows/desktop/ADSchema/c-classschema) в [схеме Active Directory](active-directory-schema.md). Этот дескриптор безопасности используется для обеспечения защиты объекта по умолчанию, если во время создания объекта не указан дескриптор безопасности.

> [!Note]  
> Записи ACE из дескриптора безопасности по умолчанию обрабатываются так, как если бы они были указаны как часть создания объекта. Таким образом, записи ACE по умолчанию помещаются перед унаследованными Aceми и переопределяют их соответствующим образом. Дополнительные сведения см. [в разделе порядок элементов ACE в списке DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

[**Дефаултсекуритидескриптор**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) задается в специальном строковом формате с использованием [языка определения дескрипторов безопасности](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL). Для преобразования двоичной формы дескриптора безопасности в формат строки и наоборот можно использовать две функции. Это следующие функции:

-   [конвертсекуритидескриптортострингсекуритидескриптор](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [конвертстрингсекуритидескриптортосекуритидескриптор](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Дополнительные сведения и дескрипторы безопасности по умолчанию предопределенных классов объектов см. на страницах справочника по классам в справочнике по схеме Active Directory справочника по [службам домен Active Directory](active-directory-domain-services-reference.md).

Дополнительные сведения и пример кода, который считывает или изменяет свойство [**дефаултсекуритидескриптор**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) класса Object, см. в разделе [Чтение Дефаултсекуритидескриптор для класса Object](reading-the-defaultsecuritydescriptor-for-an-object-class.md) и [изменение дефаултсекуритидескриптор для класса Object](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).

 

 