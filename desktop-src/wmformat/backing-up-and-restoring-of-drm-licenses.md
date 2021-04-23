---
title: Резервное копирование и восстановление лицензий DRM
description: Резервное копирование и восстановление лицензий DRM
ms.assetid: ec2777e9-76af-43fe-8bd5-4d7532d2fb32
keywords:
- Пакет SDK для Windows Media Format, резервное копирование лицензий DRM
- Windows Media Format SDK, восстановление лицензий DRM
- Windows Media Format SDK, лицензии DRM
- Пакет SDK для Windows Media Format, лицензии для DRM
- Windows Media Format SDK, функция Backup Restore
- Пакет Windows Media Format SDK, служба управления лицензиями
- Windows Media Format SDK, обнаружение мошенничества
- Управление цифровыми правами (DRM), резервное копирование лицензий
- DRM (Управление цифровыми правами), резервное копирование лицензий
- Управление цифровыми правами (DRM), восстановление лицензий
- DRM (Управление цифровыми правами), восстановление лицензий
- Управление цифровыми правами (DRM), лицензии
- DRM (Управление цифровыми правами), лицензии
- Управление цифровыми правами (DRM), функция восстановления резервных копий
- DRM (Управление цифровыми правами), функция восстановления резервных копий
- Управление цифровыми правами (DRM), служба управления лицензиями
- DRM (Управление цифровыми правами), служба управления лицензиями
- Управление цифровыми правами (DRM), обнаружение мошенничества
- DRM (Управление цифровыми правами), обнаружение мошенничества
- Резервное копирование лицензий DRM
- восстановление лицензий DRM
- лицензии, DRM
- лицензии, резервное копирование DRM
- лицензии, восстановление DRM
- Функция восстановления резервной копии
- Служба управления лицензиями
- обнаружение мошенничества
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7718f03170077f7db624f8a99b8262239a79ca9
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104339497"
---
# <a name="backing-up-and-restoring-of-drm-licenses"></a><span data-ttu-id="6a130-130">Резервное копирование и восстановление лицензий DRM</span><span class="sxs-lookup"><span data-stu-id="6a130-130">Backing Up and Restoring of DRM Licenses</span></span>

<span data-ttu-id="6a130-131">С помощью функции восстановления резервной копии пользователи могут выполнять резервное копирование и восстановление [*лицензий*](wmformat-glossary.md) на одном и том же компьютере или на других компьютерах.</span><span class="sxs-lookup"><span data-stu-id="6a130-131">With the Backup Restore feature, users can back up and restore [*licenses*](wmformat-glossary.md) to the same computer or to other computers.</span></span> <span data-ttu-id="6a130-132">Эта функция позволяет пользователям передавать лицензии на новый компьютер или обратно на тот же компьютер (например, после переформатирования жесткого диска).</span><span class="sxs-lookup"><span data-stu-id="6a130-132">This feature enables users to transfer licenses to a new computer or back to the same computer (after reformatting the hard disk, for example).</span></span> <span data-ttu-id="6a130-133">Кроме того, пользователи могут воспроизводить защищенные файлы ASF на нескольких компьютерах.</span><span class="sxs-lookup"><span data-stu-id="6a130-133">In addition, users can play protected ASF files on more than one computer.</span></span>

<span data-ttu-id="6a130-134">Чтобы обеспечить законное использование лицензии, политика обнаружения мошенничества позволяет ограничивать количество попыток восстановления лицензии.</span><span class="sxs-lookup"><span data-stu-id="6a130-134">To encourage legitimate use of a license, a fraud detection policy restricts the number of times a license can be restored.</span></span> <span data-ttu-id="6a130-135">Корпорация Майкрософт предоставляет службу, которая отслеживает количество компьютеров, на которые была восстановлена лицензия. Если достигнут предел, пользователь не сможет восстановить лицензию.</span><span class="sxs-lookup"><span data-stu-id="6a130-135">Microsoft provides a service that tracks the number of computers to which a license has been restored; if a limit is reached, the user cannot restore the license.</span></span>

## <a name="allowing-or-disallowing-the-right-to-back-up-and-restore"></a><span data-ttu-id="6a130-136">Разрешение или запрет на право на резервное копирование и восстановление</span><span class="sxs-lookup"><span data-stu-id="6a130-136">Allowing or Disallowing the Right to Back Up and Restore</span></span>

<span data-ttu-id="6a130-137">Функция восстановления резервных копий работает только для лицензий, для которых задано право резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="6a130-137">The Backup Restore feature works only for licenses for which the Backup and Restore right is given.</span></span> <span data-ttu-id="6a130-138">Если владельцам содержимого или поставщикам лицензий не нужна эта функция или они выдают лицензии, которые содержат безопасное состояние (например, подсчет операций или ограниченное время), они могут запретить это право.</span><span class="sxs-lookup"><span data-stu-id="6a130-138">If content owners or license issuers do not want this feature, or if they issue licenses that contain a secure state (such as counted operations or limited time), they can disallow this right.</span></span>

