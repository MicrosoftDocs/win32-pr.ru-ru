---
title: Преобразование в VBScript из JavaScript
description: Преобразование в VBScript из JavaScript
ms.assetid: f302e032-4e94-42f1-839b-022dab538760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eda8169a665dc93133f7ac933de12ecc612f3e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105710051"
---
# <a name="translating-to-vbscript-from-javascript"></a><span data-ttu-id="907de-103">Преобразование в VBScript из JavaScript</span><span class="sxs-lookup"><span data-stu-id="907de-103">Translating to VBScript from JavaScript</span></span>

<span data-ttu-id="907de-104">В JavaScript существует несколько типов данных, таких как числа, строки, логические значения, объекты и атрибут null.</span><span class="sxs-lookup"><span data-stu-id="907de-104">In JavaScript, there are several data types, such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="907de-105">В VBScript используется только один тип данных **Variant**, который может быть подтипа для представления строк, чисел, логических значений и т. д.</span><span class="sxs-lookup"><span data-stu-id="907de-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="907de-106">В JavaScript массивы можно развертывать динамически, задав новое значение для свойства Length массива.</span><span class="sxs-lookup"><span data-stu-id="907de-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="907de-107">В VBScript массивы не могут быть увеличены; они должны быть переизмерены с помощью оператора **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="907de-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="907de-108">Функции поддержки VBScript и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="907de-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="907de-109">Однако VBScript также поддерживает подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="907de-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="907de-110">Подпрограммы похожи на функции, за исключением того, что они не возвращают значение.</span><span class="sxs-lookup"><span data-stu-id="907de-110">Subroutines are similar to functions, except they do not return a value.</span></span>

<span data-ttu-id="907de-111">В языке JavaScript учитывается регистр символов.</span><span class="sxs-lookup"><span data-stu-id="907de-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="907de-112">Язык VBScript не является.</span><span class="sxs-lookup"><span data-stu-id="907de-112">VBScript is not.</span></span>

<span data-ttu-id="907de-113">JavaScript поддерживается в разнообразных веб-браузерах, включая Internet Explorer и Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="907de-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="907de-114">Netscape Navigator не поддерживает VBScript.</span><span class="sxs-lookup"><span data-stu-id="907de-114">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="907de-115">Сценарий VBScript поддерживает обработку ошибок через объект Err.</span><span class="sxs-lookup"><span data-stu-id="907de-115">VBScript supports error handling through its Err object.</span></span> <span data-ttu-id="907de-116">JavaScript в настоящее время не предоставляет средств перехвата и обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="907de-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="907de-117">См. также</span><span class="sxs-lookup"><span data-stu-id="907de-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="907de-118">Преобразование в VBScript</span><span class="sxs-lookup"><span data-stu-id="907de-118">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




