---
title: Функция Глфлуш (GL. h)
description: Функция Глфлуш принудительно вызывает выполнение функций OpenGL в ограниченном времени.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- Функция Глфлуш OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804055"
---
# <a name="glflush-function"></a><span data-ttu-id="44ceb-104">Функция Глфлуш</span><span class="sxs-lookup"><span data-stu-id="44ceb-104">glFlush function</span></span>

<span data-ttu-id="44ceb-105">Функция **глфлуш** принудительно вызывает выполнение функций OpenGL в ограниченном времени.</span><span class="sxs-lookup"><span data-stu-id="44ceb-105">The **glFlush** function forces execution of OpenGL functions in finite time.</span></span>

## <a name="syntax"></a><span data-ttu-id="44ceb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44ceb-106">Syntax</span></span>


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a><span data-ttu-id="44ceb-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="44ceb-107">Parameters</span></span>

<span data-ttu-id="44ceb-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="44ceb-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="44ceb-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44ceb-109">Return value</span></span>

<span data-ttu-id="44ceb-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="44ceb-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44ceb-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="44ceb-111">Error codes</span></span>

<span data-ttu-id="44ceb-112">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="44ceb-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="44ceb-113">Имя</span><span class="sxs-lookup"><span data-stu-id="44ceb-113">Name</span></span>                                                                                                  | <span data-ttu-id="44ceb-114">Значение</span><span class="sxs-lookup"><span data-stu-id="44ceb-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="44ceb-115"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="44ceb-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="44ceb-116">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="44ceb-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="44ceb-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44ceb-117">Remarks</span></span>

<span data-ttu-id="44ceb-118">Различные реализации OpenGL блокируют буферы в нескольких разных местах, включая сетевые буферы и сам графический ускоритель.</span><span class="sxs-lookup"><span data-stu-id="44ceb-118">Different OpenGL implementations buffer commands in several different locations, including network buffers and the graphics accelerator itself.</span></span> <span data-ttu-id="44ceb-119">Функция **глфлуш** очищает все эти буферы, что приводит к тому, что все выданные команды выполняются так быстро, как они принимаются фактическим подсистемой визуализации.</span><span class="sxs-lookup"><span data-stu-id="44ceb-119">The **glFlush** function empties all these buffers, causing all issued commands to be executed as quickly as they are accepted by the actual rendering engine.</span></span> <span data-ttu-id="44ceb-120">Хотя это выполнение может быть не выполнено в течение определенного периода времени, оно завершается в течение ограниченного времени.</span><span class="sxs-lookup"><span data-stu-id="44ceb-120">Though this execution may not be completed in any particular time period, it does complete in a finite amount of time.</span></span>

<span data-ttu-id="44ceb-121">Так как любая программа OpenGL может выполняться по сети или с помощью ускорителя команд, обязательно вызовите **глфлуш** в любых программах, запрашивающих, что все их выданные ранее команды завершены.</span><span class="sxs-lookup"><span data-stu-id="44ceb-121">Because any OpenGL program might be executed over a network, or on an accelerator that buffers commands, be sure to call **glFlush** in any programs requiring that all of their previously issued commands have been completed.</span></span> <span data-ttu-id="44ceb-122">Например, вызовите **глфлуш** перед ожиданием ввода пользователя, который зависит от созданного образа.</span><span class="sxs-lookup"><span data-stu-id="44ceb-122">For example, call **glFlush** before waiting for user input that depends on the generated image.</span></span>

<span data-ttu-id="44ceb-123">Функция **глфлуш** может возвращаться в любое время.</span><span class="sxs-lookup"><span data-stu-id="44ceb-123">The **glFlush** function can return at any time.</span></span> <span data-ttu-id="44ceb-124">Он не ждет завершения выполнения всех ранее выданных функций OpenGL.</span><span class="sxs-lookup"><span data-stu-id="44ceb-124">It does not wait until the execution of all previously issued OpenGL functions is complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="44ceb-125">Требования</span><span class="sxs-lookup"><span data-stu-id="44ceb-125">Requirements</span></span>



| <span data-ttu-id="44ceb-126">Требование</span><span class="sxs-lookup"><span data-stu-id="44ceb-126">Requirement</span></span> | <span data-ttu-id="44ceb-127">Значение</span><span class="sxs-lookup"><span data-stu-id="44ceb-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44ceb-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44ceb-128">Minimum supported client</span></span><br/> | <span data-ttu-id="44ceb-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44ceb-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="44ceb-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44ceb-130">Minimum supported server</span></span><br/> | <span data-ttu-id="44ceb-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44ceb-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="44ceb-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="44ceb-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="44ceb-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="44ceb-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="44ceb-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="44ceb-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="44ceb-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="44ceb-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="44ceb-136">DLL</span><span class="sxs-lookup"><span data-stu-id="44ceb-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44ceb-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44ceb-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44ceb-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44ceb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44ceb-139">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="44ceb-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="44ceb-140">**гленд**</span><span class="sxs-lookup"><span data-stu-id="44ceb-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="44ceb-141">**глфиниш**</span><span class="sxs-lookup"><span data-stu-id="44ceb-141">**glFinish**</span></span>](glfinish.md)
</dt> </dl>

 

 