<span data-ttu-id="6a130-139">Если не удается восстановить лицензию, поскольку у пользователя нет прав, [*идентификатор ключа*](wmformat-glossary.md) передается в приложение.</span><span class="sxs-lookup"><span data-stu-id="6a130-139">When a license cannot be restored because a user does not have the right, a [*key ID*](wmformat-glossary.md) is passed to the application.</span></span> <span data-ttu-id="6a130-140">Как минимум, пользователь должен получать уведомление о том, что не удалось создать резервную копию некоторых лицензий, хотя пользователь не знает, к каким лицензиям относится это сообщение.</span><span class="sxs-lookup"><span data-stu-id="6a130-140">At a minimum, the user should be notified that some licenses could not be backed up, although the user does not know which licenses this message refers to.</span></span> <span data-ttu-id="6a130-141">Если вы знакомы с ИДЕНТИФИКАТОРом ключа для доступных защищенных файлов, вы можете разработать более надежное решение, информирующее пользователя.</span><span class="sxs-lookup"><span data-stu-id="6a130-141">If you know the key ID for available protected files, you can develop a more robust solution for informing the user.</span></span>

<span data-ttu-id="6a130-142">Например, проигрыватель можно разрабатывать для Метки записи, которая предоставляет защищенные песни в Интернете.</span><span class="sxs-lookup"><span data-stu-id="6a130-142">For example, a player could be developed for a record label that provides protected songs on the Internet.</span></span> <span data-ttu-id="6a130-143">Эти песни и их идентификаторы ключей могут быть записаны в базе данных.</span><span class="sxs-lookup"><span data-stu-id="6a130-143">These songs and their key IDs could be tracked in a database.</span></span> <span data-ttu-id="6a130-144">Если не удалось создать резервную копию некоторых лицензий, приложение проигрывателя может использовать идентификатор ключа для запроса имени песни в базе данных, а затем информировать пользователя о том, для каких песен не удается создать резервную копию лицензий.</span><span class="sxs-lookup"><span data-stu-id="6a130-144">If some licenses could not be backed up, the player application could use the key ID to query the database for the name of the songs, then inform the user for which songs the licenses cannot be backed up.</span></span> <span data-ttu-id="6a130-145">Или можно создать музыкальную библиотеку для каждого пользователя локально, а идентификатор ключа можно использовать для получения дополнительных сведений о том, какие лицензии не удалось создать.</span><span class="sxs-lookup"><span data-stu-id="6a130-145">Or, a music library could be created for each user locally, and the key ID could be used to retrieve more information about which licenses could not be backed up.</span></span>

## <a name="the-license-management-service"></a><span data-ttu-id="6a130-146">Служба управления лицензиями</span><span class="sxs-lookup"><span data-stu-id="6a130-146">The License Management Service</span></span>

<span data-ttu-id="6a130-147">После реализации функции восстановления резервной копии служба управления лицензиями, размещенная корпорацией Майкрософт, управляет восстановлением лицензий.</span><span class="sxs-lookup"><span data-stu-id="6a130-147">When the Backup Restore feature is implemented, a License Management Service that is hosted by Microsoft manages the restoration of licenses.</span></span>

<span data-ttu-id="6a130-148">Сначала пользователи архивируются лицензии в приложении, например, выбрав пункт меню.</span><span class="sxs-lookup"><span data-stu-id="6a130-148">First, users back up licenses in the application, for example, by choosing a menu option.</span></span> <span data-ttu-id="6a130-149">Все лицензии на компьютере архивируются в указанное расположение, например на гибкий диск.</span><span class="sxs-lookup"><span data-stu-id="6a130-149">All licenses on the computer are backed up to a specified location, such as a floppy disk.</span></span> <span data-ttu-id="6a130-150">Затем пользователи восстанавливают лицензии с помощью приложения, например, выбрав пункт меню и указав расположение резервной копии.</span><span class="sxs-lookup"><span data-stu-id="6a130-150">Then, users restore licenses by using the application, for example, by choosing a menu option and specifying their backup location.</span></span>

