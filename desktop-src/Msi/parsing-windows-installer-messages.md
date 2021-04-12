---
description: Внешний обработчик пользовательского интерфейса может обрабатывать список сообщений установщика, указанных параметром Двмессажедфилтер функции Мсисетекстерналуи.
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: Синтаксический анализ сообщений установщик Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263839"
---
# <a name="parsing-windows-installer-messages"></a><span data-ttu-id="4ba5b-103">Синтаксический анализ сообщений установщик Windows</span><span class="sxs-lookup"><span data-stu-id="4ba5b-103">Parsing Windows Installer Messages</span></span>

<span data-ttu-id="4ba5b-104">Внешний обработчик пользовательского интерфейса может обрабатывать список сообщений установщика, указанных параметром *двмессажедфилтер* функции [**мсисетекстерналуи**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="4ba5b-104">An external UI handler can process the list of installer messages specified by the *dwMessagedFilter* parameter of the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span> <span data-ttu-id="4ba5b-105">Некоторые из этих сообщений содержат строки, которые можно использовать напрямую, а также может потребоваться синтаксический анализ и обработка других сообщений с помощью внешнего обработчика пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-105">Some of these messages contain strings that can be used directly, and other messages may need to be parsed and processed by the external UI handler to be useful.</span></span> <span data-ttu-id="4ba5b-106">Внешнему пользовательскому интерфейсу может потребоваться отслеживать только установщик Windows сообщения без выполнения каких бы то ни было операций, влияющих на установку.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-106">Your external UI handler may only need to monitor Windows Installer messages without performing any operation that affects the installation.</span></span>

<span data-ttu-id="4ba5b-107">Следующие установщик Windows сообщения содержат строки, которые могут отображаться в диалоговом окне и не требуют дополнительной обработки.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-107">The following Windows Installer messages contain strings that can be displayed by a dialog box and need no additional processing.</span></span> <span data-ttu-id="4ba5b-108">Эти сообщения содержат список кнопок и значков, отображаемых в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-108">These messages contain a list of buttons and icons that are to be displayed by a dialog box.</span></span> <span data-ttu-id="4ba5b-109">Для указания значков и кнопок можно использовать значения **\_ типемаск** **MB (МБ) \_ Иконмаск**, **MB \_ дефмаск** и MB.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-109">You can use the **MB\_ICONMASK**, **MB\_DEFMASK**, and **MB\_TYPEMASK** values to specify icons and buttons.</span></span>

<dl> <dt>

<span data-ttu-id="4ba5b-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**ИНСТАЛЛМЕССАЖЕ \_ фаталексит**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE\_FATALEXIT**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-111">Произошло преждевременное завершение установки.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-111">Premature termination of installation has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**ИНСТАЛЛМЕССАЖЕ, \_ Ошибка**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**INSTALLMESSAGE\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-113">Отформатированное сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-113">Formatted error message.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**\_предупреждение инсталлмессаже**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**INSTALLMESSAGE\_WARNING**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-115">Форматированное предупреждающее сообщение.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-115">Formatted warning message.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**\_сведения о инсталлмессаже**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**INSTALLMESSAGE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-117">Форматированное сообщение журнала.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-117">Formatted log message.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**\_пользователь инсталлмессаже**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**INSTALLMESSAGE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-119">Форматированное сообщение пользователя.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-119">Formatted user message.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**ИНСТАЛЛМЕССАЖЕ \_ аутофдискспаце**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE\_OUTOFDISKSPACE**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-121">Форматированное сообщение, указывающее на недостаточное место на диске</span><span class="sxs-lookup"><span data-stu-id="4ba5b-121">Formatted message indicating an out of disk space condition</span></span>

</dd> </dl>

<span data-ttu-id="4ba5b-122">Внешний пользовательский обработчик может использовать следующие установщик Windows сообщения для отслеживания последовательности пользовательского интерфейса установщик Windows.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-122">The external user handler can use the following Windows Installer messages to monitor a sequence of the Windows Installer UI.</span></span> <span data-ttu-id="4ba5b-123">Установщик отправляет эти сообщения в начале последовательности пользовательского интерфейса установщик Windows, когда отображается каждое диалоговое окно и в конце последовательности пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-123">The installer sends these messages at the start of a Windows Installer UI sequence, as each dialog box is displayed, and at the end of the UI sequence.</span></span> <span data-ttu-id="4ba5b-124">Для использования этих сообщений обработка не требуется.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-124">No processing is required to use these messages.</span></span>

<dl> <dt>

<span data-ttu-id="4ba5b-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>\_Завершение инсталлмессаже</span><span class="sxs-lookup"><span data-stu-id="4ba5b-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE\_TERMINATE</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-126">Это сообщение указывает на конец последовательности пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-126">This message indicates the end of the UI sequence.</span></span> <span data-ttu-id="4ba5b-127">Строка является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-127">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>\_Инициализация инсталлмессаже</span><span class="sxs-lookup"><span data-stu-id="4ba5b-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-129">Это сообщение означает, что последовательность пользовательского интерфейса запущена.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-129">This message indicates that the UI sequence has started.</span></span> <span data-ttu-id="4ba5b-130">Строка является пустой строкой.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-130">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>ИНСТАЛЛМЕССАЖЕ \_ SHOWDIALOG</span><span class="sxs-lookup"><span data-stu-id="4ba5b-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE\_SHOWDIALOG</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-132">Строка содержит имя текущего диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-132">The string contains the name of the current dialog box.</span></span>

</dd> </dl>

<span data-ttu-id="4ba5b-133">Для следующих установщик Windows сообщений требуется дополнительная обработка внешним обработчиком пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-133">The following Windows Installer messages require additional processing by the external UI handler.</span></span>

<dl> <dt>

<span data-ttu-id="4ba5b-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**ИНСТАЛЛМЕССАЖЕ \_ ресолвесаурце**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE\_RESOLVESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-135">Обработчик внешнего пользовательского интерфейса должен возвращать значение 0 и разрешить установщик Windows обработку сообщения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-135">The external user interface handler must return 0 and allow Windows Installer to handle the message.</span></span> <span data-ttu-id="4ba5b-136">Обработчик внешнего пользовательского интерфейса может отслеживать это сообщение, но не должен выполнять никаких действий, влияющих на установку.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-136">The external user interface handler can monitor for this message, but it should not perform any action that affects the installation .</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**ИНСТАЛЛМЕССАЖЕ \_ филесинусе**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE\_FILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-138">Внешний пользовательский интерфейс должен отображать [диалоговое окно филесинусе](filesinuse-dialog.md) в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-138">The external UI should display a [FilesInUse dialog](filesinuse-dialog.md) in response to this message.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**ИНСТАЛЛМЕССАЖЕ \_ рмфилесинусе**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE\_RMFILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-140">Внешний пользовательский интерфейс должен отображать [диалоговое окно мсирмфилесинусе](msirmfilesinuse-dialog.md) в ответ на это сообщение.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-140">The external UI should display a [MsiRMFilesInUse dialog](msirmfilesinuse-dialog.md) in response to this message.</span></span> <span data-ttu-id="4ba5b-141">Доступно начиная с версии установщик Windows 4,0.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-141">Available beginning with Windows Installer version 4.0.</span></span> <span data-ttu-id="4ba5b-142">Дополнительные сведения об этом сообщении см. в разделе [Использование диспетчера перезапуска с внешним пользовательским интерфейсом](using-restart-manager-with-an-external-ui-.md).</span><span class="sxs-lookup"><span data-stu-id="4ba5b-142">For more information about this message see [Using Restart Manager with an External UI](using-restart-manager-with-an-external-ui-.md).</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**ИНСТАЛЛМЕССАЖЕ \_ актионстарт**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE\_ACTIONSTART**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-144">Это сообщение содержит сведения о текущем действии.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-144">This message gives information about the current action.</span></span> <span data-ttu-id="4ba5b-145">Формат — действие \[ 1 \] : \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="4ba5b-145">The format is Action \[1\]: \[2\].</span></span> <span data-ttu-id="4ba5b-146">\[3 \] , где двоеточие используется для отделения поля 1 и поля 2, а точка используется для отделения поля 2 и поля 3.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-146">\[3\], where a colon is used to separate Field 1 and Field 2 and a period is used to separate Field 2 and Field 3.</span></span> <span data-ttu-id="4ba5b-147">Поле \[ 1 \] содержит время начала действия с использованием формата свойства [**времени**](time.md) .</span><span class="sxs-lookup"><span data-stu-id="4ba5b-147">Field \[1\] contains the time the action was started using the [**Time**](time.md) property format.</span></span> <span data-ttu-id="4ba5b-148">Поле \[ 2 \] содержит имя действия из таблицы последовательности.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-148">Field \[2\] contains the action's name from the sequence table.</span></span> <span data-ttu-id="4ba5b-149">Поле \[ 3 \] предоставляет описание действия из [таблицы актионтекст](actiontext-table.md) или из функции [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="4ba5b-149">Field \[3\] gives the action's description from the [ActionText table](actiontext-table.md) or from the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**ИНСТАЛЛМЕССАЖЕ \_ актиондата**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE\_ACTIONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-151">Формат этой строки определяется значением [шаблона](template.md) , указанным в [таблице Актионтекст](actiontext-table.md) или функцией [**мсипроцессмессаже**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="4ba5b-151">The format of this string is specified by the [Template](template.md) value provided in the [ActionText table](actiontext-table.md) or by the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="4ba5b-152">После сообщения **инсталлмессаже \_ актионстарт** может быть неограниченным числом **инсталлмессаже \_ актиондата** сообщений.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-152">There can be an unlimited number of **INSTALLMESSAGE\_ACTIONDATA** messages after the **INSTALLMESSAGE\_ACTIONSTART** message.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**ИНСТАЛЛМЕССАЖЕ \_ коммондата**</span><span class="sxs-lookup"><span data-stu-id="4ba5b-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE\_COMMONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-154">Это сообщение имеет три подтипа: язык, заголовок и Канцелшов.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-154">This message has three subtypes: Language, Caption, and CancelShow.</span></span> <span data-ttu-id="4ba5b-155">Строка может содержать три поля, разделенные знаком, за которым следует двоеточие.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-155">The string can have three fields delimited by a number followed by a colon.</span></span> <span data-ttu-id="4ba5b-156">Не все поля являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-156">Not all fields are required.</span></span> <span data-ttu-id="4ba5b-157">Сообщение может быть пустой строкой ("") или иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-157">The message can be a NULL or empty ("") string.</span></span>

<dl> <dt>

<span data-ttu-id="4ba5b-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Языке</span><span class="sxs-lookup"><span data-stu-id="4ba5b-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-159">Поле 1 содержит значение 0, указывающее, что эта строка содержит сведения о языке.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-159">Field 1 contains the value 0 to indicate this string contains language information.</span></span> <span data-ttu-id="4ba5b-160">Поле 2 содержит значение [языка](language.md) , которое является числовым идентификатором языка (LangID.) Поле 3 — это значение, представляющее кодовую страницу ANSI.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-160">Field 2 contains a [Language](language.md) value that is a numeric language identifier (LANGID.) Field 3 is a value that represents an ANSI code page.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Пояснитель</span><span class="sxs-lookup"><span data-stu-id="4ba5b-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Caption</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-162">Поле 1 содержит значение 1, указывающее, что эта строка содержит текст заголовка или заголовка.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-162">Field 1 contains the value 1 to indicate this string contains the text of a caption or title.</span></span> <span data-ttu-id="4ba5b-163">Поле 2 содержит текст, который может использоваться внешним обработчиком пользовательского интерфейса в качестве заголовка для диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-163">Field 2 contains text that an external UI handler can use as a caption of title for a dialog box.</span></span> <span data-ttu-id="4ba5b-164">Поле 3 имеет значение NULL или является пустой строкой ("").</span><span class="sxs-lookup"><span data-stu-id="4ba5b-164">Field 3 is NULL or an empty ("") string.</span></span> <span data-ttu-id="4ba5b-165">Поле 3 может отсутствовать в тексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-165">Field 3 can be absent from a the Caption message.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>канцелшов</span><span class="sxs-lookup"><span data-stu-id="4ba5b-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-167">Поле 1 содержит значение 2, указывающее, что эта строка содержит сведения о том, следует ли отображать кнопку Отмена.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-167">Field 1 contains the value 2 to indicate this string contains information about whether to display the cancel button.</span></span> <span data-ttu-id="4ba5b-168">Если кнопка отмена должна быть скрыта, поле 2 содержит значение 0.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-168">If the cancel button should be hidden, Field 2 contains the value 0.</span></span> <span data-ttu-id="4ba5b-169">Если кнопка отмена должна быть видимой, поле 2 содержит значение 1.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-169">If the cancel button should be visible, Field 2 contains the value 1.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="4ba5b-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>\_ход выполнения инсталлмессаже</span><span class="sxs-lookup"><span data-stu-id="4ba5b-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>INSTALLMESSAGE\_PROGRESS</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-171">Это сообщение имеет четыре подтипа: Reset, ActionInfo, Прогрессрепорт и Прогрессаддитион.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-171">This message has four subtypes: Reset, ActionInfo, ProgressReport, and ProgressAddition.</span></span> <span data-ttu-id="4ba5b-172">Внешний обработчик не должен действовать ни для одного из этих сообщений, пока не будет получено первое сообщение о ходе выполнения сброса.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-172">The external handler should not act upon any of these messages until the first a Reset progress message is received.</span></span> <span data-ttu-id="4ba5b-173">Это позволяет оценить общее количество тактов для индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-173">This provides an estimate of the total number of ticks for the progress bar.</span></span>

<dl> <dt>

<span data-ttu-id="4ba5b-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Перезапуск</span><span class="sxs-lookup"><span data-stu-id="4ba5b-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Reset</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-175">Поле 1 содержит значение 0, указывающее на Сброс индикатора выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-175">Field 1 contains the value 0 to indicate a reset of the progress bar.</span></span> <span data-ttu-id="4ba5b-176">Поле 2 содержит общее число тактов на индикаторе выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-176">Field 2 contains the total number of ticks in the progress bar.</span></span> <span data-ttu-id="4ba5b-177">Поле 3 содержит значение 0 для перемещения индикатора выполнения вперед.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-177">Field 3 contains the value 0 for forward progress bar motion.</span></span> <span data-ttu-id="4ba5b-178">Поле 3 содержит значение 1 для перемещения индикатора хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-178">Field 3 contains the value 1 for backward progress bar motion.</span></span> <span data-ttu-id="4ba5b-179">Значение 0 в поле 4 означает, что установка выполняется и оставшееся время может быть вычислено.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-179">The value 0 in Field 4 means the installation is in progress and the time remaining may be calculated.</span></span> <span data-ttu-id="4ba5b-180">Значение 1 в поле 4 означает, что сценарий выполняется и "Подождите..." может отображаться сообщение.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-180">The value 1 in Field 4 means script is being run and a "Please wait ..." message can be displayed.</span></span> <span data-ttu-id="4ba5b-181">Оценка общего числа тактов является приближением и может быть неточной.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-181">The estimate of the total number of ticks is an approximation and may be inaccurate.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span><span class="sxs-lookup"><span data-stu-id="4ba5b-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-183">Поле 1 содержит значение 1, указывающее, что эта строка содержит сведения о действии.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-183">Field 1 contains the value 1 to indicate this string contains action information.</span></span> <span data-ttu-id="4ba5b-184">Поле 2 содержит количество тактов, на которое перемещается индикатор выполнения для каждого сообщения Актиондата, отправленного текущим действием.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-184">Field 2 contains the number of ticks the progress bar moves for each ActionData message sent by the current action.</span></span> <span data-ttu-id="4ba5b-185">Если поле 3 содержит значение 0, не учитывать поле 2.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-185">If Field 3 contains the value 0, ignore Field 2.</span></span> <span data-ttu-id="4ba5b-186">Если поле 3 содержит значение 1, увеличьте индикатор выполнения на число тактов в поле 2 для каждого сообщения Актиондата, отправленного текущим действием.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-186">If Field 3 contains the value 1, increment the progress bar by the number of ticks in Field 2 for each ActionData message sent by the current action.</span></span> <span data-ttu-id="4ba5b-187">Поле 4 не используется.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-187">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>прогрессрепорт</span><span class="sxs-lookup"><span data-stu-id="4ba5b-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-189">Поле 1 содержит значение 2, указывающее, что эта строка содержит сведения о ходе выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-189">Field 1 contains the value 2 to indicate this string contains progress information.</span></span> <span data-ttu-id="4ba5b-190">Поле 2 содержит число тактов, на которое переместился индикатор выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-190">Field 2 contains the number of ticks the progress bar has moved.</span></span> <span data-ttu-id="4ba5b-191">Поле 3 не используется.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-191">Field 3 is unused.</span></span> <span data-ttu-id="4ba5b-192">Поле 4 не используется.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-192">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="4ba5b-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>прогрессаддитион</span><span class="sxs-lookup"><span data-stu-id="4ba5b-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span></span>
</dt> <dd>

<span data-ttu-id="4ba5b-194">Поле 1 содержит значение 3, указывающее, что действие может добавить такты на индикаторе выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-194">Field 1 contains the value 3 to indicate that an action can add ticks the progress bar.</span></span> <span data-ttu-id="4ba5b-195">Поле 2 содержит число тактов для добавления к общему ожидаемому количеству тактов хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-195">Field 2 contains the number of ticks to add to total expected count of progress ticks.</span></span> <span data-ttu-id="4ba5b-196">Поле 3 не используется.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-196">Field 3 is unused.</span></span> <span data-ttu-id="4ba5b-197">Поле 4 не используется.</span><span class="sxs-lookup"><span data-stu-id="4ba5b-197">Field 4 is unused.</span></span>

</dd> </dl> </dd> </dl>

 

 



