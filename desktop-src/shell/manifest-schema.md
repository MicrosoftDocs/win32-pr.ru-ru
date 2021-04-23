---
description: Эти элементы составляют схему XML, используемую в манифесте веб-публикации и в мастере заказов на печать в Интернете.
title: Схема перемещения манифеста
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997838"
---
# <a name="transfer-manifest-schema"></a><span data-ttu-id="62279-103">Схема перемещения манифеста</span><span class="sxs-lookup"><span data-stu-id="62279-103">Transfer Manifest Schema</span></span>

<span data-ttu-id="62279-104">Эти элементы составляют схему XML, используемую в манифесте веб-публикации и в мастере заказов на печать в Интернете.</span><span class="sxs-lookup"><span data-stu-id="62279-104">These elements make up the XML schema used in the Web Publishing and Online Print Ordering wizards' transfer manifest.</span></span>

<span data-ttu-id="62279-105">Для манифеста перемещения определены следующие элементы.</span><span class="sxs-lookup"><span data-stu-id="62279-105">The following elements are defined for the transfer manifest.</span></span>

-   [<span data-ttu-id="62279-106">канцелледпаже</span><span class="sxs-lookup"><span data-stu-id="62279-106">cancelledpage</span></span>](#syntax)
    -   [<span data-ttu-id="62279-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-107">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-108">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-108">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-110">фаилурепаже</span><span class="sxs-lookup"><span data-stu-id="62279-110">failurepage</span></span>](#syntax)
    -   [<span data-ttu-id="62279-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-111">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-112">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-113">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-113">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-114">привыч</span><span class="sxs-lookup"><span data-stu-id="62279-114">favorite</span></span>](#syntax)
    -   [<span data-ttu-id="62279-115">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-115">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-116">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-117">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-117">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-118">file</span><span class="sxs-lookup"><span data-stu-id="62279-118">file</span></span>](#syntax)
    -   [<span data-ttu-id="62279-119">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-119">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-120">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-120">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-121">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-121">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-122">filelist</span><span class="sxs-lookup"><span data-stu-id="62279-122">filelist</span></span>](#syntax)
    -   [<span data-ttu-id="62279-123">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-123">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-124">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-124">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-125">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-125">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-126">Folder</span><span class="sxs-lookup"><span data-stu-id="62279-126">folder</span></span>](#syntax)
    -   [<span data-ttu-id="62279-127">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-127">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-128">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-128">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-129">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-129">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-130">фолдерлист</span><span class="sxs-lookup"><span data-stu-id="62279-130">folderlist</span></span>](#syntax)
    -   [<span data-ttu-id="62279-131">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-131">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-132">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-132">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-133">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-133">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-134">формдата</span><span class="sxs-lookup"><span data-stu-id="62279-134">formdata</span></span>](#syntax)
    -   [<span data-ttu-id="62279-135">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-135">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-136">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-136">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-137">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-137">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-138">хтмлуи</span><span class="sxs-lookup"><span data-stu-id="62279-138">htmlui</span></span>](#syntax)
    -   [<span data-ttu-id="62279-139">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-139">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-140">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-140">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-141">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-141">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-142">имажепроперти</span><span class="sxs-lookup"><span data-stu-id="62279-142">imageproperty</span></span>](#syntax)
    -   [<span data-ttu-id="62279-143">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-143">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-144">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-144">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-145">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-145">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-146">метаданных</span><span class="sxs-lookup"><span data-stu-id="62279-146">metadata</span></span>](#syntax)
    -   [<span data-ttu-id="62279-147">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-147">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-148">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-148">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-149">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-149">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-150">нетплаце</span><span class="sxs-lookup"><span data-stu-id="62279-150">netplace</span></span>](#syntax)
    -   [<span data-ttu-id="62279-151">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-151">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-152">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-152">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-153">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-153">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-154">Поместить</span><span class="sxs-lookup"><span data-stu-id="62279-154">post</span></span>](#syntax)
    -   [<span data-ttu-id="62279-155">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-155">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-156">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-156">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-157">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-157">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-158">изменить размер</span><span class="sxs-lookup"><span data-stu-id="62279-158">resize</span></span>](#syntax)
    -   [<span data-ttu-id="62279-159">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-159">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-160">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-160">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-161">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-161">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-162">сукцесспаже</span><span class="sxs-lookup"><span data-stu-id="62279-162">successpage</span></span>](#syntax)
    -   [<span data-ttu-id="62279-163">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-163">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-164">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-164">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-165">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-165">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-166">target</span><span class="sxs-lookup"><span data-stu-id="62279-166">target</span></span>](#syntax)
    -   [<span data-ttu-id="62279-167">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-167">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-168">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-168">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-169">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-169">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-170">трансферманифест</span><span class="sxs-lookup"><span data-stu-id="62279-170">transfermanifest</span></span>](#syntax)
    -   [<span data-ttu-id="62279-171">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-171">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-172">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-172">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-173">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-173">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="62279-174">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-174">uploadinfo</span></span>](#syntax)
    -   [<span data-ttu-id="62279-175">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-175">Syntax</span></span>](#syntax)
    -   [<span data-ttu-id="62279-176">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-176">Attributes</span></span>](#attributes)
    -   [<span data-ttu-id="62279-177">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-177">Element Information</span></span>](#element-information)

## <a name="cancelledpage"></a><span data-ttu-id="62279-178">канцелледпаже</span><span class="sxs-lookup"><span data-stu-id="62279-178">cancelledpage</span></span>

<span data-ttu-id="62279-179">Задает серверную HTML-страницу, отображаемую перед закрытием мастера при нажатии пользователем кнопки **"Отмена"** .</span><span class="sxs-lookup"><span data-stu-id="62279-179">Specifies the server-side HTML page to display before the wizard is closed when the user clicks the **Cancel** button.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-180">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-180">Syntax</span></span>


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-181">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-181">Attributes</span></span>



| <span data-ttu-id="62279-182">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-182">Attribute</span></span> | <span data-ttu-id="62279-183">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-183">Description</span></span>                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62279-184">href</span><span class="sxs-lookup"><span data-stu-id="62279-184">href</span></span>      | <span data-ttu-id="62279-185">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-185">Required.</span></span> <span data-ttu-id="62279-186">URL-адрес HTML-страницы на стороне сервера, отображаемый при нажатии пользователем кнопки **"Отмена"** .</span><span class="sxs-lookup"><span data-stu-id="62279-186">The URL of the server-side HTML page to display when the user clicks the **Cancel** button.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-187">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-187">Element Information</span></span>



| <span data-ttu-id="62279-188">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-188">Parent Element</span></span>        | <span data-ttu-id="62279-189">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-189">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="62279-190">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-190">uploadinfo</span></span>](#syntax) | <span data-ttu-id="62279-191">Нет</span><span class="sxs-lookup"><span data-stu-id="62279-191">None</span></span>           |



 

## <a name="failurepage"></a><span data-ttu-id="62279-192">фаилурепаже</span><span class="sxs-lookup"><span data-stu-id="62279-192">failurepage</span></span>

<span data-ttu-id="62279-193">Указывает серверную HTML-страницу, отображаемую в случае неудачной отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-193">Specifies the server-side HTML page to display if the upload is not successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-194">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-194">Syntax</span></span>


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-195">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-195">Attributes</span></span>



| <span data-ttu-id="62279-196">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-196">Attribute</span></span> | <span data-ttu-id="62279-197">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-197">Description</span></span>                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="62279-198">href</span><span class="sxs-lookup"><span data-stu-id="62279-198">href</span></span>      | <span data-ttu-id="62279-199">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-199">Required.</span></span> <span data-ttu-id="62279-200">URL-адрес страницы на стороне сервера, отображаемой в случае неудачной отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-200">The URL of the server-side HTML page to display if the upload is not successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-201">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-201">Element Information</span></span>



| <span data-ttu-id="62279-202">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-202">Parent Element</span></span>        | <span data-ttu-id="62279-203">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-203">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="62279-204">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-204">uploadinfo</span></span>](#syntax) | <span data-ttu-id="62279-205">Нет.</span><span class="sxs-lookup"><span data-stu-id="62279-205">None.</span></span> <span data-ttu-id="62279-206">Текст разрешен.</span><span class="sxs-lookup"><span data-stu-id="62279-206">Text is allowed.</span></span> |



 

## <a name="favorite"></a><span data-ttu-id="62279-207">избранное</span><span class="sxs-lookup"><span data-stu-id="62279-207">favorite</span></span>

<span data-ttu-id="62279-208">Указывает мастеру на необходимость создания записи избранного веб-сайта в меню **"Избранное"** для данного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="62279-208">Instructs the wizard to create a favorite website entry in the **Favorites** menu for the given URL.</span></span> <span data-ttu-id="62279-209">Если этот элемент не указан, то вместо него используется элемент [хтмлуи](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="62279-209">If this element is not specified, then the [htmlui](#syntax) element is used in its place.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-210">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-210">Syntax</span></span>


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-211">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-211">Attributes</span></span>



| <span data-ttu-id="62279-212">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-212">Attribute</span></span> | <span data-ttu-id="62279-213">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-213">Description</span></span>                                                            |
|-----------|------------------------------------------------------------------------|
| <span data-ttu-id="62279-214">comment</span><span class="sxs-lookup"><span data-stu-id="62279-214">comment</span></span>   | <span data-ttu-id="62279-215">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-215">Required.</span></span> <span data-ttu-id="62279-216">Комментарий, связанный с записью **избранного** .</span><span class="sxs-lookup"><span data-stu-id="62279-216">The comment associated with the **Favorites** entry.</span></span>         |
| <span data-ttu-id="62279-217">href</span><span class="sxs-lookup"><span data-stu-id="62279-217">href</span></span>      | <span data-ttu-id="62279-218">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-218">Required.</span></span> <span data-ttu-id="62279-219">URL-адрес записи **избранного** .</span><span class="sxs-lookup"><span data-stu-id="62279-219">The URL of the **Favorites** entry.</span></span>                          |
| <span data-ttu-id="62279-220">name</span><span class="sxs-lookup"><span data-stu-id="62279-220">name</span></span>      | <span data-ttu-id="62279-221">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-221">Required.</span></span> <span data-ttu-id="62279-222">Имя URL-адреса, отображаемого в меню **"Избранное"** .</span><span class="sxs-lookup"><span data-stu-id="62279-222">The name for the URL that appears in the **Favorites** menu.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-223">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-223">Element Information</span></span>



| <span data-ttu-id="62279-224">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-224">Parent Element</span></span>        | <span data-ttu-id="62279-225">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-225">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="62279-226">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-226">uploadinfo</span></span>](#syntax) | <span data-ttu-id="62279-227">Нет.</span><span class="sxs-lookup"><span data-stu-id="62279-227">None.</span></span> <span data-ttu-id="62279-228">Текст разрешен.</span><span class="sxs-lookup"><span data-stu-id="62279-228">Text is allowed.</span></span> |



 

## <a name="file"></a><span data-ttu-id="62279-229">файл</span><span class="sxs-lookup"><span data-stu-id="62279-229">file</span></span>

<span data-ttu-id="62279-230">Описывает один файл для копирования.</span><span class="sxs-lookup"><span data-stu-id="62279-230">Describes a single file to be copied.</span></span> <span data-ttu-id="62279-231">В одном узле [FileList](#syntax) может содержаться несколько элементов [File](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="62279-231">Multiple [file](#syntax) elements may be contained under a single [filelist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-232">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-232">Syntax</span></span>


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-233">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-233">Attributes</span></span>



| <span data-ttu-id="62279-234">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-234">Attribute</span></span>   | <span data-ttu-id="62279-235">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-235">Description</span></span>                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62279-236">ContentType</span><span class="sxs-lookup"><span data-stu-id="62279-236">contenttype</span></span> | <span data-ttu-id="62279-237">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="62279-237">Optional.</span></span> <span data-ttu-id="62279-238">Тип MIME для файла.</span><span class="sxs-lookup"><span data-stu-id="62279-238">The MIME type of the file.</span></span>                                                                                                                                         |
| <span data-ttu-id="62279-239">ресурс destination</span><span class="sxs-lookup"><span data-stu-id="62279-239">destination</span></span> | <span data-ttu-id="62279-240">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-240">Required.</span></span> <span data-ttu-id="62279-241">Предлагаемый путь к файлу после его отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-241">A suggested path for the file once it is uploaded.</span></span> <span data-ttu-id="62279-242">Этот путь указывается относительно URL-адреса назначения сайта отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-242">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="62279-243">Сайт отправки может изменить это значение при необходимости.</span><span class="sxs-lookup"><span data-stu-id="62279-243">The upload site can modify this value as necessary.</span></span> |
| <span data-ttu-id="62279-244">Расширение</span><span class="sxs-lookup"><span data-stu-id="62279-244">extension</span></span>   | <span data-ttu-id="62279-245">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="62279-245">Optional.</span></span> <span data-ttu-id="62279-246">Расширение имени файла.</span><span class="sxs-lookup"><span data-stu-id="62279-246">The file name extension of the file.</span></span>                                                                                                                               |
| <span data-ttu-id="62279-247">идентификатор</span><span class="sxs-lookup"><span data-stu-id="62279-247">id</span></span>          | <span data-ttu-id="62279-248">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-248">Required.</span></span> <span data-ttu-id="62279-249">Числовой индекс файла.</span><span class="sxs-lookup"><span data-stu-id="62279-249">The numerical index of the file.</span></span>                                                                                                                                   |
| <span data-ttu-id="62279-250">size</span><span class="sxs-lookup"><span data-stu-id="62279-250">size</span></span>        | <span data-ttu-id="62279-251">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="62279-251">Optional.</span></span> <span data-ttu-id="62279-252">Размер файла в байтах.</span><span class="sxs-lookup"><span data-stu-id="62279-252">The size of the file, in bytes.</span></span>                                                                                                                                    |
| <span data-ttu-id="62279-253">source</span><span class="sxs-lookup"><span data-stu-id="62279-253">source</span></span>      | <span data-ttu-id="62279-254">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-254">Required.</span></span> <span data-ttu-id="62279-255">Полный путь к файлу в файловой системе.</span><span class="sxs-lookup"><span data-stu-id="62279-255">The full file system path for the file.</span></span>                                                                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="62279-256">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-256">Element Information</span></span>



| <span data-ttu-id="62279-257">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-257">Parent Element</span></span>      | <span data-ttu-id="62279-258">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-258">Child Elements</span></span>                                          |
|---------------------|---------------------------------------------------------|
| [<span data-ttu-id="62279-259">filelist</span><span class="sxs-lookup"><span data-stu-id="62279-259">filelist</span></span>](#syntax) | <span data-ttu-id="62279-260">[метаданные](#syntax), [POST](#syntax), [изменение размера](#syntax)</span><span class="sxs-lookup"><span data-stu-id="62279-260">[metadata](#syntax), [post](#syntax), [resize](#syntax)</span></span> |



 

## <a name="filelist"></a><span data-ttu-id="62279-261">filelist</span><span class="sxs-lookup"><span data-stu-id="62279-261">filelist</span></span>

<span data-ttu-id="62279-262">Контейнер для элементов, описывающих копируемые файлы.</span><span class="sxs-lookup"><span data-stu-id="62279-262">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="62279-263">Несколько элементов [FileList](#syntax) могут содержаться в одном [трансферманифест](#syntax) узле.</span><span class="sxs-lookup"><span data-stu-id="62279-263">Multiple [filelist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-264">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-264">Syntax</span></span>


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-265">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-265">Attributes</span></span>



| <span data-ttu-id="62279-266">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-266">Attribute</span></span>   | <span data-ttu-id="62279-267">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-267">Description</span></span>      |
|-------------|------------------|
| <span data-ttu-id="62279-268">усесфолдерс</span><span class="sxs-lookup"><span data-stu-id="62279-268">usesfolders</span></span> | <span data-ttu-id="62279-269">Не реализован.</span><span class="sxs-lookup"><span data-stu-id="62279-269">Not implemented.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-270">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-270">Element Information</span></span>



| <span data-ttu-id="62279-271">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-271">Parent Element</span></span>              | <span data-ttu-id="62279-272">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-272">Child Elements</span></span>  |
|-----------------------------|-----------------|
| [<span data-ttu-id="62279-273">трансферманифест</span><span class="sxs-lookup"><span data-stu-id="62279-273">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="62279-274">file</span><span class="sxs-lookup"><span data-stu-id="62279-274">file</span></span>](#syntax) |



 

## <a name="folder"></a><span data-ttu-id="62279-275">folder</span><span class="sxs-lookup"><span data-stu-id="62279-275">folder</span></span>

<span data-ttu-id="62279-276">Описывает папку, в которой хранятся файлы.</span><span class="sxs-lookup"><span data-stu-id="62279-276">Describes a folder in which files are stored.</span></span> <span data-ttu-id="62279-277">Несколько элементов [Folder](#syntax) могут содержаться в одном [фолдерлист](#syntax) узле.</span><span class="sxs-lookup"><span data-stu-id="62279-277">Multiple [folder](#syntax) elements may be contained under a single [folderlist](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-278">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-278">Syntax</span></span>


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-279">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-279">Attributes</span></span>



| <span data-ttu-id="62279-280">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-280">Attribute</span></span>   | <span data-ttu-id="62279-281">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-281">Description</span></span>                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62279-282">ресурс destination</span><span class="sxs-lookup"><span data-stu-id="62279-282">destination</span></span> | <span data-ttu-id="62279-283">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-283">Required.</span></span> <span data-ttu-id="62279-284">Предлагаемый путь к папке после ее отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-284">A suggested path for the folder once it is uploaded.</span></span> <span data-ttu-id="62279-285">Этот путь указывается относительно URL-адреса назначения сайта отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-285">This path is relative to the upload site's destination URL.</span></span> <span data-ttu-id="62279-286">Сайт отправки может изменить это значение при необходимости.</span><span class="sxs-lookup"><span data-stu-id="62279-286">The upload site can modify this value as necessary.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-287">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-287">Element Information</span></span>



| <span data-ttu-id="62279-288">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-288">Parent Element</span></span>        | <span data-ttu-id="62279-289">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-289">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="62279-290">фолдерлист</span><span class="sxs-lookup"><span data-stu-id="62279-290">folderlist</span></span>](#syntax) | <span data-ttu-id="62279-291">Нет</span><span class="sxs-lookup"><span data-stu-id="62279-291">None</span></span>           |



 

## <a name="folderlist"></a><span data-ttu-id="62279-292">фолдерлист</span><span class="sxs-lookup"><span data-stu-id="62279-292">folderlist</span></span>

<span data-ttu-id="62279-293">Контейнер для элементов, описывающих копируемые файлы.</span><span class="sxs-lookup"><span data-stu-id="62279-293">A container for elements describing the files to be copied.</span></span> <span data-ttu-id="62279-294">Несколько элементов [фолдерлист](#syntax) могут содержаться в одном узле [трансферманифест](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="62279-294">Multiple [folderlist](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-295">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-295">Syntax</span></span>


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-296">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-296">Attributes</span></span>

<span data-ttu-id="62279-297">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="62279-297">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="62279-298">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-298">Element Information</span></span>



| <span data-ttu-id="62279-299">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-299">Parent Element</span></span>              | <span data-ttu-id="62279-300">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-300">Child Elements</span></span>    |
|-----------------------------|-------------------|
| [<span data-ttu-id="62279-301">трансферманифест</span><span class="sxs-lookup"><span data-stu-id="62279-301">transfermanifest</span></span>](#syntax) | [<span data-ttu-id="62279-302">Folder</span><span class="sxs-lookup"><span data-stu-id="62279-302">folder</span></span>](#syntax) |



 

## <a name="formdata"></a><span data-ttu-id="62279-303">формдата</span><span class="sxs-lookup"><span data-stu-id="62279-303">formdata</span></span>

<span data-ttu-id="62279-304">Описывает необязательные данные формы в кодировке HTML, которые могут быть перенесены вместе с файлами.</span><span class="sxs-lookup"><span data-stu-id="62279-304">Describes optional HTML encoded form data that may be transferred with the files.</span></span> <span data-ttu-id="62279-305">Этот элемент добавляется службой, если он выбирает отправку файлов в виде составного сообщения.</span><span class="sxs-lookup"><span data-stu-id="62279-305">This element is added by the service if it elects to upload the files as a multi-part post.</span></span> <span data-ttu-id="62279-306">Данные формы вместе со сведениями из элемента [POST](#syntax) используются для создания заголовка POST.</span><span class="sxs-lookup"><span data-stu-id="62279-306">The form data, together with information from the [post](#syntax) element, is used to create the post header.</span></span>

<span data-ttu-id="62279-307">Несколько элементов [формдата](#syntax) могут содержаться в одном узле [уплоадинфо](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="62279-307">Multiple [formdata](#syntax) elements may be contained under a single [uploadinfo](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-308">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-308">Syntax</span></span>


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-309">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-309">Attributes</span></span>



| <span data-ttu-id="62279-310">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-310">Attribute</span></span> | <span data-ttu-id="62279-311">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-311">Description</span></span>                                                                      |
|-----------|----------------------------------------------------------------------------------|
| <span data-ttu-id="62279-312">name</span><span class="sxs-lookup"><span data-stu-id="62279-312">name</span></span>      | <span data-ttu-id="62279-313">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-313">Required.</span></span> <span data-ttu-id="62279-314">Определяет имя данных формы, связанное с этим разделом отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-314">Defines the form data name associated with this section of the upload.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-315">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-315">Element Information</span></span>



| <span data-ttu-id="62279-316">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-316">Parent Element</span></span>        | <span data-ttu-id="62279-317">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-317">Child Elements</span></span> |
|-----------------------|----------------|
| [<span data-ttu-id="62279-318">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-318">uploadinfo</span></span>](#syntax) | <span data-ttu-id="62279-319">Нет</span><span class="sxs-lookup"><span data-stu-id="62279-319">None</span></span>           |



 

## <a name="htmlui"></a><span data-ttu-id="62279-320">хтмлуи</span><span class="sxs-lookup"><span data-stu-id="62279-320">htmlui</span></span>

<span data-ttu-id="62279-321">URL-адрес HTML-страницы на стороне сервера, отображаемой при закрытии мастера.</span><span class="sxs-lookup"><span data-stu-id="62279-321">The URL of the server-side HTML page to display when the wizard is closed.</span></span> <span data-ttu-id="62279-322">Этот элемент создает запись избранной веб-страницы в меню **"Избранное"** , если элемент [избранного](#syntax) отсутствует, и указано понятное имя сайта отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-322">This element creates a favorite webpage entry in the **Favorites** menu if the [favorite](#syntax) element is absent and the upload site's friendly name is specified.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-323">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-323">Syntax</span></span>


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-324">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-324">Attributes</span></span>



| <span data-ttu-id="62279-325">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-325">Attribute</span></span> | <span data-ttu-id="62279-326">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-326">Description</span></span>                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="62279-327">href</span><span class="sxs-lookup"><span data-stu-id="62279-327">href</span></span>      | <span data-ttu-id="62279-328">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-328">Required.</span></span> <span data-ttu-id="62279-329">URL-адрес HTML-страницы на стороне сервера, отображаемой при закрытии мастера.</span><span class="sxs-lookup"><span data-stu-id="62279-329">The URL of the server-side HTML page to display when the wizard is closed.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-330">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-330">Element Information</span></span>



| <span data-ttu-id="62279-331">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-331">Parent Element</span></span>        | <span data-ttu-id="62279-332">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-332">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="62279-333">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-333">uploadinfo</span></span>](#syntax) | <span data-ttu-id="62279-334">Нет.</span><span class="sxs-lookup"><span data-stu-id="62279-334">None.</span></span> <span data-ttu-id="62279-335">Текст разрешен.</span><span class="sxs-lookup"><span data-stu-id="62279-335">Text is allowed.</span></span> |



 

## <a name="imageproperty"></a><span data-ttu-id="62279-336">имажепроперти</span><span class="sxs-lookup"><span data-stu-id="62279-336">imageproperty</span></span>

<span data-ttu-id="62279-337">Задает свойство Image, относящееся к файлу.</span><span class="sxs-lookup"><span data-stu-id="62279-337">Specifies an image property relating to the file.</span></span> <span data-ttu-id="62279-338">Несколько элементов [имажепроперти](#syntax) могут содержаться в одном узле [метаданных](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="62279-338">Multiple [imageproperty](#syntax) elements may be contained under a single [metadata](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-339">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-339">Syntax</span></span>


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-340">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-340">Attributes</span></span>



| <span data-ttu-id="62279-341">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-341">Attribute</span></span> | <span data-ttu-id="62279-342">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-342">Description</span></span>                                  |
|-----------|----------------------------------------------|
| <span data-ttu-id="62279-343">идентификатор</span><span class="sxs-lookup"><span data-stu-id="62279-343">id</span></span>        | <span data-ttu-id="62279-344">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-344">Required.</span></span> <span data-ttu-id="62279-345">Идентификатор конкретного свойства.</span><span class="sxs-lookup"><span data-stu-id="62279-345">The ID of the particular property.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-346">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-346">Element Information</span></span>



| <span data-ttu-id="62279-347">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-347">Parent Element</span></span>      | <span data-ttu-id="62279-348">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-348">Child Elements</span></span>         |
|---------------------|------------------------|
| [<span data-ttu-id="62279-349">метаданных</span><span class="sxs-lookup"><span data-stu-id="62279-349">metadata</span></span>](#syntax) | <span data-ttu-id="62279-350">Нет.</span><span class="sxs-lookup"><span data-stu-id="62279-350">None.</span></span> <span data-ttu-id="62279-351">Текст разрешен.</span><span class="sxs-lookup"><span data-stu-id="62279-351">Text is allowed.</span></span> |



 

## <a name="metadata"></a><span data-ttu-id="62279-352">метаданные</span><span class="sxs-lookup"><span data-stu-id="62279-352">metadata</span></span>

<span data-ttu-id="62279-353">Контейнер для элементов и текста, определяющий метаданные для конкретного файла.</span><span class="sxs-lookup"><span data-stu-id="62279-353">A container for elements and text defining metadata for the particular file.</span></span> <span data-ttu-id="62279-354">Несколько элементов [метаданных](#syntax) могут содержаться в одном узле [файла](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="62279-354">Multiple [metadata](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-355">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-355">Syntax</span></span>


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-356">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-356">Attributes</span></span>

<span data-ttu-id="62279-357">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="62279-357">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="62279-358">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-358">Element Information</span></span>



| <span data-ttu-id="62279-359">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-359">Parent Element</span></span>  | <span data-ttu-id="62279-360">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-360">Child Elements</span></span>           |
|-----------------|--------------------------|
| [<span data-ttu-id="62279-361">file</span><span class="sxs-lookup"><span data-stu-id="62279-361">file</span></span>](#syntax) | [<span data-ttu-id="62279-362">имажепроперти</span><span class="sxs-lookup"><span data-stu-id="62279-362">imageproperty</span></span>](#syntax) |



 

## <a name="netplace"></a><span data-ttu-id="62279-363">нетплаце</span><span class="sxs-lookup"><span data-stu-id="62279-363">netplace</span></span>

<span data-ttu-id="62279-364">Определяет целевой объект для сетевого размещения, который создается в **окне "Мое сетевое окружение** " после завершения передачи.</span><span class="sxs-lookup"><span data-stu-id="62279-364">Defines the target for a network place that is created in **My Network Places** when the upload is complete.</span></span> <span data-ttu-id="62279-365">Создание сетевого расположения может быть предотвращено с помощью метода [**ипублишингвизард:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="62279-365">Creation of a network place can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-366">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-366">Syntax</span></span>


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-367">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-367">Attributes</span></span>



| <span data-ttu-id="62279-368">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-368">Attribute</span></span> | <span data-ttu-id="62279-369">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-369">Description</span></span>                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62279-370">comment</span><span class="sxs-lookup"><span data-stu-id="62279-370">comment</span></span>   | <span data-ttu-id="62279-371">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-371">Required.</span></span> <span data-ttu-id="62279-372">Комментарий, отображаемый для значка сетевого размещения при наведении на него курсора.</span><span class="sxs-lookup"><span data-stu-id="62279-372">The comment displayed for the network place icon when the cursor rests on it.</span></span>         |
| <span data-ttu-id="62279-373">href</span><span class="sxs-lookup"><span data-stu-id="62279-373">href</span></span>      | <span data-ttu-id="62279-374">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-374">Required.</span></span> <span data-ttu-id="62279-375">URL-адрес записи сетевого размещения.</span><span class="sxs-lookup"><span data-stu-id="62279-375">The URL of the network place entry.</span></span>                                                   |
| <span data-ttu-id="62279-376">name</span><span class="sxs-lookup"><span data-stu-id="62279-376">name</span></span>      | <span data-ttu-id="62279-377">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-377">Required.</span></span> <span data-ttu-id="62279-378">Имя для значка сетевого расположения, которое отображается в папке " **Мое сетевое окружение** ".</span><span class="sxs-lookup"><span data-stu-id="62279-378">The name for the network place icon that appears in the **My Network Places** folder.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-379">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-379">Element Information</span></span>



| <span data-ttu-id="62279-380">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-380">Parent Element</span></span>        | <span data-ttu-id="62279-381">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-381">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="62279-382">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-382">uploadinfo</span></span>](#syntax) | <span data-ttu-id="62279-383">Нет.</span><span class="sxs-lookup"><span data-stu-id="62279-383">None.</span></span> <span data-ttu-id="62279-384">Текст разрешен.</span><span class="sxs-lookup"><span data-stu-id="62279-384">Text is allowed.</span></span> |



 

## <a name="post"></a><span data-ttu-id="62279-385">post</span><span class="sxs-lookup"><span data-stu-id="62279-385">post</span></span>

<span data-ttu-id="62279-386">URL-адрес, на который должен быть отправлен файл.</span><span class="sxs-lookup"><span data-stu-id="62279-386">URL to which the file should be posted.</span></span> <span data-ttu-id="62279-387">Этот элемент добавляется службой, когда передается в виде составного сообщения, а с помощью [формдата](#syntax)используется для создания заголовка POST.</span><span class="sxs-lookup"><span data-stu-id="62279-387">This element is added by the service when the transfer is done as a multi-part post and, with [formdata](#syntax), is used to build the post header.</span></span> <span data-ttu-id="62279-388">Если служба выбирает выполнение передачи файлов с помощью протокола WebDAV, он не должен добавлять этот элемент.</span><span class="sxs-lookup"><span data-stu-id="62279-388">If the service chooses to perform the file transfer using World Wide Web Distributed Authoring and Versioning (WebDAV), it should not add this element.</span></span> <span data-ttu-id="62279-389">Несколько элементов [POST](#syntax) могут содержаться в одном узле [файла](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="62279-389">Multiple [post](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-390">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-390">Syntax</span></span>


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-391">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-391">Attributes</span></span>



| <span data-ttu-id="62279-392">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-392">Attribute</span></span> | <span data-ttu-id="62279-393">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-393">Description</span></span>                                                                    |
|-----------|--------------------------------------------------------------------------------|
| <span data-ttu-id="62279-394">имя_файла</span><span class="sxs-lookup"><span data-stu-id="62279-394">filename</span></span>  | <span data-ttu-id="62279-395">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="62279-395">Optional.</span></span> <span data-ttu-id="62279-396">Имя файла для опубликованного файла.</span><span class="sxs-lookup"><span data-stu-id="62279-396">The file name for the posted file.</span></span>                                   |
| <span data-ttu-id="62279-397">href</span><span class="sxs-lookup"><span data-stu-id="62279-397">href</span></span>      | <span data-ttu-id="62279-398">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-398">Required.</span></span> <span data-ttu-id="62279-399">URL-адрес конечной папки.</span><span class="sxs-lookup"><span data-stu-id="62279-399">The URL of the destination folder.</span></span>                                   |
| <span data-ttu-id="62279-400">name</span><span class="sxs-lookup"><span data-stu-id="62279-400">name</span></span>      | <span data-ttu-id="62279-401">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-401">Required.</span></span> <span data-ttu-id="62279-402">Определяет имя данных формы, связанное с этим разделом записи.</span><span class="sxs-lookup"><span data-stu-id="62279-402">Defines the form data name associated with this section of the post.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-403">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-403">Element Information</span></span>



| <span data-ttu-id="62279-404">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-404">Parent Element</span></span>  | <span data-ttu-id="62279-405">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-405">Child Elements</span></span>      |
|-----------------|---------------------|
| [<span data-ttu-id="62279-406">file</span><span class="sxs-lookup"><span data-stu-id="62279-406">file</span></span>](#syntax) | [<span data-ttu-id="62279-407">формдата</span><span class="sxs-lookup"><span data-stu-id="62279-407">formdata</span></span>](#syntax) |



 

## <a name="resize"></a><span data-ttu-id="62279-408">изменить размер</span><span class="sxs-lookup"><span data-stu-id="62279-408">resize</span></span>

<span data-ttu-id="62279-409">Определяет масштабирование и повторное сжатие файла изображения в формате JPEG.</span><span class="sxs-lookup"><span data-stu-id="62279-409">Defines the scaling and recompression of an image file into JPEG format.</span></span> <span data-ttu-id="62279-410">Если исходный файл уже имеет формат JPEG и меньше или равен указанной ширине и высоте, размер не изменяется.</span><span class="sxs-lookup"><span data-stu-id="62279-410">If the source file is already in JPEG format and is less than or equal to the specified width and height, it is not sized.</span></span> <span data-ttu-id="62279-411">Если исходный файл не является JPEG-файлом, он преобразуется.</span><span class="sxs-lookup"><span data-stu-id="62279-411">If the source file is not a JPEG file, it is converted.</span></span> <span data-ttu-id="62279-412">Масштабирование, повторное сжатие и преобразование файла можно предотвратить с помощью метода [**ипублишингвизард:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .</span><span class="sxs-lookup"><span data-stu-id="62279-412">Scaling, recompression, and conversion of the file can be prevented through the [**IPublishingWizard::Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) method.</span></span> <span data-ttu-id="62279-413">Несколько элементов [изменения размера](#syntax) могут содержаться в одном узле [файла](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="62279-413">Multiple [resize](#syntax) elements may be contained under a single [file](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-414">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-414">Syntax</span></span>


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-415">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-415">Attributes</span></span>



| <span data-ttu-id="62279-416">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-416">Attribute</span></span> | <span data-ttu-id="62279-417">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-417">Description</span></span>                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62279-418">/CX</span><span class="sxs-lookup"><span data-stu-id="62279-418">cx</span></span>        | <span data-ttu-id="62279-419">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-419">Required.</span></span> <span data-ttu-id="62279-420">Ширина изображения в пикселях после отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-420">The width of the image, in pixels, after uploading.</span></span> <span data-ttu-id="62279-421">Если это значение равно 0, то значение **CX** вычисляется по значению **CY** для сохранения относительных измерений.</span><span class="sxs-lookup"><span data-stu-id="62279-421">If this value is 0, then **cx** is calculated from the **cy** value to preserve relative dimensions.</span></span>  |
| <span data-ttu-id="62279-422">cy</span><span class="sxs-lookup"><span data-stu-id="62279-422">cy</span></span>        | <span data-ttu-id="62279-423">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-423">Required.</span></span> <span data-ttu-id="62279-424">Высота изображения в пикселях после отправки.</span><span class="sxs-lookup"><span data-stu-id="62279-424">The height of the image, in pixels, after uploading.</span></span> <span data-ttu-id="62279-425">Если это значение равно 0, то **CY** вычисляется по значению **CX** , чтобы сохранить относительные размеры.</span><span class="sxs-lookup"><span data-stu-id="62279-425">If this value is 0, then **cy** is calculated from the **cx** value to preserve relative dimensions.</span></span> |
| <span data-ttu-id="62279-426">качество</span><span class="sxs-lookup"><span data-stu-id="62279-426">quality</span></span>   | <span data-ttu-id="62279-427">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-427">Required.</span></span> <span data-ttu-id="62279-428">Значение качества JPEG (от 0 до 100) с 100 является самым высоким качеством.</span><span class="sxs-lookup"><span data-stu-id="62279-428">The JPEG quality value, between 0 and 100, with 100 being the highest quality.</span></span>                                                                            |



 

### <a name="element-information"></a><span data-ttu-id="62279-429">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-429">Element Information</span></span>



| <span data-ttu-id="62279-430">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-430">Parent Element</span></span>  | <span data-ttu-id="62279-431">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-431">Child Elements</span></span> |
|-----------------|----------------|
| [<span data-ttu-id="62279-432">file</span><span class="sxs-lookup"><span data-stu-id="62279-432">file</span></span>](#syntax) | <span data-ttu-id="62279-433">Нет.</span><span class="sxs-lookup"><span data-stu-id="62279-433">None.</span></span>          |



 

## <a name="successpage"></a><span data-ttu-id="62279-434">сукцесспаже</span><span class="sxs-lookup"><span data-stu-id="62279-434">successpage</span></span>

<span data-ttu-id="62279-435">Указывает серверную HTML-страницу, отображаемую при успешном завершении передачи.</span><span class="sxs-lookup"><span data-stu-id="62279-435">Specifies the server-side HTML page to display if the upload is successful.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-436">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-436">Syntax</span></span>


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-437">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-437">Attributes</span></span>



| <span data-ttu-id="62279-438">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-438">Attribute</span></span> | <span data-ttu-id="62279-439">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-439">Description</span></span>                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62279-440">href</span><span class="sxs-lookup"><span data-stu-id="62279-440">href</span></span>      | <span data-ttu-id="62279-441">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-441">Required.</span></span> <span data-ttu-id="62279-442">URL-адрес страницы на стороне сервера, отображаемой при успешном завершении передачи.</span><span class="sxs-lookup"><span data-stu-id="62279-442">The URL of the server-side HTML page to display if the upload is successful.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-443">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-443">Element Information</span></span>



| <span data-ttu-id="62279-444">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-444">Parent Element</span></span>        | <span data-ttu-id="62279-445">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-445">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="62279-446">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-446">uploadinfo</span></span>](#syntax) | <span data-ttu-id="62279-447">Нет.</span><span class="sxs-lookup"><span data-stu-id="62279-447">None.</span></span> <span data-ttu-id="62279-448">Текст разрешен.</span><span class="sxs-lookup"><span data-stu-id="62279-448">Text is allowed.</span></span> |



 

## <a name="target"></a><span data-ttu-id="62279-449">target</span><span class="sxs-lookup"><span data-stu-id="62279-449">target</span></span>

<span data-ttu-id="62279-450">Папка назначения, указанная в формате UNC или на сервере WebDAV.</span><span class="sxs-lookup"><span data-stu-id="62279-450">A destination folder specified in Universal Naming Convention (UNC) format or as a WebDAV server.</span></span> <span data-ttu-id="62279-451">Служба добавляет этот целевой объект для указания целевой папки, если в процессе перемещения используется протокол WebDAV или файловая система.</span><span class="sxs-lookup"><span data-stu-id="62279-451">The service adds this target to specify a destination folder if the transfer uses a WebDAV or file system protocol.</span></span> <span data-ttu-id="62279-452">Если служба выбирает выполнение передачи файла в виде составного сообщения, она не должна добавлять этот элемент.</span><span class="sxs-lookup"><span data-stu-id="62279-452">If the service chooses to perform the file transfer as a multi-part post, it should not add this element.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-453">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-453">Syntax</span></span>


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-454">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-454">Attributes</span></span>



| <span data-ttu-id="62279-455">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-455">Attribute</span></span> | <span data-ttu-id="62279-456">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-456">Description</span></span>                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62279-457">href</span><span class="sxs-lookup"><span data-stu-id="62279-457">href</span></span>      | <span data-ttu-id="62279-458">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-458">Required.</span></span> <span data-ttu-id="62279-459">URL-адрес конечной папки.</span><span class="sxs-lookup"><span data-stu-id="62279-459">The URL of the destination folder.</span></span> <span data-ttu-id="62279-460">Используйте форму **https://** для WebDAV или форму **\\ \\ \\ общего серверного ресурса** для UNC.</span><span class="sxs-lookup"><span data-stu-id="62279-460">Use the **https://** form for WebDAV or the **\\\\server\\share** form for UNC.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-461">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-461">Element Information</span></span>



| <span data-ttu-id="62279-462">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-462">Parent Element</span></span>        | <span data-ttu-id="62279-463">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-463">Child Elements</span></span>         |
|-----------------------|------------------------|
| [<span data-ttu-id="62279-464">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-464">uploadinfo</span></span>](#syntax) | <span data-ttu-id="62279-465">Нет.</span><span class="sxs-lookup"><span data-stu-id="62279-465">None.</span></span> <span data-ttu-id="62279-466">Текст разрешен.</span><span class="sxs-lookup"><span data-stu-id="62279-466">Text is allowed.</span></span> |



 

## <a name="transfermanifest"></a><span data-ttu-id="62279-467">трансферманифест</span><span class="sxs-lookup"><span data-stu-id="62279-467">transfermanifest</span></span>

<span data-ttu-id="62279-468">Родительский узел файла манифеста перемещения.</span><span class="sxs-lookup"><span data-stu-id="62279-468">The parent node of the transfer manifest file.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-469">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-469">Syntax</span></span>


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-470">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-470">Attributes</span></span>

<span data-ttu-id="62279-471">Отсутствует.</span><span class="sxs-lookup"><span data-stu-id="62279-471">None.</span></span>

### <a name="element-information"></a><span data-ttu-id="62279-472">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-472">Element Information</span></span>



| <span data-ttu-id="62279-473">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-473">Parent Element</span></span> | <span data-ttu-id="62279-474">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-474">Child Elements</span></span>                                                    |
|----------------|-------------------------------------------------------------------|
| <span data-ttu-id="62279-475">Нет</span><span class="sxs-lookup"><span data-stu-id="62279-475">None</span></span>           | <span data-ttu-id="62279-476">[FileList](#syntax), [фолдерлист](#syntax), [уплоадинфо](#syntax)</span><span class="sxs-lookup"><span data-stu-id="62279-476">[filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax)</span></span> |



 

## <a name="uploadinfo"></a><span data-ttu-id="62279-477">уплоадинфо</span><span class="sxs-lookup"><span data-stu-id="62279-477">uploadinfo</span></span>

<span data-ttu-id="62279-478">Контейнер для элементов, предоставляющий сведения из сайта отправки, используемого в транзакции.</span><span class="sxs-lookup"><span data-stu-id="62279-478">A container for elements providing information from the upload site used in the transaction.</span></span> <span data-ttu-id="62279-479">Несколько элементов [уплоадинфо](#syntax) могут содержаться в одном узле [трансферманифест](#syntax) .</span><span class="sxs-lookup"><span data-stu-id="62279-479">Multiple [uploadinfo](#syntax) elements may be contained under a single [transfermanifest](#syntax) node.</span></span>

### <a name="syntax"></a><span data-ttu-id="62279-480">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="62279-480">Syntax</span></span>


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a><span data-ttu-id="62279-481">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="62279-481">Attributes</span></span>



| <span data-ttu-id="62279-482">Атрибут</span><span class="sxs-lookup"><span data-stu-id="62279-482">Attribute</span></span>    | <span data-ttu-id="62279-483">Описание</span><span class="sxs-lookup"><span data-stu-id="62279-483">Description</span></span>                                                                 |
|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="62279-484">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="62279-484">friendlyname</span></span> | <span data-ttu-id="62279-485">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="62279-485">Required.</span></span> <span data-ttu-id="62279-486">Понятное имя для веб-сайта, отображаемое в мастере.</span><span class="sxs-lookup"><span data-stu-id="62279-486">A friendly name for the website which is displayed in the wizard.</span></span> |



 

### <a name="element-information"></a><span data-ttu-id="62279-487">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="62279-487">Element Information</span></span>



| <span data-ttu-id="62279-488">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="62279-488">Parent Element</span></span>              | <span data-ttu-id="62279-489">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="62279-489">Child Elements</span></span>                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62279-490">трансферманифест</span><span class="sxs-lookup"><span data-stu-id="62279-490">transfermanifest</span></span>](#syntax) | <span data-ttu-id="62279-491">[канцелледпаже](#syntax), [фаилурепаже](#syntax), [Избранное](#syntax), [хтмлуи](#syntax), [нетплаце](#syntax), [сукцесспаже](#syntax), [Target](#syntax)</span><span class="sxs-lookup"><span data-stu-id="62279-491">[cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax)</span></span> |



 

 

 