<span data-ttu-id="6a130-151">На этом этапе пользователь должен быть подключен к Интернету. запрос из приложения отправляется в службу управления лицензиями.</span><span class="sxs-lookup"><span data-stu-id="6a130-151">At this point, the user must be connected to the Internet; a request from the application is sent to the License Management Service.</span></span> <span data-ttu-id="6a130-152">Если компьютер, с которого была создана резервная копия лицензии, отличается от исходного компьютера (или переформатированного исходного компьютера), служба управления лицензиями выдает новую лицензию на новый компьютер.</span><span class="sxs-lookup"><span data-stu-id="6a130-152">If the computer from which the license was backed up is different from the original computer (or the original computer has been reformatted), the License Management Service issues a new license to the new computer.</span></span> <span data-ttu-id="6a130-153">В противном случае лицензия, которая была выпущена ранее для этого компьютера, выдается повторно.</span><span class="sxs-lookup"><span data-stu-id="6a130-153">Otherwise, the license that was previously issued to that computer is reissued.</span></span>

<span data-ttu-id="6a130-154">Поскольку служба управления лицензиями получает сведения от пользователя, необходимо отобразить политику конфиденциальности Майкрософт или указать ссылку на эту страницу на [веб-сайте Майкрософт](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="6a130-154">Because the License Management Service retrieves information from the user, you must display the Microsoft privacy policy or provide a link to that page at the [Microsoft Web site](https://www.microsoft.com/licensing/default).</span></span>

> [!Note]  
> <span data-ttu-id="6a130-155">Когда пользователь восстанавливает лицензию на другой компьютер, а для этой лицензии требуется индивидуальная авторизация, конечный пользователь должен авторизовать компоненты DRM для обновления.</span><span class="sxs-lookup"><span data-stu-id="6a130-155">When an end user restores a license to a different computer and the license requires individualization, the end user must authorize the DRM components to be updated.</span></span> <span data-ttu-id="6a130-156">Для поддержки этой функции необходимо реализовать процесс в приложении проигрывателя.</span><span class="sxs-lookup"><span data-stu-id="6a130-156">You must implement a process in your player application to support this feature.</span></span>

 

## <a name="detecting-fraud"></a><span data-ttu-id="6a130-157">Обнаружение мошенничества</span><span class="sxs-lookup"><span data-stu-id="6a130-157">Detecting Fraud</span></span>

<span data-ttu-id="6a130-158">Пользователю разрешено восстанавливать лицензии ограниченное число раз.</span><span class="sxs-lookup"><span data-stu-id="6a130-158">The user is allowed to restore a license a limited number of times.</span></span> <span data-ttu-id="6a130-159">Каждый раз при восстановлении лицензии служба управления лицензиями отслеживает ее и увеличивает количество лицензий на одну.</span><span class="sxs-lookup"><span data-stu-id="6a130-159">Each time a license is restored, the License Management Service tracks it and increments the count for that license by one.</span></span> <span data-ttu-id="6a130-160">При восстановлении лицензии на компьютер, на который ранее была восстановлена лицензия (например, компьютер, с которого была создана резервная копия лицензии), счетчик не увеличивается.</span><span class="sxs-lookup"><span data-stu-id="6a130-160">When restoring a license to a computer to which the license has been restored previously (for example, the computer from which the license was backed up), the count is not increased.</span></span> <span data-ttu-id="6a130-161">Компьютер считается другим, если он имеет новую операционную систему или операционная система была установлена повторно.</span><span class="sxs-lookup"><span data-stu-id="6a130-161">A computer is considered to be different if it has a new operating system, or the operating system has been re-installed.</span></span>

<span data-ttu-id="6a130-162">В соответствии с политикой обнаружения мошенничества Майкрософт, когда лицензия была восстановлена определенное число раз, приложение получает URL-адрес от компонентов DRM и отвечает за открытие браузера и отображение веб-страницы, что означает, что лицензионное соглашение могло быть нарушено.</span><span class="sxs-lookup"><span data-stu-id="6a130-162">In accordance with Microsoft's fraud detection policy, when a license has been restored a certain number of times, the application receives a URL from the DRM components and is responsible for opening a browser and displaying the Web page, which indicates that the license agreement might have been violated.</span></span> <span data-ttu-id="6a130-163">Пользователь должен связаться с распространителем лицензий, который затем должен определить, является ли запрос допустимым.</span><span class="sxs-lookup"><span data-stu-id="6a130-163">The user must contact the license distributor, who must then determine whether the request is valid.</span></span>

> [!Note]  
> <span data-ttu-id="6a130-164">DRM не поддерживает версию этого пакета SDK на базе x64.</span><span class="sxs-lookup"><span data-stu-id="6a130-164">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6a130-165">См. также</span><span class="sxs-lookup"><span data-stu-id="6a130-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a130-166">**Функции цифровых Rights Management**</span><span class="sxs-lookup"><span data-stu-id="6a130-166">**Digital Rights Management Features**</span></span>](digital-rights-management-features.md)
</dt> <dt>

[<span data-ttu-id="6a130-167">**Резервное копирование и восстановление лицензий**</span><span class="sxs-lookup"><span data-stu-id="6a130-167">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> </dl>

 

 




