---
description: Наиболее распространены следующие значения HRESULT. Дополнительные значения содержатся в файле заголовка Winerror. h.
ms.assetid: ce52efc3-92c7-40e4-ac49-0c54049e169f
title: Общие значения HRESULT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a64d042d9531d026cda548b2a699ed60c0bebd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898633"
---
# <a name="common-hresult-values"></a><span data-ttu-id="d0673-104">Общие значения HRESULT</span><span class="sxs-lookup"><span data-stu-id="d0673-104">Common HRESULT Values</span></span>

<span data-ttu-id="d0673-105">Наиболее распространены следующие значения HRESULT.</span><span class="sxs-lookup"><span data-stu-id="d0673-105">The following HRESULT values are the most common.</span></span> <span data-ttu-id="d0673-106">Дополнительные значения содержатся в файле заголовка Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="d0673-106">More values are contained in the header file Winerror.h.</span></span>

<span data-ttu-id="d0673-107">Ниже приведены значения, перечисленные в алфавитном порядке по имени.</span><span class="sxs-lookup"><span data-stu-id="d0673-107">Here are the values listed alphabetically by name.</span></span>



| <span data-ttu-id="d0673-108">Имя</span><span class="sxs-lookup"><span data-stu-id="d0673-108">Name</span></span>            | <span data-ttu-id="d0673-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d0673-109">Description</span></span>                         | <span data-ttu-id="d0673-110">Значение</span><span class="sxs-lookup"><span data-stu-id="d0673-110">Value</span></span>      |
|-----------------|-------------------------------------|------------|
| <span data-ttu-id="d0673-111">\_ОК</span><span class="sxs-lookup"><span data-stu-id="d0673-111">S\_OK</span></span>           | <span data-ttu-id="d0673-112">Операция выполнена успешно</span><span class="sxs-lookup"><span data-stu-id="d0673-112">Operation successful</span></span>                | <span data-ttu-id="d0673-113">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0673-113">0x00000000</span></span> |
| <span data-ttu-id="d0673-114">\_прервать</span><span class="sxs-lookup"><span data-stu-id="d0673-114">E\_ABORT</span></span>        | <span data-ttu-id="d0673-115">Операция прервана</span><span class="sxs-lookup"><span data-stu-id="d0673-115">Operation aborted</span></span>                   | <span data-ttu-id="d0673-116">0x80004004</span><span class="sxs-lookup"><span data-stu-id="d0673-116">0x80004004</span></span> |
| <span data-ttu-id="d0673-117">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="d0673-117">E\_ACCESSDENIED</span></span> | <span data-ttu-id="d0673-118">Общая ошибка отказа в доступе</span><span class="sxs-lookup"><span data-stu-id="d0673-118">General access denied error</span></span>         | <span data-ttu-id="d0673-119">0x80070005</span><span class="sxs-lookup"><span data-stu-id="d0673-119">0x80070005</span></span> |
| <span data-ttu-id="d0673-120">\_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="d0673-120">E\_FAIL</span></span>         | <span data-ttu-id="d0673-121">Неопределенный сбой</span><span class="sxs-lookup"><span data-stu-id="d0673-121">Unspecified failure</span></span>                 | <span data-ttu-id="d0673-122">0x80004005</span><span class="sxs-lookup"><span data-stu-id="d0673-122">0x80004005</span></span> |
| <span data-ttu-id="d0673-123">E, \_ маркер</span><span class="sxs-lookup"><span data-stu-id="d0673-123">E\_HANDLE</span></span>       | <span data-ttu-id="d0673-124">Недопустимый Handle</span><span class="sxs-lookup"><span data-stu-id="d0673-124">Handle that is not valid</span></span>            | <span data-ttu-id="d0673-125">0x80070006</span><span class="sxs-lookup"><span data-stu-id="d0673-125">0x80070006</span></span> |
| <span data-ttu-id="d0673-126">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d0673-126">E\_INVALIDARG</span></span>   | <span data-ttu-id="d0673-127">Один или несколько аргументов недопустимы</span><span class="sxs-lookup"><span data-stu-id="d0673-127">One or more arguments are not valid</span></span> | <span data-ttu-id="d0673-128">0x80070057</span><span class="sxs-lookup"><span data-stu-id="d0673-128">0x80070057</span></span> |
| <span data-ttu-id="d0673-129">\_интерфейс E</span><span class="sxs-lookup"><span data-stu-id="d0673-129">E\_NOINTERFACE</span></span>  | <span data-ttu-id="d0673-130">Такой интерфейс не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d0673-130">No such interface supported</span></span>         | <span data-ttu-id="d0673-131">0x80004002</span><span class="sxs-lookup"><span data-stu-id="d0673-131">0x80004002</span></span> |
| <span data-ttu-id="d0673-132">E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="d0673-132">E\_NOTIMPL</span></span>      | <span data-ttu-id="d0673-133">Не реализовано</span><span class="sxs-lookup"><span data-stu-id="d0673-133">Not implemented</span></span>                     | <span data-ttu-id="d0673-134">0x80004001</span><span class="sxs-lookup"><span data-stu-id="d0673-134">0x80004001</span></span> |
| <span data-ttu-id="d0673-135">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d0673-135">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="d0673-136">Не удалось выделить требуемую память</span><span class="sxs-lookup"><span data-stu-id="d0673-136">Failed to allocate necessary memory</span></span> | <span data-ttu-id="d0673-137">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="d0673-137">0x8007000E</span></span> |
| <span data-ttu-id="d0673-138">\_указатель E</span><span class="sxs-lookup"><span data-stu-id="d0673-138">E\_POINTER</span></span>      | <span data-ttu-id="d0673-139">Недопустимый указатель</span><span class="sxs-lookup"><span data-stu-id="d0673-139">Pointer that is not valid</span></span>           | <span data-ttu-id="d0673-140">0x80004003</span><span class="sxs-lookup"><span data-stu-id="d0673-140">0x80004003</span></span> |
| <span data-ttu-id="d0673-141">\_непредвиденная E</span><span class="sxs-lookup"><span data-stu-id="d0673-141">E\_UNEXPECTED</span></span>   | <span data-ttu-id="d0673-142">Непредвиденный сбой</span><span class="sxs-lookup"><span data-stu-id="d0673-142">Unexpected failure</span></span>                  | <span data-ttu-id="d0673-143">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="d0673-143">0x8000FFFF</span></span> |



 

