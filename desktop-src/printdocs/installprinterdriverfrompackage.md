---
description: Устанавливает драйвер принтера из пакета драйверов, который находится в хранилище драйверов сервера печати.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: Функция Инсталлпринтердриверфромпаккаже (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272484"
---
# <a name="installprinterdriverfrompackage-function"></a><span data-ttu-id="f9c7d-103">Функция Инсталлпринтердриверфромпаккаже</span><span class="sxs-lookup"><span data-stu-id="f9c7d-103">InstallPrinterDriverFromPackage function</span></span>

<span data-ttu-id="f9c7d-104">Устанавливает драйвер принтера из пакета драйверов, который находится в хранилище драйверов сервера печати.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-104">Installs a printer driver from a driver package that is in the print server's driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9c7d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9c7d-105">Syntax</span></span>


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f9c7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9c7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9c7d-107">*псзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9c7d-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c7d-108">Указатель на константу, заканчивающуюся нулем строкой, которая указывает имя сервера печати.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="f9c7d-109">**Значение NULL** означает локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-109">**NULL** means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="f9c7d-110">*псзинфпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9c7d-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c7d-111">Указатель на константу, заканчивающуюся нулем строкой, которая указывает путь к INF-файлу драйвера принтера для хранилища драйверов.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-111">A pointer to a constant, null-terminated string that specifies the driver store path to the print driver's .inf file.</span></span> <span data-ttu-id="f9c7d-112">**Значение NULL** означает, что драйвер находится в INF-файле, поставляемом вместе с Windows.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-112">**NULL** means the driver is in an inf file that shipped with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f9c7d-113">*псздривернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9c7d-113">*pszDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c7d-114">Указатель на константу, заканчивающуюся нулем строкой, которая указывает имя драйвера.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-114">A pointer to a constant, null-terminated string that specifies the name of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="f9c7d-115">*псзенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9c7d-115">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c7d-116">Указатель на константу, заканчивающуюся нулем строкой, которая указывает архитектуру процессора (например, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="f9c7d-116">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="f9c7d-117">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-117">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f9c7d-118">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f9c7d-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9c7d-119">Это может быть только 0 или ИПДФП \_ Копировать \_ все \_ файлы.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-119">This can only be 0 or IPDFP\_COPY\_ALL\_FILES.</span></span> <span data-ttu-id="f9c7d-120">Значение 0 означает, что драйвер принтера должен быть добавлен, и все файлы в каталоге драйвера принтера, имеющие более новую версию, чем соответствующие файлы, используемые в данный момент, должны быть скопированы.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-120">A value of 0 means that the printer driver must be added and any files in the printer driver directory that are newer than corresponding files currently in use must be copied.</span></span> <span data-ttu-id="f9c7d-121">Значение ИПДФП \_ Copy \_ All \_ Files означает, что необходимо добавить драйвер принтера и все файлы в каталоге драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-121">A value of IPDFP\_COPY\_ALL\_FILES means the printer driver and all the files in the printer driver directory must be added.</span></span> <span data-ttu-id="f9c7d-122">Метки времени файла игнорируются, если *dwFlags* имеет значение ипдфп \_ Copy \_ All \_ Files.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-122">The file time stamps are ignored when *dwFlags* has a value of IPDFP\_COPY\_ALL\_FILES.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9c7d-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9c7d-123">Return value</span></span>

<span data-ttu-id="f9c7d-124">Если операция выполнена успешно, возвращается значение S \_ ОК, в противном случае **HRESULT** будет содержать код ошибки.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-124">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="f9c7d-125">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="f9c7d-125">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9c7d-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9c7d-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f9c7d-127">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="f9c7d-128">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="f9c7d-129">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="f9c7d-130">Хранилище драйверов обычно имеет значение% WINDIR% \\ INF или% WINDIR% \\ system32 \\ дриверсторе \\ филерепоситори.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-130">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="f9c7d-131">**Инсталлпринтердриверфромпаккаже** также устанавливает другие файлы в пакете, например цветовые профили и обработчики печати.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-131">**InstallPrinterDriverFromPackage** also installs other files in the package, such as color profiles and print processors.</span></span>

<span data-ttu-id="f9c7d-132">Пользователи должны иметь права администратора принтера для установки на удаленном компьютере или на локальном компьютере при входе пользователя в систему с помощью служб терминалов.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-132">Users must have printer administration rights to install either on a remote computer or on the local computer when the user is logged in with Terminal Services.</span></span>

<span data-ttu-id="f9c7d-133">На удаленном компьютере можно установить только подписанные пакеты.</span><span class="sxs-lookup"><span data-stu-id="f9c7d-133">Only signed packages can be installed on a remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9c7d-134">Требования</span><span class="sxs-lookup"><span data-stu-id="f9c7d-134">Requirements</span></span>



| <span data-ttu-id="f9c7d-135">Требование</span><span class="sxs-lookup"><span data-stu-id="f9c7d-135">Requirement</span></span> | <span data-ttu-id="f9c7d-136">Значение</span><span class="sxs-lookup"><span data-stu-id="f9c7d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9c7d-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9c7d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f9c7d-138">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f9c7d-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f9c7d-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9c7d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f9c7d-140">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f9c7d-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f9c7d-141">Header</span><span class="sxs-lookup"><span data-stu-id="f9c7d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9c7d-142"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f9c7d-142"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="f9c7d-143">Библиотека</span><span class="sxs-lookup"><span data-stu-id="f9c7d-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="f9c7d-144"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9c7d-144"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="f9c7d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f9c7d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9c7d-146"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9c7d-146"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="f9c7d-147">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="f9c7d-147">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="f9c7d-148">**Инсталлпринтердриверфромпаккажев** (Юникод) и **инсталлпринтердриверфромпаккажеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="f9c7d-148">**InstallPrinterDriverFromPackageW** (Unicode) and **InstallPrinterDriverFromPackageA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9c7d-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f9c7d-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c7d-150">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="f9c7d-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f9c7d-151">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="f9c7d-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

