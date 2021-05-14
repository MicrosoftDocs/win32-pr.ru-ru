---
description: Указывает определяемую приложением функцию обратного вызова, вызываемую диспетчером файлов для взаимодействия с расширением диспетчера файлов.
title: Функция обратного вызова Фмекстенсионпрок (Вфекст. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMExtensionProc
- FMExtensionProcW
api_type:
- UserDefined
api_location:
- Wfext.h
ms.assetid: 6e02d655-f7d8-460a-97d2-5b369493e941
ms.openlocfilehash: 5e7b1f0142ea77967af15087131d3036aaec505e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842245"
---
# <a name="fmextensionproc-callback-function"></a><span data-ttu-id="7d1d6-103">Функция обратного вызова Фмекстенсионпрок</span><span class="sxs-lookup"><span data-stu-id="7d1d6-103">FMExtensionProc callback function</span></span>

<span data-ttu-id="7d1d6-104">Указывает определяемую приложением функцию обратного вызова, вызываемую диспетчером файлов для взаимодействия с расширением диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-104">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d1d6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d1d6-105">Syntax</span></span>


```C++
LONG CALLBACK FMExtensionProc(
   HWND hwnd,
   WORD wMsg,
   LONG lParam
);
```



## <a name="parameters"></a><span data-ttu-id="7d1d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7d1d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d1d6-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="7d1d6-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="7d1d6-108">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-108">Type: **HWND**</span></span>

<span data-ttu-id="7d1d6-109">Обработчик окна для диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-109">A window handle to File Manager.</span></span> <span data-ttu-id="7d1d6-110">Расширение использует этот обработчик, чтобы указать родительское окно для любого диалогового окна или поля сообщения, которое оно должно отображать, а также для отправки сообщений запросов в Диспетчер файлов.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-110">An extension uses this handle to specify the parent window for any dialog box or message box it must display, and to send query messages to File Manager.</span></span>

</dd> <dt>

<span data-ttu-id="7d1d6-111">*вмсг*</span><span class="sxs-lookup"><span data-stu-id="7d1d6-111">*wMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="7d1d6-112">Тип: **слово**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-112">Type: **WORD**</span></span>

<span data-ttu-id="7d1d6-113">Одно из следующих сообщений диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-113">One of the following File Manager messages.</span></span>

<dt>

<span id="1_through_99"></span><span id="1_THROUGH_99"></span>

<span data-ttu-id="7d1d6-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**от 1 до 99**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-114"><span id="1_through_99"></span><span id="1_THROUGH_99"></span>**1 through 99**</span></span>


</dt> <dd>

<span data-ttu-id="7d1d6-115">Пользователь выбрал элемент из меню, предоставляемого расширением.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-115">User selected an item from the extension-supplied menu.</span></span> <span data-ttu-id="7d1d6-116">Значение является идентификатором выбранного пункта меню.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-116">The value is the identifier of the selected menu item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>

<span data-ttu-id="7d1d6-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**ФМЕВЕНТ \_ хелпменуитем**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-117"><span id="FMEVENT_HELPMENUITEM"></span><span id="fmevent_helpmenuitem"></span>**FMEVENT\_HELPMENUITEM**</span></span>


</dt> <dd>

<span data-ttu-id="7d1d6-118">Пользователь нажал клавишу F1 при выборе меню расширения или элемента команды панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-118">User pressed F1 while selecting an extension menu or toolbar command item.</span></span> <span data-ttu-id="7d1d6-119">Указывает, что расширение должно правильно вызывать **WinHelp** для элемента команды.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-119">Indicates that the extension should call **WinHelp** appropriately for the command item.</span></span>

</dd> <dt>

<span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>

<span data-ttu-id="7d1d6-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**ФМЕВЕНТ \_ HELPSTRING**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-120"><span id="FMEVENT_HELPSTRING"></span><span id="fmevent_helpstring"></span>**FMEVENT\_HELPSTRING**</span></span>


</dt> <dd>

<span data-ttu-id="7d1d6-121">Пользователь выбрал пункт меню или команду панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-121">User selected an extension menu or toolbar command item.</span></span> <span data-ttu-id="7d1d6-122">Указывает, что расширение должно предоставить строку справки.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-122">Indicates that the extension should supply a Help string.</span></span>

</dd> <dt>

<span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>

<span data-ttu-id="7d1d6-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**ФМЕВЕНТ \_ инитмену**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-123"><span id="FMEVENT_INITMENU"></span><span id="fmevent_initmenu"></span>**FMEVENT\_INITMENU**</span></span>


</dt> <dd>

<span data-ttu-id="7d1d6-124">Пользователь выбрал меню расширения.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-124">User selected the extension's menu.</span></span> <span data-ttu-id="7d1d6-125">Расширение должно инициализировать элементы в меню.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-125">The extension should initialize items in the menu.</span></span>

</dd> <dt>

<span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>

<span data-ttu-id="7d1d6-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**ФМЕВЕНТ \_ Загрузка**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-126"><span id="FMEVENT_LOAD"></span><span id="fmevent_load"></span>**FMEVENT\_LOAD**</span></span>


</dt> <dd>

<span data-ttu-id="7d1d6-127">Диспетчер файлов загружает библиотеку DLL расширения и запрашивает у библиотеки DLL сведения о меню, предоставленном библиотекой DLL.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-127">File Manager is loading the extension DLL and prompts the DLL for information about the menu that the DLL supplies.</span></span>

</dd> <dt>

<span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>

<span data-ttu-id="7d1d6-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**ФМЕВЕНТ \_ селчанже**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-128"><span id="FMEVENT_SELCHANGE"></span><span id="fmevent_selchange"></span>**FMEVENT\_SELCHANGE**</span></span>


</dt> <dd>

<span data-ttu-id="7d1d6-129">Был изменен выбор в окне каталога **диспетчера файлов** или в окне **результатов поиска** .</span><span class="sxs-lookup"><span data-stu-id="7d1d6-129">Selection in the **File Manager** directory window or **Search Results** window has changed.</span></span>

</dd> <dt>

<span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>

<span data-ttu-id="7d1d6-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**ФМЕВЕНТ \_ тулбарлоад**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-130"><span id="FMEVENT_TOOLBARLOAD"></span><span id="fmevent_toolbarload"></span>**FMEVENT\_TOOLBARLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="7d1d6-131">Диспетчер файлов создает панель инструментов и запрашивает у библиотеки DLL расширения сведения о любой кнопке, которую библиотека DLL добавляет на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-131">File Manager is creating the toolbar and prompts the extension DLL for information about any buttons the DLL adds to the toolbar.</span></span>

</dd> <dt>

<span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>

<span data-ttu-id="7d1d6-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**\_выгрузка фмевент**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-132"><span id="FMEVENT_UNLOAD"></span><span id="fmevent_unload"></span>**FMEVENT\_UNLOAD**</span></span>


</dt> <dd>

<span data-ttu-id="7d1d6-133">Диспетчер файлов выгружает библиотеку DLL расширения.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-133">File Manager is unloading the extension DLL.</span></span>

</dd> <dt>

<span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>

<span data-ttu-id="7d1d6-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**ФМЕВЕНТ \_ пользовательское \_ обновление**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-134"><span id="FMEVENT_USER_REFRESH"></span><span id="fmevent_user_refresh"></span>**FMEVENT\_USER\_REFRESH**</span></span>


</dt> <dd>

<span data-ttu-id="7d1d6-135">Пользователь выбрал команду " **Обновить** " в меню " **окно** ".</span><span class="sxs-lookup"><span data-stu-id="7d1d6-135">User selected the **Refresh** command from the **Window** menu.</span></span> <span data-ttu-id="7d1d6-136">При необходимости расширение должно обновлять элементы в меню.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-136">The extension should update items in the menu, if necessary.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7d1d6-137">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7d1d6-137">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7d1d6-138">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-138">Type: **LONG**</span></span>

<span data-ttu-id="7d1d6-139">Значение, зависящее от сообщения.</span><span class="sxs-lookup"><span data-stu-id="7d1d6-139">Message-specific value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d1d6-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7d1d6-140">Return value</span></span>

<span data-ttu-id="7d1d6-141">Тип: **Long**</span><span class="sxs-lookup"><span data-stu-id="7d1d6-141">Type: **LONG**</span></span>

<span data-ttu-id="7d1d6-142">Возвращает значение, зависящее от сообщения параметра *вмсг* .</span><span class="sxs-lookup"><span data-stu-id="7d1d6-142">Returns a value dependent upon the *wMsg* parameter message.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d1d6-143">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="7d1d6-143">Requirements</span></span>



| <span data-ttu-id="7d1d6-144">Требование</span><span class="sxs-lookup"><span data-stu-id="7d1d6-144">Requirement</span></span> | <span data-ttu-id="7d1d6-145">Значение</span><span class="sxs-lookup"><span data-stu-id="7d1d6-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d1d6-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d1d6-146">Minimum supported client</span></span><br/> | <span data-ttu-id="7d1d6-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d1d6-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7d1d6-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d1d6-148">Minimum supported server</span></span><br/> | <span data-ttu-id="7d1d6-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7d1d6-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7d1d6-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="7d1d6-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d1d6-151"><dt>Вфекст. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d1d6-151"><dt>Wfext.h</dt></span></span> </dl> |
| <span data-ttu-id="7d1d6-152">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="7d1d6-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="7d1d6-153">**Фмекстенсионпрокв** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="7d1d6-153">**FMExtensionProcW** (Unicode)</span></span><br/>                                          |



 

 




