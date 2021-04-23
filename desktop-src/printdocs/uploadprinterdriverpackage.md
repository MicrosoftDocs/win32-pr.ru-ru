---
description: Передает драйвер принтера в хранилище драйверов сервера печати, чтобы его можно было установить путем вызова Инсталлпринтердриверфромпаккаже.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: Функция Уплоадпринтердриверпаккаже (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272101"
---
# <a name="uploadprinterdriverpackage-function"></a><span data-ttu-id="bf673-103">Функция Уплоадпринтердриверпаккаже</span><span class="sxs-lookup"><span data-stu-id="bf673-103">UploadPrinterDriverPackage function</span></span>

<span data-ttu-id="bf673-104">Передает драйвер принтера в хранилище драйверов сервера печати, чтобы его можно было установить путем вызова [**инсталлпринтердриверфромпаккаже**](installprinterdriverfrompackage.md).</span><span class="sxs-lookup"><span data-stu-id="bf673-104">Uploads a printer driver to the print server's driver store so that it can be installed by calling [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bf673-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf673-105">Syntax</span></span>


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a><span data-ttu-id="bf673-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf673-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf673-107">*псзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf673-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf673-108">Указатель на константу, заканчивающуюся нулем строкой, которая указывает имя сервера печати.</span><span class="sxs-lookup"><span data-stu-id="bf673-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="bf673-109">Если сервер является локальным, используйте **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="bf673-109">Use **NULL** if the server is the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="bf673-110">*псзинфпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf673-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf673-111">Указатель на константу, заканчивающуюся нулем строкой, которая указывает исходный путь к INF-файлу драйвера.</span><span class="sxs-lookup"><span data-stu-id="bf673-111">A pointer to a constant ,null-terminated string that specifies the source path to the driver's .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="bf673-112">*псзенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf673-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf673-113">Указатель на константу, заканчивающуюся нулем строкой, которая указывает архитектуру процессора сервера (например, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="bf673-113">A pointer to a constant, null-terminated string that specifies the server's processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="bf673-114">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="bf673-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="bf673-115">*dwFlags* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf673-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf673-116">Это может быть любое из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="bf673-116">This can be any of the following values:</span></span>



| <span data-ttu-id="bf673-117">Значение</span><span class="sxs-lookup"><span data-stu-id="bf673-117">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="bf673-118">Значение</span><span class="sxs-lookup"><span data-stu-id="bf673-118">Meaning</span></span>                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <span data-ttu-id="bf673-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span><span class="sxs-lookup"><span data-stu-id="bf673-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span></span> </dl>             | <span data-ttu-id="bf673-120">Пользовательский интерфейс не будет отображаться во время отправки.</span><span class="sxs-lookup"><span data-stu-id="bf673-120">The UI will not be shown during the upload.</span></span><br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <span data-ttu-id="bf673-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span><span class="sxs-lookup"><span data-stu-id="bf673-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span></span> </dl>             | <span data-ttu-id="bf673-122">Файлы будут переданы, даже если пакет уже находится в хранилище драйверов сервера.</span><span class="sxs-lookup"><span data-stu-id="bf673-122">The files will be uploaded even if the package is already in the server's driver store.</span></span><br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <span data-ttu-id="bf673-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span><span class="sxs-lookup"><span data-stu-id="bf673-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span></span> </dl> | <span data-ttu-id="bf673-124">Хранилище драйверов сервера будет проверяться перед отправкой, чтобы узнать, существует ли уже пакет.</span><span class="sxs-lookup"><span data-stu-id="bf673-124">The server's driver store will be checked before upload to see if the package is already there.</span></span> <span data-ttu-id="bf673-125">Этот параметр игнорируется, если задан UPDP_UPLOAD_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="bf673-125">This setting is ignored if UPDP_UPLOAD_ALWAYS is set.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="bf673-126">*HWND* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="bf673-126">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf673-127">Маркер для копирования пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bf673-127">A handle to the copying user interface.</span></span>

</dd> <dt>

<span data-ttu-id="bf673-128">*псздестинфпас* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="bf673-128">*pszDestInfPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf673-129">Указатель на конечный путь в хранилище драйверов, в который был скопирован INF-файл драйвера.</span><span class="sxs-lookup"><span data-stu-id="bf673-129">A pointer to the destination path, in the driver store, to which the driver's .inf file was copied.</span></span>

</dd> <dt>

<span data-ttu-id="bf673-130">*пкчдестинфпас* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="bf673-130">*pcchDestInfPath* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf673-131">В поле входные данные задает размер буфера *псздестинфпас* в символах.</span><span class="sxs-lookup"><span data-stu-id="bf673-131">On input, specifies the size, in characters, of the *pszDestInfPath* buffer.</span></span> <span data-ttu-id="bf673-132">В выходных данных получает размер строки пути в символах, включая завершающий символ null.</span><span class="sxs-lookup"><span data-stu-id="bf673-132">On output, receives the size, in characters, of the path string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf673-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf673-133">Return value</span></span>

<span data-ttu-id="bf673-134">Если операция выполнена удачно, возвращаемое значение будет S_OK, в противном случае **HRESULT** будет содержать код ошибки.</span><span class="sxs-lookup"><span data-stu-id="bf673-134">If the operation succeeds, the return value is S_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="bf673-135">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="bf673-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bf673-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf673-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="bf673-137">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="bf673-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="bf673-138">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="bf673-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="bf673-139">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="bf673-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="bf673-140">Хранилище драйверов обычно имеет значение% WINDIR% \\ INF или% WINDIR% \\ system32 \\ дриверсторе \\ филерепоситори.</span><span class="sxs-lookup"><span data-stu-id="bf673-140">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="bf673-141">Можно отправить только один пакет за раз.</span><span class="sxs-lookup"><span data-stu-id="bf673-141">Only one package at a time can be uploaded.</span></span> <span data-ttu-id="bf673-142">Если пакет зависит от других, он должен быть отправлен отдельно.</span><span class="sxs-lookup"><span data-stu-id="bf673-142">If a package is dependent on others, they must be uploaded separately.</span></span>

<span data-ttu-id="bf673-143">Можно отправлять только подписанные пакеты драйверов.</span><span class="sxs-lookup"><span data-stu-id="bf673-143">Only signed driver packages can be uploaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf673-144">Требования</span><span class="sxs-lookup"><span data-stu-id="bf673-144">Requirements</span></span>



| <span data-ttu-id="bf673-145">Требование</span><span class="sxs-lookup"><span data-stu-id="bf673-145">Requirement</span></span> | <span data-ttu-id="bf673-146">Значение</span><span class="sxs-lookup"><span data-stu-id="bf673-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf673-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bf673-147">Minimum supported client</span></span><br/> | <span data-ttu-id="bf673-148">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bf673-148">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="bf673-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bf673-149">Minimum supported server</span></span><br/> | <span data-ttu-id="bf673-150">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bf673-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="bf673-151">Header</span><span class="sxs-lookup"><span data-stu-id="bf673-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf673-152"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf673-152"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="bf673-153">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bf673-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf673-154"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf673-154"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="bf673-155">DLL</span><span class="sxs-lookup"><span data-stu-id="bf673-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf673-156"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf673-156"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="bf673-157">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="bf673-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="bf673-158">**Уплоадпринтердриверпаккажев** (Юникод) и **уплоадпринтердриверпаккажеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="bf673-158">**UploadPrinterDriverPackageW** (Unicode) and **UploadPrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="bf673-159">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bf673-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf673-160">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="bf673-160">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="bf673-161">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="bf673-161">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

