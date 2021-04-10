---
title: Проверка прав доступа к элементу управления в ACL объекта
description: Чтобы проверить права доступа к списку управления доступом объекта, используйте функцию Акцессчеккбитипересултлист.
ms.assetid: 5a609622-6a1a-46ae-a336-afec504225c7
ms.tgt_platform: multiple
keywords:
- Проверка прав доступа к элементу управления в ACL объекта Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10170bd496da14657356a2334015975da1cc02ff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "104069811"
---
# <a name="checking-a-control-access-right-in-an-objects-acl"></a>Проверка прав доступа к элементу управления в ACL объекта

Чтобы проверить права доступа к списку управления доступом объекта, используйте функцию [**акцессчеккбитипересултлист**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) . Для использования этой функции приложению требуется указатель на [**\_ дескриптор безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) объекта, а не интерфейса [**иадссекуритидескриптор**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) в COM-объект дескриптора безопасности ADSI.

Чтобы проверить доступ для управляемого права доступа к объекту, выполните следующие действия.

1.  Получите указатель интерфейса [**идиректорйобжект**](/windows/desktop/api/iads/nn-iads-idirectoryobject) на объект.
2.  Чтобы получить дескриптор безопасности объекта, используйте метод [**идиректорйобжект:: жетобжектаттрибутес**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) . Имя свойства, содержащего дескриптор безопасности, — [**нтсекуритидескриптор**](/windows/desktop/ADSchema/a-ntsecuritydescriptor). Свойство возвращается в виде указателя на структуру [**\_ дескриптора безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) .
3.  Используйте структуру [**\_ дескрипторов безопасности**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) с функцией [**акцессчеккбитипересултлист**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) для проверки разрешений на доступ к указанному элементу управления для указанного клиента.

Пример кода в [примере кода для проверки прав доступа к элементу управления в списке ACL объекта](example-code-for-checking-a-control-access-right-in-an-objectampaposs-acl.md) показывает, как это сделать.

 

 