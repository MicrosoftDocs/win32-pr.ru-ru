---
title: Обработка ошибок (OpenGL)
description: Когда OpenGL обнаруживает ошибку, он записывает текущий код ошибки.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- Ошибка обработки OpenGL
- Обработка ошибок OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105672448"
---
# <a name="error-handling-opengl"></a><span data-ttu-id="95ba6-105">Обработка ошибок (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="95ba6-105">Error Handling (OpenGL)</span></span>

<span data-ttu-id="95ba6-106">Когда OpenGL обнаруживает ошибку, он записывает текущий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="95ba6-106">When OpenGL detects an error, it records a current error code.</span></span> <span data-ttu-id="95ba6-107">Функция, которая вызвала ошибку, игнорируется, поэтому она не влияет на состояние OpenGL или на содержимое буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="95ba6-107">The function that caused the error is ignored, so it has no effect on the OpenGL state or on the framebuffer contents.</span></span> <span data-ttu-id="95ba6-108">(Если ошибка записана в ГК \_ \_Не хватает \_ памяти, однако результаты функции не определены.) После записи текущий код ошибки не удаляется до тех пор, пока не будет вызвана функция запроса [**глжетеррор**](glgeterror.md) , которая возвращает текущий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="95ba6-108">(If the error recorded was GL\_OUT\_OF\_MEMORY, however, the results of the function are undefined.) Once recorded, the current error code isn't cleared until you call the [**glGetError**](glgeterror.md) query function, which returns the current error code.</span></span>

<span data-ttu-id="95ba6-109">Реализации OpenGL могут возвращать несколько текущих кодов ошибок, каждая из которых остается установленной до запроса.</span><span class="sxs-lookup"><span data-stu-id="95ba6-109">Implementations of OpenGL may return multiple current error codes, each of which remains set until queried.</span></span> <span data-ttu-id="95ba6-110">Функция **глжетеррор** ВОЗВРАЩАЕТ ошибку GL \_ , \_ когда вы запрашиваете все текущие коды ошибок или если нет ошибок.</span><span class="sxs-lookup"><span data-stu-id="95ba6-110">The **glGetError** function returns GL\_NO\_ERROR once you've queried all the current error codes or if there is no error.</span></span> <span data-ttu-id="95ba6-111">Поэтому при получении кода ошибки вызовите **глжетеррор** до тех пор, пока \_ не будет \_ возвращена ошибка GL, чтобы убедиться, что все ошибки обнаружены.</span><span class="sxs-lookup"><span data-stu-id="95ba6-111">Therefore, if you obtain an error code, call **glGetError** until GL\_NO\_ERROR is returned to be sure you've discovered all the errors.</span></span> <span data-ttu-id="95ba6-112">Список кодов ошибок см. в разделе [коды ошибок OpenGL](opengl-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="95ba6-112">For the list of error codes, see [OpenGL error codes](opengl-error-codes.md).</span></span>

<span data-ttu-id="95ba6-113">Функцию [**глуеррорстринг**](gluerrorstring.md) Glu можно использовать для получения описательной строки, соответствующей коду ошибки, переданной в.</span><span class="sxs-lookup"><span data-stu-id="95ba6-113">You can use the [**gluErrorString**](gluerrorstring.md) GLU function to obtain a descriptive string corresponding to the error code passed in.</span></span> <span data-ttu-id="95ba6-114">Дополнительные сведения о **глуеррорстринг** см. в разделе [Обработка ошибок](handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="95ba6-114">For more information on **gluErrorString**, see [Handling Errors](handling-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="95ba6-115">Функции GLU часто возвращают значения ошибок, если обнаружена ошибка.</span><span class="sxs-lookup"><span data-stu-id="95ba6-115">GLU functions often return error values if an error is detected.</span></span> <span data-ttu-id="95ba6-116">Кроме того, библиотека служебной программы OpenGL определяет коды ошибок GLU \_ недопустимое \_ перечисление, Glu \_ недопустимое \_ значение и Glu \_ нехватки \_ \_ памяти, которые имеют то же значение, что и соответствующие коды ошибок OpenGL.</span><span class="sxs-lookup"><span data-stu-id="95ba6-116">Also, the OpenGL Utility library defines the error codes GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY, which have the same meaning as the related OpenGL error codes.</span></span>

 

 

 




