---
title: Ресурс User-Defined
description: Определяемая пользователем инструкция определения ресурса определяет ресурс, содержащий данные, относящиеся к приложению.
ms.assetid: b1cfec71-5733-4900-97f6-c1cbb350c728
keywords:
- определяемый пользователем ресурс
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 909352c7f0643ed67b1d199fafba1ac8f15d2a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104253207"
---
# <a name="user-defined-resource"></a><span data-ttu-id="ab839-104">Ресурс User-Defined</span><span class="sxs-lookup"><span data-stu-id="ab839-104">User-Defined Resource</span></span>

<span data-ttu-id="ab839-105">Определяемая пользователем инструкция определения ресурса определяет ресурс, содержащий данные, относящиеся к приложению.</span><span class="sxs-lookup"><span data-stu-id="ab839-105">A user-defined resource-definition statement defines a resource that contains application-specific data.</span></span> <span data-ttu-id="ab839-106">Данные могут иметь любой формат и могут быть определены как содержимое заданного файла (если задан параметр *filename* ) или как последовательность чисел и строк (если указан *необработанный блок данных* ).</span><span class="sxs-lookup"><span data-stu-id="ab839-106">The data can have any format and can be defined either as the content of a given file (if the *filename* parameter is given) or as a series of numbers and strings (if the *raw-data* block is specified).</span></span>

``` syntax
nameID typeID filename
```

<span data-ttu-id="ab839-107">Имя *файла указывает файл* , содержащий двоичные данные ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab839-107">The *filename* specifies the name of a file containing the binary data of the resource.</span></span> <span data-ttu-id="ab839-108">Содержимое файла включается в качестве ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab839-108">The contents of the file are included as the resource.</span></span> <span data-ttu-id="ab839-109">RC не интерпретирует двоичные данные каким-либо образом.</span><span class="sxs-lookup"><span data-stu-id="ab839-109">RC does not interpret the binary data in any way.</span></span> <span data-ttu-id="ab839-110">Ответственность за то, чтобы данные должным образом совпадали с архитектурой целевого компьютера, лежит на программисте.</span><span class="sxs-lookup"><span data-stu-id="ab839-110">It is the programmer's responsibility to ensure that the data is properly aligned for the target computer architecture.</span></span>

<span data-ttu-id="ab839-111">Определяемый пользователем ресурс также можно полностью определить в скрипте ресурсов, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="ab839-111">A user-defined resource can also be defined completely in the resource script using the following syntax:</span></span>

``` syntax
nameID typeID  {  raw-data  }
```

## <a name="parameters"></a><span data-ttu-id="ab839-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab839-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab839-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="ab839-113"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="ab839-114">Уникальное имя или 16-разрядное целое число без знака, идентифицирующее ресурс.</span><span class="sxs-lookup"><span data-stu-id="ab839-114">Unique name or a 16-bit unsigned integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="ab839-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*Типа*</span><span class="sxs-lookup"><span data-stu-id="ab839-115"><span id="typeID"></span><span id="typeid"></span><span id="TYPEID"></span>*typeID*</span></span>
</dt> <dd>

<span data-ttu-id="ab839-116">Уникальное имя или 16-разрядное целое число без знака, определяющее тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab839-116">Unique name or a 16-bit unsigned integer that identifies the resource type.</span></span> <span data-ttu-id="ab839-117">Если указано число, оно должно быть больше 255.</span><span class="sxs-lookup"><span data-stu-id="ab839-117">If a number is given, it must be greater than 255.</span></span> <span data-ttu-id="ab839-118">Числа от 1 до 255 зарезервированы для существующих и будущих переопределенных типов ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ab839-118">The numbers 1 through 255 are reserved for existing and future redefined resource types.</span></span>

</dd> <dt>

<span data-ttu-id="ab839-119"><span id="filename"></span><span id="FILENAME"></span>*файлов*</span><span class="sxs-lookup"><span data-stu-id="ab839-119"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="ab839-120">Имя файла, содержащего данные ресурса.</span><span class="sxs-lookup"><span data-stu-id="ab839-120">Name of the file that contains the resource data.</span></span> <span data-ttu-id="ab839-121">Параметр должен быть допустимым именем файла; Он должен быть полным путем, если файл не находится в текущем рабочем каталоге.</span><span class="sxs-lookup"><span data-stu-id="ab839-121">The parameter must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span>

</dd> <dt>

<span data-ttu-id="ab839-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*необработанные данные*</span><span class="sxs-lookup"><span data-stu-id="ab839-122"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="ab839-123">Необработанные данные, состоящие из одного или нескольких целых чисел или строк символов.</span><span class="sxs-lookup"><span data-stu-id="ab839-123">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="ab839-124">Целые числа могут быть заданы в десятичном, восьмеричном или шестнадцатеричном формате.</span><span class="sxs-lookup"><span data-stu-id="ab839-124">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="ab839-125">Чтобы обеспечить совместимость с 16-разрядными Windows, целые числа хранятся в виде значений WORD.</span><span class="sxs-lookup"><span data-stu-id="ab839-125">To be compatible with 16-bit Windows, integers are stored as WORD values.</span></span> <span data-ttu-id="ab839-126">Целое число можно сохранить как значение типа DWORD, указав для целого числа суффикс "L".</span><span class="sxs-lookup"><span data-stu-id="ab839-126">You can store an integer as a DWORD value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="ab839-127">Строки заключаются в кавычки.</span><span class="sxs-lookup"><span data-stu-id="ab839-127">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="ab839-128">RC не добавляет автоматически завершающий нуль-символ к строке.</span><span class="sxs-lookup"><span data-stu-id="ab839-128">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="ab839-129">Каждая строка является последовательностью указанных символов ANSI, если она не указана в виде строки расширенных символов с префиксом "L".</span><span class="sxs-lookup"><span data-stu-id="ab839-129">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the "L" prefix.</span></span>

<span data-ttu-id="ab839-130">Блок данных начинается с границы **DWORD** , а RC не выполняет заполнение или выравнивание данных в блоке *необработанных данных* .</span><span class="sxs-lookup"><span data-stu-id="ab839-130">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="ab839-131">Ответственность за то, чтобы обеспечить правильное выравнивание данных внутри блока, лежит на программисте.</span><span class="sxs-lookup"><span data-stu-id="ab839-131">It is the programmer's responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

## <a name="example"></a><span data-ttu-id="ab839-132">Пример</span><span class="sxs-lookup"><span data-stu-id="ab839-132">Example</span></span>

<span data-ttu-id="ab839-133">В следующем примере показано несколько определяемых пользователем инструкций:</span><span class="sxs-lookup"><span data-stu-id="ab839-133">The following example shows several user-defined statements:</span></span>

``` syntax
array   MYRES   data.res
14      300     custom.res
18 MYRES2
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

 

 