<span data-ttu-id="d0673-144">Ниже приведены значения, перечисленные в числовом порядке по значению.</span><span class="sxs-lookup"><span data-stu-id="d0673-144">Here are the values listed in numeric order by value.</span></span>



| <span data-ttu-id="d0673-145">Значение</span><span class="sxs-lookup"><span data-stu-id="d0673-145">Value</span></span>      | <span data-ttu-id="d0673-146">Имя</span><span class="sxs-lookup"><span data-stu-id="d0673-146">Name</span></span>            | <span data-ttu-id="d0673-147">Описание</span><span class="sxs-lookup"><span data-stu-id="d0673-147">Description</span></span>                         |
|------------|-----------------|-------------------------------------|
| <span data-ttu-id="d0673-148">0x00000000</span><span class="sxs-lookup"><span data-stu-id="d0673-148">0x00000000</span></span> | <span data-ttu-id="d0673-149">\_ОК</span><span class="sxs-lookup"><span data-stu-id="d0673-149">S\_OK</span></span>           | <span data-ttu-id="d0673-150">Операция выполнена успешно</span><span class="sxs-lookup"><span data-stu-id="d0673-150">Operation successful</span></span>                |
| <span data-ttu-id="d0673-151">0x80004001</span><span class="sxs-lookup"><span data-stu-id="d0673-151">0x80004001</span></span> | <span data-ttu-id="d0673-152">E \_ нотимпл</span><span class="sxs-lookup"><span data-stu-id="d0673-152">E\_NOTIMPL</span></span>      | <span data-ttu-id="d0673-153">Не реализовано</span><span class="sxs-lookup"><span data-stu-id="d0673-153">Not implemented</span></span>                     |
| <span data-ttu-id="d0673-154">0x80004002</span><span class="sxs-lookup"><span data-stu-id="d0673-154">0x80004002</span></span> | <span data-ttu-id="d0673-155">\_интерфейс E</span><span class="sxs-lookup"><span data-stu-id="d0673-155">E\_NOINTERFACE</span></span>  | <span data-ttu-id="d0673-156">Такой интерфейс не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d0673-156">No such interface supported</span></span>         |
| <span data-ttu-id="d0673-157">0x80004003</span><span class="sxs-lookup"><span data-stu-id="d0673-157">0x80004003</span></span> | <span data-ttu-id="d0673-158">\_указатель E</span><span class="sxs-lookup"><span data-stu-id="d0673-158">E\_POINTER</span></span>      | <span data-ttu-id="d0673-159">Недопустимый указатель</span><span class="sxs-lookup"><span data-stu-id="d0673-159">Pointer that is not valid</span></span>           |
| <span data-ttu-id="d0673-160">0x80004004</span><span class="sxs-lookup"><span data-stu-id="d0673-160">0x80004004</span></span> | <span data-ttu-id="d0673-161">\_прервать</span><span class="sxs-lookup"><span data-stu-id="d0673-161">E\_ABORT</span></span>        | <span data-ttu-id="d0673-162">Операция прервана</span><span class="sxs-lookup"><span data-stu-id="d0673-162">Operation aborted</span></span>                   |
| <span data-ttu-id="d0673-163">0x80004005</span><span class="sxs-lookup"><span data-stu-id="d0673-163">0x80004005</span></span> | <span data-ttu-id="d0673-164">\_Ошибка E</span><span class="sxs-lookup"><span data-stu-id="d0673-164">E\_FAIL</span></span>         | <span data-ttu-id="d0673-165">Неопределенный сбой</span><span class="sxs-lookup"><span data-stu-id="d0673-165">Unspecified failure</span></span>                 |
| <span data-ttu-id="d0673-166">0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="d0673-166">0x8000FFFF</span></span> | <span data-ttu-id="d0673-167">\_непредвиденная E</span><span class="sxs-lookup"><span data-stu-id="d0673-167">E\_UNEXPECTED</span></span>   | <span data-ttu-id="d0673-168">Непредвиденный сбой</span><span class="sxs-lookup"><span data-stu-id="d0673-168">Unexpected failure</span></span>                  |
| <span data-ttu-id="d0673-169">0x80070005</span><span class="sxs-lookup"><span data-stu-id="d0673-169">0x80070005</span></span> | <span data-ttu-id="d0673-170">E \_ ACCESSDENIED</span><span class="sxs-lookup"><span data-stu-id="d0673-170">E\_ACCESSDENIED</span></span> | <span data-ttu-id="d0673-171">Общая ошибка отказа в доступе</span><span class="sxs-lookup"><span data-stu-id="d0673-171">General access denied error</span></span>         |
| <span data-ttu-id="d0673-172">0x80070006</span><span class="sxs-lookup"><span data-stu-id="d0673-172">0x80070006</span></span> | <span data-ttu-id="d0673-173">E, \_ маркер</span><span class="sxs-lookup"><span data-stu-id="d0673-173">E\_HANDLE</span></span>       | <span data-ttu-id="d0673-174">Недопустимый Handle</span><span class="sxs-lookup"><span data-stu-id="d0673-174">Handle that is not valid</span></span>            |
| <span data-ttu-id="d0673-175">0x8007000E</span><span class="sxs-lookup"><span data-stu-id="d0673-175">0x8007000E</span></span> | <span data-ttu-id="d0673-176">E \_ OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="d0673-176">E\_OUTOFMEMORY</span></span>  | <span data-ttu-id="d0673-177">Не удалось выделить требуемую память</span><span class="sxs-lookup"><span data-stu-id="d0673-177">Failed to allocate necessary memory</span></span> |
| <span data-ttu-id="d0673-178">0x80070057</span><span class="sxs-lookup"><span data-stu-id="d0673-178">0x80070057</span></span> | <span data-ttu-id="d0673-179">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="d0673-179">E\_INVALIDARG</span></span>   | <span data-ttu-id="d0673-180">Один или несколько аргументов недопустимы</span><span class="sxs-lookup"><span data-stu-id="d0673-180">One or more arguments are not valid</span></span> |



 

 

 



