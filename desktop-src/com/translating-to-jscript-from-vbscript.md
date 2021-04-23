---
title: Преобразование в JScript из VBScript
description: Преобразование в JScript из VBScript
ms.assetid: cdf04a01-8bc3-4f37-872b-3a0aae962f26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18c2ccb11ffa4f5f000d8cfc73f7db6f857cf6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773568"
---
# <a name="translating-to-jscript-from-vbscript"></a><span data-ttu-id="d6e3b-103">Преобразование в JScript из VBScript</span><span class="sxs-lookup"><span data-stu-id="d6e3b-103">Translating to JScript from VBScript</span></span>

<span data-ttu-id="d6e3b-104">В VBScript **для**... **Каждый** цикл выполняет перечисление элементов коллекции. в JScript **для**... **в** Loop выполняет перечисление элементов объекта или массива JScript.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="d6e3b-105">Чтобы перечислить коллекцию в JScript, используйте объект перечислителя.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="d6e3b-106">В JScript существует несколько типов данных, таких как числа, строки, логические значения, объекты и атрибут null.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-106">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="d6e3b-107">В VBScript используется только один тип данных **Variant**, который может быть подтипа для представления строк, чисел, логических значений и т. д.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-107">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="d6e3b-108">В JScript массивы можно развертывать динамически, задав новое значение для свойства Length массива.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-108">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="d6e3b-109">В VBScript массивы не могут быть увеличены; они должны быть переизмерены с помощью оператора **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="d6e3b-109">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="d6e3b-110">Функции поддержки VBScript и JScript.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-110">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="d6e3b-111">Однако VBScript также поддерживает подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-111">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="d6e3b-112">Подпрограммы похожи на функции, но не возвращают значение.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-112">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="d6e3b-113">В JScript учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-113">JScript is case-sensitive.</span></span> <span data-ttu-id="d6e3b-114">Язык VBScript не является.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-114">VBScript is not.</span></span>

<span data-ttu-id="d6e3b-115">Язык JScript поддерживается как Internet Explorer, так и Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-115">JScript is supported by both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="d6e3b-116">Netscape Navigator не поддерживает VBScript.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-116">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="d6e3b-117">JScript предоставляет объект Error, который может использоваться для перехвата и обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-117">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="d6e3b-118">Объект Error является аналогом объекта VBScript Err.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-118">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="d6e3b-119">Массивы JScript не являются массивами типа **Variant SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="d6e3b-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="d6e3b-120">Если скрипт получает переменную **SAFEARRAY типа Variant** из COM-объекта или скрипта VBScript, он должен использовать объект VBArray для доступа к переменной **типа SafeArray** .</span><span class="sxs-lookup"><span data-stu-id="d6e3b-120">If your script receives a **VARIANT SAFEARRAY** variable from a COM object or VBScript script, it must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6e3b-121">См. также</span><span class="sxs-lookup"><span data-stu-id="d6e3b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6e3b-122">Преобразование в JScript</span><span class="sxs-lookup"><span data-stu-id="d6e3b-122">Translating to JScript</span></span>](translating-to-jscript.md)
</dt> </dl>

 

 




