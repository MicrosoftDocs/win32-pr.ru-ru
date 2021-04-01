---
title: add urlacl
description: Резервирует указанный URL-адрес для пользователей и учетных записей без прав администратора.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Добавить urlacl HTTP
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/10/2021
ms.locfileid: "104000297"
---
# <a name="add-urlacl"></a>add urlacl

Резервирует указанный URL-адрес для пользователей и учетных записей без прав администратора. Список управления доступом на уровне пользователей (DACL) можно указать с помощью имени учетной записи с параметрами Listen и Delegate либо с помощью строки на языке определения дескрипторов безопасности (SDDL).

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a>Параметры

<dl> <dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[URL =] строка**
</dt> <dd>

Указывает полный URL-адрес.

</dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[USER =] строка**
</dt> <dd>

Указывает имя пользователя или группы пользователей.

</dd> <dt>

<span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[Listen = {да \| нет}\]**
</dt> <dd>

Задает одно из следующих значений:

-   Да. разрешает пользователю регистрировать URL-адреса. Это значение по умолчанию.
-   Нет: запрещает пользователю регистрировать URL-адреса.

</dd> <dt>

<span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[Delegate = {да \| нет}\]**
</dt> <dd>

Задает одно из следующих значений:

-   Да. разрешает пользователю делегировать URL-адреса.
-   Нет: запрещает пользователю делегировать URL-адреса. Это значение по умолчанию.

</dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] строка**
</dt> <dd>

Указывает строку SDDL, описывающую DACL.

</dd> </dl>

## <a name="examples"></a>Примеры

* add urlacl url=https://+:80/MyUri user=DOMAIN\\ user

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes

* add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no

 
## <a name="see-also"></a>См. также:

* [Команды HTTP для Netsh](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 