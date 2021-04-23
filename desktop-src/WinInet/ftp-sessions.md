---
title: Сеансы FTP
description: WinINet позволяет приложениям перемещаться по каталогам и файлам на FTP-сервере и управлять ими. Так как прокси-серверы CERN не поддерживают FTP, приложения, использующие прокси CERN, должны использовать функцию Интернетопенурл.
ms.assetid: 23763672-765f-4bbc-95c9-c28775e91f3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8310c2b83b81fc18b84d39153ed3dc7afda0df5a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104070299"
---
# <a name="ftp-sessions"></a><span data-ttu-id="c99b4-104">Сеансы FTP</span><span class="sxs-lookup"><span data-stu-id="c99b4-104">FTP Sessions</span></span>

<span data-ttu-id="c99b4-105">WinINet позволяет приложениям перемещаться по каталогам и файлам на FTP-сервере и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="c99b4-105">WinINet enables applications to navigate and manipulate directories and files on an ftp server.</span></span> <span data-ttu-id="c99b4-106">Так как прокси-серверы CERN не поддерживают FTP, приложения, использующие прокси CERN, должны использовать функцию [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) .</span><span class="sxs-lookup"><span data-stu-id="c99b4-106">Because CERN proxies do not support FTP, applications that use a CERN proxy exclusively must use the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function.</span></span> <span data-ttu-id="c99b4-107">Дополнительные сведения об использовании [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla)см. в разделе [доступ к URL-адресам напрямую](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="c99b4-107">For more information about how to use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="c99b4-108">Чтобы начать сеанс FTP, используйте [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) для создания обработчика сеанса.</span><span class="sxs-lookup"><span data-stu-id="c99b4-108">To begin an FTP session, use [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to create the session handle.</span></span>

<span data-ttu-id="c99b4-109">WinINet позволяет выполнять следующие действия на FTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-109">WinINet enables you to perform the following actions on an FTP server:</span></span>

-   <span data-ttu-id="c99b4-110">Переход между каталогами.</span><span class="sxs-lookup"><span data-stu-id="c99b4-110">Navigate between directories.</span></span>
-   <span data-ttu-id="c99b4-111">Перечисление, создание, удаление и переименование каталогов.</span><span class="sxs-lookup"><span data-stu-id="c99b4-111">Enumerate, create, remove, and rename directories.</span></span>
-   <span data-ttu-id="c99b4-112">Переименование, передача, скачивание и удаление файлов.</span><span class="sxs-lookup"><span data-stu-id="c99b4-112">Rename, upload, download, and delete files.</span></span>

<span data-ttu-id="c99b4-113">Навигация обеспечивается функциями [**фтпжеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) и [**фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) .</span><span class="sxs-lookup"><span data-stu-id="c99b4-113">Navigation is provided by the [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions.</span></span> <span data-ttu-id="c99b4-114">Эти функции используют обработчик сеанса, созданный предыдущим вызовом [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , для определения каталога, в котором в настоящее время находится приложение, или для изменения в другой подкаталог.</span><span class="sxs-lookup"><span data-stu-id="c99b4-114">These functions utilize the session handle created by a previous call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to determine which directory the application is currently in, or to change to a different subdirectory.</span></span>

<span data-ttu-id="c99b4-115">Перечисление каталогов выполняется с помощью функций [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) и [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) .</span><span class="sxs-lookup"><span data-stu-id="c99b4-115">Directory enumeration is performed by using the [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) and [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) functions.</span></span> <span data-ttu-id="c99b4-116">[**Фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) использует созданный с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) обработчик сеанса, чтобы найти первый файл, соответствующий заданным условиям поиска, и возвращает маркер, чтобы продолжить перечисление каталогов.</span><span class="sxs-lookup"><span data-stu-id="c99b4-116">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) to find the first file that matches the given search criteria and returns a handle to continue the directory enumeration.</span></span> <span data-ttu-id="c99b4-117">[**Интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) использует маркер, возвращенный [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) для возврата следующего файла, соответствующего исходным условиям поиска.</span><span class="sxs-lookup"><span data-stu-id="c99b4-117">[**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) uses the handle returned by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) to return the next file that matches the original search criteria.</span></span> <span data-ttu-id="c99b4-118">Приложение должно продолжать вызывать [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) , пока в каталоге не останется больше файлов.</span><span class="sxs-lookup"><span data-stu-id="c99b4-118">The application should continue to call [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until there are no more files left in the directory.</span></span>

<span data-ttu-id="c99b4-119">Используйте функцию [**фтпкреатедиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) для создания новых каталогов.</span><span class="sxs-lookup"><span data-stu-id="c99b4-119">Use the [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function to create new directories.</span></span> <span data-ttu-id="c99b4-120">Эта функция использует обработчик сеанса, созданный [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , и создает каталог, указанный в строке, передаваемой функции.</span><span class="sxs-lookup"><span data-stu-id="c99b4-120">This function uses the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and creates the directory specified by the string passed to the function.</span></span> <span data-ttu-id="c99b4-121">Строка может содержать имя каталога относительно текущего каталога или полный путь к каталогу.</span><span class="sxs-lookup"><span data-stu-id="c99b4-121">The string can contain a directory name relative to the current directory, or a fully qualified directory path.</span></span>

<span data-ttu-id="c99b4-122">Чтобы переименовать файлы или каталоги, приложение может вызвать [**фтпренамефиле**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span><span class="sxs-lookup"><span data-stu-id="c99b4-122">To rename either files or directories, the application can call [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea).</span></span> <span data-ttu-id="c99b4-123">Эта функция заменяет исходное имя новым именем, переданным в функцию.</span><span class="sxs-lookup"><span data-stu-id="c99b4-123">This function replaces the original name with the new name passed to the function.</span></span> <span data-ttu-id="c99b4-124">Имя файла или каталога может относиться к текущему каталогу или полному имени.</span><span class="sxs-lookup"><span data-stu-id="c99b4-124">The name of the file or directory can be relative to the current directory, or a fully qualified name.</span></span>

<span data-ttu-id="c99b4-125">Для отправки или размещения файлов на FTP-сервере приложение может использовать либо [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) , либо [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (вместе с [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span><span class="sxs-lookup"><span data-stu-id="c99b4-125">To upload or place files on an FTP server, the application can use either [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (along with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)).</span></span> <span data-ttu-id="c99b4-126">[**Фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) можно использовать, если файл уже существует локально, тогда как [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) и [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) можно использовать, если данные необходимо записать в файл на FTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-126">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) can be used if the file already exists locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) can be used if data needs to be written to a file on the FTP server.</span></span>

<span data-ttu-id="c99b4-127">Чтобы скачать или получить файлы, приложение может использовать либо [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) , либо [**Фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (с [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span><span class="sxs-lookup"><span data-stu-id="c99b4-127">To download or get files, the application can use either [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) or [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) (with [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile)).</span></span> <span data-ttu-id="c99b4-128">[**Фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) используется для получения файла с FTP-сервера и локального сохранения, в то время как [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) и [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) можно использовать для управления расположением загруженных данных (например, приложение может отображать информацию в поле ввода).</span><span class="sxs-lookup"><span data-stu-id="c99b4-128">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) is used to retrieve a file from an FTP server and store it locally, while [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) can be used to control where the downloaded information is going (for example, the application could display the information in an edit box).</span></span>

<span data-ttu-id="c99b4-129">Удалите файлы на FTP-сервере с помощью функции [**фтпделетефиле**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="c99b4-129">Delete files on an FTP server by using the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="c99b4-130">Эта функция удаляет имя файла, которое относится либо к текущему каталогу, либо к полному имени файла с FTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="c99b4-130">This function removes a file name that is relative either to the current directory or to a fully qualified file name from the FTP server.</span></span> <span data-ttu-id="c99b4-131">[**Фтпделетефиле**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) требует, чтобы в [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta)был возвращен обработчик сеанса.</span><span class="sxs-lookup"><span data-stu-id="c99b4-131">[**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) requires a session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>

## <a name="ftp-function-handles"></a><span data-ttu-id="c99b4-132">Дескрипторы функций FTP</span><span class="sxs-lookup"><span data-stu-id="c99b4-132">FTP Function Handles</span></span>

<span data-ttu-id="c99b4-133">Для правильной работы функции FTP требуются определенные типы дескрипторов [**хинтернет**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="c99b4-133">To work properly, the FTP functions require certain types of [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="c99b4-134">Эти дескрипторы должны создаваться в определенном порядке, начиная с корневого дескриптора, созданного [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="c99b4-134">These handles must be created in a specific order, starting with the root handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="c99b4-135">Затем [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) может создать обработчик сеанса FTP.</span><span class="sxs-lookup"><span data-stu-id="c99b4-135">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) can then create an FTP session handle.</span></span>

<span data-ttu-id="c99b4-136">На следующей диаграмме показаны функции, зависящие от обработчика сеанса FTP, возвращаемого функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-136">The following diagram shows the functions that are dependent on the FTP session handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="c99b4-137">Затененные поля представляют функции, которые возвращают дескрипторы [**хинтернет**](appendix-a-hinternet-handles.md) , а обычные поля представляют функции, ИСПОЛЬЗУЮЩИЕ дескриптор хинтернет, созданный функцией, от которой они зависят.</span><span class="sxs-lookup"><span data-stu-id="c99b4-137">The shaded boxes represent functions that return [**HINTERNET**](appendix-a-hinternet-handles.md) handles, while the plain boxes represent functions that use the HINTERNET handle created by the function on which they depend.</span></span>

![функции FTP, зависящие от обработчика сеанса FTP, возвращенного интернетконнект](images/ax-wnt06.png)

<span data-ttu-id="c99b4-139">На следующей диаграмме показаны две функции, которые возвращают дескрипторы [хинтернет](appendix-a-hinternet-handles.md) и зависящие от них функции.</span><span class="sxs-lookup"><span data-stu-id="c99b4-139">The following diagram shows the two functions that return [HINTERNET](appendix-a-hinternet-handles.md) handles and the functions that are dependent on them.</span></span> <span data-ttu-id="c99b4-140">Затененные поля представляют функции, которые возвращают дескрипторы **хинтернет** , а обычные поля представляют функции, использующие дескриптор **хинтернет** , созданный функцией, от которой они зависят.</span><span class="sxs-lookup"><span data-stu-id="c99b4-140">The shaded boxes represent functions that return **HINTERNET** handles, while the plain boxes represent functions that use the **HINTERNET** handle created by the function on which they depend.</span></span>

![функции FTP, возвращающие дескрипторы хинтернет](images/ax-wnt03.png)

<span data-ttu-id="c99b4-142">Дополнительные сведения см. в разделе [Хинтернет Handles](appendix-a-hinternet-handles.md).</span><span class="sxs-lookup"><span data-stu-id="c99b4-142">For more information, see [HINTERNET Handles](appendix-a-hinternet-handles.md).</span></span>

## <a name="using-the-wininet-functions-for-ftp-sessions"></a><span data-ttu-id="c99b4-143">Использование функций WinINet для сеансов FTP</span><span class="sxs-lookup"><span data-stu-id="c99b4-143">Using the WinINet Functions for FTP Sessions</span></span>

<span data-ttu-id="c99b4-144">Во время сеансов FTP используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="c99b4-144">The following functions are used during FTP sessions.</span></span> <span data-ttu-id="c99b4-145">Эти функции не распознаются прокси-серверами CERN.</span><span class="sxs-lookup"><span data-stu-id="c99b4-145">These functions are not recognized by CERN proxies.</span></span> <span data-ttu-id="c99b4-146">Приложения, которые должны работать через прокси-серверы CERN, должны использовать [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) и обращаться к ресурсам напрямую.</span><span class="sxs-lookup"><span data-stu-id="c99b4-146">Applications that must function through CERN proxies should use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and access the resources directly.</span></span> <span data-ttu-id="c99b4-147">Дополнительные сведения о прямом доступе к ресурсам см. в разделе [доступ к URL-адресам напрямую](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="c99b4-147">For more information on direct resource access, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>



| <span data-ttu-id="c99b4-148">Функция</span><span class="sxs-lookup"><span data-stu-id="c99b4-148">Function</span></span>                                                 | <span data-ttu-id="c99b4-149">Описание</span><span class="sxs-lookup"><span data-stu-id="c99b4-149">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c99b4-150">**фтпкреатедиректори**</span><span class="sxs-lookup"><span data-stu-id="c99b4-150">**FtpCreateDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya)         | <span data-ttu-id="c99b4-151">Создает новый каталог на сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-151">Creates a new directory on the server.</span></span> <span data-ttu-id="c99b4-152">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-152">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                  |
| [<span data-ttu-id="c99b4-153">**фтпделетефиле**</span><span class="sxs-lookup"><span data-stu-id="c99b4-153">**FtpDeleteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea)                   | <span data-ttu-id="c99b4-154">Удаляет файл с сервера.</span><span class="sxs-lookup"><span data-stu-id="c99b4-154">Deletes a file from the server.</span></span> <span data-ttu-id="c99b4-155">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-155">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                         |
| [<span data-ttu-id="c99b4-156">**фтпфиндфирстфиле**</span><span class="sxs-lookup"><span data-stu-id="c99b4-156">**FtpFindFirstFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)             | <span data-ttu-id="c99b4-157">Запускает перечисление файлов или поиск файлов в текущем каталоге.</span><span class="sxs-lookup"><span data-stu-id="c99b4-157">Starts file enumeration or file search in the current directory.</span></span> <span data-ttu-id="c99b4-158">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-158">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>        |
| [<span data-ttu-id="c99b4-159">**фтпжеткуррентдиректори**</span><span class="sxs-lookup"><span data-stu-id="c99b4-159">**FtpGetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) | <span data-ttu-id="c99b4-160">Возвращает текущий каталог клиента на сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-160">Returns the client's current directory on the server.</span></span> <span data-ttu-id="c99b4-161">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-161">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="c99b4-162">**фтпжетфиле**</span><span class="sxs-lookup"><span data-stu-id="c99b4-162">**FtpGetFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)                         | <span data-ttu-id="c99b4-163">Извлекает файл с сервера.</span><span class="sxs-lookup"><span data-stu-id="c99b4-163">Retrieves a file from the server.</span></span> <span data-ttu-id="c99b4-164">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-164">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                       |
| [<span data-ttu-id="c99b4-165">**фтпопенфиле**</span><span class="sxs-lookup"><span data-stu-id="c99b4-165">**FtpOpenFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea)                       | <span data-ttu-id="c99b4-166">Инициирует доступ к файлу на сервере для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="c99b4-166">Initiates access to a file on the server for either reading or writing.</span></span> <span data-ttu-id="c99b4-167">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-167">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> |
| [<span data-ttu-id="c99b4-168">**фтппутфиле**</span><span class="sxs-lookup"><span data-stu-id="c99b4-168">**FtpPutFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea)                         | <span data-ttu-id="c99b4-169">Записывает файл на сервер.</span><span class="sxs-lookup"><span data-stu-id="c99b4-169">Writes a file to the server.</span></span> <span data-ttu-id="c99b4-170">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-170">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                            |
| [<span data-ttu-id="c99b4-171">**фтпремоведиректори**</span><span class="sxs-lookup"><span data-stu-id="c99b4-171">**FtpRemoveDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya)         | <span data-ttu-id="c99b4-172">Удаляет каталог на сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-172">Deletes a directory on the server.</span></span> <span data-ttu-id="c99b4-173">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-173">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                      |
| [<span data-ttu-id="c99b4-174">**фтпренамефиле**</span><span class="sxs-lookup"><span data-stu-id="c99b4-174">**FtpRenameFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea)                   | <span data-ttu-id="c99b4-175">Переименовывает файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-175">Renames a file on the server.</span></span> <span data-ttu-id="c99b4-176">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-176">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                                           |
| [<span data-ttu-id="c99b4-177">**фтпсеткуррентдиректори**</span><span class="sxs-lookup"><span data-stu-id="c99b4-177">**FtpSetCurrentDirectory**</span></span>](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) | <span data-ttu-id="c99b4-178">Изменяет текущий каталог клиента на сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-178">Changes the client's current directory on the server.</span></span> <span data-ttu-id="c99b4-179">Эта функция требует создания маркера, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-179">This function requires a handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span>                   |
| [<span data-ttu-id="c99b4-180">**интернетвритефиле**</span><span class="sxs-lookup"><span data-stu-id="c99b4-180">**InternetWriteFile**</span></span>](/windows/desktop/api/Wininet/nf-wininet-internetwritefile)           | <span data-ttu-id="c99b4-181">Записывает данные в открытый файл на сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-181">Writes data to an open file on the server.</span></span> <span data-ttu-id="c99b4-182">Эта функция требует создания маркера, созданного с помощью [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span><span class="sxs-lookup"><span data-stu-id="c99b4-182">This function requires a handle created by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea).</span></span>                                      |



 

### <a name="starting-an-ftp-session"></a><span data-ttu-id="c99b4-183">Запуск сеанса FTP</span><span class="sxs-lookup"><span data-stu-id="c99b4-183">Starting an FTP Session</span></span>

<span data-ttu-id="c99b4-184">Приложение устанавливает сеанс FTP, вызывая [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) для маркера, созданного с помощью [**интернетопен**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="c99b4-184">The application establishes an FTP session by calling [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) on a handle created by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="c99b4-185">[**Интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) требуется имя сервера, номер порта, имя пользователя, пароль и тип службы (который должен быть установлен на \_ FTP-службу Internet \_ ).</span><span class="sxs-lookup"><span data-stu-id="c99b4-185">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) needs the server name, port number, user name, password, and service type (which must be set to INTERNET\_SERVICE\_FTP).</span></span> <span data-ttu-id="c99b4-186">Для пассивной семантики FTP приложение также должно установить флаг [ \_ \_ пассивного](api-flags.md) подключения к Интернету.</span><span class="sxs-lookup"><span data-stu-id="c99b4-186">For passive FTP semantics, the application must also set the [INTERNET\_FLAG\_PASSIVE](api-flags.md) flag.</span></span>

<span data-ttu-id="c99b4-187">\_ \_ \_ \_ \_ \_ Для номера порта можно использовать FTP-порт Интернета по умолчанию и значения недопустимых номеров портов в Интернете.</span><span class="sxs-lookup"><span data-stu-id="c99b4-187">The INTERNET\_DEFAULT\_FTP\_PORT and INTERNET\_INVALID\_PORT\_NUMBER values can be used for the port number.</span></span> <span data-ttu-id="c99b4-188">\_ \_ FTP-порт по умолчанию в Интернете \_ использует порт FTP по умолчанию, но тип службы по-прежнему должен быть установлен.</span><span class="sxs-lookup"><span data-stu-id="c99b4-188">INTERNET\_DEFAULT\_FTP\_PORT uses the default FTP port, but the service type still must be set.</span></span> <span data-ttu-id="c99b4-189">\_Недопустимый \_ \_ номер порта в Интернете использует значение по умолчанию для указанного типа службы.</span><span class="sxs-lookup"><span data-stu-id="c99b4-189">INTERNET\_INVALID\_PORT\_NUMBER uses the default value for the indicated service type.</span></span>

<span data-ttu-id="c99b4-190">Значения имени пользователя и пароля могут быть **равны NULL**.</span><span class="sxs-lookup"><span data-stu-id="c99b4-190">The values for the user name and password can be set to **NULL**.</span></span> <span data-ttu-id="c99b4-191">Если оба значения имеют значение **null**, [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) использует "Anonymous" для имени пользователя и адрес электронной почты пользователя для пароля.</span><span class="sxs-lookup"><span data-stu-id="c99b4-191">If both values are set to **NULL**, [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses "anonymous" for the user name, and the user's email address for the password.</span></span> <span data-ttu-id="c99b4-192">Если для пароля задано **значение NULL**, имя пользователя, передаваемое в [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , используется для имени пользователя, а для пароля используется пустая строка.</span><span class="sxs-lookup"><span data-stu-id="c99b4-192">If only the password is set to **NULL**, the user name passed to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) is used for the user name, and an empty string is used for the password.</span></span> <span data-ttu-id="c99b4-193">Если ни одно из этих значений не равно **null**, используются имя пользователя и пароль, присвоенные [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) .</span><span class="sxs-lookup"><span data-stu-id="c99b4-193">If neither value is **NULL**, the user name and password given to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) are used.</span></span>

### <a name="enumerating-directories"></a><span data-ttu-id="c99b4-194">Перечисление каталогов</span><span class="sxs-lookup"><span data-stu-id="c99b4-194">Enumerating Directories</span></span>

<span data-ttu-id="c99b4-195">Перечисление каталога на FTP-сервере требует создания обработчика с помощью [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="c99b4-195">Enumeration of a directory on an FTP server requires the creation of a handle by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="c99b4-196">Этот обработчик является ветвью обработчика сеанса, созданного с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-196">This handle is a branch of the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="c99b4-197">[**Фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) находит первый файл или каталог на сервере и возвращает его в структуре [**\_ \_ данных Win32 Find**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) .</span><span class="sxs-lookup"><span data-stu-id="c99b4-197">[**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) locates the first file or directory on the server and returns it in a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure.</span></span> <span data-ttu-id="c99b4-198">Используйте [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) , пока не вернется [**сообщение об ошибке больше \_ нет \_ \_ файлов**](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c99b4-198">Use [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) until it returns [**ERROR\_NO\_MORE\_FILES**](wininet-errors.md).</span></span> <span data-ttu-id="c99b4-199">Этот метод находит все последующие файлы и каталоги на сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-199">This method finds all subsequent files and directories on the server.</span></span> <span data-ttu-id="c99b4-200">Дополнительные сведения о [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea)см. [в разделе Поиск следующего файла](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c99b4-200">For more information on [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea), see [Finding the Next File](common-functions.md).</span></span>

<span data-ttu-id="c99b4-201">Чтобы определить, является ли файл, полученный с помощью [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) или [**интернетфинднекстфиле**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) , каталогом, проверьте, равен ли он каталогу атрибутов файла в **Двфилеаттрибутес** члене структуры [**\_ \_ данных Win32 Find**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c99b4-201">To determine if the file retrieved by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) or [**InternetFindNextFile**](/windows/desktop/api/Wininet/nf-wininet-internetfindnextfilea) is a directory, check the **dwFileAttributes** member of the [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure to see if it is equal to FILE\_ATTRIBUTE\_DIRECTORY.</span></span>

<span data-ttu-id="c99b4-202">Если приложение вносит изменения на FTP-сервере или при частом изменении FTP-сервера, [флаг Internet \_ Flag \_ без \_ \_ записи в кэш](api-flags.md) и флаги [ \_ \_ перезагрузки в Интернете](api-flags.md) должны быть установлены в [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="c99b4-202">If the application makes changes on the FTP server or if the FTP server changes frequently, the [INTERNET\_FLAG\_NO\_CACHE\_WRITE](api-flags.md) and [INTERNET\_FLAG\_RELOAD](api-flags.md) flags should be set in [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="c99b4-203">Эти флаги гарантируют, что данные каталога, извлекаемые с FTP-сервера, являются актуальными.</span><span class="sxs-lookup"><span data-stu-id="c99b4-203">These flags ensure that the directory information being retrieved from the FTP server is current.</span></span>

<span data-ttu-id="c99b4-204">После того как приложение завершит перечисление каталогов, приложение должно выполнить вызов [**интернетклосехандле**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) для маркера, созданного [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span><span class="sxs-lookup"><span data-stu-id="c99b4-204">After the application completes the directory enumeration, the application must make a call to [**InternetCloseHandle**](/windows/desktop/api/Wininet/nf-wininet-internetclosehandle) on the handle created by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea).</span></span> <span data-ttu-id="c99b4-205">До закрытия этого обработчика приложение не сможет снова вызвать [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) в обработчике сеанса, созданном с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-205">Until that handle is closed, the application cannot call [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) again on the session handle created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="c99b4-206">Если вызов [**фтпфиндфирстфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) выполняется для одного и того же обработчика сеанса до закрытия предыдущего вызова той же функции, происходит сбой функции, возвращающей [ошибку \_ FTP- \_ передачи \_ \_](wininet-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c99b4-206">If a call to [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea) is made on the same session handle before the previous call to the same function is closed, the function fails, returning [ERROR\_FTP\_TRANSFER\_IN\_PROGRESS](wininet-errors.md).</span></span>

<span data-ttu-id="c99b4-207">В следующем примере выполняется перечисление содержимого FTP-каталога в элемент управления "список".</span><span class="sxs-lookup"><span data-stu-id="c99b4-207">The following example enumerates the contents of an FTP directory into a list box control.</span></span> <span data-ttu-id="c99b4-208">Параметр *хконнектион* — это маркер, возвращаемый функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после того, как он устанавливает сеанс FTP.</span><span class="sxs-lookup"><span data-stu-id="c99b4-208">The *hConnection* parameter is a handle returned by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function after it establishes an FTP session.</span></span> <span data-ttu-id="c99b4-209">Пример исходного кода для функции Интернетеррораут, упоминаемой в этом примере, можно найти в разделе [Обработка ошибок](appendix-c-handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="c99b4-209">Sample source code for the InternetErrorOut function referenced in this example can be found in the [Handling Errors](appendix-c-handling-errors.md)topic.</span></span>


```C++
#include <windows.h>
#include <strsafe.h>
#include <wininet.h>

#pragma comment(lib, "wininet.lib")
#pragma comment(lib, "user32.lib")

#define  FTP_FUNCTIONS_BUFFER_SIZE          MAX_PATH+8

BOOL WINAPI DisplayFtpDir(
                           HWND hDlg,
                           HINTERNET hConnection,
                           DWORD dwFindFlags,
                           int nListBoxId )
{
  WIN32_FIND_DATA dirInfo;
  HINTERNET       hFind;
  DWORD           dwError;
  BOOL            retVal = FALSE;
  TCHAR           szMsgBuffer[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR           szFName[FTP_FUNCTIONS_BUFFER_SIZE];
  
  SendDlgItemMessage( hDlg, nListBoxId, LB_RESETCONTENT, 0, 0 );
  hFind = FtpFindFirstFile( hConnection, TEXT( "*.*" ), 
                            &dirInfo, dwFindFlags, 0 );
  if ( hFind == NULL )
  {
    dwError = GetLastError( );
    if( dwError == ERROR_NO_MORE_FILES )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "No files found at FTP location specified." ) );
      retVal = TRUE;
      goto DisplayDirError_1;
    }
    StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
      TEXT( "FtpFindFirstFile failed." ) );
    goto DisplayDirError_1;
  }

  do
  {
    if( FAILED( StringCchCopy( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
                  dirInfo.cFileName ) ) ||
        ( ( dirInfo.dwFileAttributes & FILE_ATTRIBUTE_DIRECTORY ) &&
        ( FAILED( StringCchCat( szFName, FTP_FUNCTIONS_BUFFER_SIZE,
         TEXT( " <DIR> " ) ) ) ) ) )
    {
      StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
        TEXT( "Failed to copy a file or directory name." ) );
      retVal = FALSE;
      goto DisplayDirError_2;
    }
    SendDlgItemMessage( hDlg, nListBoxId, LB_ADDSTRING, 
                        0, (LPARAM) szFName );
  } while( InternetFindNextFile( hFind, (LPVOID) &dirInfo ) );

  if( ( dwError = GetLastError( ) ) == ERROR_NO_MORE_FILES )
  {
    InternetCloseHandle(hFind);
    return( TRUE );
  }
  StringCchCopy( szMsgBuffer, FTP_FUNCTIONS_BUFFER_SIZE,
    TEXT( "FtpFindNextFile failed." ) );

DisplayDirError_2:
  InternetCloseHandle( hFind );
DisplayDirError_1:
  MessageBox( hDlg,
    (LPCTSTR) szMsgBuffer,
    TEXT( "DisplayFtpDir( ) Problem" ),
    MB_OK | MB_ICONERROR );
  return( retVal );
}
```



### <a name="navigating-directories"></a><span data-ttu-id="c99b4-210">Перемещение по каталогам</span><span class="sxs-lookup"><span data-stu-id="c99b4-210">Navigating Directories</span></span>

<span data-ttu-id="c99b4-211">Функции [**фтпжеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) и [**фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) обработают навигацию по каталогам.</span><span class="sxs-lookup"><span data-stu-id="c99b4-211">The [**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) and [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) functions handle directory navigation.</span></span>

<span data-ttu-id="c99b4-212">[**Фтпжеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) возвращает текущий каталог приложения на FTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-212">[**FtpGetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpgetcurrentdirectorya) returns the application's current directory on the FTP server.</span></span> <span data-ttu-id="c99b4-213">Путь к каталогу из корневого каталога на FTP-сервере включен.</span><span class="sxs-lookup"><span data-stu-id="c99b4-213">The directory path from the root directory on the FTP server is included.</span></span>

<span data-ttu-id="c99b4-214">[**Фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) изменяет рабочий каталог на сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-214">[**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the working directory on the server.</span></span> <span data-ttu-id="c99b4-215">Сведения о каталоге, передаваемые в [**фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) , могут быть либо частично, либо полным именем пути относительно текущего каталога.</span><span class="sxs-lookup"><span data-stu-id="c99b4-215">The directory information passed to [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) can be either a partially or fully qualified path name relative to the current directory.</span></span> <span data-ttu-id="c99b4-216">Например, если приложение находится в каталоге "общедоступная/информационная", а путь — "FTP/example", [**фтпсеткуррентдиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) изменяет текущий каталог на "общедоступный/информационный/FTP/example".</span><span class="sxs-lookup"><span data-stu-id="c99b4-216">For example, if the application is currently in the directory "public/info" and the path is "ftp/example", [**FtpSetCurrentDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpsetcurrentdirectorya) changes the current directory to "public/info/ftp/example".</span></span>

<span data-ttu-id="c99b4-217">В следующем примере используется обработчик сеанса FTP Хконнектион, возвращаемый [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="c99b4-217">The following example uses the FTP session handle hConnection, which is returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="c99b4-218">Новое имя каталога берется из поля редактирования родительского диалогового окна, IDC которого передается в параметр *ндирнамеид* .</span><span class="sxs-lookup"><span data-stu-id="c99b4-218">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="c99b4-219">Перед изменением каталога функция получает текущий каталог и сохраняет ее в том же поле ввода.</span><span class="sxs-lookup"><span data-stu-id="c99b4-219">Before the directory change is made, the function retrieves the current directory and stores it in the same edit box.</span></span> <span data-ttu-id="c99b4-220">Код источник для функции Дисплайфтпдир, вызываемой в конце, приведен выше.</span><span class="sxs-lookup"><span data-stu-id="c99b4-220">The souce code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI ChangeFtpDir( HWND hDlg, 
                          HINTERNET hConnection,
                          int nDirNameId, 
                          int nListBoxId )
{
  DWORD dwSize;
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szOldDirName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR* szFailedFunctionName;

  dwSize = FTP_FUNCTIONS_BUFFER_SIZE;

  if( !GetDlgItemText( hDlg, nDirNameId, szNewDirName, dwSize ) )
  {
    szFailedFunctionName = TEXT( "GetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if ( !FtpGetCurrentDirectory( hConnection, szOldDirName, &dwSize ))
  {
    szFailedFunctionName = TEXT( "FtpGetCurrentDirectory" );
    goto ChangeFtpDirError;
  }

  if( !SetDlgItemText( hDlg, nDirNameId, szOldDirName ) )
  {
    szFailedFunctionName = TEXT( "SetDlgItemText" );
    goto ChangeFtpDirError;
  }

  if( !FtpSetCurrentDirectory( hConnection, szNewDirName ) )
  {
    szFailedFunctionName = TEXT( "FtpSetCurrentDirectory" );
    goto ChangeFtpDirError;
  }
  return( DisplayFtpDir( hDlg, hConnection, 0, nListBoxId ) );

ChangeFtpDirError:
  InternetErrorOut( hDlg, GetLastError( ), szFailedFunctionName );
  DisplayFtpDir( hDlg, hConnection, INTERNET_FLAG_RELOAD, nListBoxId);
  return( FALSE );
}
```



### <a name="manipulating-directories-on-an-ftp-server"></a><span data-ttu-id="c99b4-221">Управление каталогами на FTP-сервере</span><span class="sxs-lookup"><span data-stu-id="c99b4-221">Manipulating Directories on an FTP Server</span></span>

<span data-ttu-id="c99b4-222">WinINet предоставляет возможность создавать и удалять каталоги на FTP-сервере, к которому приложение имеет необходимые привилегии.</span><span class="sxs-lookup"><span data-stu-id="c99b4-222">WinINet provides the capability to create and remove directories on an FTP server to which the application has the necessary privileges.</span></span> <span data-ttu-id="c99b4-223">Если приложение должно входить на сервер с указанными именем пользователя и паролем, эти значения можно использовать в [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) при создании обработчика сеанса FTP.</span><span class="sxs-lookup"><span data-stu-id="c99b4-223">If the application must log on to a server with a specific user name and password, the values can be used in [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) when creating the FTP session handle.</span></span>

<span data-ttu-id="c99b4-224">Функция [**фтпкреатедиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) принимает допустимый код FTP-сеанса и строку, завершающуюся **нулем**, которая содержит либо полный путь, либо имя относительно текущего каталога, и создает каталог на FTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-224">The [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya) function takes a valid FTP session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and creates a directory on the FTP server.</span></span>

<span data-ttu-id="c99b4-225">В следующем примере показаны два отдельных вызова [**фтпкреатедиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span><span class="sxs-lookup"><span data-stu-id="c99b4-225">The following example shows two separate calls to [**FtpCreateDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpcreatedirectorya).</span></span> <span data-ttu-id="c99b4-226">В обоих примерах Хфтпсессион — это обработчик сеанса, созданный функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , а корневой каталог — текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="c99b4-226">In both examples, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span>

``` syntax
/* Creates the directory "test" in the current (root) directory. */
FtpCreateDirectory( hFtpSession, "test" );

/* Creates the directory "example" in the test directory. */
FtpCreateDirectory( hFtpSession, "\\test\\example" );
```

<span data-ttu-id="c99b4-227">Функция [**фтпремоведиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) принимает обработчик сеанса и строку, завершающуюся **нулем**, которая содержит либо полный путь, либо имя относительно текущего каталога, а также удаляет этот каталог с FTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="c99b4-227">The [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya) function takes a session handle and a **null**-terminated string that contains either a fully qualified path or a name relative to the current directory and removes that directory from the FTP server.</span></span>

<span data-ttu-id="c99b4-228">В следующем примере показаны два примера вызовов [**фтпремоведиректори**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span><span class="sxs-lookup"><span data-stu-id="c99b4-228">The following example shows two sample calls to [**FtpRemoveDirectory**](/windows/desktop/api/Wininet/nf-wininet-ftpremovedirectorya).</span></span> <span data-ttu-id="c99b4-229">В обоих вызовах Хфтпсессион — это обработчик сеанса, созданный функцией [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) , а корневой каталог — текущий каталог.</span><span class="sxs-lookup"><span data-stu-id="c99b4-229">In both calls, hFtpSession is the session handle created by the [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function, and the root directory is the current directory.</span></span> <span data-ttu-id="c99b4-230">В корневом каталоге есть каталог с именем Test и каталог «example» в каталоге Test.</span><span class="sxs-lookup"><span data-stu-id="c99b4-230">There is a directory called "test" in the root directory and a directory called "example" in the "test" directory.</span></span>

``` syntax
/* Removes the "example" directory (plus any files/directories it contains) from the "test" directory. */
FtpRemoveDirectory(hFtpSession,"\\test\\example");

/* Removes the "test" directory (plus any files/directories it contains) from the root directory. */
FtpRemoveDirectory(hFtpSession, "test");
```


```C++
FtpRemoveDirectory(hFtpSession,TEXT("\\test\\example"));
/* Removes the "example" directory and any files or 
directories contained in it from the "test" directory. */

FtpRemoveDirectory(hFtpSession, TEXT("test"));
/* Removes the "test" directory and any files or 
directories contained in it from the root directory. */
```



<span data-ttu-id="c99b4-231">В следующем примере создается новый каталог на FTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-231">The following example creates a new directory on the FTP server.</span></span> <span data-ttu-id="c99b4-232">Новое имя каталога берется из поля редактирования родительского диалогового окна, IDC которого передается в параметр *ндирнамеид* .</span><span class="sxs-lookup"><span data-stu-id="c99b4-232">The new directory name is taken from the edit box of the parent dialog whose IDC is passed in the *nDirNameId* parameter.</span></span> <span data-ttu-id="c99b4-233">Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP.</span><span class="sxs-lookup"><span data-stu-id="c99b4-233">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="c99b4-234">Исходный код для функции Дисплайфтпдир, вызываемой в конце, приведен выше.</span><span class="sxs-lookup"><span data-stu-id="c99b4-234">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI CreateFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szNewDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, 
                       szNewDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Create FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpCreateDirectory( hConnection, szNewDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpCreateDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, 
                         nListBoxId ) );
}
```



<span data-ttu-id="c99b4-235">В следующем примере удаляется каталог с FTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="c99b4-235">The following example deletes a directory from the FTP server.</span></span> <span data-ttu-id="c99b4-236">Имя удаляемого каталога берется из поля ввода в родительском диалоговом окне, для которого IDC передается в параметр *ндирнамеид* .</span><span class="sxs-lookup"><span data-stu-id="c99b4-236">The name of the directory to be deleted is taken from the edit box in the parent dialog whose IDC is passed into the *nDirNameId* parameter.</span></span> <span data-ttu-id="c99b4-237">Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP.</span><span class="sxs-lookup"><span data-stu-id="c99b4-237">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="c99b4-238">Исходный код для функции Дисплайфтпдир, вызываемой в конце, приведен выше.</span><span class="sxs-lookup"><span data-stu-id="c99b4-238">The source code for the DisplayFtpDir function called at the end is listed above.</span></span>


```C++
BOOL WINAPI RemoveFtpDir( HWND hDlg, HINTERNET hConnection,
                          int nDirNameId, int nListBoxId )
{
  TCHAR szDelDirName[FTP_FUNCTIONS_BUFFER_SIZE];

  if( !GetDlgItemText( hDlg, nDirNameId, szDelDirName, 
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Error: Directory Name Must Be Specified" ),
                TEXT( "Remove FTP Directory" ), 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRemoveDirectory( hConnection, szDelDirName ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), 
                      TEXT( "FtpRemoveDirectory" ) );
    return( FALSE );
  }

  return( DisplayFtpDir( hDlg, hConnection, 
                         INTERNET_FLAG_RELOAD, nListBoxId ) );
}
```



### <a name="getting-files-on-an-ftp-server"></a><span data-ttu-id="c99b4-239">Получение файлов на FTP-сервере</span><span class="sxs-lookup"><span data-stu-id="c99b4-239">Getting Files on an FTP Server</span></span>

<span data-ttu-id="c99b4-240">Существует три метода извлечения файлов с FTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="c99b4-240">There are three methods for retrieving files from an FTP server:</span></span>

-   <span data-ttu-id="c99b4-241">Используйте [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) и [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="c99b4-241">Use [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="c99b4-242">Используйте [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) и [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span><span class="sxs-lookup"><span data-stu-id="c99b4-242">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile).</span></span>
-   <span data-ttu-id="c99b4-243">Используйте [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span><span class="sxs-lookup"><span data-stu-id="c99b4-243">Use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea).</span></span>

<span data-ttu-id="c99b4-244">Дополнительные сведения об использовании функции [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) см. в разделе [чтение файлов](common-functions.md).</span><span class="sxs-lookup"><span data-stu-id="c99b4-244">For more information about using the [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) function, see [Reading Files](common-functions.md).</span></span>

<span data-ttu-id="c99b4-245">Если URL-адрес файла доступен, приложение может вызвать [**интернетопенурл**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) для подключения к этому URL-адресу, а затем использовать [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) для управления загрузкой файла.</span><span class="sxs-lookup"><span data-stu-id="c99b4-245">If the URL of the file is available, the application can call [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) to connect to that URL, then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to control the download of the file.</span></span> <span data-ttu-id="c99b4-246">Это позволяет более строго контролировать загрузку и идеально подходит для ситуаций, когда на FTP-сервере не нужно вносить никаких других операций.</span><span class="sxs-lookup"><span data-stu-id="c99b4-246">This allows the application tighter control over the download and is ideal for situations where no other operations need to be made on the FTP server.</span></span> <span data-ttu-id="c99b4-247">Дополнительные сведения о непосредственном доступе к ресурсам см. в разделе [доступ к URL-адресам напрямую](handling-uniform-resource-locators.md).</span><span class="sxs-lookup"><span data-stu-id="c99b4-247">For more information about how to directly access resources, see [Accessing URLs Directly](handling-uniform-resource-locators.md).</span></span>

<span data-ttu-id="c99b4-248">Если приложение установило для сервера обработчик FTP-сеанса с помощью [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), приложение может вызвать [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) с существующим именем файла и с новым именем для локального хранимого файла.</span><span class="sxs-lookup"><span data-stu-id="c99b4-248">If the application has established an FTP session handle to the server with [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta), the application can call [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with the existing file name and with a new name for the locally stored file.</span></span> <span data-ttu-id="c99b4-249">Затем приложение может использовать [**интернетреадфиле**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) для загрузки файла.</span><span class="sxs-lookup"><span data-stu-id="c99b4-249">The application can then use [**InternetReadFile**](/windows/desktop/api/Wininet/nf-wininet-internetreadfile) to download the file.</span></span> <span data-ttu-id="c99b4-250">Это позволяет более строго контролировать загрузку и поддерживать подключение к FTP-серверу, что позволяет выполнять дополнительные команды.</span><span class="sxs-lookup"><span data-stu-id="c99b4-250">This allows the application tighter control over the download and keeps the connection to the FTP server, so more commands can be executed.</span></span>

<span data-ttu-id="c99b4-251">Если приложению не требуется тщательный контроль над загрузкой, приложение может использовать [**фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) с обработчиком сеанса FTP, именем удаленного файла и именем локального файла для получения файла.</span><span class="sxs-lookup"><span data-stu-id="c99b4-251">If the application does not need tight control over the download, the application can use [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) with the FTP session handle, remote file name, and local file name to retrieve the file.</span></span> <span data-ttu-id="c99b4-252">[**Фтпжетфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) выполняет все операции по регистрации и издержки, связанные с чтением файла с FTP-сервера и сохранением его на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-252">[**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea) performs all the bookkeeping and overhead associated with reading a file from an FTP server and storing it locally.</span></span>

<span data-ttu-id="c99b4-253">Следующий пример извлекает файл с FTP-сервера и сохраняет его локально.</span><span class="sxs-lookup"><span data-stu-id="c99b4-253">The following example retrieves a file from an FTP server and saves it locally.</span></span> <span data-ttu-id="c99b4-254">Имя файла на FTP-сервере берется из поля ввода в родительском диалоговом окне, в которое передается параметр *нфтпфиленамеид* , а локальное имя, под которым сохраняется файл, берется из поля ввода, которое передается в параметр *нлокалфиленамеид* .</span><span class="sxs-lookup"><span data-stu-id="c99b4-254">The name of the file on the FTP server is taken from the edit box in the parent dialog whose IDC is passed in the *nFtpFileNameId* parameter, and the local name under which the file is saved is taken from the edit box whose IDC is passed in the *nLocalFileNameId* parameter.</span></span> <span data-ttu-id="c99b4-255">Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP.</span><span class="sxs-lookup"><span data-stu-id="c99b4-255">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI GetFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Download FTP File" );
  TCHAR szAsciiQuery[] =
    TEXT("Do you want to download as ASCII text?(Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT( "Target File or Destination File Missing" ),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType = ( MessageBox( hDlg, 
                                 szAsciiQuery, 
                                 szBoxTitle, 
                                 MB_YESNO ) == IDYES ) ?
                   FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;
  dwTransferType |= INTERNET_FLAG_RELOAD;

  if( !FtpGetFile( hConnection, szFtpFileName, szLocalFileName, FALSE,
                   FILE_ATTRIBUTE_NORMAL, dwTransferType, 0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,( dwTransferType == 
                      (FTP_TRANSFER_TYPE_ASCII | INTERNET_FLAG_RELOAD)) ?
                      szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );
}
```



### <a name="placing-files-on-an-ftp-server"></a><span data-ttu-id="c99b4-256">Размещение файлов на FTP-сервере</span><span class="sxs-lookup"><span data-stu-id="c99b4-256">Placing Files on an FTP Server</span></span>

<span data-ttu-id="c99b4-257">Существует два способа размещения файла на FTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-257">There are two methods for placing a file on an FTP server:</span></span>

-   <span data-ttu-id="c99b4-258">Используйте [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) с [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span><span class="sxs-lookup"><span data-stu-id="c99b4-258">Use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) with [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile).</span></span>
-   <span data-ttu-id="c99b4-259">Используйте [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="c99b4-259">Use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>

<span data-ttu-id="c99b4-260">Приложение, которое должно отправить данные на FTP-сервер, но не имеет локального файла, содержащего все данные, должно использовать [**фтпопенфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) для создания и открытия файла на FTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-260">An application that must send data to an FTP server, but does not have a local file that contains all the data, should use [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) to create and open a file on the ftp server.</span></span> <span data-ttu-id="c99b4-261">Затем приложение может использовать [**интернетвритефиле**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) для передачи сведений в файл.</span><span class="sxs-lookup"><span data-stu-id="c99b4-261">The application then can use [**InternetWriteFile**](/windows/desktop/api/Wininet/nf-wininet-internetwritefile) to upload the information to the file.</span></span>

<span data-ttu-id="c99b4-262">Если файл уже существует локально, приложение может использовать [**фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) для передачи файла на FTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="c99b4-262">If the file already exists locally, the application can use [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) to upload the file to the FTP server.</span></span> <span data-ttu-id="c99b4-263">[**Фтппутфиле**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) выполняет все издержки, которые передаются при передаче локального файла на удаленный FTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="c99b4-263">[**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea) performs all the overhead that goes with uploading a local file to a remote FTP server.</span></span>

<span data-ttu-id="c99b4-264">В следующем примере локальный файл копируется на FTP-сервер.</span><span class="sxs-lookup"><span data-stu-id="c99b4-264">The following example copies a local file onto the FTP server.</span></span> <span data-ttu-id="c99b4-265">Локальное имя файла берется из поля ввода в родительском диалоговом окне, IDC которого передается в параметре *нлокалфиленамеид* , а имя, под которым файл сохраняется на FTP-сервере, берется из поля ввода, которое передается в параметр *нфтпфиленамеид* .</span><span class="sxs-lookup"><span data-stu-id="c99b4-265">The local name of the file is taken from the edit box in the parent dialog whose IDC is passed in the *nLocalFileNameId* parameter, and the name under which the file is saved on the FTP server is taken from the edit box whose IDC is passed in the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="c99b4-266">Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP.</span><span class="sxs-lookup"><span data-stu-id="c99b4-266">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span>


```C++
BOOL WINAPI PutFtpFile( HWND hDlg, HINTERNET hConnection,
                        int nFtpFileNameId, int nLocalFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szLocalFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  DWORD dwTransferType;
  TCHAR szBoxTitle[] = TEXT( "Upload FTP File" );
  TCHAR szASCIIQuery[] =
    TEXT("Do you want to upload as ASCII text? (Default is binary)");
  TCHAR szAsciiDone[] = 
    TEXT( "ASCII Transfer completed successfully..." );
  TCHAR szBinaryDone[] = 
    TEXT( "Binary Transfer completed successfully..." );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nLocalFileNameId, szLocalFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, 
                TEXT("Target File or Destination File Missing"),
                szBoxTitle, 
                MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  dwTransferType =
    ( MessageBox( hDlg, 
                  szASCIIQuery, 
                  szBoxTitle, 
                  MB_YESNO ) == IDYES ) ?
    FTP_TRANSFER_TYPE_ASCII : FTP_TRANSFER_TYPE_BINARY;

  if( !FtpPutFile( hConnection, 
                   szLocalFileName, 
                   szFtpFileName, 
                   dwTransferType, 
                   0 ) )
  {
    InternetErrorOut( hDlg, GetLastError( ), TEXT( "FtpGetFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg,
              ( dwTransferType == FTP_TRANSFER_TYPE_ASCII ) ?
                szAsciiDone : szBinaryDone, szBoxTitle, MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="deleting-files-from-an-ftp-server"></a><span data-ttu-id="c99b4-267">Удаление файлов с FTP-сервера</span><span class="sxs-lookup"><span data-stu-id="c99b4-267">Deleting Files from an FTP Server</span></span>

<span data-ttu-id="c99b4-268">Чтобы удалить файл с FTP-сервера, используйте функцию [**фтпделетефиле**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) .</span><span class="sxs-lookup"><span data-stu-id="c99b4-268">To delete a file from an FTP server, use the [**FtpDeleteFile**](/windows/desktop/api/Wininet/nf-wininet-ftpdeletefilea) function.</span></span> <span data-ttu-id="c99b4-269">Вызывающее приложение должно иметь необходимые привилегии для удаления файла с FTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="c99b4-269">The calling application must have the necessary privileges to delete a file from the FTP server.</span></span>

<span data-ttu-id="c99b4-270">В следующем примере файл удаляется с FTP-сервера.</span><span class="sxs-lookup"><span data-stu-id="c99b4-270">The following example deletes a file from the FTP server.</span></span> <span data-ttu-id="c99b4-271">Имя удаляемого файла берется из поля ввода в родительском диалоговом окне, для которого IDC передается параметр *нфтпфиленамеид* int.</span><span class="sxs-lookup"><span data-stu-id="c99b4-271">The name of the file to be deleted is taken from the edit box in the parent dialog whose IDC is passed int the *nFtpFileNameId* parameter.</span></span> <span data-ttu-id="c99b4-272">Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP.</span><span class="sxs-lookup"><span data-stu-id="c99b4-272">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="c99b4-273">Так как эта функция не обновляет списки файлов или отображение каталогов, вызывающий процесс должен сделать это после успешного удаления.</span><span class="sxs-lookup"><span data-stu-id="c99b4-273">Since this function does not refresh file listings or directory display, the calling process should do so upon successful deletion.</span></span>


```C++
BOOL WINAPI DeleteFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nFtpFileNameId )
{
  TCHAR szFtpFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Delete FTP File" );

  if( !GetDlgItemText( hDlg, nFtpFileNameId, szFtpFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg, TEXT( "File Name Must Be Specified!" ),
                szBoxTitle, MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpDeleteFile( hConnection, szFtpFileName ) )
  {
    InternetErrorOut( hDlg, 
                      GetLastError( ), 
                      TEXT( "FtpDeleteFile" ) );
    return( FALSE );
  }

  MessageBox( hDlg, 
              TEXT( "File has been deleted" ), 
              szBoxTitle, 
              MB_OK );
  return( TRUE );  // Remember to refresh directory listing
}
```



### <a name="renaming-files-and-directories-on-an-ftp-server"></a><span data-ttu-id="c99b4-274">Переименование файлов и каталогов на FTP-сервере</span><span class="sxs-lookup"><span data-stu-id="c99b4-274">Renaming Files and Directories on an FTP Server</span></span>

<span data-ttu-id="c99b4-275">Файлы и каталоги на FTP-сервере можно переименовывать с помощью функции [**фтпренамефиле**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) .</span><span class="sxs-lookup"><span data-stu-id="c99b4-275">Files and directories on an FTP server can be renamed using the [**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) function.</span></span> <span data-ttu-id="c99b4-276">[**Фтпренамефиле**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) **принимает две строки**, заканчивающиеся нулем, которые содержат либо частичное, либо полное имя относительно текущего каталога.</span><span class="sxs-lookup"><span data-stu-id="c99b4-276">[**FtpRenameFile**](/windows/desktop/api/Wininet/nf-wininet-ftprenamefilea) accepts two **null**-terminated strings that contain either partially or fully qualified names relative to the current directory.</span></span> <span data-ttu-id="c99b4-277">Функция изменяет имя файла, обозначенного первой строкой, на имя, определяемое второй строкой.</span><span class="sxs-lookup"><span data-stu-id="c99b4-277">The function changes the name of the file designated by the first string to the name designated by the second string.</span></span>

<span data-ttu-id="c99b4-278">В следующем примере переименовывается файл или каталог на FTP-сервере.</span><span class="sxs-lookup"><span data-stu-id="c99b4-278">The following example renames a file or directory on the FTP server.</span></span> <span data-ttu-id="c99b4-279">Текущее имя файла или каталога берется из поля ввода в родительском диалоговом окне, для которого в качестве параметра *нолдфиленамеид* передается значение IDC, а новое имя берется из поля ввода, которое передается в параметр *нневфиленамеид* .</span><span class="sxs-lookup"><span data-stu-id="c99b4-279">The current name of the file or directory is taken from the edit box in the parent dialog whose IDC is passed in the *nOldFileNameId* parameter, and the new name is taken from the edit box whose IDC is passed in the *nNewFileNameId* parameter.</span></span> <span data-ttu-id="c99b4-280">Обработчик *хконнектион* был создан [**интернетконнект**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) после установки сеанса FTP.</span><span class="sxs-lookup"><span data-stu-id="c99b4-280">The *hConnection* handle was created by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) after establishing an FTP session.</span></span> <span data-ttu-id="c99b4-281">Так как эта функция не обновляет списки файлов или отображение каталогов, вызывающий процесс должен сделать это после успешного переименования.</span><span class="sxs-lookup"><span data-stu-id="c99b4-281">Since this function does not refresh file listings or directory display, the calling process should do so upon successful renaming.</span></span>


```C++
BOOL WINAPI RenameFtpFile( HWND hDlg, HINTERNET hConnection,
                           int nOldFileNameId, int nNewFileNameId )
{
  TCHAR szOldFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szNewFileName[FTP_FUNCTIONS_BUFFER_SIZE];
  TCHAR szBoxTitle[] = TEXT( "Rename FTP File" );

  if( !GetDlgItemText( hDlg, nOldFileNameId, szOldFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) ||
      !GetDlgItemText( hDlg, nNewFileNameId, szNewFileName,
                       FTP_FUNCTIONS_BUFFER_SIZE ) )
  {
    MessageBox( hDlg,
        TEXT( "Both the current and new file names must be supplied" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }

  if( !FtpRenameFile( hConnection, szOldFileName, szNewFileName ) )
  {
    MessageBox( hDlg,
        TEXT( "FtpRenameFile failed" ),
        szBoxTitle, 
        MB_OK | MB_ICONERROR );
    return( FALSE );
  }
  return( TRUE );  // Remember to refresh directory listing
}
```



> [!Note]  
> <span data-ttu-id="c99b4-282">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="c99b4-282">WinINet does not support server implementations.</span></span> <span data-ttu-id="c99b4-283">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="c99b4-283">In addition, it should not be used from a service.</span></span> <span data-ttu-id="c99b4-284">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="c99b4-284">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 