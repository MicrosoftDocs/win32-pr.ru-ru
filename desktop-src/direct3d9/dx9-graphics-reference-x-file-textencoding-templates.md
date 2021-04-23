---
description: Шаблоны определяют, как интерпретируется поток данных. данные обрабатываются с помощью определения шаблона. В этом разделе обсуждаются следующие аспекты шаблона и приводится пример шаблона.
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: Шаблоны (формат файла X, кодировка текста)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805194"
---
# <a name="templates-x-file-format-text-encoding"></a><span data-ttu-id="d0741-104">Шаблоны (формат файла X, кодировка текста)</span><span class="sxs-lookup"><span data-stu-id="d0741-104">Templates (X file format, text encoding)</span></span>

<span data-ttu-id="d0741-105">Шаблоны определяют, как интерпретируется поток данных. данные обрабатываются с помощью определения шаблона.</span><span class="sxs-lookup"><span data-stu-id="d0741-105">Templates define how the data stream is interpreted - the data is modulated by the template definition.</span></span> <span data-ttu-id="d0741-106">В этом разделе обсуждаются следующие аспекты шаблона и приводится пример шаблона.</span><span class="sxs-lookup"><span data-stu-id="d0741-106">This section discusses the following aspects of a template and provides an example template.</span></span>

<span data-ttu-id="d0741-107">Существует один специальный шаблон — шаблон заголовка.</span><span class="sxs-lookup"><span data-stu-id="d0741-107">There is one special template - the header template.</span></span> <span data-ttu-id="d0741-108">Рекомендуется, чтобы каждое приложение определяло шаблон заголовка и использовало его для определения сведений, относящихся к конкретному приложению, таких как сведения о версии.</span><span class="sxs-lookup"><span data-stu-id="d0741-108">It is recommended that each application define a header template and use it to define application-specific information, such as version information.</span></span> <span data-ttu-id="d0741-109">При наличии этот заголовок считывается API-интерфейсом формата файла. x.</span><span class="sxs-lookup"><span data-stu-id="d0741-109">If present, this header is read by the .x file format API.</span></span> <span data-ttu-id="d0741-110">Если элемент flags доступен, он используется для определения интерпретации следующих данных.</span><span class="sxs-lookup"><span data-stu-id="d0741-110">If a flags member is available, it is used to determine how the following data is interpreted.</span></span> <span data-ttu-id="d0741-111">Элемент flags, если он определен, должен иметь значение типа DWORD.</span><span class="sxs-lookup"><span data-stu-id="d0741-111">The flags member, if defined, should be a DWORD.</span></span> <span data-ttu-id="d0741-112">Один бит в настоящее время определен — бит 0.</span><span class="sxs-lookup"><span data-stu-id="d0741-112">One bit is currently defined - bit 0.</span></span> <span data-ttu-id="d0741-113">Если этот бит является понятным, следующие данные в файле являются двоичными.</span><span class="sxs-lookup"><span data-stu-id="d0741-113">If this bit is clear, the following data in the file is binary.</span></span> <span data-ttu-id="d0741-114">Если задано, то следующие данные являются текстом.</span><span class="sxs-lookup"><span data-stu-id="d0741-114">If set, the following data is text.</span></span> <span data-ttu-id="d0741-115">Для переключения между двоичным и текстовым файлами в файле можно использовать несколько объектов данных заголовков.</span><span class="sxs-lookup"><span data-stu-id="d0741-115">You can use multiple header data objects to switch between binary and text within the file.</span></span>

## <a name="template-form-name-and-uuid"></a><span data-ttu-id="d0741-116">Форма шаблона, имя и UUID</span><span class="sxs-lookup"><span data-stu-id="d0741-116">Template Form, Name, and UUID</span></span>

<span data-ttu-id="d0741-117">Шаблон имеет следующую форму.</span><span class="sxs-lookup"><span data-stu-id="d0741-117">A template has the following form.</span></span>


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



