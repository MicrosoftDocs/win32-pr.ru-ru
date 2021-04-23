---
title: Преобразование в JavaScript из VBScript
description: Преобразование в JavaScript из VBScript
ms.assetid: 39a712c5-f8d7-4441-a602-93cda43c24d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ff950c58c87e926c8593e5c009db4efbce0a371
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328651"
---
# <a name="translating-to-javascript-from-vbscript"></a><span data-ttu-id="6a946-103">Преобразование в JavaScript из VBScript</span><span class="sxs-lookup"><span data-stu-id="6a946-103">Translating to JavaScript from VBScript</span></span>

<span data-ttu-id="6a946-104">В JavaScript существует несколько типов данных, таких как числа, строки, логические значения, объекты и атрибут null.</span><span class="sxs-lookup"><span data-stu-id="6a946-104">In JavaScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="6a946-105">В VBScript используется только один тип данных **Variant**, который может быть подтипа для представления строк, чисел, логических значений и т. д.</span><span class="sxs-lookup"><span data-stu-id="6a946-105">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="6a946-106">В JavaScript массивы можно развертывать динамически, задав новое значение для свойства Length массива.</span><span class="sxs-lookup"><span data-stu-id="6a946-106">In JavaScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="6a946-107">В VBScript массивы не могут быть увеличены; они должны быть переизмерены с помощью оператора **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="6a946-107">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="6a946-108">Функции поддержки VBScript и JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6a946-108">Both VBScript and JavaScript support functions.</span></span> <span data-ttu-id="6a946-109">Однако VBScript также поддерживает подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="6a946-109">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="6a946-110">Подпрограммы похожи на функции, но не возвращают значение.</span><span class="sxs-lookup"><span data-stu-id="6a946-110">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="6a946-111">В языке JavaScript учитывается регистр символов.</span><span class="sxs-lookup"><span data-stu-id="6a946-111">JavaScript is case-sensitive.</span></span> <span data-ttu-id="6a946-112">Язык VBScript не является.</span><span class="sxs-lookup"><span data-stu-id="6a946-112">VBScript is not.</span></span>

<span data-ttu-id="6a946-113">JavaScript поддерживается в разнообразных веб-браузерах, включая Internet Explorer и Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="6a946-113">JavaScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="6a946-114">VBScript поддерживается только Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="6a946-114">VBScript is only supported by Internet Explorer.</span></span>

<span data-ttu-id="6a946-115">VBScript обеспечивает поддержку обработки ошибок через объект Err.</span><span class="sxs-lookup"><span data-stu-id="6a946-115">VBScript provides error handling support through its Err object.</span></span> <span data-ttu-id="6a946-116">JavaScript в настоящее время не предоставляет средств перехвата и обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="6a946-116">JavaScript does not currently provide a means of trapping and handling errors.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6a946-117">См. также</span><span class="sxs-lookup"><span data-stu-id="6a946-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a946-118">Преобразование в JavaScript</span><span class="sxs-lookup"><span data-stu-id="6a946-118">Translating to JavaScript</span></span>](translating-to-javascript.md)
</dt> </dl>

 

 




