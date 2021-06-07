---
title: Возвращаемые значения (специальные возможности Windows)
description: В этом разделе описываются наиболее распространенные возвращаемые значения и другие возвращаемые значения, которые могут отображаться реже.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd0f073c401682eb78d9fdf9270709a84ed77ae2
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443995"
---
# <a name="return-values-windows-accessibility-features"></a><span data-ttu-id="25bb5-103">Возвращаемые значения (специальные возможности Windows)</span><span class="sxs-lookup"><span data-stu-id="25bb5-103">Return Values (Windows Accessibility features)</span></span>

<span data-ttu-id="25bb5-104">В этом разделе описываются наиболее распространенные возвращаемые значения и другие возвращаемые значения, которые могут отображаться реже.</span><span class="sxs-lookup"><span data-stu-id="25bb5-104">This topic describes the most common return values, and other return values that you might see less frequently.</span></span>

## <a name="common-return-values"></a><span data-ttu-id="25bb5-105">Общие возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="25bb5-105">Common Return Values</span></span>

<span data-ttu-id="25bb5-106">Методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) возвращают одно из следующих значений, определенных в файле Winerror. h, или другой стандартный код ошибки модели объектов компонента (com):</span><span class="sxs-lookup"><span data-stu-id="25bb5-106">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods return one of the following values, defined in winerror.h, or another standard Component Object Model (COM) error code:</span></span>



|   <span data-ttu-id="25bb5-107">Значение</span><span class="sxs-lookup"><span data-stu-id="25bb5-107">Value</span></span>                      |   <span data-ttu-id="25bb5-108">Описание</span><span class="sxs-lookup"><span data-stu-id="25bb5-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25bb5-109">\_ОК</span><span class="sxs-lookup"><span data-stu-id="25bb5-109">S\_OK</span></span>                   | <span data-ttu-id="25bb5-110">Метод выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="25bb5-110">The method succeeded.</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="25bb5-111">S \_ false</span><span class="sxs-lookup"><span data-stu-id="25bb5-111">S\_FALSE</span></span>                | <span data-ttu-id="25bb5-112">Метод был создан частично.</span><span class="sxs-lookup"><span data-stu-id="25bb5-112">The method succeeded in part.</span></span> <span data-ttu-id="25bb5-113">Это происходит, когда метод выполняется, но запрошенные сведения недоступны.</span><span class="sxs-lookup"><span data-stu-id="25bb5-113">This happens when the method succeeds, but the requested information is not available.</span></span> <span data-ttu-id="25bb5-114">Например, Microsoft Active Accessibility возвращает \_ значение false, если вызывается метод [**IAccessible:: акчиттест**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) для получения дочернего объекта в заданной точке, а указанная точка не находится внутри объекта или дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="25bb5-114">For example, Microsoft Active Accessibility returns S\_FALSE if you call [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) to retrieve a child object at a given point, and the specified point is not within the object or the object's child.</span></span> |
| <span data-ttu-id="25bb5-115">\_вымембернотфаунд E \_</span><span class="sxs-lookup"><span data-stu-id="25bb5-115">DISP\_E\_MEMBERNOTFOUND</span></span> | <span data-ttu-id="25bb5-116">Объект не поддерживает запрошенное свойство или действие.</span><span class="sxs-lookup"><span data-stu-id="25bb5-116">The object does not support the requested property or action.</span></span> <span data-ttu-id="25bb5-117">Например, кнопка отправки возвращает это значение, если вы запрашиваете [свойство Value](value-property.md), так как оно не имеет свойства Value.</span><span class="sxs-lookup"><span data-stu-id="25bb5-117">For example, a push button returns this value if you request its [Value property](value-property.md), because it does not have a Value property.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="25bb5-118">E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="25bb5-118">E\_NOTIMPL</span></span>              | <span data-ttu-id="25bb5-119">Метод не реализован.</span><span class="sxs-lookup"><span data-stu-id="25bb5-119">The method is not implemented.</span></span> <span data-ttu-id="25bb5-120">Это значение возникает, когда клиент вызывает метод, который еще не поддерживается в этой операционной системе.</span><span class="sxs-lookup"><span data-stu-id="25bb5-120">This value occurs when a client calls a method that is not yet supported in that operating system.</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="25bb5-121">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="25bb5-121">E\_INVALIDARG</span></span>           | <span data-ttu-id="25bb5-122">Один или несколько аргументов были недопустимыми.</span><span class="sxs-lookup"><span data-stu-id="25bb5-122">One or more arguments were not valid.</span></span> <span data-ttu-id="25bb5-123">Эта ошибка возникает, когда вызывающая сторона пытается определить дочерний объект с помощью идентификатора, который не распознает сервер.</span><span class="sxs-lookup"><span data-stu-id="25bb5-123">This error occurs when the caller attempts to identify a child object using an identifier that the server does not recognize.</span></span> <span data-ttu-id="25bb5-124">Эта ошибка также возникает, когда клиент пытается опознать дочерний объект в объекте, который не имеет дочерних элементов.</span><span class="sxs-lookup"><span data-stu-id="25bb5-124">This error also results when a client attempts to identify a child object within an object that has no children.</span></span>                                                                                                      |
| <span data-ttu-id="25bb5-125">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="25bb5-125">E\_OUTOFMEMORY</span></span>          | <span data-ttu-id="25bb5-126">Методу не удалось выделить память, необходимую для завершения операции, которая является решающей для ее успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="25bb5-126">The method was unable to allocate memory required to complete an operation crucial to its success.</span></span>                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="25bb5-127">\_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="25bb5-127">E\_FAIL</span></span>                 | <span data-ttu-id="25bb5-128">Произошла неизвестная или универсальная ошибка.</span><span class="sxs-lookup"><span data-stu-id="25bb5-128">An unknown or generic error occurred.</span></span>                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a><span data-ttu-id="25bb5-129">Дополнительные возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="25bb5-129">Additional Return Values</span></span>

<span data-ttu-id="25bb5-130">Ниже приведены возвращаемые значения, которые могут возвращать методы [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="25bb5-130">The following are return values that [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods might return.</span></span> <span data-ttu-id="25bb5-131">Эти возвращаемые значения не так распространены, как предыдущие, но их следует учитывать.</span><span class="sxs-lookup"><span data-stu-id="25bb5-131">These return values are not as common as the previous ones, but you should be aware of them.</span></span>



|    <span data-ttu-id="25bb5-132">Значение</span><span class="sxs-lookup"><span data-stu-id="25bb5-132">Value</span></span>                    |    <span data-ttu-id="25bb5-133">Описание</span><span class="sxs-lookup"><span data-stu-id="25bb5-133">Description</span></span>                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="25bb5-134">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="25bb5-134">E\_ACCESSDENIED</span></span>        | <span data-ttu-id="25bb5-135">Это значение возвращается при вызове get \_ акквалуе для получения значения элемента управления пароля.</span><span class="sxs-lookup"><span data-stu-id="25bb5-135">This is returned when you call get\_accValue to get the value of a password control.</span></span> |
| <span data-ttu-id="25bb5-136">отображаемое \_ \_ исключение E</span><span class="sxs-lookup"><span data-stu-id="25bb5-136">DISP\_E\_EXCEPTION</span></span>     |                                                                                      |
| <span data-ttu-id="25bb5-137">CO \_ E \_ обжнотконнектед</span><span class="sxs-lookup"><span data-stu-id="25bb5-137">CO\_E\_OBJNOTCONNECTED</span></span> |                                                                                      |



 

 

 




