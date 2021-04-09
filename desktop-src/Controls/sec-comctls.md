---
title: Вопросы безопасности элементы управления Microsoft Windows
description: В этом разделе содержатся сведения о вопросах безопасности, связанных с элементами управления Windows.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/09/2020
ms.locfileid: "104134734"
---
# <a name="security-considerations-microsoft-windows-controls"></a><span data-ttu-id="d7fd0-103">Вопросы безопасности: элементы управления Microsoft Windows</span><span class="sxs-lookup"><span data-stu-id="d7fd0-103">Security Considerations: Microsoft Windows Controls</span></span>

<span data-ttu-id="d7fd0-104">В этом разделе содержатся сведения о вопросах безопасности, связанных с элементами управления Windows.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-104">This topic provides information about security considerations related to the Windows controls.</span></span> <span data-ttu-id="d7fd0-105">Сведения в этом разделе не предоставляют все, что нужно знать о проблемах безопасности — используйте его в качестве отправной точки и ссылки для этой области.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-105">The information in this topic does not provide all you need to know about security issues—use it as a starting point and reference for this technology area.</span></span>

<span data-ttu-id="d7fd0-106">Взаимодействие между компьютерами является типичным; главным фактором разработчика должна быть безопасность приложений.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-106">Interconnectivity among computers is common; a developer's chief concern must be application security.</span></span> <span data-ttu-id="d7fd0-107">В следующих разделах рассматриваются некоторые потенциальные проблемы безопасности, которые следует учитывать при программировании элементов управления Windows.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-107">The following sections discuss some potential security issues to consider when programming Windows controls.</span></span>

