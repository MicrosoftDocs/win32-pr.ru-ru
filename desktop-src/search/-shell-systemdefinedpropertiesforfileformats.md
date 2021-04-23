---
description: Microsoft Windows предоставляет ряд системных свойств, которые можно использовать для форматов файлов.
ms.assetid: 3a25c4fb-ffea-4524-b59b-912416b2fc7d
title: Свойства System-Defined для пользовательских форматов файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1a3645e383ea751298f766eacf60f5ac95ece3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144053"
---
# <a name="system-defined-properties-for-custom-file-formats"></a><span data-ttu-id="00201-103">Свойства System-Defined для пользовательских форматов файлов</span><span class="sxs-lookup"><span data-stu-id="00201-103">System-Defined Properties for Custom File Formats</span></span>

<span data-ttu-id="00201-104">Microsoft Windows предоставляет ряд системных свойств, которые можно использовать для форматов файлов.</span><span class="sxs-lookup"><span data-stu-id="00201-104">Microsoft Windows supplies a number of system properties that you can use for your file formats.</span></span> <span data-ttu-id="00201-105">При создании пользовательского формата файла необходимо поддерживать как можно больше системных свойств.</span><span class="sxs-lookup"><span data-stu-id="00201-105">If you are creating a custom file format, you should support as many system-defined properties as you can.</span></span> <span data-ttu-id="00201-106">Перед созданием обработчика настраиваемого свойства необходимо просмотреть обработчики, предоставляемые системой, чтобы определить, можно ли использовать его вместо написания собственного.</span><span class="sxs-lookup"><span data-stu-id="00201-106">Before creating a custom property handler, you should review the system-supplied handlers to see if you can use one instead of writing your own.</span></span>

<span data-ttu-id="00201-107">В следующей таблице приведены категории форматов файлов, а затем перечислены наиболее важные системные свойства, которые должен поддерживать ваш формат файла.</span><span class="sxs-lookup"><span data-stu-id="00201-107">The following table categorizes file formats and then lists the most important system properties your file format should support.</span></span> <span data-ttu-id="00201-108">Чтобы обеспечить хорошую работу пользователей, необходимо поддерживать все свойства приоритета 1 и 2 для категории формата файлов.</span><span class="sxs-lookup"><span data-stu-id="00201-108">To provide a good user experience, you should support all priority 1 and 2 properties for your category of file format.</span></span>

