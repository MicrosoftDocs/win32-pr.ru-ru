---
title: Общие функции (Windows Internet)
description: Различные протоколы Интернета (например, FTP и HTTP) используют несколько функций WinINet для работы с информацией в Интернете.
ms.assetid: c80768cf-c8c0-4bdf-9ea2-f82c92ade05a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1893b085da1b3e77228e4a9abf75acc166d84726
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105710417"
---
# <a name="common-functions-windows-internet"></a><span data-ttu-id="26843-103">Общие функции (Windows Internet)</span><span class="sxs-lookup"><span data-stu-id="26843-103">Common Functions (Windows Internet)</span></span>

<span data-ttu-id="26843-104">Различные протоколы Интернета (например, FTP и HTTP) используют несколько функций WinINet для работы с информацией в Интернете.</span><span class="sxs-lookup"><span data-stu-id="26843-104">The different Internet protocols (such as ftp and http) use several of the same WinINet functions to handle information on the Internet.</span></span> <span data-ttu-id="26843-105">Эти общие функции обрабатывают свои задачи согласованно, независимо от конкретного протокола, к которому они применяются.</span><span class="sxs-lookup"><span data-stu-id="26843-105">These common functions handle their tasks in a consistent manner, regardless of the particular protocol to which they are being applied.</span></span> <span data-ttu-id="26843-106">Приложения могут использовать эти функции для создания функций общего назначения, обрабатывающих задачи в различных протоколах (например, чтение файлов для FTP и HTTP).</span><span class="sxs-lookup"><span data-stu-id="26843-106">Applications can use these functions to create general-purpose functions that handle tasks across the different protocols (such as reading files for ftp and http).</span></span>

<span data-ttu-id="26843-107">Общие функции обрабатывали следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="26843-107">The common functions handle the following tasks:</span></span>

