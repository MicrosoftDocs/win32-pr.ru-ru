---
title: Создание идентификаторов UUID интерфейса
description: Создание универсальных уникальных идентификаторов интерфейса (UUID) и использование uuidgen.
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775740"
---
# <a name="generating-interface-uuids"></a><span data-ttu-id="930ec-103">Создание идентификаторов UUID интерфейса</span><span class="sxs-lookup"><span data-stu-id="930ec-103">Generating Interface UUIDs</span></span>

<span data-ttu-id="930ec-104">В этом разделе представлены сведения об универсальных уникальных идентификаторах (UUID) и служебной программе uuidgen в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="930ec-104">This section presents information on Universal Unique Identifiers (UUIDs) and the Uuidgen utility in the following topics:</span></span>

-   [<span data-ttu-id="930ec-105">Что такое UUID?</span><span class="sxs-lookup"><span data-stu-id="930ec-105">What is a UUID?</span></span>](#what-is-a-uuid)
-   [<span data-ttu-id="930ec-106">Использование uuidgen</span><span class="sxs-lookup"><span data-stu-id="930ec-106">Using Uuidgen</span></span>](#using-uuidgen)

## <a name="what-is-a-uuid"></a><span data-ttu-id="930ec-107">Что такое UUID?</span><span class="sxs-lookup"><span data-stu-id="930ec-107">What is a UUID?</span></span>

<span data-ttu-id="930ec-108">Все интерфейсы должны быть однозначно идентифицированы в сети, чтобы клиенты могли их найти.</span><span class="sxs-lookup"><span data-stu-id="930ec-108">All interfaces must be uniquely identified on a network so that clients can find them.</span></span> <span data-ttu-id="930ec-109">В небольших сетях только имя интерфейса может быть достаточным для его распознавания.</span><span class="sxs-lookup"><span data-stu-id="930ec-109">On small networks, the interface's name alone may be sufficient to identify it.</span></span> <span data-ttu-id="930ec-110">Однако это обычно нецелесообразно для больших сетей.</span><span class="sxs-lookup"><span data-stu-id="930ec-110">However, that is usually not feasible on large networks.</span></span> <span data-ttu-id="930ec-111">Таким образом, разработчики обычно присваивают каждому интерфейсу универсальный уникальный идентификатор (UUID, взаимозаменяемый с термином GUID или глобальный уникальный идентификатор).</span><span class="sxs-lookup"><span data-stu-id="930ec-111">Therefore, developers typically assign a Universal Unique Identifier (UUID, interchangeable with the term GUID, or Globally Unique Identifier) to each interface.</span></span> <span data-ttu-id="930ec-112">UUID — это строка, содержащая набор шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="930ec-112">A UUID is a string that contains a set of hexadecimal digits.</span></span> <span data-ttu-id="930ec-113">Каждый интерфейс имеет другой UUID.</span><span class="sxs-lookup"><span data-stu-id="930ec-113">Each interface has a different UUID.</span></span> <span data-ttu-id="930ec-114">Дополнительные сведения см. в разделе [строковый UUID](string-uuid.md).</span><span class="sxs-lookup"><span data-stu-id="930ec-114">For details, see [String UUID](string-uuid.md).</span></span>

<span data-ttu-id="930ec-115">Текстовое представление UUID — это строка, состоящая из 8 шестнадцатеричных цифр, за которыми следует дефис, за которым следуют три группы, разделенные дефисами 4 шестнадцатеричных цифр, за которыми следует дефис, за которым следуют 12 шестнадцатеричных цифр.</span><span class="sxs-lookup"><span data-stu-id="930ec-115">The textual representation of a UUID is a string consisting of 8 hexadecimal digits followed by a hyphen, followed by three hyphen-separated groups of 4 hexadecimal digits, followed by a hyphen, followed by 12 hexadecimal digits.</span></span> <span data-ttu-id="930ec-116">Следующий пример является допустимой строкой UUID:</span><span class="sxs-lookup"><span data-stu-id="930ec-116">The following example is a valid UUID string:</span></span>

<span data-ttu-id="930ec-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span><span class="sxs-lookup"><span data-stu-id="930ec-117">ba209999-0c6c-11d2-97cf-00c04f8eea45</span></span>

<span data-ttu-id="930ec-118">Пустые UUID называются пустыми UUID, а не **нулевыми** UUID.</span><span class="sxs-lookup"><span data-stu-id="930ec-118">Empty UUIDs are referred to as nil UUIDs rather than **NULL** UUIDs.</span></span> <span data-ttu-id="930ec-119">Термин nil означает все, что равно нулю, пусто, пусто или не инициализировано.</span><span class="sxs-lookup"><span data-stu-id="930ec-119">The term nil indicates anything that is zero, blank, empty, or uninitialized.</span></span> <span data-ttu-id="930ec-120">Пустая строка, пустая запись базы данных или неинициализированный UUID являются примерами пустых значений.</span><span class="sxs-lookup"><span data-stu-id="930ec-120">An empty string, an empty database record, or an uninitialized UUID are all examples of nil values.</span></span>

> [!Note]  
> <span data-ttu-id="930ec-121">Значение **null** — это конкретное нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="930ec-121">The value **NULL** is the specific value zero.</span></span> <span data-ttu-id="930ec-122">Он часто используется в программировании C и C++ вместе с указателями.</span><span class="sxs-lookup"><span data-stu-id="930ec-122">It is often used in C and C++ programming in conjunction with pointers.</span></span> <span data-ttu-id="930ec-123">Nil является более общим термином, чем **null**.</span><span class="sxs-lookup"><span data-stu-id="930ec-123">Nil is a more general term than **NULL**.</span></span> <span data-ttu-id="930ec-124">Неинициализированные UUID интерфейсов объектов всегда должны называться пустыми UUID, а не **нулевыми** UUID.</span><span class="sxs-lookup"><span data-stu-id="930ec-124">Uninitialized object interface UUIDs should always be referred to as nil UUIDs rather than **NULL** UUIDs.</span></span>

 

## <a name="using-uuidgen"></a><span data-ttu-id="930ec-125">Использование uuidgen</span><span class="sxs-lookup"><span data-stu-id="930ec-125">Using Uuidgen</span></span>

<span data-ttu-id="930ec-126">Корпорация Майкрософт предоставляет служебную программу с именем uuidgen для создания идентификаторов UUID.</span><span class="sxs-lookup"><span data-stu-id="930ec-126">Microsoft provides a utility program called Uuidgen to generate your UUIDs.</span></span> <span data-ttu-id="930ec-127">Служебная программа Uuidgen создает UUID в формате IDL-файла или в формате языка C.</span><span class="sxs-lookup"><span data-stu-id="930ec-127">The Uuidgen utility generates the UUID in IDL file format or C-language format.</span></span>

<span data-ttu-id="930ec-128">При запуске служебной программы uuidgen из командной строки можно использовать следующие параметры команды.</span><span class="sxs-lookup"><span data-stu-id="930ec-128">When you run the Uuidgen utility from the command line, you can use the following command switches.</span></span>



| <span data-ttu-id="930ec-129">Uuidgen, параметр</span><span class="sxs-lookup"><span data-stu-id="930ec-129">Uuidgen switch</span></span>           | <span data-ttu-id="930ec-130">Описание</span><span class="sxs-lookup"><span data-stu-id="930ec-130">Description</span></span>                                                                |
|--------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="930ec-131">**/I**</span><span class="sxs-lookup"><span data-stu-id="930ec-131">**/I**</span></span>                   | <span data-ttu-id="930ec-132">Выводит UUID в шаблон интерфейса IDL.</span><span class="sxs-lookup"><span data-stu-id="930ec-132">Outputs UUID to an IDL interface template.</span></span>                                 |
| <span data-ttu-id="930ec-133">**/s**</span><span class="sxs-lookup"><span data-stu-id="930ec-133">**/s**</span></span>                   | <span data-ttu-id="930ec-134">Выводит UUID в виде инициализированной структуры C.</span><span class="sxs-lookup"><span data-stu-id="930ec-134">Outputs UUID as an initialized C structure.</span></span>                                |
| <span data-ttu-id="930ec-135">**/o** < *имя файла*></span><span class="sxs-lookup"><span data-stu-id="930ec-135">**/o**<*filename*></span></span> | <span data-ttu-id="930ec-136">Перенаправляет выходные данные в файл; указывается сразу после параметра **/o** .</span><span class="sxs-lookup"><span data-stu-id="930ec-136">Redirects output to a file; specified immediately after the **/o** switch.</span></span> |
| <span data-ttu-id="930ec-137">**/n** < *число*></span><span class="sxs-lookup"><span data-stu-id="930ec-137">**/n**<*number*></span></span>   | <span data-ttu-id="930ec-138">Указывает число создаваемых UUID.</span><span class="sxs-lookup"><span data-stu-id="930ec-138">Specifies the number of UUIDs to generate.</span></span>                                 |
| <span data-ttu-id="930ec-139">**/v**</span><span class="sxs-lookup"><span data-stu-id="930ec-139">**/v**</span></span>                   | <span data-ttu-id="930ec-140">Отображает сведения о версии uuidgen.</span><span class="sxs-lookup"><span data-stu-id="930ec-140">Displays version information about Uuidgen.</span></span>                                |
| <span data-ttu-id="930ec-141">**/h** или **?**</span><span class="sxs-lookup"><span data-stu-id="930ec-141">**/h** or **?**</span></span>          | <span data-ttu-id="930ec-142">Отображает сводку по параметрам команды.</span><span class="sxs-lookup"><span data-stu-id="930ec-142">Displays command-option summary.</span></span>                                           |



 

<span data-ttu-id="930ec-143">Как правило, используется служебная программа Uuidgen, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="930ec-143">Typically, you will use the Uuidgen utility as shown in the following example.</span></span>

<span data-ttu-id="930ec-144">**uuidgen-i-Омяпп. idl**</span><span class="sxs-lookup"><span data-stu-id="930ec-144">**uuidgen -i -oMyApp.idl**</span></span>

<span data-ttu-id="930ec-145">Эта команда создает UUID и сохраняет его в файле MIDL, который можно использовать в качестве шаблона.</span><span class="sxs-lookup"><span data-stu-id="930ec-145">This command generates a UUID and stores it in a MIDL file that you can use as a template.</span></span> <span data-ttu-id="930ec-146">При выполнении предыдущей команды содержимое файла MyApp. idl будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="930ec-146">When the preceding command is executed, the contents of MyApp.idl are similar to the following:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

<span data-ttu-id="930ec-147">Следующим шагом будет замена имени заполнителя, INTERFACENAME, фактическим именем интерфейса.</span><span class="sxs-lookup"><span data-stu-id="930ec-147">The next step would be to replace the placeholder name, INTERFACENAME, with the actual name of your interface.</span></span>

 

 




