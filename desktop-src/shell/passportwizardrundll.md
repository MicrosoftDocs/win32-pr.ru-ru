---
description: Запускает мастер паспорта при использовании с Rundll32.exe.
title: Функция Пасспортвизардрундлл
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PassportWizardRunDll
api_type:
- DllExport
api_location:
- Netplwiz.dll
ms.assetid: 015c3875-698e-4d80-bbfc-4fc8a71197b7
ms.openlocfilehash: 1678677bcb305b7e5c47d28f5168d1e596ca3e26
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842515"
---
# <a name="passportwizardrundll-function"></a><span data-ttu-id="53bcb-103">Функция Пасспортвизардрундлл</span><span class="sxs-lookup"><span data-stu-id="53bcb-103">PassportWizardRunDll function</span></span>

<span data-ttu-id="53bcb-104">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="53bcb-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="53bcb-105">Он может быть изменен или недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="53bcb-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="53bcb-106">Запускает мастер паспорта при использовании с Rundll32.exe.</span><span class="sxs-lookup"><span data-stu-id="53bcb-106">Launches the Passport Wizard when used with Rundll32.exe.</span></span>

## <a name="syntax"></a><span data-ttu-id="53bcb-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53bcb-107">Syntax</span></span>


```C++
void PassportWizardRunDll(
  _In_ HWND      hwndStub,
  _In_ HINSTANCE hAppInstance,
  _In_ LPTSTR    lpszCmdLine,
  _In_ int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="53bcb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="53bcb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53bcb-109">*хвндстуб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53bcb-109">*hwndStub* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53bcb-110">Тип: **HWND**</span><span class="sxs-lookup"><span data-stu-id="53bcb-110">Type: **HWND**</span></span>

<span data-ttu-id="53bcb-111">Маркер окна-владельца.</span><span class="sxs-lookup"><span data-stu-id="53bcb-111">A handle to an owner window.</span></span> <span data-ttu-id="53bcb-112">Обычно этот параметр имеет значение **null**.</span><span class="sxs-lookup"><span data-stu-id="53bcb-112">This parameter is typically set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="53bcb-113">*хаппинстанце* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53bcb-113">*hAppInstance* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53bcb-114">Тип: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="53bcb-114">Type: **HINSTANCE**</span></span>

<span data-ttu-id="53bcb-115">Обработчик файла библиотеки, полученный в виде возвращаемого значения из [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("нетплвиз").</span><span class="sxs-lookup"><span data-stu-id="53bcb-115">A handle to the library file, obtained as a return value from [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)("netplwiz").</span></span>

</dd> <dt>

<span data-ttu-id="53bcb-116">*лпсзкмдлине* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53bcb-116">*lpszCmdLine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53bcb-117">Тип: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="53bcb-117">Type: **LPTSTR**</span></span>

<span data-ttu-id="53bcb-118">Данные аргумента.</span><span class="sxs-lookup"><span data-stu-id="53bcb-118">Argument data.</span></span> <span data-ttu-id="53bcb-119">Это значение всегда будет пустым.</span><span class="sxs-lookup"><span data-stu-id="53bcb-119">This value will always be empty.</span></span>

</dd> <dt>

<span data-ttu-id="53bcb-120">*нкмдшов* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53bcb-120">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53bcb-121">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="53bcb-121">Type: **int**</span></span>

<span data-ttu-id="53bcb-122">Задает режим просмотра для окна.</span><span class="sxs-lookup"><span data-stu-id="53bcb-122">Sets the display mode for the window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53bcb-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53bcb-123">Return value</span></span>

<span data-ttu-id="53bcb-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="53bcb-124">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="53bcb-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="53bcb-125">Remarks</span></span>

<span data-ttu-id="53bcb-126">Мастер паспорта используется для получения паспорта по умолчанию для Windows.</span><span class="sxs-lookup"><span data-stu-id="53bcb-126">The Passport Wizard is used to obtain a default Passport for Windows.</span></span> <span data-ttu-id="53bcb-127">Паспорт предоставляет пользователю персонализированный доступ ко всем веб-сайтам MSN и другим сайтам с поддержкой Passport, используя адрес электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="53bcb-127">A Passport gives the user personalized access to all MSN websites and other Passport-enabled sites using the user's email address.</span></span> <span data-ttu-id="53bcb-128">Использование **пасспортвизардрундлл** в качестве точки входа в файл Netplwiz.dll с помощью команды rundll32 позволяет запускать мастер паспорта из командной строки, как будто это исполняемый файл.</span><span class="sxs-lookup"><span data-stu-id="53bcb-128">Using **PassportWizardRunDll** as an entry point into the Netplwiz.dll file through a Rundll32 command allows you to launch the Passport Wizard from a command line as though it were an executable file.</span></span>

<span data-ttu-id="53bcb-129">**Пасспортвизардрундлл** используется исключительно в контексте Rundll32.exe команды следующим образом:</span><span class="sxs-lookup"><span data-stu-id="53bcb-129">**PassportWizardRunDll** is used solely in the context of a Rundll32.exe command as follows:</span></span>

<span data-ttu-id="53bcb-130">**rundll32.exe netplwiz.dll, Пасспортвизардрундлл**</span><span class="sxs-lookup"><span data-stu-id="53bcb-130">**rundll32.exe netplwiz.dll, PassportWizardRunDll**</span></span>

<span data-ttu-id="53bcb-131">Использование функции точки входа с Rundll32.exe не похоже на вызов обычной функции.</span><span class="sxs-lookup"><span data-stu-id="53bcb-131">Using an entry point function with Rundll32.exe does not resemble a normal function call.</span></span> <span data-ttu-id="53bcb-132">Имя функции и имя DLL-файла, где она хранится, используются только в качестве параметров командной строки.</span><span class="sxs-lookup"><span data-stu-id="53bcb-132">The function name and the name of the .dll file where it is stored are used only as command-line parameters.</span></span> <span data-ttu-id="53bcb-133">Определение функции, показанное в разделе синтаксис, является только стандартным прототипом для всех функций, которые можно вызывать с помощью rundll32.</span><span class="sxs-lookup"><span data-stu-id="53bcb-133">The function definition shown under Syntax is only a standard prototype for all functions that you can call using Rundll32.</span></span> <span data-ttu-id="53bcb-134">Определенные значения для *хвндстуб*, *хаппинстанце* и *нкмдшов* не предоставляются пользователем, но обрабатываются в фоновом режиме с помощью rundll32.</span><span class="sxs-lookup"><span data-stu-id="53bcb-134">The specific values for *hwndStub*, *hAppInstance*, and *nCmdShow* are not provided by the user, but are handled behind the scenes by Rundll32.</span></span> <span data-ttu-id="53bcb-135">**Пасспортвизардрундлл** не использует значение *лпсзкмдлине* , поэтому дополнительные данные не требуются.</span><span class="sxs-lookup"><span data-stu-id="53bcb-135">**PassportWizardRunDll** does not use the *lpszCmdLine* value, so no additional data is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="53bcb-136">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="53bcb-136">Requirements</span></span>



| <span data-ttu-id="53bcb-137">Требование</span><span class="sxs-lookup"><span data-stu-id="53bcb-137">Requirement</span></span> | <span data-ttu-id="53bcb-138">Значение</span><span class="sxs-lookup"><span data-stu-id="53bcb-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53bcb-139">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53bcb-139">Minimum supported client</span></span><br/> | <span data-ttu-id="53bcb-140">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="53bcb-140">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="53bcb-141">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53bcb-141">Minimum supported server</span></span><br/> | <span data-ttu-id="53bcb-142">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="53bcb-142">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="53bcb-143">Заголовок</span><span class="sxs-lookup"><span data-stu-id="53bcb-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="53bcb-144"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="53bcb-144"><dt>None</dt></span></span> </dl>                                 |
| <span data-ttu-id="53bcb-145">DLL</span><span class="sxs-lookup"><span data-stu-id="53bcb-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53bcb-146"><dt>Netplwiz.dll (версия 5,60 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="53bcb-146"><dt>Netplwiz.dll (version 5.60 or later)</dt></span></span> </dl> |



 

 