-   [<span data-ttu-id="00201-109">Операции взаимодействия</span><span class="sxs-lookup"><span data-stu-id="00201-109">Communications</span></span>](#communications)
-   [<span data-ttu-id="00201-110">Контакты</span><span class="sxs-lookup"><span data-stu-id="00201-110">Contacts</span></span>](#contacts)
-   [<span data-ttu-id="00201-111">Документы</span><span class="sxs-lookup"><span data-stu-id="00201-111">Documents</span></span>](#documents)
-   [<span data-ttu-id="00201-112">Универсальный шаблон</span><span class="sxs-lookup"><span data-stu-id="00201-112">Generic</span></span>](#generic)
-   [<span data-ttu-id="00201-113">Музыка</span><span class="sxs-lookup"><span data-stu-id="00201-113">Music</span></span>](#music)
-   [<span data-ttu-id="00201-114">Рисунки</span><span class="sxs-lookup"><span data-stu-id="00201-114">Pictures</span></span>](#pictures)
-   [<span data-ttu-id="00201-115">Видео</span><span class="sxs-lookup"><span data-stu-id="00201-115">Videos</span></span>](#videos)
-   [<span data-ttu-id="00201-116">См. также</span><span class="sxs-lookup"><span data-stu-id="00201-116">Related topics</span></span>](#related-topics)

## <a name="communications"></a><span data-ttu-id="00201-117">Коммуникации</span><span class="sxs-lookup"><span data-stu-id="00201-117">Communications</span></span>



| <span data-ttu-id="00201-118">Имя</span><span class="sxs-lookup"><span data-stu-id="00201-118">Name</span></span>            | <span data-ttu-id="00201-119">Свойство</span><span class="sxs-lookup"><span data-stu-id="00201-119">Property</span></span>                               | <span data-ttu-id="00201-120">Приоритет</span><span class="sxs-lookup"><span data-stu-id="00201-120">Priority</span></span> |
|-----------------|----------------------------------------|----------|
| <span data-ttu-id="00201-121">Дата получения</span><span class="sxs-lookup"><span data-stu-id="00201-121">Date received</span></span>   | <span data-ttu-id="00201-122">System. Message. Датерецеивед</span><span class="sxs-lookup"><span data-stu-id="00201-122">System.Message.DateReceived</span></span>            | <span data-ttu-id="00201-123">1</span><span class="sxs-lookup"><span data-stu-id="00201-123">1</span></span>        |
| <span data-ttu-id="00201-124">Из имен</span><span class="sxs-lookup"><span data-stu-id="00201-124">From names</span></span>      | <span data-ttu-id="00201-125">System. Message. Фромнаме</span><span class="sxs-lookup"><span data-stu-id="00201-125">System.Message.FromName</span></span>                | <span data-ttu-id="00201-126">1</span><span class="sxs-lookup"><span data-stu-id="00201-126">1</span></span>        |
| <span data-ttu-id="00201-127">Имеет вложения</span><span class="sxs-lookup"><span data-stu-id="00201-127">Has attachments</span></span> | <span data-ttu-id="00201-128">System. Message. Хасаттачментс</span><span class="sxs-lookup"><span data-stu-id="00201-128">System.Message.HasAttachments</span></span>          | <span data-ttu-id="00201-129">1</span><span class="sxs-lookup"><span data-stu-id="00201-129">1</span></span>        |
| <span data-ttu-id="00201-130">Mailbox</span><span class="sxs-lookup"><span data-stu-id="00201-130">Mailbox</span></span>         | <span data-ttu-id="00201-131">System. Communication. стореддисплайнаме</span><span class="sxs-lookup"><span data-stu-id="00201-131">System.Communication.storeddisplayname</span></span> | <span data-ttu-id="00201-132">1</span><span class="sxs-lookup"><span data-stu-id="00201-132">1</span></span>        |
| <span data-ttu-id="00201-133">name</span><span class="sxs-lookup"><span data-stu-id="00201-133">Name</span></span>            | <span data-ttu-id="00201-134">System. имя_файла</span><span class="sxs-lookup"><span data-stu-id="00201-134">System.FileName</span></span>                        | <span data-ttu-id="00201-135">1</span><span class="sxs-lookup"><span data-stu-id="00201-135">1</span></span>        |
| <span data-ttu-id="00201-136">Субъект</span><span class="sxs-lookup"><span data-stu-id="00201-136">Subject</span></span>         | <span data-ttu-id="00201-137">System. subject</span><span class="sxs-lookup"><span data-stu-id="00201-137">System.Subject</span></span>                         | <span data-ttu-id="00201-138">1</span><span class="sxs-lookup"><span data-stu-id="00201-138">1</span></span>        |
| <span data-ttu-id="00201-139">В имена</span><span class="sxs-lookup"><span data-stu-id="00201-139">To names</span></span>        | <span data-ttu-id="00201-140">System. Message. Тонаме</span><span class="sxs-lookup"><span data-stu-id="00201-140">System.Message.ToName</span></span>                  | <span data-ttu-id="00201-141">1</span><span class="sxs-lookup"><span data-stu-id="00201-141">1</span></span>        |
| <span data-ttu-id="00201-142">Категория</span><span class="sxs-lookup"><span data-stu-id="00201-142">Category</span></span>        | <span data-ttu-id="00201-143">System. Category</span><span class="sxs-lookup"><span data-stu-id="00201-143">System.Category</span></span>                        | <span data-ttu-id="00201-144">2</span><span class="sxs-lookup"><span data-stu-id="00201-144">2</span></span>        |
| <span data-ttu-id="00201-145">Тип</span><span class="sxs-lookup"><span data-stu-id="00201-145">Type</span></span>            | <span data-ttu-id="00201-146">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="00201-146">System.PerceivedType</span></span>                   | <span data-ttu-id="00201-147">2</span><span class="sxs-lookup"><span data-stu-id="00201-147">2</span></span>        |



 

## <a name="contacts"></a><span data-ttu-id="00201-148">Контакты</span><span class="sxs-lookup"><span data-stu-id="00201-148">Contacts</span></span>



| <span data-ttu-id="00201-149">Имя</span><span class="sxs-lookup"><span data-stu-id="00201-149">Name</span></span>             | <span data-ttu-id="00201-150">Свойство</span><span class="sxs-lookup"><span data-stu-id="00201-150">Property</span></span>                           | <span data-ttu-id="00201-151">Приоритет</span><span class="sxs-lookup"><span data-stu-id="00201-151">Priority</span></span> |
|------------------|------------------------------------|----------|
| <span data-ttu-id="00201-152">Имя учетной записи</span><span class="sxs-lookup"><span data-stu-id="00201-152">Account Name</span></span>     | <span data-ttu-id="00201-153">System. Communication. AccountName</span><span class="sxs-lookup"><span data-stu-id="00201-153">System.Communication.AccountName</span></span>   | <span data-ttu-id="00201-154">1</span><span class="sxs-lookup"><span data-stu-id="00201-154">1</span></span>        |
| <span data-ttu-id="00201-155">Business Phone</span><span class="sxs-lookup"><span data-stu-id="00201-155">Business Phone</span></span>   | <span data-ttu-id="00201-156">System. Contact. Бусинесстелефоне</span><span class="sxs-lookup"><span data-stu-id="00201-156">System.Contact.BusinessTelephone</span></span>   | <span data-ttu-id="00201-157">1</span><span class="sxs-lookup"><span data-stu-id="00201-157">1</span></span>        |
| <span data-ttu-id="00201-158">Company</span><span class="sxs-lookup"><span data-stu-id="00201-158">Company</span></span>          | <span data-ttu-id="00201-159">System. Company</span><span class="sxs-lookup"><span data-stu-id="00201-159">System.Company</span></span>                     | <span data-ttu-id="00201-160">1</span><span class="sxs-lookup"><span data-stu-id="00201-160">1</span></span>        |
| <span data-ttu-id="00201-161">Электронная почта</span><span class="sxs-lookup"><span data-stu-id="00201-161">Email Address</span></span>    | <span data-ttu-id="00201-162">System. Contact. Примаремаиладдресс</span><span class="sxs-lookup"><span data-stu-id="00201-162">System.Contact.PrimaryEmailAddress</span></span> | <span data-ttu-id="00201-163">1</span><span class="sxs-lookup"><span data-stu-id="00201-163">1</span></span>        |
| <span data-ttu-id="00201-164">Важность</span><span class="sxs-lookup"><span data-stu-id="00201-164">Importance</span></span>       | <span data-ttu-id="00201-165">System. Импортанцетекст</span><span class="sxs-lookup"><span data-stu-id="00201-165">System.ImportanceText</span></span>              | <span data-ttu-id="00201-166">1</span><span class="sxs-lookup"><span data-stu-id="00201-166">1</span></span>        |
| <span data-ttu-id="00201-167">Мобильный телефон</span><span class="sxs-lookup"><span data-stu-id="00201-167">Mobile Phone</span></span>     | <span data-ttu-id="00201-168">System. Contact. Мобилетелефоне</span><span class="sxs-lookup"><span data-stu-id="00201-168">System.Contact.MobileTelephone</span></span>     | <span data-ttu-id="00201-169">1</span><span class="sxs-lookup"><span data-stu-id="00201-169">1</span></span>        |
| <span data-ttu-id="00201-170">Рабочий адрес</span><span class="sxs-lookup"><span data-stu-id="00201-170">Business address</span></span> | <span data-ttu-id="00201-171">System. Contact. Бусинессаддресс</span><span class="sxs-lookup"><span data-stu-id="00201-171">System.Contact.BusinessAddress</span></span>     | <span data-ttu-id="00201-172">2</span><span class="sxs-lookup"><span data-stu-id="00201-172">2</span></span>        |
| <span data-ttu-id="00201-173">Бизнес-Факс</span><span class="sxs-lookup"><span data-stu-id="00201-173">Business fax</span></span>     | <span data-ttu-id="00201-174">System. Contact. Бусинессфакснумбер</span><span class="sxs-lookup"><span data-stu-id="00201-174">System.Contact.BusinessFaxNumber</span></span>   | <span data-ttu-id="00201-175">2</span><span class="sxs-lookup"><span data-stu-id="00201-175">2</span></span>        |
| <span data-ttu-id="00201-176">Категория</span><span class="sxs-lookup"><span data-stu-id="00201-176">Category</span></span>         | <span data-ttu-id="00201-177">System. Category</span><span class="sxs-lookup"><span data-stu-id="00201-177">System.Category</span></span>                    | <span data-ttu-id="00201-178">2</span><span class="sxs-lookup"><span data-stu-id="00201-178">2</span></span>        |
| <span data-ttu-id="00201-179">Домашний адрес</span><span class="sxs-lookup"><span data-stu-id="00201-179">Home address</span></span>     | <span data-ttu-id="00201-180">System. Contact. HomeAddress</span><span class="sxs-lookup"><span data-stu-id="00201-180">System.Contact.HomeAddress</span></span>         | <span data-ttu-id="00201-181">2</span><span class="sxs-lookup"><span data-stu-id="00201-181">2</span></span>        |
| <span data-ttu-id="00201-182">Домашний телефон</span><span class="sxs-lookup"><span data-stu-id="00201-182">Home phone</span></span>       | <span data-ttu-id="00201-183">System. Contact. Хометелефоне</span><span class="sxs-lookup"><span data-stu-id="00201-183">System.Contact.HomeTelephone</span></span>       | <span data-ttu-id="00201-184">2</span><span class="sxs-lookup"><span data-stu-id="00201-184">2</span></span>        |
| <span data-ttu-id="00201-185">Название</span><span class="sxs-lookup"><span data-stu-id="00201-185">Title</span></span>            | <span data-ttu-id="00201-186">System.Title</span><span class="sxs-lookup"><span data-stu-id="00201-186">System.Title</span></span>                       | <span data-ttu-id="00201-187">2</span><span class="sxs-lookup"><span data-stu-id="00201-187">2</span></span>        |



 

## <a name="documents"></a><span data-ttu-id="00201-188">Документы</span><span class="sxs-lookup"><span data-stu-id="00201-188">Documents</span></span>



| <span data-ttu-id="00201-189">Имя</span><span class="sxs-lookup"><span data-stu-id="00201-189">Name</span></span>      | <span data-ttu-id="00201-190">Свойство</span><span class="sxs-lookup"><span data-stu-id="00201-190">Property</span></span>             | <span data-ttu-id="00201-191">Приоритет</span><span class="sxs-lookup"><span data-stu-id="00201-191">Priority</span></span> |
|-----------|----------------------|----------|
| <span data-ttu-id="00201-192">Авторы</span><span class="sxs-lookup"><span data-stu-id="00201-192">Authors</span></span>   | <span data-ttu-id="00201-193">System.Author</span><span class="sxs-lookup"><span data-stu-id="00201-193">System.Author</span></span>        | <span data-ttu-id="00201-194">1</span><span class="sxs-lookup"><span data-stu-id="00201-194">1</span></span>        |
| <span data-ttu-id="00201-195">Полнотекстовый</span><span class="sxs-lookup"><span data-stu-id="00201-195">Full Text</span></span> | <span data-ttu-id="00201-196">System. FullText</span><span class="sxs-lookup"><span data-stu-id="00201-196">System.FullText</span></span>      | <span data-ttu-id="00201-197">1</span><span class="sxs-lookup"><span data-stu-id="00201-197">1</span></span>        |
| <span data-ttu-id="00201-198">Теги</span><span class="sxs-lookup"><span data-stu-id="00201-198">Tags</span></span>      | <span data-ttu-id="00201-199">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="00201-199">System.Keywords</span></span>      | <span data-ttu-id="00201-200">1</span><span class="sxs-lookup"><span data-stu-id="00201-200">1</span></span>        |
| <span data-ttu-id="00201-201">Тип</span><span class="sxs-lookup"><span data-stu-id="00201-201">Type</span></span>      | <span data-ttu-id="00201-202">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="00201-202">System.PerceivedType</span></span> | <span data-ttu-id="00201-203">1</span><span class="sxs-lookup"><span data-stu-id="00201-203">1</span></span>        |
| <span data-ttu-id="00201-204">Категория</span><span class="sxs-lookup"><span data-stu-id="00201-204">Category</span></span>  | <span data-ttu-id="00201-205">System. Category</span><span class="sxs-lookup"><span data-stu-id="00201-205">System.Category</span></span>      | <span data-ttu-id="00201-206">2</span><span class="sxs-lookup"><span data-stu-id="00201-206">2</span></span>        |
| <span data-ttu-id="00201-207">Название</span><span class="sxs-lookup"><span data-stu-id="00201-207">Title</span></span>     | <span data-ttu-id="00201-208">System.Title</span><span class="sxs-lookup"><span data-stu-id="00201-208">System.Title</span></span>         | <span data-ttu-id="00201-209">2</span><span class="sxs-lookup"><span data-stu-id="00201-209">2</span></span>        |



 

## <a name="generic"></a><span data-ttu-id="00201-210">Универсальный шаблон</span><span class="sxs-lookup"><span data-stu-id="00201-210">Generic</span></span>



| <span data-ttu-id="00201-211">Имя</span><span class="sxs-lookup"><span data-stu-id="00201-211">Name</span></span>     | <span data-ttu-id="00201-212">Свойство</span><span class="sxs-lookup"><span data-stu-id="00201-212">Property</span></span>             | <span data-ttu-id="00201-213">Приоритет</span><span class="sxs-lookup"><span data-stu-id="00201-213">Priority</span></span> |
|----------|----------------------|----------|
| <span data-ttu-id="00201-214">Авторы</span><span class="sxs-lookup"><span data-stu-id="00201-214">Authors</span></span>  | <span data-ttu-id="00201-215">System.Author</span><span class="sxs-lookup"><span data-stu-id="00201-215">System.Author</span></span>        | <span data-ttu-id="00201-216">1</span><span class="sxs-lookup"><span data-stu-id="00201-216">1</span></span>        |
| <span data-ttu-id="00201-217">Заголовок</span><span class="sxs-lookup"><span data-stu-id="00201-217">Title</span></span>    | <span data-ttu-id="00201-218">System.Title</span><span class="sxs-lookup"><span data-stu-id="00201-218">System.Title</span></span>         | <span data-ttu-id="00201-219">1</span><span class="sxs-lookup"><span data-stu-id="00201-219">1</span></span>        |
| <span data-ttu-id="00201-220">Тип</span><span class="sxs-lookup"><span data-stu-id="00201-220">Type</span></span>     | <span data-ttu-id="00201-221">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="00201-221">System.PerceivedType</span></span> | <span data-ttu-id="00201-222">1</span><span class="sxs-lookup"><span data-stu-id="00201-222">1</span></span>        |
| <span data-ttu-id="00201-223">Категория</span><span class="sxs-lookup"><span data-stu-id="00201-223">Category</span></span> | <span data-ttu-id="00201-224">System. Category</span><span class="sxs-lookup"><span data-stu-id="00201-224">System.Category</span></span>      | <span data-ttu-id="00201-225">2</span><span class="sxs-lookup"><span data-stu-id="00201-225">2</span></span>        |
| <span data-ttu-id="00201-226">Теги</span><span class="sxs-lookup"><span data-stu-id="00201-226">Tags</span></span>     | <span data-ttu-id="00201-227">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="00201-227">System.Keywords</span></span>      | <span data-ttu-id="00201-228">2</span><span class="sxs-lookup"><span data-stu-id="00201-228">2</span></span>        |



 

## <a name="music"></a><span data-ttu-id="00201-229">Музыка</span><span class="sxs-lookup"><span data-stu-id="00201-229">Music</span></span>



| <span data-ttu-id="00201-230">Имя</span><span class="sxs-lookup"><span data-stu-id="00201-230">Name</span></span>         | <span data-ttu-id="00201-231">Свойство</span><span class="sxs-lookup"><span data-stu-id="00201-231">Property</span></span>                     | <span data-ttu-id="00201-232">Приоритет</span><span class="sxs-lookup"><span data-stu-id="00201-232">Priority</span></span> |
|--------------|------------------------------|----------|
| \#           | <span data-ttu-id="00201-233">System. Music. Траккнумбер</span><span class="sxs-lookup"><span data-stu-id="00201-233">System.Music.TrackNumber</span></span>     | <span data-ttu-id="00201-234">1</span><span class="sxs-lookup"><span data-stu-id="00201-234">1</span></span>        |
| <span data-ttu-id="00201-235">Музыкальных</span><span class="sxs-lookup"><span data-stu-id="00201-235">Album</span></span>        | <span data-ttu-id="00201-236">System. Music. Албумтитле</span><span class="sxs-lookup"><span data-stu-id="00201-236">System.Music.AlbumTitle</span></span>      | <span data-ttu-id="00201-237">1</span><span class="sxs-lookup"><span data-stu-id="00201-237">1</span></span>        |
| <span data-ttu-id="00201-238">Исполнител</span><span class="sxs-lookup"><span data-stu-id="00201-238">Artists</span></span>      | <span data-ttu-id="00201-239">System. Music. исполнителя</span><span class="sxs-lookup"><span data-stu-id="00201-239">System.Music.Artist</span></span>          | <span data-ttu-id="00201-240">1</span><span class="sxs-lookup"><span data-stu-id="00201-240">1</span></span>        |
| <span data-ttu-id="00201-241">Genre</span><span class="sxs-lookup"><span data-stu-id="00201-241">Genre</span></span>        | <span data-ttu-id="00201-242">System. Music. Жанр</span><span class="sxs-lookup"><span data-stu-id="00201-242">System.Music.Genre</span></span>           | <span data-ttu-id="00201-243">1</span><span class="sxs-lookup"><span data-stu-id="00201-243">1</span></span>        |
| <span data-ttu-id="00201-244">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="00201-244">Rating</span></span>       | <span data-ttu-id="00201-245">System. Оценка</span><span class="sxs-lookup"><span data-stu-id="00201-245">System.Rating</span></span>                | <span data-ttu-id="00201-246">1</span><span class="sxs-lookup"><span data-stu-id="00201-246">1</span></span>        |
| <span data-ttu-id="00201-247">Заголовок</span><span class="sxs-lookup"><span data-stu-id="00201-247">Title</span></span>        | <span data-ttu-id="00201-248">System.Title</span><span class="sxs-lookup"><span data-stu-id="00201-248">System.Title</span></span>                 | <span data-ttu-id="00201-249">1</span><span class="sxs-lookup"><span data-stu-id="00201-249">1</span></span>        |
| <span data-ttu-id="00201-250">Исполнитель альбома</span><span class="sxs-lookup"><span data-stu-id="00201-250">Album Artist</span></span> | <span data-ttu-id="00201-251">System. Music. Албумартист</span><span class="sxs-lookup"><span data-stu-id="00201-251">System.Music.AlbumArtist</span></span>     | <span data-ttu-id="00201-252">2</span><span class="sxs-lookup"><span data-stu-id="00201-252">2</span></span>        |
| <span data-ttu-id="00201-253">Скорость</span><span class="sxs-lookup"><span data-stu-id="00201-253">Bit Rate</span></span>     | <span data-ttu-id="00201-254">System. Audio. Енкодингбитрате</span><span class="sxs-lookup"><span data-stu-id="00201-254">System.Audio.EncodingBitrate</span></span> | <span data-ttu-id="00201-255">2</span><span class="sxs-lookup"><span data-stu-id="00201-255">2</span></span>        |
| <span data-ttu-id="00201-256">Поведения</span><span class="sxs-lookup"><span data-stu-id="00201-256">Conductors</span></span>   | <span data-ttu-id="00201-257">System. Music. Проводник</span><span class="sxs-lookup"><span data-stu-id="00201-257">System.Music.Conductor</span></span>       | <span data-ttu-id="00201-258">2</span><span class="sxs-lookup"><span data-stu-id="00201-258">2</span></span>        |
| <span data-ttu-id="00201-259">Длина</span><span class="sxs-lookup"><span data-stu-id="00201-259">Length</span></span>       | <span data-ttu-id="00201-260">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="00201-260">System.Media.Duration</span></span>        | <span data-ttu-id="00201-261">2</span><span class="sxs-lookup"><span data-stu-id="00201-261">2</span></span>        |
| <span data-ttu-id="00201-262">Защищенный</span><span class="sxs-lookup"><span data-stu-id="00201-262">Protected</span></span>    | <span data-ttu-id="00201-263">System. DRM. для защиты</span><span class="sxs-lookup"><span data-stu-id="00201-263">System.DRM.IsProtected</span></span>       | <span data-ttu-id="00201-264">2</span><span class="sxs-lookup"><span data-stu-id="00201-264">2</span></span>        |
| <span data-ttu-id="00201-265">Year;</span><span class="sxs-lookup"><span data-stu-id="00201-265">Year</span></span>         | <span data-ttu-id="00201-266">System. Media. Year</span><span class="sxs-lookup"><span data-stu-id="00201-266">System.Media.Year</span></span>            | <span data-ttu-id="00201-267">2</span><span class="sxs-lookup"><span data-stu-id="00201-267">2</span></span>        |



 

## <a name="pictures"></a><span data-ttu-id="00201-268">Изображения</span><span class="sxs-lookup"><span data-stu-id="00201-268">Pictures</span></span>



| <span data-ttu-id="00201-269">Имя</span><span class="sxs-lookup"><span data-stu-id="00201-269">Name</span></span>          | <span data-ttu-id="00201-270">Свойство</span><span class="sxs-lookup"><span data-stu-id="00201-270">Property</span></span>                        | <span data-ttu-id="00201-271">Приоритет</span><span class="sxs-lookup"><span data-stu-id="00201-271">Priority</span></span> |
|---------------|---------------------------------|----------|
| <span data-ttu-id="00201-272">Дата импорта</span><span class="sxs-lookup"><span data-stu-id="00201-272">Date imported</span></span> | <span data-ttu-id="00201-273">System. Датеимпортед</span><span class="sxs-lookup"><span data-stu-id="00201-273">System.DateImported</span></span>             | <span data-ttu-id="00201-274">1</span><span class="sxs-lookup"><span data-stu-id="00201-274">1</span></span>        |
| <span data-ttu-id="00201-275">Дата съемки</span><span class="sxs-lookup"><span data-stu-id="00201-275">Date Taken</span></span>    | <span data-ttu-id="00201-276">System. photo. Датетакен</span><span class="sxs-lookup"><span data-stu-id="00201-276">System.Photo.DateTaken</span></span>          | <span data-ttu-id="00201-277">1</span><span class="sxs-lookup"><span data-stu-id="00201-277">1</span></span>        |
| <span data-ttu-id="00201-278">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="00201-278">Rating</span></span>        | <span data-ttu-id="00201-279">System. Оценка</span><span class="sxs-lookup"><span data-stu-id="00201-279">System.Rating</span></span>                   | <span data-ttu-id="00201-280">1</span><span class="sxs-lookup"><span data-stu-id="00201-280">1</span></span>        |
| <span data-ttu-id="00201-281">Теги</span><span class="sxs-lookup"><span data-stu-id="00201-281">Tags</span></span>          | <span data-ttu-id="00201-282">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="00201-282">System.Keywords</span></span>                 | <span data-ttu-id="00201-283">1</span><span class="sxs-lookup"><span data-stu-id="00201-283">1</span></span>        |
| <span data-ttu-id="00201-284">Тип</span><span class="sxs-lookup"><span data-stu-id="00201-284">Type</span></span>          | <span data-ttu-id="00201-285">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="00201-285">System.PerceivedType</span></span>            | <span data-ttu-id="00201-286">1</span><span class="sxs-lookup"><span data-stu-id="00201-286">1</span></span>        |
| <span data-ttu-id="00201-287">Авторы</span><span class="sxs-lookup"><span data-stu-id="00201-287">Authors</span></span>       | <span data-ttu-id="00201-288">System.Author</span><span class="sxs-lookup"><span data-stu-id="00201-288">System.Author</span></span>                   | <span data-ttu-id="00201-289">2</span><span class="sxs-lookup"><span data-stu-id="00201-289">2</span></span>        |
| <span data-ttu-id="00201-290">Камера, изготовитель</span><span class="sxs-lookup"><span data-stu-id="00201-290">Camera maker</span></span>  | <span data-ttu-id="00201-291">System. photo. Камерамануфактурер</span><span class="sxs-lookup"><span data-stu-id="00201-291">System.Photo.CameraManufacturer</span></span> | <span data-ttu-id="00201-292">2</span><span class="sxs-lookup"><span data-stu-id="00201-292">2</span></span>        |
| <span data-ttu-id="00201-293">Модель камеры</span><span class="sxs-lookup"><span data-stu-id="00201-293">Camera model</span></span>  | <span data-ttu-id="00201-294">System. photo. Камерамодел</span><span class="sxs-lookup"><span data-stu-id="00201-294">System.Photo.CameraModel</span></span>        | <span data-ttu-id="00201-295">2</span><span class="sxs-lookup"><span data-stu-id="00201-295">2</span></span>        |
| <span data-ttu-id="00201-296">Комментарии</span><span class="sxs-lookup"><span data-stu-id="00201-296">Comments</span></span>      | <span data-ttu-id="00201-297">System. комментарий</span><span class="sxs-lookup"><span data-stu-id="00201-297">System.Comment</span></span>                  | <span data-ttu-id="00201-298">2</span><span class="sxs-lookup"><span data-stu-id="00201-298">2</span></span>        |
| <span data-ttu-id="00201-299">Измерения</span><span class="sxs-lookup"><span data-stu-id="00201-299">Dimensions</span></span>    | <span data-ttu-id="00201-300">System. Image. Dimensions</span><span class="sxs-lookup"><span data-stu-id="00201-300">System.Image.Dimensions</span></span>         | <span data-ttu-id="00201-301">2</span><span class="sxs-lookup"><span data-stu-id="00201-301">2</span></span>        |



 

## <a name="videos"></a><span data-ttu-id="00201-302">Видеоролики</span><span class="sxs-lookup"><span data-stu-id="00201-302">Videos</span></span>



| <span data-ttu-id="00201-303">Имя</span><span class="sxs-lookup"><span data-stu-id="00201-303">Name</span></span>         | <span data-ttu-id="00201-304">Свойство</span><span class="sxs-lookup"><span data-stu-id="00201-304">Property</span></span>                 | <span data-ttu-id="00201-305">Приоритет</span><span class="sxs-lookup"><span data-stu-id="00201-305">Priority</span></span> |
|--------------|--------------------------|----------|
| <span data-ttu-id="00201-306">Длина</span><span class="sxs-lookup"><span data-stu-id="00201-306">Length</span></span>       | <span data-ttu-id="00201-307">System. Media. Duration</span><span class="sxs-lookup"><span data-stu-id="00201-307">System.Media.Duration</span></span>    | <span data-ttu-id="00201-308">1</span><span class="sxs-lookup"><span data-stu-id="00201-308">1</span></span>        |
| <span data-ttu-id="00201-309">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="00201-309">Rating</span></span>       | <span data-ttu-id="00201-310">System. Оценка</span><span class="sxs-lookup"><span data-stu-id="00201-310">System.Rating</span></span>            | <span data-ttu-id="00201-311">1</span><span class="sxs-lookup"><span data-stu-id="00201-311">1</span></span>        |
| <span data-ttu-id="00201-312">Теги</span><span class="sxs-lookup"><span data-stu-id="00201-312">Tags</span></span>         | <span data-ttu-id="00201-313">System.Keywords</span><span class="sxs-lookup"><span data-stu-id="00201-313">System.Keywords</span></span>          | <span data-ttu-id="00201-314">1</span><span class="sxs-lookup"><span data-stu-id="00201-314">1</span></span>        |
| <span data-ttu-id="00201-315">Тип</span><span class="sxs-lookup"><span data-stu-id="00201-315">Type</span></span>         | <span data-ttu-id="00201-316">System.PerceivedType</span><span class="sxs-lookup"><span data-stu-id="00201-316">System.PerceivedType</span></span>     | <span data-ttu-id="00201-317">1</span><span class="sxs-lookup"><span data-stu-id="00201-317">1</span></span>        |
| <span data-ttu-id="00201-318">Высота рамки</span><span class="sxs-lookup"><span data-stu-id="00201-318">Frame height</span></span> | <span data-ttu-id="00201-319">System. Video. Фрамехеигхт</span><span class="sxs-lookup"><span data-stu-id="00201-319">System.Video.FrameHeight</span></span> | <span data-ttu-id="00201-320">2</span><span class="sxs-lookup"><span data-stu-id="00201-320">2</span></span>        |
| <span data-ttu-id="00201-321">Ширина рамки</span><span class="sxs-lookup"><span data-stu-id="00201-321">Frame width</span></span>  | <span data-ttu-id="00201-322">System. Video. Фрамевидс</span><span class="sxs-lookup"><span data-stu-id="00201-322">System.Video.FrameWidth</span></span>  | <span data-ttu-id="00201-323">2</span><span class="sxs-lookup"><span data-stu-id="00201-323">2</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="00201-324">См. также</span><span class="sxs-lookup"><span data-stu-id="00201-324">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="00201-325">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="00201-325">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="00201-326">Разработка обработчиков свойств для поиска Windows</span><span class="sxs-lookup"><span data-stu-id="00201-326">Developing Property Handlers for Windows Search</span></span>](-search-3x-wds-extidx-propertyhandlers.md)
</dt> <dt>

<span data-ttu-id="00201-327">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="00201-327">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="00201-328">Система свойств</span><span class="sxs-lookup"><span data-stu-id="00201-328">Property System</span></span>](../properties/building-property-handlers.md)
</dt> <dt>

<span data-ttu-id="00201-329">[Свойства системы](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="00201-329">[System Properties](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)</span></span>
</dt> </dl>

 

 
