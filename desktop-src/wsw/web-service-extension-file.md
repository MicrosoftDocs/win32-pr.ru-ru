---
title: Файл расширения веб-службы
description: В этом разделе описывается файл расширения веб-службы.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Веб-службы файла расширения веб-службы для Windows
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0802e31895aa5dd5051c94746e774033a1ebe677
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339709"
---
# <a name="web-service-extension-file"></a>Файл расширения веб-службы

В этом разделе описывается файл расширения веб-службы.


Файл WSX (расширение службы WCF) — это наш файл расширения, позволяющий приложению управлять локальными поведениями, не влияющими на представление данных передачи. Он должен быть расширяемым, чтобы мы могли добавлять новые функции в будущем без нарушения взаимодействия.

Общая структура WSX будет имитировать структуру файла XSD или WSDL, которая представляет собой XML-файл, который поддерживает ту же структуру, что и основной входной файл. Дополнительные атрибуты в том же именованном маркере в файле main определяют атрибуты, которые приложение хочет контролировать по умолчанию.

Мы можем не делать ничего здесь в M3. В версии v1 я могу увидеть, что мы поддерживаем следующие атрибуты:

Использование с указанием аргумента счетчика или поля параметра.

Это атрибут элемента, но применим только к типу массива. Атрибут Искаунтоф задает элемент массива. Поле счетчика/параметр не отображается на канале связи.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="FooInParam">
  <complexType> 
   <!-- MyArray field is presented in WSDL file as an element -->
    <element name="MyArrayCount" IsCountOf="MyArray"></element>
   </complexType>
  </element>
 </xs:schema>
```

Указание обратного вызова для чтения и записи для пользовательского типа

Эти атрибуты принудительно wsutil.exe для [**создания \_ пользовательского \_ типа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) для указанного типа. Пользовательский \_ атрибут реадкаллбакк указывает подпрограммы [**обратного вызова чтения**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) , а Custom \_ вритекаллбакк — подпрограммы [**обратного вызова записи**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

Для описания его локального поведения можно использовать соответствующий файл WSX:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">

 <element name="FooInParam" DataValidationRoutine="MyArrayValidation">
  <complexType> 
   <element name="MyLocalArrayCount" IsCountOf="MyArray"></element> 
  </complexType>
 </element>
</xs:schema>
```

WsUtil.exe создает следующий прототип для структуры:

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




