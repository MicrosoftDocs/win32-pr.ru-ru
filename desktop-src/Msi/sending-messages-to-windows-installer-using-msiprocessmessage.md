---
description: Сообщения, отправленные с помощью Мсипроцессмессаже, — это те же сообщения, которые были получены \_ функцией обратного вызова обработчика инсталлуи, если был вызван мсисетекстерналуи.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Отправка сообщений в установщик Windows с помощью Мсипроцессмессаже
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999585"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a><span data-ttu-id="e013e-103">Отправка сообщений в установщик Windows с помощью Мсипроцессмессаже</span><span class="sxs-lookup"><span data-stu-id="e013e-103">Sending Messages to Windows Installer Using MsiProcessMessage</span></span>

<span data-ttu-id="e013e-104">Сообщения, отправленные с помощью [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) , — это те же сообщения, которые были получены функцией обратного вызова [**\_ обработчика инсталлуи**](/windows/desktop/api/Msi/nc-msi-installui_handlera) , если был вызван [**мсисетекстерналуи**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="e013e-104">The messages sent using [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are the same messages that are received by the [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera) callback function if [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) was called.</span></span> <span data-ttu-id="e013e-105">В противном случае установщик Windows обрабатывает сообщения.</span><span class="sxs-lookup"><span data-stu-id="e013e-105">Otherwise, Windows Installer handles the messages.</span></span> <span data-ttu-id="e013e-106">Дополнительные сведения см. в разделе [анализ установщик Windows сообщений](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="e013e-106">For details, see [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="e013e-107">Например, чтобы отправить \_ сообщение об ошибке инсталлмессаже с \_ значком МБ иконварнинг и \_ кнопками МБ абортретриканцел:</span><span class="sxs-lookup"><span data-stu-id="e013e-107">For example, to send an INSTALLMESSAGE\_ERROR message with the MB\_ICONWARNING icon and the MB\_ABORTRETRYCANCEL buttons:</span></span>


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



<span data-ttu-id="e013e-108">Где *хинсталл* — это обработчик установки, предоставленный настраиваемому действию или обработчику *хпродукт* из [**Мсиопенпродукт**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) или [**мсиопенпаккаже**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), а *хрек* — это запись, содержащая сведения об ошибке для форматирования.</span><span class="sxs-lookup"><span data-stu-id="e013e-108">Where *hInstall* is the handle to the installation, provided to a custom action or the *hProduct* handle from [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) or [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), and *hRec* is the record containing the error information to format.</span></span> <span data-ttu-id="e013e-109">Сведения о том, как выполняется форматирование, см. в разделе [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span><span class="sxs-lookup"><span data-stu-id="e013e-109">For information on how formatting is performed, see [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span></span>

<span data-ttu-id="e013e-110">По умолчанию при \_ отправке сообщения об ошибке инсталлмессаже или инсталлмессаже \_ фаталексит без указания типов кнопок или значков, МБ \_ ОК, значок и МБ \_ DEFBUTTON1 используются.</span><span class="sxs-lookup"><span data-stu-id="e013e-110">By default, if an INSTALLMESSAGE\_ERROR or INSTALLMESSAGE\_FATALEXIT message is sent without specifying button type or icon types, MB\_OK, no icon, and MB\_DEFBUTTON1 are used.</span></span>

<span data-ttu-id="e013e-111">Установщик Windows не помечает кнопку **Abort** строкой "Abort" при отображении MessageBox с \_ указанием кнопки "абортретригноре МБ", вместо этого он отмечает кнопку строкой "Cancel".</span><span class="sxs-lookup"><span data-stu-id="e013e-111">Windows Installer does not label the **ABORT** button with the "Abort" string when displaying a MessageBox with the MB\_ABORTRETRYIGNORE button specification, instead it labels the button with the "Cancel" string.</span></span> <span data-ttu-id="e013e-112">Все сообщения об ошибках отменяют использование слова «Abort», а вместо этого используют слово «Cancel».</span><span class="sxs-lookup"><span data-stu-id="e013e-112">All error messages refrain from using the word "Abort" and instead use the word "Cancel".</span></span>

<span data-ttu-id="e013e-113">Параметр *хрекорд* функции [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) зависит от типа сообщений, отправляемого в [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="e013e-113">The *hRecord* parameter of the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function depends upon the message type sent to the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="e013e-114">В следующем списке приведены требования к записи относительно типа сообщений.</span><span class="sxs-lookup"><span data-stu-id="e013e-114">The following list details the requirements of the record in relation to the message type:</span></span>

<span data-ttu-id="e013e-115">ИНСТАЛЛМЕССАЖЕ \_ фаталексит</span><span class="sxs-lookup"><span data-stu-id="e013e-115">INSTALLMESSAGE\_FATALEXIT</span></span>

 

<span data-ttu-id="e013e-116">\_сведения о инсталлмессаже</span><span class="sxs-lookup"><span data-stu-id="e013e-116">INSTALLMESSAGE\_INFO</span></span>

 

<span data-ttu-id="e013e-117">ИНСТАЛЛМЕССАЖЕ \_ аутофдискспаце</span><span class="sxs-lookup"><span data-stu-id="e013e-117">INSTALLMESSAGE\_OUTOFDISKSPACE</span></span>



| <span data-ttu-id="e013e-118">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-118">Field</span></span>         | <span data-ttu-id="e013e-119">Описание</span><span class="sxs-lookup"><span data-stu-id="e013e-119">Description</span></span>                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e013e-120">0</span><span class="sxs-lookup"><span data-stu-id="e013e-120">0</span></span>             | <span data-ttu-id="e013e-121">Шаблон для форматирования результирующей строки.</span><span class="sxs-lookup"><span data-stu-id="e013e-121">Template for the formatting of the resultant string.</span></span> <span data-ttu-id="e013e-122">Дополнительные сведения см. в разделе [**мсиформатрекорд**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) .</span><span class="sxs-lookup"><span data-stu-id="e013e-122">See [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) for more information.</span></span> <span data-ttu-id="e013e-123">Поля записи указываются по \[ 1 \] для поля 1, \[ 2 — \] для поля 2 и т. д.</span><span class="sxs-lookup"><span data-stu-id="e013e-123">The fields of the record are referenced using \[1\] for field 1, \[2\] for field 2, etc.</span></span> |
| <span data-ttu-id="e013e-124">от 1 до *n*</span><span class="sxs-lookup"><span data-stu-id="e013e-124">1 through *n*</span></span> | <span data-ttu-id="e013e-125">Все последующие поля напрямую связаны с полями, на которые ссылается шаблон в поле 0.</span><span class="sxs-lookup"><span data-stu-id="e013e-125">All subsequent fields are directly related to the fields referenced by the template in field 0.</span></span>                                                                                                                    |



 

<span data-ttu-id="e013e-126">Если поле 0 имеет значение null, то строка, полученная обработчиком пользовательского интерфейса, форматируется следующим образом: 1: \[ данные из поля 1 \] 2. \[ данные из поля 2 \] означают, что для каждого поля записи строка содержит номер поля, за которым следуют данные, хранящиеся в поле.</span><span class="sxs-lookup"><span data-stu-id="e013e-126">If field 0 is null, the string received by the UI handler is formatted as: 1: \[data from field 1\] 2: \[data from field 2\] meaning that for each field of the record, the string contains the field number followed by the data stored in the field.</span></span>

<span data-ttu-id="e013e-127">Информационные сообщения от [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) регистрируются, когда [**мсиенаблелог**](/windows/desktop/api/Msi/nf-msi-msienableloga), [параметр командной строки](command-line-options.md)"/l" или [Политика ведения журнала](logging.md) указывают "I" или инсталллогмоде \_ info.</span><span class="sxs-lookup"><span data-stu-id="e013e-127">Information messages from [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are logged when [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), the '/l' [command line option](command-line-options.md), or the [logging policy](logging.md) specify 'I' or INSTALLLOGMODE\_INFO.</span></span>

<span data-ttu-id="e013e-128">ИНСТАЛЛМЕССАЖЕ, \_ Ошибка</span><span class="sxs-lookup"><span data-stu-id="e013e-128">INSTALLMESSAGE\_ERROR</span></span>

 

<span data-ttu-id="e013e-129">\_предупреждение инсталлмессаже</span><span class="sxs-lookup"><span data-stu-id="e013e-129">INSTALLMESSAGE\_WARNING</span></span>

 

<span data-ttu-id="e013e-130">\_пользователь инсталлмессаже</span><span class="sxs-lookup"><span data-stu-id="e013e-130">INSTALLMESSAGE\_USER</span></span>

<span data-ttu-id="e013e-131">Для использования сообщения из таблицы ошибок.</span><span class="sxs-lookup"><span data-stu-id="e013e-131">To use a message from the Error table.</span></span>



| <span data-ttu-id="e013e-132">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-132">Field</span></span>         | <span data-ttu-id="e013e-133">Описание</span><span class="sxs-lookup"><span data-stu-id="e013e-133">Description</span></span>                                           |
|---------------|-------------------------------------------------------|
| <span data-ttu-id="e013e-134">0</span><span class="sxs-lookup"><span data-stu-id="e013e-134">0</span></span>             | <span data-ttu-id="e013e-135">Должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="e013e-135">Must be null.</span></span>                                         |
| <span data-ttu-id="e013e-136">1</span><span class="sxs-lookup"><span data-stu-id="e013e-136">1</span></span>             | <span data-ttu-id="e013e-137">Номер сообщения в [таблице ошибок](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="e013e-137">Message number in the [Error table](error-table.md).</span></span> |
| <span data-ttu-id="e013e-138">от 2 до *n*</span><span class="sxs-lookup"><span data-stu-id="e013e-138">2 through *n*</span></span> | <span data-ttu-id="e013e-139">Связан с указанным сообщением в таблице ошибок.</span><span class="sxs-lookup"><span data-stu-id="e013e-139">Related to the specified message in the Error table.</span></span>  |



 

<span data-ttu-id="e013e-140">Например, если выбран диапазон 10.0.0.0/20 для виртуальной сети, для пространства клиентских адресов можно выбрать 10.1.0.0/24.</span><span class="sxs-lookup"><span data-stu-id="e013e-140">For example.</span></span>



| <span data-ttu-id="e013e-141">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-141">Field</span></span> | <span data-ttu-id="e013e-142">Тип</span><span class="sxs-lookup"><span data-stu-id="e013e-142">Type</span></span>   | <span data-ttu-id="e013e-143">Данные</span><span class="sxs-lookup"><span data-stu-id="e013e-143">Data</span></span>       |
|-------|--------|------------|
| <span data-ttu-id="e013e-144">0</span><span class="sxs-lookup"><span data-stu-id="e013e-144">0</span></span>     | <span data-ttu-id="e013e-145">строка</span><span class="sxs-lookup"><span data-stu-id="e013e-145">string</span></span> | <span data-ttu-id="e013e-146">null</span><span class="sxs-lookup"><span data-stu-id="e013e-146">null</span></span>       |
| <span data-ttu-id="e013e-147">1</span><span class="sxs-lookup"><span data-stu-id="e013e-147">1</span></span>     | <span data-ttu-id="e013e-148">INT</span><span class="sxs-lookup"><span data-stu-id="e013e-148">int</span></span>    | <span data-ttu-id="e013e-149">1304</span><span class="sxs-lookup"><span data-stu-id="e013e-149">1304</span></span>       |
| <span data-ttu-id="e013e-150">2</span><span class="sxs-lookup"><span data-stu-id="e013e-150">2</span></span>     | <span data-ttu-id="e013e-151">строка</span><span class="sxs-lookup"><span data-stu-id="e013e-151">string</span></span> | <span data-ttu-id="e013e-152">Myfile.txt</span><span class="sxs-lookup"><span data-stu-id="e013e-152">Myfile.txt</span></span> |



 

<span data-ttu-id="e013e-153">Полученное из обработчика пользовательского интерфейса сообщение получает следующее:</span><span class="sxs-lookup"><span data-stu-id="e013e-153">The resulting message received from the UI handler is:</span></span>

<span data-ttu-id="e013e-154">Ошибка 1304.</span><span class="sxs-lookup"><span data-stu-id="e013e-154">Error 1304.</span></span> <span data-ttu-id="e013e-155">Ошибка записи в файл: Myfile.txt.</span><span class="sxs-lookup"><span data-stu-id="e013e-155">Error writing to file: Myfile.txt.</span></span> <span data-ttu-id="e013e-156">Убедитесь, что у вас есть доступ к этому каталогу.</span><span class="sxs-lookup"><span data-stu-id="e013e-156">Verify that you have access to that directory.</span></span>

<span data-ttu-id="e013e-157">Если поле 0 не равно null, сообщение из таблицы ошибок переопределяется.</span><span class="sxs-lookup"><span data-stu-id="e013e-157">If field 0 is not null, the message from the error table is overridden.</span></span> <span data-ttu-id="e013e-158">Вместо этого шаблон поля 0 определяет формат сообщения.</span><span class="sxs-lookup"><span data-stu-id="e013e-158">Instead, the field 0 template determines the format of the message.</span></span>

<span data-ttu-id="e013e-159">В сообщении также могут быть указаны кнопки, включая кнопку по умолчанию, и значок для использования с сообщением, как упоминалось выше.</span><span class="sxs-lookup"><span data-stu-id="e013e-159">The message may also specify the buttons, including the default button, and the icon for use with the message as mentioned above.</span></span> <span data-ttu-id="e013e-160">Кнопки и типы значков перечислены в [**\_ обработчике инсталлуи**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span><span class="sxs-lookup"><span data-stu-id="e013e-160">The button and icon types are listed in [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span></span>

<span data-ttu-id="e013e-161">ИНСТАЛЛМЕССАЖЕ \_ коммондата</span><span class="sxs-lookup"><span data-stu-id="e013e-161">INSTALLMESSAGE\_COMMONDATA</span></span>

<span data-ttu-id="e013e-162">Это сообщение отправляется для включения или отключения кнопки **Отмена** в диалоговом окне хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="e013e-162">This message is sent to enable or disable the **Cancel** button in a progress dialog box.</span></span>



| <span data-ttu-id="e013e-163">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-163">Field</span></span> | <span data-ttu-id="e013e-164">Описание</span><span class="sxs-lookup"><span data-stu-id="e013e-164">Description</span></span>                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e013e-165">0</span><span class="sxs-lookup"><span data-stu-id="e013e-165">0</span></span>     | <span data-ttu-id="e013e-166">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e013e-166">Unused.</span></span>                                                                                                                                      |
| <span data-ttu-id="e013e-167">1</span><span class="sxs-lookup"><span data-stu-id="e013e-167">1</span></span>     | <span data-ttu-id="e013e-168">2 — это кнопка **отмены** .</span><span class="sxs-lookup"><span data-stu-id="e013e-168">2 refers to the **Cancel** button.</span></span>                                                                                                           |
| <span data-ttu-id="e013e-169">2</span><span class="sxs-lookup"><span data-stu-id="e013e-169">2</span></span>     | <span data-ttu-id="e013e-170">Значение 1 указывает, что кнопка **Отмена** должна быть видимой.</span><span class="sxs-lookup"><span data-stu-id="e013e-170">A value of 1 indicates the **Cancel** button should be visible.</span></span> <span data-ttu-id="e013e-171">Значение 0 указывает, что кнопка **Отмена** должна быть невидимой.</span><span class="sxs-lookup"><span data-stu-id="e013e-171">A value of 0 indicates the **Cancel** button should be invisible.</span></span><br/> |



 

<span data-ttu-id="e013e-172">Например, чтобы отключить или скрыть кнопку **Отмена** , запись будет выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e013e-172">For example, to disable or hide the **Cancel** button, the record would appear as follows.</span></span>



| <span data-ttu-id="e013e-173">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-173">Field</span></span> | <span data-ttu-id="e013e-174">Тип</span><span class="sxs-lookup"><span data-stu-id="e013e-174">Type</span></span>   | <span data-ttu-id="e013e-175">Данные</span><span class="sxs-lookup"><span data-stu-id="e013e-175">Data</span></span> |
|-------|--------|------|
| <span data-ttu-id="e013e-176">0</span><span class="sxs-lookup"><span data-stu-id="e013e-176">0</span></span>     | <span data-ttu-id="e013e-177">строка</span><span class="sxs-lookup"><span data-stu-id="e013e-177">string</span></span> | <span data-ttu-id="e013e-178">null</span><span class="sxs-lookup"><span data-stu-id="e013e-178">null</span></span> |
| <span data-ttu-id="e013e-179">1</span><span class="sxs-lookup"><span data-stu-id="e013e-179">1</span></span>     | <span data-ttu-id="e013e-180">INT</span><span class="sxs-lookup"><span data-stu-id="e013e-180">int</span></span>    | <span data-ttu-id="e013e-181">2</span><span class="sxs-lookup"><span data-stu-id="e013e-181">2</span></span>    |
| <span data-ttu-id="e013e-182">2</span><span class="sxs-lookup"><span data-stu-id="e013e-182">2</span></span>     | <span data-ttu-id="e013e-183">INT</span><span class="sxs-lookup"><span data-stu-id="e013e-183">int</span></span>    | <span data-ttu-id="e013e-184">0</span><span class="sxs-lookup"><span data-stu-id="e013e-184">0</span></span>    |



 

<span data-ttu-id="e013e-185">ИНСТАЛЛМЕССАЖЕ \_ актионстарт</span><span class="sxs-lookup"><span data-stu-id="e013e-185">INSTALLMESSAGE\_ACTIONSTART</span></span>

 

<span data-ttu-id="e013e-186">ИНСТАЛЛМЕССАЖЕ \_ актиондата</span><span class="sxs-lookup"><span data-stu-id="e013e-186">INSTALLMESSAGE\_ACTIONDATA</span></span>

<span data-ttu-id="e013e-187">Запись ИНСТАЛЛМЕССАЖЕ \_ актионстарт определяет формат записи актиондата.</span><span class="sxs-lookup"><span data-stu-id="e013e-187">The INSTALLMESSAGE\_ACTIONSTART record determines the format of the ActionData record.</span></span>



| <span data-ttu-id="e013e-188">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-188">Field</span></span> | <span data-ttu-id="e013e-189">Описание</span><span class="sxs-lookup"><span data-stu-id="e013e-189">Description</span></span>                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e013e-190">0</span><span class="sxs-lookup"><span data-stu-id="e013e-190">0</span></span>     | <span data-ttu-id="e013e-191">null</span><span class="sxs-lookup"><span data-stu-id="e013e-191">null</span></span>                                                                                                          |
| <span data-ttu-id="e013e-192">1</span><span class="sxs-lookup"><span data-stu-id="e013e-192">1</span></span>     | <span data-ttu-id="e013e-193">Имя действия.</span><span class="sxs-lookup"><span data-stu-id="e013e-193">Action name.</span></span> <span data-ttu-id="e013e-194">Имя в этом поле не должно быть пустым.</span><span class="sxs-lookup"><span data-stu-id="e013e-194">The name in this field must be non-null.</span></span>                                                         |
| <span data-ttu-id="e013e-195">2</span><span class="sxs-lookup"><span data-stu-id="e013e-195">2</span></span>     | <span data-ttu-id="e013e-196">Описание действия.</span><span class="sxs-lookup"><span data-stu-id="e013e-196">Action description.</span></span>                                                                                           |
| <span data-ttu-id="e013e-197">3</span><span class="sxs-lookup"><span data-stu-id="e013e-197">3</span></span>     | <span data-ttu-id="e013e-198">Шаблон действия.</span><span class="sxs-lookup"><span data-stu-id="e013e-198">Action template.</span></span> <span data-ttu-id="e013e-199">Используется для Актиондата, сообщение которого форматируется в соответствии с этим шаблоном.</span><span class="sxs-lookup"><span data-stu-id="e013e-199">This is used for the ActionData whose message is being formatted according to this template.</span></span> |



 

<span data-ttu-id="e013e-200">Не сослаться на поле 0 в сообщении шаблона действия.</span><span class="sxs-lookup"><span data-stu-id="e013e-200">Do not reference field 0 in the Action template message.</span></span>

<span data-ttu-id="e013e-201">\_Запись АКТИОНДАТА инсталлмессаже имеет следующий формат.</span><span class="sxs-lookup"><span data-stu-id="e013e-201">The INSTALLMESSAGE\_ACTIONDATA record is formatted as follows.</span></span>



| <span data-ttu-id="e013e-202">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-202">Field</span></span>         | <span data-ttu-id="e013e-203">Описание</span><span class="sxs-lookup"><span data-stu-id="e013e-203">Description</span></span>                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e013e-204">0</span><span class="sxs-lookup"><span data-stu-id="e013e-204">0</span></span>             | <span data-ttu-id="e013e-205">null</span><span class="sxs-lookup"><span data-stu-id="e013e-205">null</span></span>                                                                                                                                               |
| <span data-ttu-id="e013e-206">от 1 до *n*</span><span class="sxs-lookup"><span data-stu-id="e013e-206">1 through *n*</span></span> | <span data-ttu-id="e013e-207">Зависит от поля 3 соответствующего \_ сообщения инсталлмессаже актионстарт или шаблона, указанного в [таблице актионтекст](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="e013e-207">Dependent upon field 3 of the corresponding INSTALLMESSAGE\_ACTIONSTART message or template specified in [ActionText table](actiontext-table.md).</span></span> |



 

<span data-ttu-id="e013e-208">Например, \_ запись инсталлмессаже актионстарт.</span><span class="sxs-lookup"><span data-stu-id="e013e-208">For example, the INSTALLMESSAGE\_ACTIONSTART record.</span></span>



| <span data-ttu-id="e013e-209">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-209">Field</span></span> | <span data-ttu-id="e013e-210">Тип</span><span class="sxs-lookup"><span data-stu-id="e013e-210">Type</span></span>   | <span data-ttu-id="e013e-211">Данные</span><span class="sxs-lookup"><span data-stu-id="e013e-211">Data</span></span>                                                            |
|-------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="e013e-212">0</span><span class="sxs-lookup"><span data-stu-id="e013e-212">0</span></span>     | <span data-ttu-id="e013e-213">строка</span><span class="sxs-lookup"><span data-stu-id="e013e-213">string</span></span> | <span data-ttu-id="e013e-214">null</span><span class="sxs-lookup"><span data-stu-id="e013e-214">null</span></span>                                                            |
| <span data-ttu-id="e013e-215">1</span><span class="sxs-lookup"><span data-stu-id="e013e-215">1</span></span>     | <span data-ttu-id="e013e-216">строка</span><span class="sxs-lookup"><span data-stu-id="e013e-216">string</span></span> | <span data-ttu-id="e013e-217">мяктион</span><span class="sxs-lookup"><span data-stu-id="e013e-217">MyAction</span></span>                                                        |
| <span data-ttu-id="e013e-218">2</span><span class="sxs-lookup"><span data-stu-id="e013e-218">2</span></span>     | <span data-ttu-id="e013e-219">строка</span><span class="sxs-lookup"><span data-stu-id="e013e-219">string</span></span> | <span data-ttu-id="e013e-220">Это описание «Мяктион»</span><span class="sxs-lookup"><span data-stu-id="e013e-220">This is the description of "MyAction"</span></span>                           |
| <span data-ttu-id="e013e-221">3</span><span class="sxs-lookup"><span data-stu-id="e013e-221">3</span></span>     | <span data-ttu-id="e013e-222">строка</span><span class="sxs-lookup"><span data-stu-id="e013e-222">string</span></span> | <span data-ttu-id="e013e-223">Шаблон Мяктион: field1 Data — \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e013e-223">MyAction template: field1 data is \[1\].</span></span> <span data-ttu-id="e013e-224">данные поля 2 — \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="e013e-224">field 2 data is \[2\].</span></span> |



 

<span data-ttu-id="e013e-225">Шаблон для ИНСТАЛЛМЕССАЖЕ \_ актионстарт (поле 3) ссылается на поля 1 и 2, запись инсталлмессаже \_ актиондата должна содержать 2 поля, содержащие гарантированные данные.</span><span class="sxs-lookup"><span data-stu-id="e013e-225">The template for INSTALLMESSAGE\_ACTIONSTART (field 3) references fields 1 and 2, the INSTALLMESSAGE\_ACTIONDATA record should have 2 fields containing the warranted data.</span></span> <span data-ttu-id="e013e-226">Поля могут быть либо строками, либо целочисленными полями.</span><span class="sxs-lookup"><span data-stu-id="e013e-226">The fields could be either string or integer fields.</span></span>

<span data-ttu-id="e013e-227">\_Запись АКТИОНДАТА инсталлмессаже.</span><span class="sxs-lookup"><span data-stu-id="e013e-227">INSTALLMESSAGE\_ACTIONDATA record.</span></span>



| <span data-ttu-id="e013e-228">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-228">Field</span></span> | <span data-ttu-id="e013e-229">Тип</span><span class="sxs-lookup"><span data-stu-id="e013e-229">Type</span></span>   | <span data-ttu-id="e013e-230">Данные</span><span class="sxs-lookup"><span data-stu-id="e013e-230">Data</span></span>                    |
|-------|--------|-------------------------|
| <span data-ttu-id="e013e-231">0</span><span class="sxs-lookup"><span data-stu-id="e013e-231">0</span></span>     | <span data-ttu-id="e013e-232">строка</span><span class="sxs-lookup"><span data-stu-id="e013e-232">string</span></span> | <span data-ttu-id="e013e-233">null</span><span class="sxs-lookup"><span data-stu-id="e013e-233">null</span></span>                    |
| <span data-ttu-id="e013e-234">1</span><span class="sxs-lookup"><span data-stu-id="e013e-234">1</span></span>     | <span data-ttu-id="e013e-235">INT</span><span class="sxs-lookup"><span data-stu-id="e013e-235">int</span></span>    | <span data-ttu-id="e013e-236">2</span><span class="sxs-lookup"><span data-stu-id="e013e-236">2</span></span>                       |
| <span data-ttu-id="e013e-237">2</span><span class="sxs-lookup"><span data-stu-id="e013e-237">2</span></span>     | <span data-ttu-id="e013e-238">строка</span><span class="sxs-lookup"><span data-stu-id="e013e-238">string</span></span> | <span data-ttu-id="e013e-239">Актиондата для Мяктион</span><span class="sxs-lookup"><span data-stu-id="e013e-239">ActionData for MyAction</span></span> |



 

<span data-ttu-id="e013e-240">ИНСТАЛЛМЕССАЖЕ \_ филесинусе</span><span class="sxs-lookup"><span data-stu-id="e013e-240">INSTALLMESSAGE\_FILESINUSE</span></span>

<span data-ttu-id="e013e-241">Запись ФИЛЕСИНУСЕ является записью переменной длины.</span><span class="sxs-lookup"><span data-stu-id="e013e-241">The FILESINUSE record is a variable length record.</span></span>



| <span data-ttu-id="e013e-242">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-242">Field</span></span> | <span data-ttu-id="e013e-243">Описание</span><span class="sxs-lookup"><span data-stu-id="e013e-243">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e013e-244">0</span><span class="sxs-lookup"><span data-stu-id="e013e-244">0</span></span>     | <span data-ttu-id="e013e-245">Это поле может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="e013e-245">This field can be null.</span></span> <span data-ttu-id="e013e-246">Для установки с использованием базового пользовательского интерфейса в этом поле может быть указан статический текст для вывода в [элементе управления ListBox](listbox-control.md) [диалогового окна филесинусе](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="e013e-246">For an installation using a basic UI, this field may specify static text for display in the [ListBox control](listbox-control.md) of the [FilesInUse dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="e013e-247">Для установки с использованием полного пользовательского интерфейса это поле не действует, так как текст задается при создании пользовательского диалогового окна Филесинусе.</span><span class="sxs-lookup"><span data-stu-id="e013e-247">For an installation using a full UI, this field has no effect because the text is specified by the authoring of the custom FilesInUse dialog box.</span></span> |
| <span data-ttu-id="e013e-248">1</span><span class="sxs-lookup"><span data-stu-id="e013e-248">1</span></span>     | <span data-ttu-id="e013e-249">Имя используемого файла.</span><span class="sxs-lookup"><span data-stu-id="e013e-249">Name of the file in use.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="e013e-250">2</span><span class="sxs-lookup"><span data-stu-id="e013e-250">2</span></span>     | <span data-ttu-id="e013e-251">Это поле определяет процесс, в котором используется файл. **Установщик Windows версии 4,0:** Идентификатор процесса (PID) процесса или заголовок окна для процесса.</span><span class="sxs-lookup"><span data-stu-id="e013e-251">This field identifies the process holding the file in use.**Windows Installer version 4.0:** The process id (PID) of the process, or the title of the window for the process.</span></span><br/> <span data-ttu-id="e013e-252">**Установщик Windows версии 3,1 и более ранних версий:** Это поле должно быть идентификатором процесса (PID) процесса.</span><span class="sxs-lookup"><span data-stu-id="e013e-252">**Windows Installer version 3.1 and earlier:** This field must be the process id (PID) of the process.</span></span><br/>                                                      |



 

<span data-ttu-id="e013e-253">Например, чтобы отправить сообщение Филесинусе, в котором используются два файла, red.exe и blue.exe, запись содержит четыре поля плюс поле 0.</span><span class="sxs-lookup"><span data-stu-id="e013e-253">For example, to send a FilesInUse message showing two files in use, red.exe and blue.exe, the record has four fields plus the 0 field.</span></span> <span data-ttu-id="e013e-254">Формат записи будет выглядеть так, как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="e013e-254">The format of the record would be as shown in the following table.</span></span> <span data-ttu-id="e013e-255">Для этого примера требуется установщик Windows версии 4,0.</span><span class="sxs-lookup"><span data-stu-id="e013e-255">This example requires Windows Installer version 4.0.</span></span>

<span data-ttu-id="e013e-256">**Установщик Windows версии 3,1 и более ранних версий:** Поля 2 и 4 в следующем примере должны содержать идентификаторы PID процессов, содержащих red.exe и blue.exe.</span><span class="sxs-lookup"><span data-stu-id="e013e-256">**Windows Installer version 3.1 and earlier:** Fields 2 and 4 in the following example must contain the PIDs of the processes holding red.exe and blue.exe in use.</span></span>



| <span data-ttu-id="e013e-257">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-257">Field</span></span> | <span data-ttu-id="e013e-258">Описание</span><span class="sxs-lookup"><span data-stu-id="e013e-258">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="e013e-259">0</span><span class="sxs-lookup"><span data-stu-id="e013e-259">0</span></span>     | <span data-ttu-id="e013e-260">null</span><span class="sxs-lookup"><span data-stu-id="e013e-260">null</span></span>              |
| <span data-ttu-id="e013e-261">1</span><span class="sxs-lookup"><span data-stu-id="e013e-261">1</span></span>     | <span data-ttu-id="e013e-262">Red.exe</span><span class="sxs-lookup"><span data-stu-id="e013e-262">Red.exe</span></span>           |
| <span data-ttu-id="e013e-263">2</span><span class="sxs-lookup"><span data-stu-id="e013e-263">2</span></span>     | <span data-ttu-id="e013e-264">Заголовок Красного окна</span><span class="sxs-lookup"><span data-stu-id="e013e-264">Red Window Title</span></span>  |
| <span data-ttu-id="e013e-265">3</span><span class="sxs-lookup"><span data-stu-id="e013e-265">3</span></span>     | <span data-ttu-id="e013e-266">Blue.exe</span><span class="sxs-lookup"><span data-stu-id="e013e-266">Blue.exe</span></span>          |
| <span data-ttu-id="e013e-267">4</span><span class="sxs-lookup"><span data-stu-id="e013e-267">4</span></span>     | <span data-ttu-id="e013e-268">Заголовок синего окна</span><span class="sxs-lookup"><span data-stu-id="e013e-268">Blue Window Title</span></span> |



 

> [!Note]  
> <span data-ttu-id="e013e-269">В установщик Windows версии 4,0, если идентификатор процесса, переданный из службы, не имеет заголовка окна, например приложения панели задач, файл не отображается, а подробный журнал содержит следующие сообщения.</span><span class="sxs-lookup"><span data-stu-id="e013e-269">On Windows Installer version 4.0, if the PID passed from the service does not have a window title, such as a system tray application, the file is not be displayed and the verbose log contains the following messages.</span></span>

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

<span data-ttu-id="e013e-270">ИНСТАЛЛМЕССАЖЕ \_ ресолвесаурце</span><span class="sxs-lookup"><span data-stu-id="e013e-270">INSTALLMESSAGE\_RESOLVESOURCE</span></span>

<span data-ttu-id="e013e-271">\_Запись РЕСОЛВЕСАУРЦЕ инсталлмессаже содержит семь полей.</span><span class="sxs-lookup"><span data-stu-id="e013e-271">The INSTALLMESSAGE\_RESOLVESOURCE record has seven fields.</span></span> <span data-ttu-id="e013e-272">Для \_ правильной работы инсталлмессаже ресолвесаурце внешний обработчик пользовательского интерфейса может не справиться с \_ сообщением инсталлмессаже ресолвесаурце.</span><span class="sxs-lookup"><span data-stu-id="e013e-272">For INSTALLMESSAGE\_RESOLVESOURCE to work correctly, an external UI handler may not handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="e013e-273">Установщик Windows должен выполнять обработку \_ сообщения РЕСОЛВЕСАУРЦЕ инсталлмессаже.</span><span class="sxs-lookup"><span data-stu-id="e013e-273">Windows Installer must handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="e013e-274">То есть внешний обработчик пользовательского интерфейса возвращает 0, чтобы указать, что при фильтрации сообщения ИНСТАЛЛМЕССАЖЕ ресолвесаурце не предпринято никаких действий \_ .</span><span class="sxs-lookup"><span data-stu-id="e013e-274">That is, the external UI handler returns 0 to indicate "no action taken" when filtering the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="e013e-275">Рекомендуется избегать отправки сообщения РЕСОЛВЕСАУРЦЕ.</span><span class="sxs-lookup"><span data-stu-id="e013e-275">The best practice is to avoid sending a RESOLVESOURCE message.</span></span>



| <span data-ttu-id="e013e-276">Поле</span><span class="sxs-lookup"><span data-stu-id="e013e-276">Field</span></span> | <span data-ttu-id="e013e-277">Описание</span><span class="sxs-lookup"><span data-stu-id="e013e-277">Description</span></span>                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e013e-278">0</span><span class="sxs-lookup"><span data-stu-id="e013e-278">0</span></span>     | <span data-ttu-id="e013e-279">null</span><span class="sxs-lookup"><span data-stu-id="e013e-279">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="e013e-280">1</span><span class="sxs-lookup"><span data-stu-id="e013e-280">1</span></span>     | <span data-ttu-id="e013e-281">null</span><span class="sxs-lookup"><span data-stu-id="e013e-281">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="e013e-282">2</span><span class="sxs-lookup"><span data-stu-id="e013e-282">2</span></span>     | <span data-ttu-id="e013e-283">Имя пакета.</span><span class="sxs-lookup"><span data-stu-id="e013e-283">Package name.</span></span>                                                                                                                                                      |
| <span data-ttu-id="e013e-284">3</span><span class="sxs-lookup"><span data-stu-id="e013e-284">3</span></span>     | <span data-ttu-id="e013e-285">Код продукта.</span><span class="sxs-lookup"><span data-stu-id="e013e-285">Product code.</span></span>                                                                                                                                                      |
| <span data-ttu-id="e013e-286">4</span><span class="sxs-lookup"><span data-stu-id="e013e-286">4</span></span>     | <span data-ttu-id="e013e-287">Относительный путь, если он известен, может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="e013e-287">Relative path if known, can be null.</span></span>                                                                                                                               |
| <span data-ttu-id="e013e-288">5</span><span class="sxs-lookup"><span data-stu-id="e013e-288">5</span></span>     | <span data-ttu-id="e013e-289">0</span><span class="sxs-lookup"><span data-stu-id="e013e-289">0</span></span>                                                                                                                                                                  |
| <span data-ttu-id="e013e-290">6</span><span class="sxs-lookup"><span data-stu-id="e013e-290">6</span></span>     | <span data-ttu-id="e013e-291">Следует ли проверять код пакета.</span><span class="sxs-lookup"><span data-stu-id="e013e-291">Whether to validate the package code.</span></span> <span data-ttu-id="e013e-292">Значение "1" указывает, что код пакета должен быть проверен.</span><span class="sxs-lookup"><span data-stu-id="e013e-292">A value of '1' indicates the package code should be validated.</span></span> <span data-ttu-id="e013e-293">Значение "0" указывает, что пакет не должен проверяться.</span><span class="sxs-lookup"><span data-stu-id="e013e-293">A value of '0' indicates the package should not be validated.</span></span> |
| <span data-ttu-id="e013e-294">7</span><span class="sxs-lookup"><span data-stu-id="e013e-294">7</span></span>     | <span data-ttu-id="e013e-295">Требуемый диск из таблицы носителей.</span><span class="sxs-lookup"><span data-stu-id="e013e-295">Required disk from media table.</span></span> <span data-ttu-id="e013e-296">Значение "0" указывает, что любой диск приемлем.</span><span class="sxs-lookup"><span data-stu-id="e013e-296">A value of '0' indicates that any disk is acceptable.</span></span>                                                                              |



 

 

 