<span data-ttu-id="d0741-118">Имя шаблона — это буквенно-цифровое имя, которое может содержать символ подчеркивания ( \_ ).</span><span class="sxs-lookup"><span data-stu-id="d0741-118">The template name is an alphanumeric name that can include the underscore character (\_).</span></span> <span data-ttu-id="d0741-119">Оно не должно начинаться с цифры.</span><span class="sxs-lookup"><span data-stu-id="d0741-119">It must not begin with a digit.</span></span> <span data-ttu-id="d0741-120">UUID — это универсальный уникальный идентификатор, отформатированный в стандарт распределенной вычислительной среды Open Software Foundation и заключенный в угловые скобки (< >).</span><span class="sxs-lookup"><span data-stu-id="d0741-120">The UUID is a universally unique identifier formatted to the Open Software Foundation's Distributed Computing Environment standard and enclosed by angle brackets (< >).</span></span> <span data-ttu-id="d0741-121">Например: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span><span class="sxs-lookup"><span data-stu-id="d0741-121">For example: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span></span>

## <a name="template-members"></a><span data-ttu-id="d0741-122">Элементы шаблона</span><span class="sxs-lookup"><span data-stu-id="d0741-122">Template Members</span></span>

<span data-ttu-id="d0741-123">Элементы шаблона состоят из именованного типа данных, за которым следует необязательное имя или массив именованного типа данных.</span><span class="sxs-lookup"><span data-stu-id="d0741-123">Template members consist of a named data type followed by an optional name or an array of a named data type.</span></span> <span data-ttu-id="d0741-124">Допустимые примитивные типы данных определены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="d0741-124">Valid primitive data types are defined in the following table.</span></span>



| <span data-ttu-id="d0741-125">Тип</span><span class="sxs-lookup"><span data-stu-id="d0741-125">Type</span></span>    | <span data-ttu-id="d0741-126">Размер</span><span class="sxs-lookup"><span data-stu-id="d0741-126">Size</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="d0741-127">WORD</span><span class="sxs-lookup"><span data-stu-id="d0741-127">WORD</span></span>    | <span data-ttu-id="d0741-128">16 бит</span><span class="sxs-lookup"><span data-stu-id="d0741-128">16 bits</span></span>                            |
| <span data-ttu-id="d0741-129">DWORD</span><span class="sxs-lookup"><span data-stu-id="d0741-129">DWORD</span></span>   | <span data-ttu-id="d0741-130">32 бита</span><span class="sxs-lookup"><span data-stu-id="d0741-130">32 bits</span></span>                            |
| <span data-ttu-id="d0741-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="d0741-131">FLOAT</span></span>   | <span data-ttu-id="d0741-132">IEEE float</span><span class="sxs-lookup"><span data-stu-id="d0741-132">IEEE float</span></span>                         |
| <span data-ttu-id="d0741-133">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="d0741-133">DOUBLE</span></span>  | <span data-ttu-id="d0741-134">64 бита</span><span class="sxs-lookup"><span data-stu-id="d0741-134">64 bits</span></span>                            |
| <span data-ttu-id="d0741-135">CHAR</span><span class="sxs-lookup"><span data-stu-id="d0741-135">CHAR</span></span>    | <span data-ttu-id="d0741-136">8 бит</span><span class="sxs-lookup"><span data-stu-id="d0741-136">8 bits</span></span>                             |
| <span data-ttu-id="d0741-137">учар</span><span class="sxs-lookup"><span data-stu-id="d0741-137">UCHAR</span></span>   | <span data-ttu-id="d0741-138">8 бит</span><span class="sxs-lookup"><span data-stu-id="d0741-138">8 bits</span></span>                             |
| <span data-ttu-id="d0741-139">BYTE</span><span class="sxs-lookup"><span data-stu-id="d0741-139">BYTE</span></span>    | <span data-ttu-id="d0741-140">8 бит</span><span class="sxs-lookup"><span data-stu-id="d0741-140">8 bits</span></span>                             |
| <span data-ttu-id="d0741-141">STRING</span><span class="sxs-lookup"><span data-stu-id="d0741-141">STRING</span></span>  | <span data-ttu-id="d0741-142">Строка, заканчивающаяся нулем</span><span class="sxs-lookup"><span data-stu-id="d0741-142">NULL terminated string</span></span>             |
| <span data-ttu-id="d0741-143">CSTRING</span><span class="sxs-lookup"><span data-stu-id="d0741-143">CSTRING</span></span> | <span data-ttu-id="d0741-144">Форматированная строка C (не поддерживается)</span><span class="sxs-lookup"><span data-stu-id="d0741-144">Formatted C string (not supported)</span></span> |
| <span data-ttu-id="d0741-145">UNICODE</span><span class="sxs-lookup"><span data-stu-id="d0741-145">UNICODE</span></span> | <span data-ttu-id="d0741-146">Строка в Юникоде (не поддерживается)</span><span class="sxs-lookup"><span data-stu-id="d0741-146">Unicode string (not supported)</span></span>     |



 

