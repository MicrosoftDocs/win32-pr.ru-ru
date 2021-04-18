---
title: delete cache
description: Очищает весь кэш URL-адресов или удаляет записи в соответствии с указанным URL-адресом.
ms.assetid: 499ce0f9-01db-4648-89f7-1ecafd25a805
keywords:
- удалить HTTP-кэш кэша
topic_type:
- apiref
api_name:
- delete cache
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f963d12812140d11923460235ef780a621ba3db5
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2019
ms.locfileid: "105681572"
---
# <a name="delete-cache"></a>delete cache

Очищает весь кэш URL-адресов или удаляет записи в соответствии с указанным URL-адресом.

``` syntax
delete cache [url=]string [[recursive=]{yes|no}]
 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>**\[URL = \] * * * строка*
</dt> <dd>

Обязательный. Указывает полный URL-адрес.

</dd> </dl>

<dl> <dt>

<span id="_recursive___yes_no_"></span><span id="_RECURSIVE___YES_NO_"></span>**\[recursive = \] {Да \| нет}**
</dt> <dd>

Если да, удаляет все записи с указанным URL-адресом.

</dd> </dl>

## <a name="examples"></a>Примеры

**удалить URL-адрес кэша = https://www.contoso.com:80/myresource/ recursive = да**

 

 




