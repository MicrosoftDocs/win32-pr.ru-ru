---
title: Распространенные ошибки (ADSI)
description: Все ошибки, относящиеся к ADSI, имеют шестнадцатеричную форму 80005xxx. Наиболее распространенные коды ошибок описаны в следующей таблице.
ms.assetid: fdee4f0a-b39e-4011-af4f-9fe408f6ca6c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd870871d7a8e2939cda546178e2f31fe92644d
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/11/2019
ms.locfileid: "104335987"
---
# <a name="common-errors-adsi"></a><span data-ttu-id="c7ef6-104">Распространенные ошибки (ADSI)</span><span class="sxs-lookup"><span data-stu-id="c7ef6-104">Common Errors (ADSI)</span></span>

<span data-ttu-id="c7ef6-105">Все ошибки, относящиеся к ADSI, имеют шестнадцатеричную форму 80005xxx.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-105">All ADSI-specific errors have a hexadecimal form of 80005xxx.</span></span> <span data-ttu-id="c7ef6-106">Наиболее распространенные коды ошибок описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-106">The most common error codes encountered are outlined in the following table.</span></span>



| <span data-ttu-id="c7ef6-107">Шестнадцатеричный код ошибки ADSI</span><span class="sxs-lookup"><span data-stu-id="c7ef6-107">ADSI hex error code</span></span> | <span data-ttu-id="c7ef6-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c7ef6-108">Description</span></span>                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ef6-109">80005000</span><span class="sxs-lookup"><span data-stu-id="c7ef6-109">80005000</span></span><br/> | <span data-ttu-id="c7ef6-110">Передан недопустимый путь ADSI.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-110">An invalid ADSI pathname was passed.</span></span> <span data-ttu-id="c7ef6-111">Эта ошибка возникает при передаче неправильно сформированного значения ADsPath в **GetObject при привязке к объекту** .</span><span class="sxs-lookup"><span data-stu-id="c7ef6-111">This error results from passing a poorly formed ADsPath to **GetObject** when binding to an object.</span></span><br/> |
| <span data-ttu-id="c7ef6-112">8000500D</span><span class="sxs-lookup"><span data-stu-id="c7ef6-112">8000500D</span></span><br/> | <span data-ttu-id="c7ef6-113">Не удается найти свойство ADSI в кэше свойств.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-113">The ADSI property cannot be found in the property cache.</span></span><br/>                                                                                 |
| <span data-ttu-id="c7ef6-114">8000500E</span><span class="sxs-lookup"><span data-stu-id="c7ef6-114">8000500E</span></span><br/> | <span data-ttu-id="c7ef6-115">Объект ADSI существует.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-115">The ADSI object exists.</span></span> <span data-ttu-id="c7ef6-116">При попытке создать объект ADSI с тем же именем, что и у существующего объекта ADSI, возникнет эта ошибка.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-116">If you attempt to create an ADSI object with the same name as an existing ADSI object, this error will occur.</span></span><br/>    |



 

<span data-ttu-id="c7ef6-117">Полный список кодов ошибок ADSI см. в разделе [Общие коды ошибок ADSI](generic-adsi-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c7ef6-117">For a complete list of ADSI error codes, see [Generic ADSI Error Codes](generic-adsi-error-codes.md).</span></span>

## <a name="com-errors"></a><span data-ttu-id="c7ef6-118">Ошибки COM</span><span class="sxs-lookup"><span data-stu-id="c7ef6-118">COM Errors</span></span>

<span data-ttu-id="c7ef6-119">Так как ADSI состоит из COM-объектов, он возвращает коды стандартных ошибок COM.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-119">Since ADSI is composed of COM objects, it will return standard COM error codes.</span></span> <span data-ttu-id="c7ef6-120">В следующей таблице перечислены коды ошибок COM, наиболее часто встречающиеся при программировании с помощью ADSI.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-120">The following table lists the COM error codes most commonly encountered in ADSI programming.</span></span>



| <span data-ttu-id="c7ef6-121">Код шестнадцатеричной ошибки COM</span><span class="sxs-lookup"><span data-stu-id="c7ef6-121">COM hex error code</span></span>  | <span data-ttu-id="c7ef6-122">Описание</span><span class="sxs-lookup"><span data-stu-id="c7ef6-122">Description</span></span>                                                                                                                   |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7ef6-123">80004005</span><span class="sxs-lookup"><span data-stu-id="c7ef6-123">80004005</span></span><br/> | <span data-ttu-id="c7ef6-124">Незаданная ошибка.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-124">Unspecified error.</span></span> <span data-ttu-id="c7ef6-125">Причина сбоя COM-объекта определена интерфейсом ADSI.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-125">The cause of the COM object failure is indeterminate by ADSI.</span></span> <br/>                                  |
| <span data-ttu-id="c7ef6-126">800041E4</span><span class="sxs-lookup"><span data-stu-id="c7ef6-126">800041E4</span></span><br/> | <span data-ttu-id="c7ef6-127">Объект не найден.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-127">Object not found.</span></span> <span data-ttu-id="c7ef6-128">Эта ошибка в основном возникает из-за неправильного написания строки ADsPath при привязке к объекту.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-128">This error predominantly occurs due to misspelling the ADsPath string when binding to an object.</span></span><br/> |



 

<span data-ttu-id="c7ef6-129">Дополнительные примеры ошибок COM, которые могут возникнуть в программировании ADSI, см. в разделе [Общие коды ошибок COM](generic-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c7ef6-129">See [Generic COM Error Codes](generic-com-error-codes.md) for a few more examples of COM errors that may occur in ADSI programming.</span></span>

## <a name="win32-errors"></a><span data-ttu-id="c7ef6-130">Ошибки Win32</span><span class="sxs-lookup"><span data-stu-id="c7ef6-130">Win32 Errors</span></span>

<span data-ttu-id="c7ef6-131">Любой код ошибки шестнадцатеричной формы 8007xxxx — это стандартный код ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-131">Any error code of the hexadecimal form 8007xxxx is a standard Win32 error code.</span></span> <span data-ttu-id="c7ef6-132">Если вы преобразуете последние четыре цифры из шестнадцатеричного в десятичное, вы можете получить доступ к ошибке из командной строки Windows 2000:</span><span class="sxs-lookup"><span data-stu-id="c7ef6-132">If you convert the last four digits from hexadecimal to decimal, you can access the error from the Windows 2000 command line:</span></span>

<span data-ttu-id="c7ef6-133">**NET HELPMSG <number>**</span><span class="sxs-lookup"><span data-stu-id="c7ef6-133">**net helpmsg <number>**</span></span>

<span data-ttu-id="c7ef6-134">В командной строке выше " &lt; Number &gt; " — это десятичное число, полученное путем преобразования последних четырех цифр кода ошибки из шестнадцатеричного числа.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-134">In the command line above, "&lt;number&gt;" is the decimal number obtained by converting the last four digits of the error code from hexadecimal.</span></span> <span data-ttu-id="c7ef6-135">Эта командная строка предоставит более полезное описание ошибки Win32, которая может быть полезной для отладки сценария.</span><span class="sxs-lookup"><span data-stu-id="c7ef6-135">This command line will provide a more useful description of the Win32 error, which can be of great help in debugging your script.</span></span>

 

 





