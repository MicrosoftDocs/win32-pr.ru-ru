---
title: Обработка ошибок COM в Java и Visual Basic
description: Обработка ошибок COM в Java и Visual Basic
ms.assetid: 1130a038-3c18-4530-a6d7-9f538352297f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea12dc040218e14098ce2394fbb5cd2ebeff1704
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104413833"
---
# <a name="com-error-handling-in-java-and-visual-basic"></a><span data-ttu-id="22114-103">Обработка ошибок COM в Java и Visual Basic</span><span class="sxs-lookup"><span data-stu-id="22114-103">COM Error Handling in Java and Visual Basic</span></span>

<span data-ttu-id="22114-104">Существует три интерфейса и три функции, которые можно использовать в COM для обеспечения обработки ошибок при программировании на Java или Microsoft Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="22114-104">There are three interfaces and three functions that can be used in COM to provide error handling when programming in Java or Microsoft Visual Basic.</span></span> <span data-ttu-id="22114-105">В Java и Visual Basic вызов метода не возвращает **HRESULT** в качестве возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="22114-105">In Java and Visual Basic, the method call does not return an **HRESULT** as the return value.</span></span> <span data-ttu-id="22114-106">Вместо этого эти языки используют COM-интерфейсы и функции для получения значений **HRESULT** и для управления ошибками или исключениями.</span><span class="sxs-lookup"><span data-stu-id="22114-106">Instead, these languages use the COM interfaces and functions to obtain **HRESULT** values and to handle errors or exceptions.</span></span> <span data-ttu-id="22114-107">(Исключения — это события, которые выходят за рамки управления программой, например проблемы с файлами или недопустимые параметры.)</span><span class="sxs-lookup"><span data-stu-id="22114-107">(Exceptions are events beyond the program's control, such as file problems or invalid parameters.)</span></span>

<span data-ttu-id="22114-108">В следующей таблице приведены три интерфейса, обеспечивающие поддержку для **HRESULT** s.</span><span class="sxs-lookup"><span data-stu-id="22114-108">The three interfaces that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                          |                                                                                                                      |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22114-109">**икреатирроринфо**</span><span class="sxs-lookup"><span data-stu-id="22114-109">**ICreateErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-icreateerrorinfo)<br/>  | <span data-ttu-id="22114-110">Задает сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="22114-110">Sets error information.</span></span><br/>                                                                                   |
| [<span data-ttu-id="22114-111">**IErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="22114-111">**IErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo)<br/>        | <span data-ttu-id="22114-112">Возвращает сведения из объекта ошибки.</span><span class="sxs-lookup"><span data-stu-id="22114-112">Returns information from an error object.</span></span><br/>                                                                 |
| [<span data-ttu-id="22114-113">**ISupportErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="22114-113">**ISupportErrorInfo**</span></span>](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)<br/> | <span data-ttu-id="22114-114">Определяет объект как поддерживающий интерфейс [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) .</span><span class="sxs-lookup"><span data-stu-id="22114-114">Identifies the object as supporting the [**IErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-ierrorinfo) interface.</span></span><br/> |



 

<span data-ttu-id="22114-115">Три функции, которые обеспечивают поддержку для **HRESULT** s, перечислены и кратко описаны в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="22114-115">The three functions that provide support for **HRESULT** s are listed and described briefly in the following table.</span></span>



|                                                                        |                                                                                                                                                                      |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22114-116">**креатирроринфо**</span><span class="sxs-lookup"><span data-stu-id="22114-116">**CreateErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-createerrorinfo)<br/> | <span data-ttu-id="22114-117">Создает экземпляр универсального объекта Error.</span><span class="sxs-lookup"><span data-stu-id="22114-117">Creates an instance of a generic error object.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="22114-118">**GetErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="22114-118">**GetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-geterrorinfo)<br/>    | <span data-ttu-id="22114-119">Получает указатель сведений об ошибке, заданный предыдущим вызовом [**сетерроринфо**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) в текущем логическом потоке.</span><span class="sxs-lookup"><span data-stu-id="22114-119">Obtains the error information pointer set by the previous call to [**SetErrorInfo**](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo) in the current logical thread.</span></span><br/> |
| [<span data-ttu-id="22114-120">**сетерроринфо**</span><span class="sxs-lookup"><span data-stu-id="22114-120">**SetErrorInfo**</span></span>](/windows/win32/api/oleauto/nf-oleauto-seterrorinfo)<br/>    | <span data-ttu-id="22114-121">Задает объект сведений об ошибке для текущего потока выполнения.</span><span class="sxs-lookup"><span data-stu-id="22114-121">Sets the error information object for the current thread of execution.</span></span><br/>                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="22114-122">См. также</span><span class="sxs-lookup"><span data-stu-id="22114-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22114-123">Обработка ошибок в COM</span><span class="sxs-lookup"><span data-stu-id="22114-123">Error Handling in COM</span></span>](error-handling-in-com.md)
</dt> </dl>

 