<span data-ttu-id="d0741-147">Дополнительные типы данных, определенные шаблонами, обнаруженными ранее в потоке данных, также можно ссылаться в определении шаблона.</span><span class="sxs-lookup"><span data-stu-id="d0741-147">Additional data types defined by templates encountered earlier in the data stream can also be referenced within a template definition.</span></span> <span data-ttu-id="d0741-148">Прямые ссылки не допускаются.</span><span class="sxs-lookup"><span data-stu-id="d0741-148">No forward references are allowed.</span></span>

<span data-ttu-id="d0741-149">Любой допустимый тип данных может быть выражен в определении шаблона в виде массива.</span><span class="sxs-lookup"><span data-stu-id="d0741-149">Any valid data type can be expressed as an array in the template definition.</span></span> <span data-ttu-id="d0741-150">Базовый синтаксис показан в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d0741-150">The basic syntax is shown in the following example.</span></span>


```
array <data-type> <name>[<dimension-size>];
```



<span data-ttu-id="d0741-151"><> размера измерения может быть либо целым числом, либо именованной ссылкой на другой элемент шаблона, значение которого затем подставляется.</span><span class="sxs-lookup"><span data-stu-id="d0741-151"><dimension-size> can either be an integer or a named reference to another template member whose value is then substituted.</span></span> <span data-ttu-id="d0741-152">Массивы могут быть n-мерный, где n определяется числом парных квадратных скобок, завершающим оператор, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="d0741-152">Arrays can be n-dimensional, where n is determined by the number of paired square brackets trailing the statement, as in the following example.</span></span>


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a><span data-ttu-id="d0741-153">Ограничения шаблона</span><span class="sxs-lookup"><span data-stu-id="d0741-153">Template Restrictions</span></span>

<span data-ttu-id="d0741-154">Шаблоны могут быть открытыми, закрытыми или ограниченными.</span><span class="sxs-lookup"><span data-stu-id="d0741-154">Templates can be open, closed, or restricted.</span></span> <span data-ttu-id="d0741-155">Эти ограничения определяют, какие типы данных могут отображаться в немедленной иерархии объекта данных, определенного шаблоном.</span><span class="sxs-lookup"><span data-stu-id="d0741-155">These restrictions determine which data types can appear in the immediate hierarchy of a data object defined by the template.</span></span> <span data-ttu-id="d0741-156">Открытый шаблон не имеет ограничений, закрытый шаблон отклоняет все типы данных, а шаблон с ограниченным доступом допускает именованный список типов данных.</span><span class="sxs-lookup"><span data-stu-id="d0741-156">An open template has no restrictions, a closed template rejects all data types, and a restricted template allows a named list of data types.</span></span>

<span data-ttu-id="d0741-157">Синтаксис, указывающий на открытый шаблон, состоит из трех точек, заключенных в квадратные скобки.</span><span class="sxs-lookup"><span data-stu-id="d0741-157">The syntax for indicating an open template is three periods enclosed by square brackets.</span></span>


```
[ ... ]
```



<span data-ttu-id="d0741-158">Список именованных типов данных с разделителями-запятыми, а также их UUID, заключенные в квадратные скобки, обозначают ограниченный шаблон.</span><span class="sxs-lookup"><span data-stu-id="d0741-158">A comma-separated list of named data types followed optionally by their UUIDs enclosed by square brackets indicates a restricted template.</span></span>


```
[ { data-type [ UUID ] , } ... ]
```



<span data-ttu-id="d0741-159">Отсутствие любого из указанных выше указывает на закрытый шаблон.</span><span class="sxs-lookup"><span data-stu-id="d0741-159">The absence of either of the above indicates a closed template.</span></span>

## <a name="template-example"></a><span data-ttu-id="d0741-160">Пример шаблона</span><span class="sxs-lookup"><span data-stu-id="d0741-160">Template Example</span></span>

<span data-ttu-id="d0741-161">Ниже приведен пример шаблона.</span><span class="sxs-lookup"><span data-stu-id="d0741-161">The following shows an example template.</span></span>


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a><span data-ttu-id="d0741-162">См. также</span><span class="sxs-lookup"><span data-stu-id="d0741-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0741-163">Кодировка текста</span><span class="sxs-lookup"><span data-stu-id="d0741-163">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



