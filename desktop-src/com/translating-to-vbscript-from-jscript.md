---
title: Преобразование в VBScript из JScript
description: Преобразование в VBScript из JScript
ms.assetid: db1115e1-2abd-4b06-ad8d-c1f917cd3087
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 704f5ac608e94f883edc3b319fd04625e9a08d18
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067664"
---
# <a name="translating-to-vbscript-from-jscript"></a><span data-ttu-id="5e0af-103">Преобразование в VBScript из JScript</span><span class="sxs-lookup"><span data-stu-id="5e0af-103">Translating to VBScript from JScript</span></span>

<span data-ttu-id="5e0af-104">В VBScript **для**... **Каждый** цикл выполняет перечисление элементов коллекции. в JScript **для**... **в** Loop выполняет перечисление элементов объекта или массива JScript.</span><span class="sxs-lookup"><span data-stu-id="5e0af-104">In VBScript, the **For**...**Each** loop enumerates the members of a collection; in JScript, the **for**...**in** loop enumerates the members of a JScript object or array.</span></span> <span data-ttu-id="5e0af-105">Чтобы перечислить коллекцию в JScript, используйте объект перечислителя.</span><span class="sxs-lookup"><span data-stu-id="5e0af-105">To enumerate a collection in JScript, use an Enumerator object.</span></span>

<span data-ttu-id="5e0af-106">JScript предоставляет объект Error, который может использоваться для перехвата и обработки ошибок.</span><span class="sxs-lookup"><span data-stu-id="5e0af-106">JScript provides the Error object, which can be used to trap and handle errors.</span></span> <span data-ttu-id="5e0af-107">Объект Error является аналогом объекта VBScript Err.</span><span class="sxs-lookup"><span data-stu-id="5e0af-107">The Error object is analogous to the VBScript Err object.</span></span>

<span data-ttu-id="5e0af-108">В JScript существует несколько типов данных, таких как числа, строки, логические значения, объекты и атрибут null.</span><span class="sxs-lookup"><span data-stu-id="5e0af-108">In JScript, there are several data types such as numbers, strings, Booleans, objects, and the null attribute.</span></span> <span data-ttu-id="5e0af-109">В VBScript используется только один тип данных **Variant**, который может быть подтипа для представления строк, чисел, логических значений и т. д.</span><span class="sxs-lookup"><span data-stu-id="5e0af-109">VBScript only uses one data type, **Variant**, which can be subtyped to represent strings, numbers, Booleans, and so on.</span></span>

<span data-ttu-id="5e0af-110">В JScript массивы можно развертывать динамически, задав новое значение для свойства Length массива.</span><span class="sxs-lookup"><span data-stu-id="5e0af-110">In JScript, arrays can be expanded dynamically by setting a new value for the array's length property.</span></span> <span data-ttu-id="5e0af-111">В VBScript массивы не могут быть увеличены; они должны быть переизмерены с помощью оператора **ReDim** .</span><span class="sxs-lookup"><span data-stu-id="5e0af-111">In VBScript, arrays cannot be enlarged; they must be redimensioned using the **redim** statement.</span></span>

<span data-ttu-id="5e0af-112">Функции поддержки VBScript и JScript.</span><span class="sxs-lookup"><span data-stu-id="5e0af-112">Both VBScript and JScript support functions.</span></span> <span data-ttu-id="5e0af-113">Однако VBScript также поддерживает подпрограммы.</span><span class="sxs-lookup"><span data-stu-id="5e0af-113">VBScript, however, also supports subroutines.</span></span> <span data-ttu-id="5e0af-114">Подпрограммы похожи на функции, но не возвращают значение.</span><span class="sxs-lookup"><span data-stu-id="5e0af-114">Subroutines are similar to functions but do not return a value.</span></span>

<span data-ttu-id="5e0af-115">В JScript учитывается регистр.</span><span class="sxs-lookup"><span data-stu-id="5e0af-115">JScript is case-sensitive.</span></span> <span data-ttu-id="5e0af-116">Язык VBScript не является.</span><span class="sxs-lookup"><span data-stu-id="5e0af-116">VBScript is not.</span></span>

<span data-ttu-id="5e0af-117">Язык JScript поддерживается многими веб-браузерами, включая Internet Explorer и Netscape Navigator.</span><span class="sxs-lookup"><span data-stu-id="5e0af-117">JScript is supported by a wide variety of Web browsers, including both Internet Explorer and Netscape Navigator.</span></span> <span data-ttu-id="5e0af-118">Netscape Navigator не поддерживает VBScript.</span><span class="sxs-lookup"><span data-stu-id="5e0af-118">Netscape Navigator does not support VBScript.</span></span>

<span data-ttu-id="5e0af-119">Массивы JScript не являются массивами типа **Variant SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="5e0af-119">JScript arrays are not arrays of the variable type **VARIANT SAFEARRAY**.</span></span> <span data-ttu-id="5e0af-120">Для доступа к переменной **типа SafeArray Variant** в скрипте JScript должен использоваться объект VBArray.</span><span class="sxs-lookup"><span data-stu-id="5e0af-120">A JScript script must use a VBArray object to access the **VARIANT SAFEARRAY** variable.</span></span> <span data-ttu-id="5e0af-121">Скрипты VBScript могут напрямую обращаться к переменным **SAFEARRAY типа Variant**.</span><span class="sxs-lookup"><span data-stu-id="5e0af-121">VBScript scripts can access **VARIANT SAFEARRAY** variables directly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e0af-122">См. также</span><span class="sxs-lookup"><span data-stu-id="5e0af-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e0af-123">Преобразование в VBScript</span><span class="sxs-lookup"><span data-stu-id="5e0af-123">Translating to VBScript</span></span>](translating-to-vbscript.md)
</dt> </dl>

 

 




