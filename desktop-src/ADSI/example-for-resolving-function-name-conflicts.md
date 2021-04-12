---
title: Пример разрешения конфликтов имен функций
description: В этом разделе описывается, как разрешать конфликты имен функций при создании расширения для ADSI.
ms.assetid: 8121f037-3845-44ba-a2cd-8d7f15e0beb2
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, пример кода Visual Basic, разрешение конфликтов имен функций
- разрешение конфликтов имен функций ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 049f9ce6447bf6d6ead783db3e34f74374333f10
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339249"
---
# <a name="example-for-resolving-function-name-conflicts"></a>Пример разрешения конфликтов имен функций

Рассмотрим следующий пример.

-   IADs0 не поддерживает Func0.
-   IADs1 поддерживает func1 и Func0.
-   IADs2 поддерживает Func2 и Func0.

Все три интерфейса являются сдвоенными интерфейсами.


```C++
IADs0 : IDispatch
{
    OtherFunc();
}

IADs1 : IDispatch
{
    Func0() 
    Func1();
}

IADs2 : IDispatch
{
    Func0()
    Func2();
}
```




```VB
Dim myInf1 as IADs1
 
myInf1.Func1  ' IADs1::Func1 is invoked using direct vtable access 
 
myInf1.Func2  ' IADs2::Func2 is invoked using GetIDsOfNames/Invoke
```



Имейте в виду, что несмотря на то, что IADs1 не поддерживает Func2, клиент ADSI распознает один интерфейс [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) , поддерживающий все сдвоенные и диспетчеризации интерфейсы в модели. Таким же клиент ADSI может напрямую вызвать Func2 с помощью myInf1. Func2, не разрешая интерфейс, поддерживающий Func2.


```VB
myInf1.Func2
```



Как IADs1, так и IADs2 имеют функцию с именем Func0, но IADs1:: Func0 вызывается напрямую с помощью доступа к таблице vtable, так как оба следующих условия применимы к клиенту:

-   Клиент имеет указатель на объект IADs1 с двойным интерфейсом, который имеет функцию с именем Func0.
-   Visual Basic поддерживает прямой доступ к vtable, предполагая, что тип данных доступен через библиотеку типов.

В следующем примере кода клиент имеет сдвоенный указатель на IADs2 вместо IADs1. Таким образом, IADs2:: Func0 вызывается с помощью прямого доступа vtable.


```VB
Dim myInf2 as IADs2
Set myInf2 = myInf1 ' Query for pointer to IADs2 
myInf2.Func0
```



Опять же, в следующем примере кода и IADs1, и IADs2 имеют функцию с именем Func0, но здесь клиент имеет указатель на сдвоенный интерфейс IADs0, который не имеет функции с именем Func0. Таким образом, прямой доступ к vtable не может быть выполнен. Вместо этого вызываются [**IDispatch:: GetIdsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) и [**Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) для вызова Func0.


```VB
Dim myInfNone as IADs0
Set myInfNone = myInf1    ' The aggregated object that 
   ' supports IADs1 and IADs2.
myInfNone.Func0
```



Рассмотрим следующие два варианта:

-   IADs1 и IADs2 реализуются двумя COM-компонентами, Ext1 и ext2 соответственно. Если Ext1 находится перед ext2 в реестре, вызывается IADs1:: Func0. Однако если ext2 находится в реестре первыми, вызывается IADs2:: Func0.
-   Если IADs1 и ADs2 реализуются одним и тем же объектом расширения, Func0 всегда вызывается методами [**иадсекстенсион::P риватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) и [**приватеинвоке**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) расширения.

Разработчик расширений должен определить, как разрешать конфликты функций или свойств различных сдвоенных интерфейсов [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) с одинаковым именем в расширении. Реализация методов [**иадсекстенсион::P риватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) и [**приватеинвоке**](/windows/desktop/api/Iads/nf-iads-iadsextension-privateinvoke) должна устранить этот конфликт. Например, если используются IMyInterface1:: Func1 и IMyInterface2:: Func1, где IMyInterface1 и IMyInterface2 — сдвоенные интерфейсы **IDispatch** , поддерживаемые одним и тем же объектом расширения. Методы **приватежетидсофнамес** и **приватеинвоке** должны определять, какой func1 следует вызывать всегда.

То же относится и к конфликтующим идентификаторам DISPID в разных интерфейсах Dual или [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .

Например, DISPID IMyInterface1:: Y имеет значение 2 в файле IMyInterface1. odl или IMyInterface1. idl. Идентификатор DISPID IMyInterface2:: X также равен 2 в iMyInterface2. ODL. [**Иадсекстенсион::P риватежетидсофнамес**](/windows/desktop/api/Iads/nf-iads-iadsextension-privategetidsofnames) должен возвращать уникальный идентификатор DISPID в самом расширении для каждого, вместо того чтобы возвращать один и тот же DISPID для обоих.

ADSI разрешает первую проблему, не поддерживая несколько интерфейсов с конфликтующими именами функций или свойств. Она разрешает вторую проблему, добавляя уникальный объект, который находится в том же объекте расширения, но не в неиспользуемые биты DISPID.

 

 