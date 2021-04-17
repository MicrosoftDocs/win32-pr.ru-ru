---
title: Синтаксис объекта (DS-DN)
description: Строка, содержащая различающееся имя (DN).
ms.assetid: 089104c4-ff82-49ea-a8db-a6dadc3a18bc
ms.tgt_platform: multiple
keywords:
- Схема AD синтаксиса object (DS-DN)
topic_type:
- apiref
api_name:
- Object(DS-DN)
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45154985fa7fbfc4d95d563196357d43eac2ea72
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104535663"
---
# <a name="objectds-dn-syntax"></a>Синтаксис объекта (DS-DN)

Строка, содержащая различающееся имя (DN). Для атрибутов с этим синтаксисом Active Directory обрабатывает значения атрибутов как ссылки на объект, идентифицируемый DN, и автоматически обновляет значение при перемещении или переименовании объекта. Для запросов, содержащих атрибуты синтаксиса DN в фильтре, укажите полные различающиеся имена. Подстановочные знаки (например, CN = John \* ) не поддерживаются.



| Ввод | Значение |
|--------------|------------------------------------------------------------------------|
| Имя         | Object(DS-DN)                                                          |
| Идентификатор синтаксиса    | 2.5.5.1                                                                |
| ИДЕНТИФИКАТОР OM        | 127                                                                    |
| Тип MAPI    | OBJECT                                                                 |
| Тип ADS     | \_строка различающегося имени адстипе \_                                                    |
| Тип варианта | VT \_ BSTR                                                               |
| Тип SDS     | [System.String](/dotnet/api/system.string) |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[System.String](/dotnet/api/system.string)
</dt> </dl>

 

 
