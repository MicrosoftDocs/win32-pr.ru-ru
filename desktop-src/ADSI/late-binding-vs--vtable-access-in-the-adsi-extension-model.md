---
title: Позднее связывание и доступ к vtable в модели расширения ADSI
description: Сдвоенный интерфейс обеспечивает прямой доступ к всем функциям vtable при отсутствии интерфейса диспетчеризации.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- позднее связывание и доступ к vtable в модели расширения ADSI
- расширения ADSI, позднее связывание и доступ vtable в модели расширения ADSI
- ADSI ADSI, пример кода Visual Basic, использование Иадсдуалинф
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105654368"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Позднее связывание и доступ к vtable в модели расширения ADSI

Сдвоенный интерфейс обеспечивает прямой доступ к всем функциям vtable при отсутствии интерфейса диспетчеризации. Клиент C/C++ может запросить указатель сдвоенного интерфейса и использовать прямой доступ к таблице vtable для вызова своих функций. Это обеспечивает более быстрый доступ, чем вызов функции с помощью функций [**IDispatch:: GetIdsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) и [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) . Это особенно справедливо в модели расширения, так как все сдвоенные интерфейсы в объекте расширения должны сначала делегировать свои **GetIDsOfNames** и **вызывать** функции в агрегатор (ADSI). Затем агрегатор должен выполнить дополнительные внутренние шаги, чтобы выяснить, какой объект расширения, возможно, включая сам агрегатор, предоставляет поддержку функции, которая называется, и перенаправить вызов к соответствующему объекту.

Visual Basic также вызывает функцию с двумя интерфейсами, используя прямой доступ к таблице vtable, если у нее есть указатель на интерфейс и доступ к данным типа из библиотеки типов. Клиенты ADSI, написанные на Visual Basic, могут указать указатель на сдвоенный интерфейс, например [**iAds**](/windows/desktop/api/Iads/nn-iads-iads), явно, и таким образом разрешить доступ vtable к функциям в интерфейсе.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Так как интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) не поддерживает доступ vtable, этот пример не применяется. Это значит, что функция диспетчеризации всегда вызывается только с помощью функций [**IDispatch:: GetIdsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) и [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .

Текущие выпуски VBScript и JScript также не поддерживают доступ к vtable. Таким образом, сдвоенный интерфейс в среде VBScript или JScript работает как интерфейс диспетчеризации.

 

 