---
title: import - атрибут
description: Директива Import указывает другой файл IDL, ODL или заголовок, содержащий определения, на которые вы хотите ссылаться из основного IDL-файла.
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- Импорт атрибута MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104336985"
---
# <a name="import-attribute"></a><span data-ttu-id="41e5b-104">import - атрибут</span><span class="sxs-lookup"><span data-stu-id="41e5b-104">import attribute</span></span>

<span data-ttu-id="41e5b-105">Директива **Import** указывает другой файл IDL, ODL или заголовок, содержащий определения, на которые вы хотите ссылаться из основного IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="41e5b-105">The **import** directive specifies another IDL, ODL, or header file containing definitions you wish to reference from your main IDL file.</span></span>

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a><span data-ttu-id="41e5b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="41e5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41e5b-107">*filename*</span><span class="sxs-lookup"><span data-stu-id="41e5b-107">*filename*</span></span> 
</dt> <dd>

<span data-ttu-id="41e5b-108">Задает имя импортируемого файла header, IDL или ODL.</span><span class="sxs-lookup"><span data-stu-id="41e5b-108">Specifies the name of the header, IDL, or ODL file to import.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="41e5b-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="41e5b-109">Remarks</span></span>

<span data-ttu-id="41e5b-110">С помощью директивы **Import** все инструкции IDL в импортируемом файле, такие как typedef, объявления константы и определения интерфейса, становятся доступными для импорта. IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="41e5b-110">With the **import** directive, all IDL statements in the imported file, such as typedefs, constant declarations, and interface definitions become available to the importing .IDL file.</span></span>

<span data-ttu-id="41e5b-111">Импортированный файл обрабатывается отдельно (это означает, что препроцессор CPP вызывается независимо) из импортированного IDL-файла.</span><span class="sxs-lookup"><span data-stu-id="41e5b-111">The imported file is processed separately (meaning that CPP preprocessor is invoked independently) from the importing IDL file.</span></span> <span data-ttu-id="41e5b-112">Таким образом, директивы предварительного процессора, такие как \# define, не переносятся из импортированного или IDL-файла в импортируемый IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="41e5b-112">In this way, pre-processor directives, such as \#define, do not carry over from an imported header or IDL file to the importing IDL file.</span></span>

<span data-ttu-id="41e5b-113">Как и в макросе препроцессора C **\#**-Language, Директива **Import** указывает компилятору включать типы данных, определенные в импортированных IDL-файлах.</span><span class="sxs-lookup"><span data-stu-id="41e5b-113">Like the C-language preprocessor macro **\#include**, the **import** directive tells the compiler to include data types that were defined in the imported IDL files.</span></span> <span data-ttu-id="41e5b-114">В отличие от директивы **\# include** , Директива **Import** игнорирует прототипы процедур, так как для импортированного файла не создаются заглушки.</span><span class="sxs-lookup"><span data-stu-id="41e5b-114">Unlike the **\#include** directive, the **import** directive ignores procedure prototypes, since no stubs are generated for anything in the imported file.</span></span>

<span data-ttu-id="41e5b-115">Конкретные сведения об использовании **импорта** для включения файлов заголовков в IDL-файле см. в разделе [Импорт системных файлов заголовков](importing-system-header-files.md).</span><span class="sxs-lookup"><span data-stu-id="41e5b-115">For specific information on using **import** to include header files in an IDL file, see [Importing System Header Files](importing-system-header-files.md).</span></span>

<span data-ttu-id="41e5b-116">Заголовок C-Language (. H) файл, созданный для интерфейса, не содержит непосредственно импортированных типов, а вместо этого создает директиву **\# include** для файла заголовка, соответствующего импортированному интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="41e5b-116">The C-language header (.H) file generated for the interface does not directly contain the imported types but instead generates a **\#include** directive for the header file corresponding to the imported interface.</span></span> <span data-ttu-id="41e5b-117">Например, при импорте базы. IDL в ПРОИЗВОДный. IDL, сформированный файл заголовка является ПРОИЗВОДным. H будет содержать директиву, **\# включающую** Base. H.</span><span class="sxs-lookup"><span data-stu-id="41e5b-117">For example, when you import BASE.IDL into your DERIVED.IDL, the generated header file DERIVED.H will contain the directive **\#include** BASE.H.</span></span>

<span data-ttu-id="41e5b-118">Применяются следующие правила.</span><span class="sxs-lookup"><span data-stu-id="41e5b-118">The following rules apply:</span></span>

