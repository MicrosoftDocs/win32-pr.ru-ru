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
# <a name="web-service-extension-file"></a><span data-ttu-id="84365-106">Файл расширения веб-службы</span><span class="sxs-lookup"><span data-stu-id="84365-106">Web Service Extension File</span></span>

<span data-ttu-id="84365-107">В этом разделе описывается файл расширения веб-службы.</span><span class="sxs-lookup"><span data-stu-id="84365-107">This section outlines Web Service extension file.</span></span>


<span data-ttu-id="84365-108">Файл WSX (расширение службы WCF) — это наш файл расширения, позволяющий приложению управлять локальными поведениями, не влияющими на представление данных передачи.</span><span class="sxs-lookup"><span data-stu-id="84365-108">WSX file (WCF service extension) is our extension file to allow application to manipulate local behaviors that do not affect wire data representation.</span></span> <span data-ttu-id="84365-109">Он должен быть расширяемым, чтобы мы могли добавлять новые функции в будущем без нарушения взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="84365-109">It should be extensible that we can add new features in the future without breaking interoperability.</span></span>

<span data-ttu-id="84365-110">Общая структура WSX будет имитировать структуру файла XSD или WSDL, которая представляет собой XML-файл, который поддерживает ту же структуру, что и основной входной файл.</span><span class="sxs-lookup"><span data-stu-id="84365-110">The overall structure of WSX would mimic the structure of XSD or WSDL file, which is a XML file that maintains the same structure as the main input file.</span></span> <span data-ttu-id="84365-111">Дополнительные атрибуты в том же именованном маркере в файле main определяют атрибуты, которые приложение хочет контролировать по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="84365-111">Extra attributes on the same named token in main file would specify the attributes that application wants to control over the default behavior.</span></span>

<span data-ttu-id="84365-112">Мы можем не делать ничего здесь в M3.</span><span class="sxs-lookup"><span data-stu-id="84365-112">We might not do anything here in M3.</span></span> <span data-ttu-id="84365-113">В версии v1 я могу увидеть, что мы поддерживаем следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="84365-113">In V1, I can see we support the following attributes:</span></span>

<span data-ttu-id="84365-114">Использование с указанием аргумента счетчика или поля параметра.</span><span class="sxs-lookup"><span data-stu-id="84365-114">Usage Specifying count argument/parameter field.</span></span>

<span data-ttu-id="84365-115">Это атрибут элемента, но применим только к типу массива.</span><span class="sxs-lookup"><span data-stu-id="84365-115">This is an element attribute but applicable to array type only.</span></span> <span data-ttu-id="84365-116">Атрибут Искаунтоф задает элемент массива.</span><span class="sxs-lookup"><span data-stu-id="84365-116">IsCountOf attribute specifies the array element.</span></span> <span data-ttu-id="84365-117">Поле счетчика/параметр не отображается на канале связи.</span><span class="sxs-lookup"><span data-stu-id="84365-117">The count field/parameter does not appear on wire.</span></span>

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

<span data-ttu-id="84365-118">Указание обратного вызова для чтения и записи для пользовательского типа</span><span class="sxs-lookup"><span data-stu-id="84365-118">Specifying read/write callback for custom type</span></span>

<span data-ttu-id="84365-119">Эти атрибуты принудительно wsutil.exe для [**создания \_ пользовательского \_ типа WS**](/windows/desktop/api/WebServices/ne-webservices-ws_type) для указанного типа.</span><span class="sxs-lookup"><span data-stu-id="84365-119">These attributes force wsutil.exe to generate [**WS\_CUSTOM\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) for specified type.</span></span> <span data-ttu-id="84365-120">Пользовательский \_ атрибут реадкаллбакк указывает подпрограммы [**обратного вызова чтения**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) , а Custom \_ вритекаллбакк — подпрограммы [**обратного вызова записи**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) .</span><span class="sxs-lookup"><span data-stu-id="84365-120">custom\_readcallback attribute specifies the [**read callback**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) routine, and custom\_writecallback specifies the [**write callback**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) routine.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

<span data-ttu-id="84365-121">Для описания его локального поведения можно использовать соответствующий файл WSX:</span><span class="sxs-lookup"><span data-stu-id="84365-121">We can have a matching WSX file to describe its local behavior:</span></span>

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

<span data-ttu-id="84365-122">WsUtil.exe создает следующий прототип для структуры:</span><span class="sxs-lookup"><span data-stu-id="84365-122">WsUtil.exe generates the following prototype for the structure:</span></span>

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




