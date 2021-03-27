---
description: Отображает окно справки, соответствующее текущему параметру языка пользовательского интерфейса.
title: Функция Млхтмлхелп
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MLHtmlHelp
- MLHtmlHelpA
- MLHtmlHelpW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.assetid: 1108614d-7034-48da-a4a5-544f8d9af3ca
ms.openlocfilehash: a477ef549b3b8437ba891259c7fecea4730f759e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997267"
---
# <a name="mlhtmlhelp-function"></a><span data-ttu-id="94920-103">Функция Млхтмлхелп</span><span class="sxs-lookup"><span data-stu-id="94920-103">MLHtmlHelp function</span></span>

<span data-ttu-id="94920-104">\[Эта функция доступна в Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="94920-104">\[This function is available through Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="94920-105">Он может быть изменен или недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="94920-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="94920-106">Отображает окно справки, соответствующее текущему параметру языка пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="94920-106">Displays a help window that corresponds to the current UI language setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="94920-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="94920-107">Syntax</span></span>


```C++
HWND MLHtmlHelp(
  _In_ HWND      hwndCaller,
  _In_ LPCTSTR   pszFile,
  _In_ UINT      uCommand,
  _In_ DWORD_PTR dwData,
  _In_ DWORD     dwCrossCodePage
);
```



## <a name="parameters"></a><span data-ttu-id="94920-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="94920-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94920-109">*хвндкаллер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94920-109">*hwndCaller* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94920-110">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="94920-110">Type: **HWND**</span></span>

<span data-ttu-id="94920-111">Маркер родительского окна, вызывающего эту функцию.</span><span class="sxs-lookup"><span data-stu-id="94920-111">A handle to the parent window that calls this function.</span></span>

</dd> <dt>

<span data-ttu-id="94920-112">*псзфиле* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94920-112">*pszFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94920-113">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="94920-113">Type: **LPCTSTR**</span></span>

<span data-ttu-id="94920-114">Указатель на буфер, содержащий полный путь скомпилированного файла справки (CHM) или файл раздела в указанном файле справки.</span><span class="sxs-lookup"><span data-stu-id="94920-114">A pointer to a buffer that contains the fully qualified path of a compiled help (.chm) file, or a topic file within a specified help file.</span></span>

</dd> <dt>

<span data-ttu-id="94920-115">*укомманд* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94920-115">*uCommand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94920-116">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="94920-116">Type: **UINT**</span></span>

<span data-ttu-id="94920-117">Команда для выполнения.</span><span class="sxs-lookup"><span data-stu-id="94920-117">The command to complete.</span></span> <span data-ttu-id="94920-118">Эта функция напрямую поддерживает только [ \_ выводимые \_ ](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) на экран разделы и [ \_ \_ \_ всплывающее окно с отображаемым текстом HH](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span><span class="sxs-lookup"><span data-stu-id="94920-118">This function directly supports only [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) and [HH\_DISPLAY\_TEXT\_POPUP](/previous-versions/windows/desktop/htmlhelp/hh-display-text-popup-command).</span></span> <span data-ttu-id="94920-119">В случае любой другой команды вызов перенаправляется без значения *двкросскодепаже* в [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span><span class="sxs-lookup"><span data-stu-id="94920-119">In the case of any other command, the call is forwarded without the *dwCrossCodePage* value to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api).</span></span>

</dd> <dt>

<span data-ttu-id="94920-120">*двдата* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94920-120">*dwData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94920-121">Тип: **DWORD \_ ptr**</span><span class="sxs-lookup"><span data-stu-id="94920-121">Type: **DWORD\_PTR**</span></span>

<span data-ttu-id="94920-122">Любые данные, которые могут потребоваться в зависимости от значения параметра *укомманд* .</span><span class="sxs-lookup"><span data-stu-id="94920-122">Any data that may be required, based on the value of the *uCommand* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="94920-123">*двкросскодепаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94920-123">*dwCrossCodePage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94920-124">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="94920-124">Type: **DWORD**</span></span>

<span data-ttu-id="94920-125">Значение **типа DWORD** , указывающее кодовую страницу текущего параметра языка пользовательского интерфейса, например CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="94920-125">The **DWORD** value indicating the code page of the current UI language setting, such as CP\_ACP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94920-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="94920-126">Return value</span></span>

<span data-ttu-id="94920-127">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="94920-127">Type: **HWND**</span></span>

<span data-ttu-id="94920-128">В зависимости от указанного *укомманд* и результата **млхтмлхелп** возвращает одно или оба из следующих данных:</span><span class="sxs-lookup"><span data-stu-id="94920-128">Depending on the specified *uCommand* and the result, **MLHtmlHelp** returns one or both of the following:</span></span>

-   <span data-ttu-id="94920-129">Дескриптор (HWND) окна справки.</span><span class="sxs-lookup"><span data-stu-id="94920-129">The handle (hwnd) of the help window.</span></span>
-   <span data-ttu-id="94920-130">**Значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="94920-130">**NULL**.</span></span> <span data-ttu-id="94920-131">В некоторых случаях **значение NULL** указывает на ошибку; в других случаях **значение NULL** указывает, что окно справки еще не создано.</span><span class="sxs-lookup"><span data-stu-id="94920-131">In some cases, **NULL** indicates failure; in other cases, **NULL** indicates that the help window has not yet been created.</span></span>

## <a name="remarks"></a><span data-ttu-id="94920-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="94920-132">Remarks</span></span>

<span data-ttu-id="94920-133">При возникновении проблемы с путем к файлу справки для текущего языка вызов перенаправляется в [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) для стандартной обработки.</span><span class="sxs-lookup"><span data-stu-id="94920-133">If a problem arises with the path of the help file for the current language, the call is forwarded to [HtmlHelp](/previous-versions/windows/desktop/htmlhelp/accessing-the-html-help-api) for standard handling.</span></span>

<span data-ttu-id="94920-134">Когда окно справки закрывается, фокус возвращается владельцу, если только владелец не является рабочим столом.</span><span class="sxs-lookup"><span data-stu-id="94920-134">When the help window is closed, focus returns to the owner unless the owner is the desktop.</span></span> <span data-ttu-id="94920-135">Если *хвндкаллер* является настольным компьютером, операционная система определяет, где будет возвращен фокус.</span><span class="sxs-lookup"><span data-stu-id="94920-135">If *hwndCaller* is the desktop, then the operating system determines where focus is returned.</span></span>

<span data-ttu-id="94920-136">Кроме того, если **млхтмлхелп** отправляет сообщения уведомлений из окна справки, сообщения отправляются в *хвндкаллер* при условии, что в определении окна справки включено отслеживание [сообщений уведомления](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) .</span><span class="sxs-lookup"><span data-stu-id="94920-136">In addition, if **MLHtmlHelp** sends any notification messages from the help window, the messages are sent to *hwndCaller* as long as you have enabled [notification message](/previous-versions/windows/desktop/htmlhelp/about-notification-messages) tracking in the help window definition.</span></span>

## <a name="examples"></a><span data-ttu-id="94920-137">Примеры</span><span class="sxs-lookup"><span data-stu-id="94920-137">Examples</span></span>

<span data-ttu-id="94920-138">В следующем примере вызывается команда [чч \_ отобразить \_ раздел](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) , чтобы открыть файл справки с именем Help. chm и отобразить его раздел по умолчанию в окне справки с именем `Mainwin` .</span><span class="sxs-lookup"><span data-stu-id="94920-138">The following example calls the [HH\_DISPLAY\_TOPIC](/previous-versions/windows/desktop/htmlhelp/hh-display-topic-command) command to open the help file named Help.chm and display its default topic in the help window named `Mainwin`.</span></span> <span data-ttu-id="94920-139">Как правило, окно справки, указанное в этой команде, является стандартным окном [справки HTML](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span><span class="sxs-lookup"><span data-stu-id="94920-139">Generally, the help window specified in this command is a standard [HTML Help Viewer](/previous-versions/windows/desktop/htmlhelp/html-help-viewer-topics).</span></span>

``` syntax
HWND hwnd = HtmlHelp(GetDesktopWindow(),
                     "c:\\Help.chm::/Intro.htm>Mainwin",
                     HH_DISPLAY_TOPIC,
                     NULL,
                     CP_ACP);
```

> [!Note]  
> <span data-ttu-id="94920-140">При использовании этой функции задайте размер стека исполняемого объекта размещения не менее 100 КБ.</span><span class="sxs-lookup"><span data-stu-id="94920-140">When using this function, set the stack size of the hosting executable to at least 100k.</span></span> <span data-ttu-id="94920-141">Если определенный размер стека слишком мал, то поток, созданный для запуска справки HTML, также будет создан с этим размером стека, и операция может завершиться ошибкой.</span><span class="sxs-lookup"><span data-stu-id="94920-141">If the defined stack size is too small, then the thread created to run HTML Help will also be created with this stack size, and the operation could fail.</span></span> <span data-ttu-id="94920-142">При необходимости можно удалить параметр/STACK из командной строки компоновки, а также удалить все параметры СТЕКа в DEF-файле исполняемого файла (в этом случае размер стека по умолчанию — 1 МБ).</span><span class="sxs-lookup"><span data-stu-id="94920-142">Optionally, you can remove /STACK from the link command line, and also remove any STACK setting in the executable's DEF file (default stack size is 1MB in this case).</span></span> <span data-ttu-id="94920-143">Размер стека также можно задать с помощью команды компилятора/Фнумбер (компилятор передаст это компоновщику как/STACK).</span><span class="sxs-lookup"><span data-stu-id="94920-143">You can also set the stack size using the /Fnumber compiler command (the compiler will pass this to the linker as /STACK).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="94920-144">Требования</span><span class="sxs-lookup"><span data-stu-id="94920-144">Requirements</span></span>



| <span data-ttu-id="94920-145">Требование</span><span class="sxs-lookup"><span data-stu-id="94920-145">Requirement</span></span> | <span data-ttu-id="94920-146">Значение</span><span class="sxs-lookup"><span data-stu-id="94920-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94920-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94920-147">Minimum supported client</span></span><br/> | <span data-ttu-id="94920-148">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="94920-148">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="94920-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94920-149">Minimum supported server</span></span><br/> | <span data-ttu-id="94920-150">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="94920-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="94920-151">Header</span><span class="sxs-lookup"><span data-stu-id="94920-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="94920-152"><dt>Нет</dt></span><span class="sxs-lookup"><span data-stu-id="94920-152"><dt>None</dt></span></span> </dl>                               |
| <span data-ttu-id="94920-153">DLL</span><span class="sxs-lookup"><span data-stu-id="94920-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94920-154"><dt>Shlwapi.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="94920-154"><dt>Shlwapi.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="94920-155">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="94920-155">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="94920-156">**Млхтмлхелпв** (Юникод) и **млхтмлхелпа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="94920-156">**MLHtmlHelpW** (Unicode) and **MLHtmlHelpA** (ANSI)</span></span><br/>                                               |



 

 