-   <span data-ttu-id="41e5b-119">Ключевое слово **Import** является необязательным и может ОТОБРАЖАТЬСЯ в IDL-файле ноль или более раз.</span><span class="sxs-lookup"><span data-stu-id="41e5b-119">The **import** keyword is optional and can appear zero or more times in the IDL file.</span></span>
-   <span data-ttu-id="41e5b-120">Каждое ключевое слово **Import** может быть связано с более чем одним именем файла.</span><span class="sxs-lookup"><span data-stu-id="41e5b-120">Each **import** keyword can be associated with more than one file name.</span></span>
-   <span data-ttu-id="41e5b-121">Несколько имен файлов следует разделять запятыми.</span><span class="sxs-lookup"><span data-stu-id="41e5b-121">Separate multiple file names with commas.</span></span>
-   <span data-ttu-id="41e5b-122">Имя файла необходимо заключить в кавычки и завершить инструкцию import точкой с запятой (;).</span><span class="sxs-lookup"><span data-stu-id="41e5b-122">You must enclose the file name within quotation marks and end the import statement with a semicolon (;).</span></span>
-   <span data-ttu-id="41e5b-123">Вы можете импортировать интерфейс, не имеющий атрибутов, в другой IDL-файл.</span><span class="sxs-lookup"><span data-stu-id="41e5b-123">You can import an interface that has no attributes into another IDL file.</span></span> <span data-ttu-id="41e5b-124">Однако интерфейс должен содержать только типы типа. она не может содержать какие бы то ни было процедуры.</span><span class="sxs-lookup"><span data-stu-id="41e5b-124">However, the interface must contain only datatypes; it cannot contain any procedures.</span></span> <span data-ttu-id="41e5b-125">Если в импортированном интерфейсе содержится даже одна процедура, необходимо указать атрибут [**Local**](local.md) или [**UUID**](uuid.md) .</span><span class="sxs-lookup"><span data-stu-id="41e5b-125">If even one procedure is contained in the imported interface, you must specify a [**local**](local.md) or [**UUID**](uuid.md) attribute.</span></span>
-   <span data-ttu-id="41e5b-126">Функция **импорта** идемпотентâ «в том, что импорт интерфейса более одного раза не имеет дополнительного воздействия.</span><span class="sxs-lookup"><span data-stu-id="41e5b-126">The **import** function is idempotentÂ â€”Â that is, importing an interface more than once has no additional effect.</span></span>

> [!Note]  
> <span data-ttu-id="41e5b-127">Поведение директивы **Import** не зависит от режима компилятора MIDL переключает [**/МС \_ ext**](-ms-ext.md) (по умолчанию), [**/ОСФ**](-osf.md)и [**/АПП \_ config**](-app-config.md).</span><span class="sxs-lookup"><span data-stu-id="41e5b-127">The behavior of the **import** directive is independent of the MIDL compiler mode switches [**/ms\_ext**](-ms-ext.md) (the default), [**/osf**](-osf.md), and [**/app\_config**](-app-config.md).</span></span> <span data-ttu-id="41e5b-128">Однако режим компилятора (**/ОСФ** или **/МС \_ ext**) может повлиять на Декорирование атрибутов указателя на импортированных типах.</span><span class="sxs-lookup"><span data-stu-id="41e5b-128">However, the compiler mode (**/osf** or **/ms\_ext**) can affect pointer attribute decoration on imported types.</span></span> <span data-ttu-id="41e5b-129">Дополнительные сведения см. в разделе [наследование типа атрибута указателя](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span><span class="sxs-lookup"><span data-stu-id="41e5b-129">For details see [Pointer-Attribute Type Inheritance](/windows/desktop/Rpc/pointer-attribute-type-inheritance).</span></span>

 

## <a name="examples"></a><span data-ttu-id="41e5b-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="41e5b-130">Examples</span></span>

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a><span data-ttu-id="41e5b-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="41e5b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41e5b-132">**\_Конфигурация/АПП**</span><span class="sxs-lookup"><span data-stu-id="41e5b-132">**/app\_config**</span></span>](-app-config.md)
</dt> <dt>

[<span data-ttu-id="41e5b-133">Файл определения интерфейса (IDL)</span><span class="sxs-lookup"><span data-stu-id="41e5b-133">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="41e5b-134">**importlib**</span><span class="sxs-lookup"><span data-stu-id="41e5b-134">**importlib**</span></span>](importlib.md)
</dt> <dt>

[<span data-ttu-id="41e5b-135">**относится**</span><span class="sxs-lookup"><span data-stu-id="41e5b-135">**include**</span></span>](include.md)
</dt> <dt>

[<span data-ttu-id="41e5b-136">Импорт системных файлов заголовков</span><span class="sxs-lookup"><span data-stu-id="41e5b-136">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> <dt>

[<span data-ttu-id="41e5b-137">Импорт файлов и библиотек типов</span><span class="sxs-lookup"><span data-stu-id="41e5b-137">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="41e5b-138">**/МС \_ ext**</span><span class="sxs-lookup"><span data-stu-id="41e5b-138">**/ms\_ext**</span></span>](-ms-ext.md)
</dt> <dt>

[<span data-ttu-id="41e5b-139">**/осф**</span><span class="sxs-lookup"><span data-stu-id="41e5b-139">**/osf**</span></span>](-osf.md)
</dt> </dl>

 

 