-   <span data-ttu-id="26843-108">Загрузка ресурсов из Интернета ([**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**интернетсетфилепоинтер**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)и [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span><span class="sxs-lookup"><span data-stu-id="26843-108">Downloading resources from the Internet ([**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile), [**InternetSetFilePointer**](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer), [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), and [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable)).</span></span>
-   <span data-ttu-id="26843-109">Настройка асинхронных операций ([**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span><span class="sxs-lookup"><span data-stu-id="26843-109">Setting up asynchronous operations ([**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)).</span></span>
-   <span data-ttu-id="26843-110">Просмотр и изменение параметров ([**интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) и [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span><span class="sxs-lookup"><span data-stu-id="26843-110">Viewing and changing options ([**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)).</span></span>
-   <span data-ttu-id="26843-111">Закрытие всех типов дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) ([**интернетклосехандле**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span><span class="sxs-lookup"><span data-stu-id="26843-111">Closing all types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles ([**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle)).</span></span>
-   <span data-ttu-id="26843-112">Размещение и удаление блокировок ресурсов ([**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) и [**интернетунлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span><span class="sxs-lookup"><span data-stu-id="26843-112">Placing and removing locks on resources ([**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) and [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)).</span></span>

## <a name="using-common-functions"></a><span data-ttu-id="26843-113">Использование общих функций</span><span class="sxs-lookup"><span data-stu-id="26843-113">Using Common Functions</span></span>

<span data-ttu-id="26843-114">В следующей таблице перечислены общие функции, входящие в функции WinINet.</span><span class="sxs-lookup"><span data-stu-id="26843-114">The following table lists the common functions included in the WinINet functions.</span></span> <span data-ttu-id="26843-115">Общие функции могут использоваться для различных типов дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) или использоваться во время различных типов сеансов.</span><span class="sxs-lookup"><span data-stu-id="26843-115">The common functions can be used on different types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles or can be used during different types of sessions.</span></span>



| <span data-ttu-id="26843-116">Функция</span><span class="sxs-lookup"><span data-stu-id="26843-116">Function</span></span>                                                         | <span data-ttu-id="26843-117">Описание</span><span class="sxs-lookup"><span data-stu-id="26843-117">Description</span></span>                                                                                                                                                                                                                                             |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26843-118">**интернетфинднекстфиле**</span><span class="sxs-lookup"><span data-stu-id="26843-118">**InternetFindNextFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)             | <span data-ttu-id="26843-119">Продолжит перечисление файлов или поиск.</span><span class="sxs-lookup"><span data-stu-id="26843-119">Continues file enumeration or search.</span></span> <span data-ttu-id="26843-120">Требуется обработчик, созданный функцией [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="26843-120">Requires a handle created by the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span>                                                                            |
| [<span data-ttu-id="26843-121">**интернетлоккрекуестфиле**</span><span class="sxs-lookup"><span data-stu-id="26843-121">**InternetLockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile)       | <span data-ttu-id="26843-122">Позволяет пользователю поместить блокировку на используемый файл.</span><span class="sxs-lookup"><span data-stu-id="26843-122">Allows the user to place a lock on the file that is being used.</span></span> <span data-ttu-id="26843-123">Для этой функции требуется маркер, возвращенный функцией [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="26843-123">This function requires a handle returned by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> |
| [<span data-ttu-id="26843-124">**интернеткуеридатааваилабле**</span><span class="sxs-lookup"><span data-stu-id="26843-124">**InternetQueryDataAvailable**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) | <span data-ttu-id="26843-125">Получает доступный объем данных.</span><span class="sxs-lookup"><span data-stu-id="26843-125">Retrieves the amount of data available.</span></span> <span data-ttu-id="26843-126">Требуется обработчик, созданный функцией [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="26843-126">Requires a handle created by the [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                                    |
| [<span data-ttu-id="26843-127">**интернеткуерйоптион**</span><span class="sxs-lookup"><span data-stu-id="26843-127">**InternetQueryOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona)               | <span data-ttu-id="26843-128">Возвращает значение параметра Интернета.</span><span class="sxs-lookup"><span data-stu-id="26843-128">Retrieves the setting of an Internet option.</span></span>                                                                                                                                                                                                            |
| [<span data-ttu-id="26843-129">**интернетреадфиле**</span><span class="sxs-lookup"><span data-stu-id="26843-129">**InternetReadFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)                     | <span data-ttu-id="26843-130">Считывает данные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="26843-130">Reads URL data.</span></span> <span data-ttu-id="26843-131">Требуется обработчик, созданный функцией [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="26843-131">Requires a handle created by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>                                                                |
| [<span data-ttu-id="26843-132">**интернетсетфилепоинтер**</span><span class="sxs-lookup"><span data-stu-id="26843-132">**InternetSetFilePointer**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetfilepointer)         | <span data-ttu-id="26843-133">Задает расположение следующего считывания в файле.</span><span class="sxs-lookup"><span data-stu-id="26843-133">Sets the position for the next read in a file.</span></span> <span data-ttu-id="26843-134">Требуется обработчик, созданный [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (только для URL-адреса HTTP) или созданный с помощью [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) токен с помощью команды GET HTTP.</span><span class="sxs-lookup"><span data-stu-id="26843-134">Requires a handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (on an HTTP URL only) or a handle created by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) using the GET HTTP verb.</span></span>                 |
| [<span data-ttu-id="26843-135">**интернетсетоптион**</span><span class="sxs-lookup"><span data-stu-id="26843-135">**InternetSetOption**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona)                   | <span data-ttu-id="26843-136">Задает параметр Интернета.</span><span class="sxs-lookup"><span data-stu-id="26843-136">Sets an Internet option.</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="26843-137">**интернетсетстатускаллбакк**</span><span class="sxs-lookup"><span data-stu-id="26843-137">**InternetSetStatusCallback**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback)   | <span data-ttu-id="26843-138">Задает функцию обратного вызова, которая получает сведения о состоянии.</span><span class="sxs-lookup"><span data-stu-id="26843-138">Sets a callback function that receives status information.</span></span> <span data-ttu-id="26843-139">Присваивает функцию обратного вызова назначенному дескриптору [**хинтернет**](appendix-a-hinternet-handles.md) и всем дескрипторам, производным от него.</span><span class="sxs-lookup"><span data-stu-id="26843-139">Assigns a callback function to the designated [**HINTERNET**](appendix-a-hinternet-handles.md) handle and all handles derived from it.</span></span>                                                      |
| [<span data-ttu-id="26843-140">**интернетунлоккрекуестфиле**</span><span class="sxs-lookup"><span data-stu-id="26843-140">**InternetUnlockRequestFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile)   | <span data-ttu-id="26843-141">Разблокирует файл, который был заблокирован с помощью функции [**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) .</span><span class="sxs-lookup"><span data-stu-id="26843-141">Unlocks a file that was locked using the [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function.</span></span>                                                                                                                                           |



 

<span data-ttu-id="26843-142">Чтение файлов, поиск следующего файла, Управление параметрами и настройка асинхронных операций являются общими для функций, поддерживающих различные протоколы и типы обработки [**хинтернет**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="26843-142">Reading files, finding the next file, manipulating options, and setting up asynchronous operations are common to the functions that support various protocols and [**HINTERNET**](appendix-a-hinternet-handles.md) handle types.</span></span>

### <a name="reading-files"></a><span data-ttu-id="26843-143">Чтение файлов</span><span class="sxs-lookup"><span data-stu-id="26843-143">Reading Files</span></span>

<span data-ttu-id="26843-144">Функция [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) используется для загрузки ресурсов из [**хинтернет**](appendix-a-hinternet-handles.md) -маркера, возвращаемого функцией [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="26843-144">The [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function is used to download resources from an [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function.</span></span>

<span data-ttu-id="26843-145">[**Интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) принимает переменную указателя void, содержащую адрес буфера, и указатель на переменную, содержащую длину буфера.</span><span class="sxs-lookup"><span data-stu-id="26843-145">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) accepts a void pointer variable that contains the address of a buffer and a pointer to a variable that contains the length of the buffer.</span></span> <span data-ttu-id="26843-146">Функция возвращает данные в буфере и объем данных, загружаемых в буфер.</span><span class="sxs-lookup"><span data-stu-id="26843-146">The function returns the data in the buffer and the amount of data downloaded into the buffer.</span></span>

<span data-ttu-id="26843-147">Функции WinINet предоставляют два метода загрузки всего ресурса:</span><span class="sxs-lookup"><span data-stu-id="26843-147">The WinINet functions provide two techniques to download an entire resource:</span></span>

-   <span data-ttu-id="26843-148">Функция [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) .</span><span class="sxs-lookup"><span data-stu-id="26843-148">The [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) function.</span></span>
-   <span data-ttu-id="26843-149">Возвращаемые значения [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="26843-149">The return values of [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>

<span data-ttu-id="26843-150">[**Интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) принимает маркер [**Хинтернет**](appendix-a-hinternet-handles.md) , созданный [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (после вызова [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) в обработчике), и возвращает количество доступных байтов.</span><span class="sxs-lookup"><span data-stu-id="26843-150">[**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) takes the [**HINTERNET**](appendix-a-hinternet-handles.md) handle created by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) has been called on the handle) and returns the number of bytes available.</span></span> <span data-ttu-id="26843-151">Приложение должно выделить буфер, равный количеству доступных байтов, плюс 1 для завершающего **нуль** -символа и использовать этот буфер с [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="26843-151">The application should allocate a buffer equal to the number of bytes available, plus 1 for the terminating **null** character, and use that buffer with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span> <span data-ttu-id="26843-152">Этот метод не всегда работает, так как [**интернеткуеридатааваилабле**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) проверяет размер файла, указанного в заголовке, а не на сам файл.</span><span class="sxs-lookup"><span data-stu-id="26843-152">This method does not always work because [**InternetQueryDataAvailable**](/windows/desktop/api/Wininet/nf-wininet-internetquerydataavailable) is checking the file size listed in the header and not the actual file.</span></span> <span data-ttu-id="26843-153">Сведения в файле заголовка могут быть устаревшими, или файл заголовка может отсутствовать, поскольку в настоящее время он не требуется для всех стандартов.</span><span class="sxs-lookup"><span data-stu-id="26843-153">The information in the header file could be outdated, or the header file could be missing, since it is not currently required under all standards.</span></span>

<span data-ttu-id="26843-154">В следующем примере считывается содержимое ресурса, к которому обращается обработчик Хресаурце, и отображается в поле ввода, указанном параметром Интктрлид.</span><span class="sxs-lookup"><span data-stu-id="26843-154">The following example reads the contents of the resource accessed by the hResource handle and displayed in the edit box indicated by intCtrlID.</span></span>


```C++
int WINAPI Dumper(HWND hX, int intCtrlID, HINTERNET hResource)
{
    LPTSTR    lpszData;           // buffer for the data
    DWORD     dwSize;             // size of the data available
    DWORD     dwDownloaded;       // size of the downloaded data
    DWORD     dwSizeSum=0;        // size of the data in the text box
    LPTSTR    lpszHolding;        // buffer to merge the text box 
                                  // data and buffer

    // Set the cursor to an hourglass.
    SetCursor(LoadCursor(NULL,IDC_WAIT));

    // This loop handles reading the data.  
    do
    {
        // The call to InternetQueryDataAvailable determines the
        // amount of data available to download.
        if (!InternetQueryDataAvailable(hResource,&dwSize,0,0))
        {
            ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
            SetCursor(LoadCursor(NULL,IDC_ARROW));
            return FALSE;
        }
        else
        {    
            // Allocate a buffer of the size returned by
            // InternetQueryDataAvailable.
            lpszData = new TCHAR[dwSize+1];

            // Read the data from the HINTERNET handle.
            if(!InternetReadFile(hResource,(LPVOID)lpszData,
                                 dwSize,&dwDownloaded))
            {
                ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
                delete[] lpszData;
                break;
            }
            else
            {
                // Add a null terminator to the end of the 
                // data buffer.
                lpszData[dwDownloaded]='\0';

                // Allocate the holding buffer.
                lpszHolding = new TCHAR[dwSizeSum + dwDownloaded + 1];
                    
                // Check if there has been any data written to 
                // the text box.
                if (dwSizeSum != 0)
                {
                    // Retrieve the data stored in the text 
                    // box, if any.
                    GetDlgItemText(hX,intCtrlID,
                                   (LPTSTR)lpszHolding, 
                                   dwSizeSum);
                         
                    // Add a null terminator at the end of 
                    // the text box data.
                    lpszHolding[dwSizeSum]='\0';
                }
                else
                {
                    // Make the holding buffer an empty string. 
                    lpszHolding[0]='\0';
                }

                size_t cchDest = dwSizeSum + dwDownloaded + 
                                 dwDownloaded + 1;
                LPTSTR pszDestEnd;
                size_t cchRemaining;

                // Add the new data to the holding buffer.
                HRESULT hr = StringCchCatEx(lpszHolding, cchDest, 
                                            lpszData, &pszDestEnd, 
                                            &cchRemaining, 
                                            STRSAFE_NO_TRUNCATION);
                if(SUCCEEDED(hr))
                {
                    // Write the holding buffer to the text box.
                    SetDlgItemText(hX,intCtrlID,(LPTSTR)lpszHolding);

                    // Delete the two buffers.
                    delete[] lpszHolding;
                    delete[] lpszData;

                    // Add the size of the downloaded data to 
                    // the text box data size.
                    dwSizeSum = dwSizeSum + dwDownloaded + 1;

                    // Check the size of the remaining data.  
                    // If it is zero, break.
                    if (dwDownloaded == 0)
                    {
                        break;
                    }                    
                    else
                    {
                        //  Insert error handling code here.
                    }
                }
            }
        }
    }
    while(TRUE);

    // Close the HINTERNET handle.
    InternetCloseHandle(hResource);

    // Set the cursor back to an arrow.
    SetCursor(LoadCursor(NULL,IDC_ARROW));

    // Return.
    return TRUE;
}
```



<span data-ttu-id="26843-155">[**Интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) возвращает нулевые байты для чтения и завершения после считывания всех доступных данных.</span><span class="sxs-lookup"><span data-stu-id="26843-155">[**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) returns zero bytes read and completes successfully when all available data has been read.</span></span> <span data-ttu-id="26843-156">Это позволяет приложению использовать [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) в цикле для загрузки данных и выхода, когда оно возвращает нулевые байты, прочитанные и завершенные успешно.</span><span class="sxs-lookup"><span data-stu-id="26843-156">This allows an application to use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) in a loop to download the data and exit when it returns zero bytes read and completes successfully.</span></span>

<span data-ttu-id="26843-157">Следующий пример считывает ресурс из Интернета и отображает ресурс в поле ввода, указанном параметром Интктрлид.</span><span class="sxs-lookup"><span data-stu-id="26843-157">The following example reads the resource from the Internet and displays the resource in the edit box indicated by intCtrlID.</span></span> <span data-ttu-id="26843-158">[**Интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)или [**хттпопенрекуест**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) вернула [**хинтернет**](appendix-a-hinternet-handles.md) [**-маркер**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta), хинтернет.</span><span class="sxs-lookup"><span data-stu-id="26843-158">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hInternet, was returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) (after being sent by [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta)).</span></span>


```C++
int WINAPI Dump(HWND hX, int intCtrlID, HINTERNET hResource)
{
     DWORD dwSize = 0;
     LPTSTR lpszData;
     LPTSTR lpszOutPut;
     LPTSTR lpszHolding = TEXT("");
     int nCounter = 1;
     int nBufferSize = 0;
     DWORD BigSize = 8000;

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Begin the loop that reads the data.
     do
     {
          // Allocate the buffer.
          lpszData =new TCHAR[BigSize+1];

          // Read the data.
          if(!InternetReadFile(hResource,
                              (LPVOID)lpszData,
                              BigSize,&dwSize))
          {
               ErrorOut(hX,GetLastError(),TEXT("InternetReadFile"));
               delete []lpszData;
               break;
          }
          else
          {
               // Add a null terminator to the end of the buffer.
               lpszData[dwSize]='\0';

               // Check if all of the data has been read.  This should
               // never get called on the first time through the loop.
               if (dwSize == 0)
               {
                    // Write the final data to the text box.
                    SetDlgItemText(hX,intCtrlID,lpszHolding);

                    // Delete the existing buffers.
                    delete [] lpszData;
                    delete [] lpszHolding;
                    break;
               }

               // Determine the buffer size to hold the new data and
               // the data already written to the text box (if any).
               nBufferSize = (nCounter*BigSize)+1;

               // Increment the number of buffers read.
               nCounter++;               

               // Allocate the output buffer.
               lpszOutPut = new TCHAR[nBufferSize];

               // Make sure the buffer is not the initial buffer.
               if(nBufferSize != int(BigSize+1))
               {
                    // Copy the data in the holding buffer.
                    StringCchCopy(lpszOutPut,nBufferSize,lpszHolding);
                    // Add error handling code here.

                    // Concatenate the new buffer with the 
                    // output buffer.
                    StringCchCat(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
     
                    // Delete the holding buffer.
                    delete [] lpszHolding;
               }
               else
               {
                    // Copy the data buffer.
                    StringCchCopy(lpszOutPut, nBufferSize, lpszData);
                    // Add error handling code here.
               }

               // Allocate a holding buffer.
               lpszHolding = new TCHAR[nBufferSize]; 

               // Copy the output buffer into the holding buffer.
               memcpy(lpszHolding,lpszOutPut,nBufferSize);

               // Delete the other buffers.
               delete [] lpszData;
               delete [] lpszOutPut;

          }

     }
     while (TRUE);

     // Close the HINTERNET handle.
     InternetCloseHandle(hResource);

     // Set the cursor back to an arrow.
     SetCursor(LoadCursor(NULL,IDC_ARROW));

     // Return.
     return TRUE;
}
```



### <a name="finding-the-next-file"></a><span data-ttu-id="26843-159">Поиск следующего файла</span><span class="sxs-lookup"><span data-stu-id="26843-159">Finding the Next File</span></span>

<span data-ttu-id="26843-160">Функция [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) используется для поиска следующего файла в поиске файла с помощью параметров поиска и [**хинтернетного**](appendix-a-hinternet-handles.md) маркера из [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="26843-160">The [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) function is used to find the next file in a file search, using the search parameters and [**HINTERNET**](appendix-a-hinternet-handles.md) handle from [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="26843-161">Чтобы завершить поиск файла, продолжайте вызывать [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) с помощью маркера [**хинтернет**](appendix-a-hinternet-handles.md) , возвращенного [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), или [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) до тех пор, пока функция не завершится с ошибкой расширенного сообщения об ошибке, больше [ \_ нет \_ \_ файлов](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="26843-161">To complete a file search, continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) using the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), or [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) until the function fails with the extended error message [ERROR\_NO\_MORE\_FILES](wininet-errors.md).</span></span> <span data-ttu-id="26843-162">Чтобы получить расширенные сведения об ошибке, вызовите функцию [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="26843-162">To get the extended error information, call the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

<span data-ttu-id="26843-163">В следующем примере показано содержимое FTP-каталога в списке, указанном параметром Лстдиректори.</span><span class="sxs-lookup"><span data-stu-id="26843-163">The following example displays the contents of an FTP directory in the list box indicated by lstDirectory.</span></span> <span data-ttu-id="26843-164">Обработчик [**хинтернет**](appendix-a-hinternet-handles.md) , хконнект, возвращается функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после того, как она устанавливает сеанс FTP.</span><span class="sxs-lookup"><span data-stu-id="26843-164">The [**HINTERNET**](appendix-a-hinternet-handles.md) handle, hConnect, is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span>


```C++
bool WINAPI DisplayDir( HWND hX, 
                        int lstDirectory, 
                        HINTERNET hConnect, 
                        DWORD dwFlag )
{
     WIN32_FIND_DATA pDirInfo;
     HINTERNET hDir;
     TCHAR DirList[MAX_PATH];

     // Set the cursor to an hourglass.
     SetCursor(LoadCursor(NULL,IDC_WAIT));

     // Reset the list box.
     SendDlgItemMessage(hX, lstDirectory,LB_RESETCONTENT,0,0);

     // Find the first file.
     hDir = FtpFindFirstFile (hConnect, TEXT ("*.*"), 
                              &pDirInfo, dwFlag, 0);
     if (!hDir)                                     
     {
          // Check if the error was because there were no files.
          if (GetLastError()  == ERROR_NO_MORE_FILES) 
          {
               // Alert user.
               MessageBox(hX, TEXT("There are no files here!!!"), 
                          TEXT("Display Dir"), MB_OK);

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return TRUE;
          }
          else 
          {
               // Call error handler.
               ErrorOut (hX, GetLastError (), TEXT("FindFirst error: "));

               // Close the HINTERNET handle.
               InternetCloseHandle(hDir);

               // Set the cursor back to an arrow.
               SetCursor(LoadCursor(NULL,IDC_ARROW));

               // Return.
               return FALSE;
          }
     }
     else
     {
          // Write the file name to a string.
          StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

          // Check the type of file.
          if (pDirInfo.dwFileAttributes == FILE_ATTRIBUTE_DIRECTORY)
          {
               // Add <DIR> to indicate that this is 
               // a directory to the user.
               StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
               // Add error handling code here.
          }
       
          // Add the file name (or directory) to the list box.
          SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                             0, (LPARAM)DirList);
     }
     do
     {
          // Find the next file.
          if (!InternetFindNextFile (hDir, &pDirInfo))
          {
               // Check if there are no more files left. 
               if ( GetLastError() == ERROR_NO_MORE_FILES ) 
               {
                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return TRUE;
               }
               else
               {   
                    // Handle the error.
                    ErrorOut (hX, GetLastError(), 
                              TEXT("InternetFindNextFile"));

                    // Close the HINTERNET handle.
                    InternetCloseHandle(hDir);

                    // Set the cursor back to an arrow.
                    SetCursor(LoadCursor(NULL,IDC_ARROW));

                    // Return.
                    return FALSE;
               }
           }
           else
           {
               // Write the file name to a string.
               StringCchPrintf(DirList, MAX_PATH, pDirInfo.cFileName);

               // Check the type of file.
               if(pDirInfo.dwFileAttributes==FILE_ATTRIBUTE_DIRECTORY)
               {
                    // Add <DIR> to indicate that this is a 
                    // directory to the user.
                    StringCchCat(DirList, MAX_PATH, TEXT(" <DIR> "));
                    // Add error handling code here.
               }
     
               // Add the file name (or directory) to the list box.
               SendDlgItemMessage(hX, lstDirectory, LB_ADDSTRING,
                                  0, (LPARAM)DirList);
           }
     }
     while ( TRUE);
     
}
```



### <a name="manipulating-options"></a><span data-ttu-id="26843-165">Параметры управления</span><span class="sxs-lookup"><span data-stu-id="26843-165">Manipulating Options</span></span>

<span data-ttu-id="26843-166">[**Интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) и [**интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) используются для работы с параметрами WinInet.</span><span class="sxs-lookup"><span data-stu-id="26843-166">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) and [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) are used to manipulate the WinINet options.</span></span>

<span data-ttu-id="26843-167">[**Интернетсетоптион**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) принимает переменную, которая указывает параметр для установки, буфер для хранения параметра параметра и указатель, содержащий адрес переменной, содержащей длину буфера.</span><span class="sxs-lookup"><span data-stu-id="26843-167">[**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) accepts a variable that indicates the option to set, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

<span data-ttu-id="26843-168">[**Интернеткуерйоптион**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) принимает переменную, которая указывает возвращаемый параметр, буфер для хранения параметра параметра и указатель, содержащий адрес переменной, содержащей длину буфера.</span><span class="sxs-lookup"><span data-stu-id="26843-168">[**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) accepts a variable that indicates the option to retrieve, a buffer to hold the option setting, and a pointer that contains the address of the variable that contains the length of the buffer.</span></span>

### <a name="setting-up-asynchronous-operations"></a><span data-ttu-id="26843-169">Настройка асинхронных операций</span><span class="sxs-lookup"><span data-stu-id="26843-169">Setting Up Asynchronous Operations</span></span>

<span data-ttu-id="26843-170">По умолчанию функции WinINet работают синхронно.</span><span class="sxs-lookup"><span data-stu-id="26843-170">By default, the WinINet functions operate synchronously.</span></span> <span data-ttu-id="26843-171">Приложение может запросить асинхронную операцию, установив флаг [Internet \_ Flag \_ Async](api-flags.md) в вызове функции [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) .</span><span class="sxs-lookup"><span data-stu-id="26843-171">An application can request asynchronous operation by setting the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in the call to the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function.</span></span> <span data-ttu-id="26843-172">Все будущие вызовы дескрипторов, производных от дескрипторов, возвращенных из [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena) , выполняются асинхронно.</span><span class="sxs-lookup"><span data-stu-id="26843-172">All future calls made against handles derived from the handle returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) are made asynchronously.</span></span>

<span data-ttu-id="26843-173">Обоснование асинхронной и синхронной операций заключается в том, чтобы позволить однопотоковому приложению максимально увеличить использование ЦП без ожидания завершения сетевых операций ввода-вывода.</span><span class="sxs-lookup"><span data-stu-id="26843-173">The rationale for asynchronous versus synchronous operation is to allow a single-threaded application to maximize its utilization of the CPU without having to wait for network I/O to complete.</span></span> <span data-ttu-id="26843-174">Таким образом, в зависимости от запроса операция может завершиться синхронно или асинхронно.</span><span class="sxs-lookup"><span data-stu-id="26843-174">Therefore, depending on the request, the operation might complete synchronously or asynchronously.</span></span> <span data-ttu-id="26843-175">Приложение должно проверить код возврата.</span><span class="sxs-lookup"><span data-stu-id="26843-175">The application should check the return code.</span></span> <span data-ttu-id="26843-176">Если функция возвращает **значение false** или **null**, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает сообщение об ошибке \_ ввода-вывода \_ , запрос был выполнен асинхронно и приложение вызывается обратно с \_ запросом состояния в Интернете после завершения \_ \_ функции.</span><span class="sxs-lookup"><span data-stu-id="26843-176">If a function returns **FALSE** or **NULL**, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_IO\_PENDING, the request has been made asynchronously, and the application is called back with INTERNET\_STATUS\_REQUEST\_COMPLETE when the function has completed.</span></span>

<span data-ttu-id="26843-177">Чтобы начать асинхронную операцию, приложение должно установить флаг [" \_ \_ Async Internet Flag](api-flags.md) " в вызове [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="26843-177">To begin asynchronous operation, the application must set the [INTERNET\_FLAG\_ASYNC](api-flags.md) flag in its call to [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="26843-178">Приложение должно зарегистрировать допустимую функцию обратного вызова с помощью [**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span><span class="sxs-lookup"><span data-stu-id="26843-178">The application must then register a valid callback function, using [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback).</span></span>

<span data-ttu-id="26843-179">После регистрации функции обратного вызова для обработчика все операции с этим обработчиком могут формировать события состояния при условии, что значение контекста, указанное при создании маркера, не равно нулю.</span><span class="sxs-lookup"><span data-stu-id="26843-179">After a callback function is registered for a handle, all operations on that handle can generate status indications, provided that the context value that was supplied when the handle was created was not zero.</span></span> <span data-ttu-id="26843-180">Если задать нулевое значение контекста, операция завершится синхронно, даже если в [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena)был указан [ \_ Модификатор Internet Flag \_ Async](api-flags.md) .</span><span class="sxs-lookup"><span data-stu-id="26843-180">Providing a zero context value forces an operation to complete synchronously, even though [INTERNET\_FLAG\_ASYNC](api-flags.md) was specified in [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span>

<span data-ttu-id="26843-181">События состояния дают отзыв о ходе выполнения сетевых операций, таких как разрешение имени узла, подключение к серверу и получение данных.</span><span class="sxs-lookup"><span data-stu-id="26843-181">Status indications give the application feedback about the progress of network operations, such as resolving a host name, connecting to a server, and receiving data.</span></span> <span data-ttu-id="26843-182">Для маркера можно создавать три назначения состояния:</span><span class="sxs-lookup"><span data-stu-id="26843-182">Three special-purpose status indications can be made for a handle:</span></span>

-   <span data-ttu-id="26843-183">\_ \_ Закрытие обработчика состояния Интернета \_ — это последняя индикация состояния, сделанная для маркера.</span><span class="sxs-lookup"><span data-stu-id="26843-183">INTERNET\_STATUS\_HANDLE\_CLOSING is the last status indication that is made for a handle.</span></span>
-   <span data-ttu-id="26843-184">\_ \_ Созданный обработчик состояния Интернета \_ указывает, когда был создан этот маркер.</span><span class="sxs-lookup"><span data-stu-id="26843-184">INTERNET\_STATUS\_HANDLE\_CREATED indicates when the handle is initially created.</span></span>
-   <span data-ttu-id="26843-185">\_Запрос состояния Интернета " \_ завершен" \_ означает, что асинхронная операция завершена.</span><span class="sxs-lookup"><span data-stu-id="26843-185">INTERNET\_STATUS\_REQUEST\_COMPLETE indicates an asynchronous operation has completed.</span></span>

<span data-ttu-id="26843-186">Приложение должно проверить структуру [**\_ асинхронного \_ результата Интернета**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) , чтобы определить, завершилась ли операция успешно или неудачно после получения сообщения \_ о состоянии Интернета \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="26843-186">The application must check the [**INTERNET\_ASYNC\_RESULT**](/windows/desktop/api/Wininet/ns-wininet-internet_async_result) structure to determine whether the operation succeeded or failed after receiving an INTERNET\_STATUS\_REQUEST\_COMPLETE indication.</span></span>

<span data-ttu-id="26843-187">В следующем примере показан пример функции обратного вызова и вызов [**интернетсетстатускаллбакк**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) для регистрации функции в качестве функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="26843-187">The following sample shows an example of a callback function and a call to [**InternetSetStatusCallback**](/windows/desktop/api/Wininet/nf-wininet-internetsetstatuscallback) to register the function as the callback function.</span></span>


```C++
void CALLBACK InternetCallback(
    HINTERNET hInternet,
    DWORD_PTR dwcontext,
    DWORD dwInternetStatus,
    LPVOID lpvStatusInformation,
    DWORD dwStatusInformationLength
    )
{
    _tprintf(TEXT("%0xd %0xp %0xd %0xp %0xd\n"),
             hInternet,
             dwcontext,
             dwInternetStatus,
             lpvStatusInformation,
             dwStatusInformationLength);
};

INTERNET_STATUS_CALLBACK dwISC =
    InternetSetStatusCallback(hInternet, InternetCallback); 
```



### <a name="closing-hinternet-handles"></a><span data-ttu-id="26843-188">Закрытие дескрипторов ХИНТЕРНЕТ</span><span class="sxs-lookup"><span data-stu-id="26843-188">Closing HINTERNET Handles</span></span>

<span data-ttu-id="26843-189">Все дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) можно закрыть с помощью функции [**интернетклосехандле**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="26843-189">All [**HINTERNET**](appendix-a-hinternet-handles.md) handles can be closed by using the [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) function.</span></span> <span data-ttu-id="26843-190">Клиентские приложения должны закрыть все дескрипторы **хинтернет** , производные от дескриптора **хинтернет** , которые они пытаются закрыть перед вызовом [**интернетклосехандле**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) для дескриптора.</span><span class="sxs-lookup"><span data-stu-id="26843-190">Client applications must close all **HINTERNET** handles derived from the **HINTERNET** handle they are trying to close before calling [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle.</span></span>

<span data-ttu-id="26843-191">В следующем примере показана иерархия Handle.</span><span class="sxs-lookup"><span data-stu-id="26843-191">The following example illustrates the handle hierarchy.</span></span>


```C++
HINTERNET hRootHandle, hOpenUrlHandle;

hRootHandle = InternetOpen( TEXT("Example"), 
                            INTERNET_OPEN_TYPE_DIRECT, 
                            NULL, 
                            NULL, 0);

hOpenUrlHandle = InternetOpenUrl(hRootHandle, 
    TEXT("https://www.server.com/default.htm"), NULL, 0, 
    INTERNET_FLAG_RAW_DATA,0);

// Close the handle created by InternetOpenUrl so that the
// InternetOpen handle can be closed.
InternetCloseHandle(hOpenUrlHandle); 

// Close the handle created by InternetOpen.
InternetCloseHandle(hRootHandle);
```



### <a name="locking-and-unlocking-resources"></a><span data-ttu-id="26843-192">Блокировка и разблокировка ресурсов</span><span class="sxs-lookup"><span data-stu-id="26843-192">Locking and Unlocking Resources</span></span>

<span data-ttu-id="26843-193">Функция [**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) позволяет приложению гарантировать, что кэшированный ресурс, связанный с переданным в него обработчиком [**хинтернет**](appendix-a-hinternet-handles.md) , не исчезнет из кэша.</span><span class="sxs-lookup"><span data-stu-id="26843-193">The [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) function allows an application to ensure that the cached resource associated with the [**HINTERNET**](appendix-a-hinternet-handles.md) handle passed to it does not disappear from the cache.</span></span> <span data-ttu-id="26843-194">Если другой файл загрузки пытается зафиксировать ресурс с тем же URL-адресом, что и заблокированный файл, кэш позволяет избежать удаления файла путем выполнения безопасного удаления.</span><span class="sxs-lookup"><span data-stu-id="26843-194">If another download tries to commit a resource that has the same URL as the locked file, the cache avoids removing the file by doing a safe delete.</span></span> <span data-ttu-id="26843-195">После того как приложение вызовет функцию [**интернетунлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) , кэш получает разрешение на удаление файла.</span><span class="sxs-lookup"><span data-stu-id="26843-195">After the application calls the [**InternetUnlockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetunlockrequestfile) function, the cache is given permission to delete the file.</span></span>

<span data-ttu-id="26843-196">Если не установлен флаг [Интернета флаг кэширования \_ \_ \_ \_ записи](api-flags.md) или подключения к [Интернету \_ флага \_ \_ кэша не](api-flags.md) , [**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) создает временный файл с расширением TMP, если только этот маркер не подключен к ресурсу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="26843-196">If the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) or [INTERNET\_FLAG\_DONT\_CACHE](api-flags.md) flag has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) creates a temporary file with the extension TMP, unless the handle is connected to an https resource.</span></span> <span data-ttu-id="26843-197">Если функция обращается к ресурсу HTTPS и \_ флагу Интернета \_ не \_ задано кэширование \_ записи кэша (или \_ кэш не Internet Flag \_ \_ ), [**интернетлоккрекуестфиле**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="26843-197">If the function accesses an https resource and INTERNET\_FLAG\_NO\_CACHE\_WRITE (or INTERNET\_FLAG\_DONT\_CACHE) has been set, [**InternetLockRequestFile**](/windows/desktop/api/Wininet/nf-wininet-internetlockrequestfile) fails.</span></span>

> [!Note]  
> <span data-ttu-id="26843-198">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="26843-198">WinINet does not support server implementations.</span></span> <span data-ttu-id="26843-199">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="26843-199">In addition, it should not be used from a service.</span></span> <span data-ttu-id="26843-200">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="26843-200">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 
