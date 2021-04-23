---
title: Функция Глфиниш (GL. h)
description: Функция Глфиниш блокируется до тех пор, пока не завершится все выполнение OpenGL.
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- Функция Глфиниш OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731ffc91dbb8d31137a792b59d3ebc36bb4d5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535516"
---
# <a name="glfinish-function"></a><span data-ttu-id="a9d27-104">Функция Глфиниш</span><span class="sxs-lookup"><span data-stu-id="a9d27-104">glFinish function</span></span>

<span data-ttu-id="a9d27-105">Функция **глфиниш** блокируется до тех пор, пока не завершится все выполнение OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a9d27-105">The **glFinish** function blocks until all OpenGL execution is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d27-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9d27-106">Syntax</span></span>


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a><span data-ttu-id="a9d27-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="a9d27-107">Parameters</span></span>

<span data-ttu-id="a9d27-108">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="a9d27-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a9d27-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a9d27-109">Return value</span></span>

<span data-ttu-id="a9d27-110">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a9d27-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a9d27-111">Коды ошибок</span><span class="sxs-lookup"><span data-stu-id="a9d27-111">Error codes</span></span>

<span data-ttu-id="a9d27-112">С помощью функции [**глжетеррор**](glgeterror.md) можно получить следующий код ошибки.</span><span class="sxs-lookup"><span data-stu-id="a9d27-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="a9d27-113">Имя</span><span class="sxs-lookup"><span data-stu-id="a9d27-113">Name</span></span>                                                                                                  | <span data-ttu-id="a9d27-114">Значение</span><span class="sxs-lookup"><span data-stu-id="a9d27-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a9d27-115"><dt>**\_Недопустимая \_ Операция GL**</dt></span><span class="sxs-lookup"><span data-stu-id="a9d27-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="a9d27-116">Функция была вызвана между вызовом [**глбегин**](glbegin.md) и соответствующим вызовом [**гленд**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="a9d27-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a9d27-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a9d27-117">Remarks</span></span>

<span data-ttu-id="a9d27-118">Функция **глфиниш** не возвращает результат, пока не будут выполнены эффекты всех ранее вызванных функций OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a9d27-118">The **glFinish** function does not return until the effects of all previously called OpenGL functions are complete.</span></span> <span data-ttu-id="a9d27-119">К таким эффектам относятся все изменения состояния OpenGL, все изменения состояния подключения и все изменения в содержимом буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="a9d27-119">Such effects include all changes to the OpenGL state, all changes to the connection state, and all changes to the framebuffer contents.</span></span>

<span data-ttu-id="a9d27-120">Функция **глфиниш** требует круговой путь к серверу.</span><span class="sxs-lookup"><span data-stu-id="a9d27-120">The **glFinish** function requires a round trip to the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d27-121">Требования</span><span class="sxs-lookup"><span data-stu-id="a9d27-121">Requirements</span></span>



| <span data-ttu-id="a9d27-122">Требование</span><span class="sxs-lookup"><span data-stu-id="a9d27-122">Requirement</span></span> | <span data-ttu-id="a9d27-123">Значение</span><span class="sxs-lookup"><span data-stu-id="a9d27-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d27-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a9d27-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d27-125">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9d27-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a9d27-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a9d27-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d27-127">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a9d27-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a9d27-128">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a9d27-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9d27-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9d27-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="a9d27-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a9d27-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="a9d27-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9d27-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="a9d27-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a9d27-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9d27-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9d27-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d27-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a9d27-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d27-135">**глбегин**</span><span class="sxs-lookup"><span data-stu-id="a9d27-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="a9d27-136">**гленд**</span><span class="sxs-lookup"><span data-stu-id="a9d27-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="a9d27-137">**глфлуш**</span><span class="sxs-lookup"><span data-stu-id="a9d27-137">**glFlush**</span></span>](glflush.md)
</dt> </dl>

 

 