-   [<span data-ttu-id="d7fd0-108">Управляющие сообщения, заканчивающиеся нулем</span><span class="sxs-lookup"><span data-stu-id="d7fd0-108">Null-terminated Control Messages</span></span>](#null-terminated-control-messages)
-   [<span data-ttu-id="d7fd0-109">Использование строк</span><span class="sxs-lookup"><span data-stu-id="d7fd0-109">String Use</span></span>](#string-use)
-   [<span data-ttu-id="d7fd0-110">Проверка входных данных</span><span class="sxs-lookup"><span data-stu-id="d7fd0-110">Input Validation</span></span>](#input-validation)
-   [<span data-ttu-id="d7fd0-111">Использование пароля</span><span class="sxs-lookup"><span data-stu-id="d7fd0-111">Password Use</span></span>](#password-use)
-   [<span data-ttu-id="d7fd0-112">Оповещения системы безопасности</span><span class="sxs-lookup"><span data-stu-id="d7fd0-112">Security Alerts</span></span>](#security-alerts)
-   [<span data-ttu-id="d7fd0-113">См. также</span><span class="sxs-lookup"><span data-stu-id="d7fd0-113">Related topics</span></span>](#related-topics)

## <a name="null-terminated-control-messages"></a><span data-ttu-id="d7fd0-114">Управляющие сообщения, заканчивающиеся нулем</span><span class="sxs-lookup"><span data-stu-id="d7fd0-114">Null-terminated Control Messages</span></span>

<span data-ttu-id="d7fd0-115">Многие управляющие сообщения и макросы имеют строковые параметры.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-115">Many of the control messages and macros have string parameters.</span></span> <span data-ttu-id="d7fd0-116">Часто эти сообщения не проверяют входные строки, в частности, не выполняют проверку на завершение `'\0'` .</span><span class="sxs-lookup"><span data-stu-id="d7fd0-116">Often these messages do not validate the input strings, in particular, they do not check for a terminating `'\0'`.</span></span> <span data-ttu-id="d7fd0-117">При вызове сообщения, использующего строку в качестве параметра, явно указывает, что строка завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-117">When you call a message that uses a string as a parameter, explicitly specify that the string is null-terminated.</span></span>

## <a name="string-use"></a><span data-ttu-id="d7fd0-118">Использование строк</span><span class="sxs-lookup"><span data-stu-id="d7fd0-118">String Use</span></span>

<span data-ttu-id="d7fd0-119">При программировании элементов управления Windows необходимо управлять строками.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-119">When you program Windows controls, it is necessary to manipulate strings.</span></span> <span data-ttu-id="d7fd0-120">Почти каждый элемент управления требует вставки текста.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-120">Almost every control requires text to be inserted.</span></span> <span data-ttu-id="d7fd0-121">Например, чтобы заполнить окно списка, необходимо загрузить строки в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-121">For example, to populate a list box you must load strings into the control.</span></span> <span data-ttu-id="d7fd0-122">Поскольку неправильное использование строк часто приводит к переполнению буфера, примите меры предосторожности, чтобы избежать этой угрозы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-122">Because using strings incorrectly often causes buffer overruns, take precautions to avoid this security risk.</span></span>

<span data-ttu-id="d7fd0-123">Дополнительные сведения о переполнении буфера см. в статье *написание безопасного кода* с помощью Майкла Ховарда и Дэвида Леблана, Microsoft Press, 2002 и рекомендаций [по использованию API-интерфейсов безопасности](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span><span class="sxs-lookup"><span data-stu-id="d7fd0-123">For more information about buffer overruns, see *Writing Secure Code* by Michael Howard and David LeBlanc, Microsoft Press, 2002 and [Best Practices for the Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span>

## <a name="input-validation"></a><span data-ttu-id="d7fd0-124">Проверка входных данных</span><span class="sxs-lookup"><span data-stu-id="d7fd0-124">Input Validation</span></span>

<span data-ttu-id="d7fd0-125">Следующие управляющие сообщения могут представлять проблемы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-125">The following control messages can present security problems.</span></span>

-   [<span data-ttu-id="d7fd0-126">**\_ЖЕТЛБТЕКСТ CB**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-126">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)
-   [<span data-ttu-id="d7fd0-127">**LVM \_ жетисеарчстринг**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-127">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md)
-   [<span data-ttu-id="d7fd0-128">**SB ( \_ SMS)**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-128">**SB\_GETTEXT**</span></span>](sb-gettext.md)
-   [<span data-ttu-id="d7fd0-129">**SB \_ жеттиптекст**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-129">**SB\_GETTIPTEXT**</span></span>](sb-gettiptext.md)
-   [<span data-ttu-id="d7fd0-130">**\_ЖЕТБУТТОНТЕКСТ ТБ**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-130">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)
-   [<span data-ttu-id="d7fd0-131">**ТТМ \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-131">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)
-   [<span data-ttu-id="d7fd0-132">**TVM \_ жетисеарчстринг**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-132">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md)

<span data-ttu-id="d7fd0-133">Если текст изменяется между вызовом для получения длины текста и времени отображения или использования текста, может произойти переполнение буфера.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-133">If the text changes between the call to get the text length and the time the text is displayed or used, a buffer overrun can occur.</span></span> <span data-ttu-id="d7fd0-134">Чтобы избежать этого, необходимо проверить строку перед ее использованием.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-134">To avoid this, you must validate the string before using it.</span></span> <span data-ttu-id="d7fd0-135">Кроме того, сообщения, которые получают текст, [**CB \_ жетлбтекст**](cb-getlbtext.md), [**ТБ \_ жетбуттонтекст**](tb-getbuttontext.md)и [**ТТМ \_ gettext**](ttm-gettext.md), не имеют параметра размера буфера, который представляет потенциал для переполнения буфера.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-135">In addition, the messages that retrieve text, [**CB\_GETLBTEXT**](cb-getlbtext.md), [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), and [**TTM\_GETTEXT**](ttm-gettext.md), have no buffer size parameter that presents the potential for a buffer overrun.</span></span>

<span data-ttu-id="d7fd0-136">При использовании [**\_ жетлбтекст CB**](cb-getlbtext.md) или SB необходимо сначала вызвать [**CB \_ жетлбтекстлен**](cb-getlbtextlen.md) или [**SB \_ жеттекстленгс**](sb-gettextlength.md) , чтобы получить размер буфера. [**\_**](sb-gettext.md)</span><span class="sxs-lookup"><span data-stu-id="d7fd0-136">When you use [**CB\_GETLBTEXT**](cb-getlbtext.md) or [**SB\_GETTEXT**](sb-gettext.md), you should first call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) or [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size.</span></span> <span data-ttu-id="d7fd0-137">Некоторые из этих сообщений, [**ТБ \_ жетбуттонтекст**](tb-getbuttontext.md), [**LVM \_ жетисеарчстринг**](lvm-getisearchstring.md)и [**TVM \_ жетисеарчстринг**](tvm-getisearchstring.md), можно вызвать с **нулевым** значением параметра, чтобы получить длину строки перед вызовом сообщения для получения строки.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-137">Some of these messages, [**TB\_GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM\_GETISEARCHSTRING**](lvm-getisearchstring.md), and [**TVM\_GETISEARCHSTRING**](tvm-getisearchstring.md), can be called with a **NULL** parameter value to obtain the length of the string before invoking the message to retrieve the string.</span></span>

<span data-ttu-id="d7fd0-138">Сообщение о том, что следует обратить особое внимание на, — это строка состояния с сообщением о [**\_ жеттиптекст**](sb-gettiptext.md) .</span><span class="sxs-lookup"><span data-stu-id="d7fd0-138">A message that you should pay particular attention to is the status bar [**SB\_GETTIPTEXT**](sb-gettiptext.md) message.</span></span> <span data-ttu-id="d7fd0-139">Это сообщение не дает возможности запрашивать длину извлекаемой строки.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-139">This message provides no way to query the length of the string that is to be retrieved.</span></span>

## <a name="password-use"></a><span data-ttu-id="d7fd0-140">Использование пароля</span><span class="sxs-lookup"><span data-stu-id="d7fd0-140">Password Use</span></span>

<span data-ttu-id="d7fd0-141">Если вы используете защищенные паролем элементы управления редактирования (например,[**\_ пароль ES**](edit-control-styles.md) ), буфер, содержащий полученный текст, должен быть установлен в значение 0 как можно скорее, чтобы избежать предоставления пароля пользователя в памяти.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-141">If you use password-protected edit controls ([**ES\_PASSWORD**](edit-control-styles.md) style), the buffer that contains the retrieved text must be set to zero as soon as possible to avoid exposing the user's password in memory.</span></span>

## <a name="security-alerts"></a><span data-ttu-id="d7fd0-142">Оповещения системы безопасности</span><span class="sxs-lookup"><span data-stu-id="d7fd0-142">Security Alerts</span></span>

<span data-ttu-id="d7fd0-143">В следующей таблице перечислены функции, которые при неправильном использовании могут поставить под угрозу безопасность приложений.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-143">The following table lists features that, if used incorrectly, can compromise the security of your applications.</span></span> <span data-ttu-id="d7fd0-144">Указанные здесь сообщения не содержат параметр, указывающий размер буфера.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-144">The messages listed here do not provide a parameter that specifies the buffer size.</span></span>



| <span data-ttu-id="d7fd0-145">Функция</span><span class="sxs-lookup"><span data-stu-id="d7fd0-145">Feature</span></span>                                               | <span data-ttu-id="d7fd0-146">Меры по снижению риска</span><span class="sxs-lookup"><span data-stu-id="d7fd0-146">Mitigation</span></span>                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d7fd0-147">**длгдирлисткомбобокс**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-147">**DlgDirListComboBox**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | <span data-ttu-id="d7fd0-148">Убедитесь, что буфер, используемый функцией, может быть записан в и завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-148">Make sure the buffer used by the function can be written to and is null-terminated.</span></span>                                                                     |
| [<span data-ttu-id="d7fd0-149">**\_ЖЕТЛБТЕКСТ CB**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-149">**CB\_GETLBTEXT**</span></span>](cb-getlbtext.md)                 | <span data-ttu-id="d7fd0-150">Вызовите [**CB \_ жетлбтекстлен**](cb-getlbtextlen.md) , чтобы получить размер буфера, а затем вызовите [**CB \_ жетлбтекст**](cb-getlbtext.md) , чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-150">Call [**CB\_GETLBTEXTLEN**](cb-getlbtextlen.md) to obtain the buffer size, and then call [**CB\_GETLBTEXT**](cb-getlbtext.md) to retrieve the string.</span></span> |
| [<span data-ttu-id="d7fd0-151">**LVM \_ жетисеарчстринг**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-151">**LVM\_GETISEARCHSTRING**</span></span>](lvm-getisearchstring.md) | <span data-ttu-id="d7fd0-152">Вызовите сообщение с **нулевым** значением параметра, чтобы получить размер буфера, а затем вызовите сообщение еще раз, чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-152">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="d7fd0-153">**SB ( \_ SMS)**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-153">**SB\_GETTEXT**</span></span>](sb-gettext.md)                     | <span data-ttu-id="d7fd0-154">Вызовите [**SB \_ жеттекстленгс**](sb-gettextlength.md) , чтобы получить размер буфера, а затем вызовите [**SB \_ gettext**](sb-gettext.md) , чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-154">Call [**SB\_GETTEXTLENGTH**](sb-gettextlength.md) to obtain the buffer size, and then call [**SB\_GETTEXT**](sb-gettext.md) to retrieve the string.</span></span>   |
| [<span data-ttu-id="d7fd0-155">**\_ЖЕТБУТТОНТЕКСТ ТБ**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-155">**TB\_GETBUTTONTEXT**</span></span>](tb-getbuttontext.md)         | <span data-ttu-id="d7fd0-156">Вызовите сообщение с **нулевым** значением параметра, чтобы получить размер буфера, а затем вызовите сообщение еще раз, чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-156">Call the message with a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>             |
| [<span data-ttu-id="d7fd0-157">**ТТМ \_ gettext**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-157">**TTM\_GETTEXT**</span></span>](ttm-gettext.md)                   | <span data-ttu-id="d7fd0-158">Это сообщение не дает способа определить или указать размер буфера.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-158">This message does not provide a way for you to know or specify the size of the buffer.</span></span>                                                                  |
| [<span data-ttu-id="d7fd0-159">**TVM \_ жетисеарчстринг**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-159">**TVM\_GETISEARCHSTRING**</span></span>](tvm-getisearchstring.md) | <span data-ttu-id="d7fd0-160">Вызовите сообщение, передав значение параметра **null** , чтобы получить размер буфера, а затем вызовите сообщение еще раз, чтобы получить строку.</span><span class="sxs-lookup"><span data-stu-id="d7fd0-160">Call the message by passing a **NULL** parameter value to obtain the buffer size, and then call the message a second time to retrieve the string.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="d7fd0-161">См. также</span><span class="sxs-lookup"><span data-stu-id="d7fd0-161">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d7fd0-162">**Другие ресурсы**</span><span class="sxs-lookup"><span data-stu-id="d7fd0-162">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="d7fd0-163">Microsoft Security</span><span class="sxs-lookup"><span data-stu-id="d7fd0-163">Microsoft Security</span></span>](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[<span data-ttu-id="d7fd0-164">Безопасность</span><span class="sxs-lookup"><span data-stu-id="d7fd0-164">Security</span></span>](/windows/desktop/security)
</dt> <dt>

[<span data-ttu-id="d7fd0-165">Материалы по безопасности TechNet</span><span class="sxs-lookup"><span data-stu-id="d7fd0-165">TechNet Security Resources</span></span>](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[<span data-ttu-id="d7fd0-166">Рекомендации по использованию API безопасности</span><span class="sxs-lookup"><span data-stu-id="d7fd0-166">Best Practices for the Security APIs</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 