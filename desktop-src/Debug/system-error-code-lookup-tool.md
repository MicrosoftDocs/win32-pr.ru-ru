---
description: Описание использования средства Microsoft Error Lookup для поиска текстовых объяснений шестнадцатеричных кодов ошибок в Windows.
title: Средство поиска ошибок (Майкрософт)
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105719256"
---
# <a name="the-microsoft-error-lookup-tool"></a><span data-ttu-id="3ae89-103">Средство поиска ошибок (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="3ae89-103">The Microsoft Error Lookup Tool</span></span>

<span data-ttu-id="3ae89-104">Средство поиска ошибок (Майкрософт) отображает текст сообщения, связанного с шестнадцатеричным кодом состояния (или другим кодом).</span><span class="sxs-lookup"><span data-stu-id="3ae89-104">The Microsoft Error Lookup Tool displays the message text that is associated with a hexadecimal status code (or other code).</span></span> <span data-ttu-id="3ae89-105">Этот текст определен в различных файлах заголовков исходного кода Майкрософт, таких как Winerror. h, Setupapi. h и т. д.</span><span class="sxs-lookup"><span data-stu-id="3ae89-105">This text is defined in various Microsoft source-code header files, such as Winerror.h, Setupapi.h, and so on.</span></span>

<span data-ttu-id="3ae89-106">Средство подписано цифровой подписью корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="3ae89-106">The tool is digitally signed by Microsoft.</span></span> <span data-ttu-id="3ae89-107">Ниже приведены сведения о SHA256 для скачивания файла.</span><span class="sxs-lookup"><span data-stu-id="3ae89-107">The following is the SHA256 information for the file download:</span></span>  

|<span data-ttu-id="3ae89-108">Алгоритм</span><span class="sxs-lookup"><span data-stu-id="3ae89-108">Algorithm</span></span> |<span data-ttu-id="3ae89-109">Хэш</span><span class="sxs-lookup"><span data-stu-id="3ae89-109">Hash</span></span> |
| --- | --- |
|<span data-ttu-id="3ae89-110">SHA256</span><span class="sxs-lookup"><span data-stu-id="3ae89-110">SHA256</span></span> |<span data-ttu-id="3ae89-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span><span class="sxs-lookup"><span data-stu-id="3ae89-111">88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A</span></span> |

> [!NOTE]
> <span data-ttu-id="3ae89-112">Бизнес-среды могут ограничивать, какие файлы могут выполняться и откуда.</span><span class="sxs-lookup"><span data-stu-id="3ae89-112">Business environments may restrict which files can run and from where.</span></span> <span data-ttu-id="3ae89-113">Перед загрузкой и запуском этого средства ознакомьтесь со следующими сведениями:</span><span class="sxs-lookup"><span data-stu-id="3ae89-113">Before you download and run this tool, check the following details:</span></span>
> - <span data-ttu-id="3ae89-114">Требуется ли разрешение или исключение безопасности для загрузки или запуска средства?</span><span class="sxs-lookup"><span data-stu-id="3ae89-114">Do you have to have permission or a security exception in order to download or run the tool?</span></span>
> - <span data-ttu-id="3ae89-115">Можно ли хранить и запускать этот инструмент на компьютере (например, в папке "документы")?</span><span class="sxs-lookup"><span data-stu-id="3ae89-115">Can you store and run this tool on your computer (for example, in your Documents folder)?</span></span> <span data-ttu-id="3ae89-116">Или необходимо сохранить и запустить средство на специализированном компьютере, например на центральном файловом сервере?</span><span class="sxs-lookup"><span data-stu-id="3ae89-116">Or do you have to store and run the tool on a specialized computer, such as a central file server?</span></span>

## <a name="usage"></a><span data-ttu-id="3ae89-117">Использование</span><span class="sxs-lookup"><span data-stu-id="3ae89-117">Usage</span></span>

1. <span data-ttu-id="3ae89-118">Скачайте средство, щелкнув [эту ссылку](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span><span class="sxs-lookup"><span data-stu-id="3ae89-118">Download the tool by selecting [this link](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).</span></span>
1. <span data-ttu-id="3ae89-119">Если вы не указали расположение на шаге 1, перейдите в папку загрузки и скопируйте или переместите скачанный файл (Err_6.4.5.exe) в папку, в которой будет храниться средство.</span><span class="sxs-lookup"><span data-stu-id="3ae89-119">If you didn't specify a location in step 1, go to your download folder, and copy or move the downloaded file (Err_6.4.5.exe) to folder in which you will store the tool.</span></span> <span data-ttu-id="3ae89-120">Не нужно расширять или устанавливать этот файл.</span><span class="sxs-lookup"><span data-stu-id="3ae89-120">You do not have to expand or install the file.</span></span>
   > [!NOTE]
   > <span data-ttu-id="3ae89-121">При копировании или перемещении файла в папку, указанную в переменной среды **path** операционной системы, она будет работать в любой командной строке.</span><span class="sxs-lookup"><span data-stu-id="3ae89-121">If you copy or move the file to a folder that is listed in your operating system's **Path** environment variable, it will work at any command prompt.</span></span>

1. <span data-ttu-id="3ae89-122">Откройте окно командной строки и</span><span class="sxs-lookup"><span data-stu-id="3ae89-122">Open a Command Prompt window.</span></span> <span data-ttu-id="3ae89-123">При необходимости измените каталог на расположение средства поиска ошибок.</span><span class="sxs-lookup"><span data-stu-id="3ae89-123">If necessary, change the directory to the location of the Error Lookup Tool.</span></span>
1. <span data-ttu-id="3ae89-124">Выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="3ae89-124">Run the following command:</span></span>
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > <span data-ttu-id="3ae89-125">В этой команде \<*error code*> представляет шестнадцатеричный код, который требуется найти.</span><span class="sxs-lookup"><span data-stu-id="3ae89-125">In this command, \<*error code*> represents the hexadecimal code that you want to look up.</span></span>

## <a name="examples"></a><span data-ttu-id="3ae89-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="3ae89-126">Examples</span></span>

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a><span data-ttu-id="3ae89-127">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="3ae89-127">More information</span></span>

<span data-ttu-id="3ae89-128">Помните, что это средство «точка во времени».</span><span class="sxs-lookup"><span data-stu-id="3ae89-128">Keep in mind that this is a "point-in-time" tool.</span></span> <span data-ttu-id="3ae89-129">Средство поиска ошибок (Майкрософт) декодирует большинство кодов ошибок Майкрософт на дату компиляции инструмента.</span><span class="sxs-lookup"><span data-stu-id="3ae89-129">The Microsoft Error Lookup Tool decodes most Microsoft error codes as of the date on which the tool was compiled.</span></span> <span data-ttu-id="3ae89-130">Новые выпуски Windows добавляют новые коды событий и ошибок, поэтому может потребоваться Скачать новую версию средства поиска ошибок.</span><span class="sxs-lookup"><span data-stu-id="3ae89-130">As new releases of Windows add new event and error codes, you may have to download a new version of the Error Lookup Tool.</span></span> <span data-ttu-id="3ae89-131">Проверьте наличие новой версии в центре загрузки Майкрософт или просмотрите [коды ошибок](system-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3ae89-131">Check the Microsoft Download Center for a new version, or see [Error Codes](system-error-codes.md).</span></span>
