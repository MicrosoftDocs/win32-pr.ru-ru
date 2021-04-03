---
description: В этом разделе содержатся сведения об API низкого уровня, используемых инфраструктурой клиента Windows.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Поддержка прочих Low-Level клиентов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895269"
---
# <a name="miscellaneous-low-level-client-support"></a><span data-ttu-id="9f5af-103">Поддержка прочих Low-Level клиентов</span><span class="sxs-lookup"><span data-stu-id="9f5af-103">Miscellaneous Low-Level Client Support</span></span>

<span data-ttu-id="9f5af-104">В этом разделе содержатся сведения об API низкого уровня, используемых инфраструктурой клиента Windows.</span><span class="sxs-lookup"><span data-stu-id="9f5af-104">This topic contains information about low-level APIs that are used by the Windows client infrastructure.</span></span>

### <a name="functions"></a><span data-ttu-id="9f5af-105">Функции</span><span class="sxs-lookup"><span data-stu-id="9f5af-105">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9f5af-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="9f5af-106">Topic</span></span></th>
<th><span data-ttu-id="9f5af-107">Содержимое</span><span class="sxs-lookup"><span data-stu-id="9f5af-107">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9f5af-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-109">Функция _lclose закрывает указанный файл, чтобы он больше не был доступен для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="9f5af-109">The _lclose function closes the specified file so that it is no longer available for reading or writing.</span></span> <span data-ttu-id="9f5af-110">Эта функция обеспечивает совместимость с 16-разрядными версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="9f5af-110">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="9f5af-111">Приложения на основе Win32 должны использовать функцию CloseHandle.</span><span class="sxs-lookup"><span data-stu-id="9f5af-111">Win32-based applications should use the CloseHandle function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-113">Функция _lopen открывает существующий файл и устанавливает указатель файла на начало файла.</span><span class="sxs-lookup"><span data-stu-id="9f5af-113">The _lopen function opens an existing file and sets the file pointer to the beginning of the file.</span></span> <span data-ttu-id="9f5af-114">Эта функция обеспечивает совместимость с 16-разрядными версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="9f5af-114">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="9f5af-115">Приложения на основе Win32 должны использовать функцию CreateFile.</span><span class="sxs-lookup"><span data-stu-id="9f5af-115">Win32-based applications should use the CreateFile function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-117">Функция _lread считывает данные из указанного файла.</span><span class="sxs-lookup"><span data-stu-id="9f5af-117">The _lread function reads data from the specified file.</span></span> <span data-ttu-id="9f5af-118">Эта функция обеспечивает совместимость с 16-разрядными версиями Windows.</span><span class="sxs-lookup"><span data-stu-id="9f5af-118">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="9f5af-119">Приложения на основе Win32 должны использовать функцию ReadFile.</span><span class="sxs-lookup"><span data-stu-id="9f5af-119">Win32-based applications should use the ReadFile function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>аредвдкодексенаблед</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-121">Возвращает значение, указывающее, включены ли на текущем устройстве кодеки DVD.</span><span class="sxs-lookup"><span data-stu-id="9f5af-121">Returns a value indicating whether DVD codecs are enabled on the current device.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>дисаблепроцессвиндовсгхостинг</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-123">Отключает функцию дублирования окна для вызывающего графического пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9f5af-123">Disables the window ghosting feature for the calling GUI process.</span></span> <span data-ttu-id="9f5af-124">Несинхронизированные окна — это функция диспетчера Windows, которая позволяет пользователю легко выполнять, перемещать и закрывать главное окно приложения, которое не отвечает.</span><span class="sxs-lookup"><span data-stu-id="9f5af-124">Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>жетмедиакомпонентпаккажеинфо</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-126">Возвращает список свойств для всех кодеков мультимедиа, установленных в системе в соответствии с указанными требованиями.</span><span class="sxs-lookup"><span data-stu-id="9f5af-126">Returns a list of properties for all media codecs installed on the system that meet the specified requirements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>жетмедиаекстенсионкоммуникатионфактори</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-128">Создает фабрику связи для регистрации расширения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="9f5af-128">Creates a communication factory for registering a media extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>инстантиатекомпонентфромпаккаже</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-130">Создает экземпляр класса в пакете приложения.</span><span class="sxs-lookup"><span data-stu-id="9f5af-130">Creates an instance of a class in an application package.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>исмедиабехавиоренаблед</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-132">Возвращает значение, указывающее, включен ли режим мультимедиа, связанный с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="9f5af-132">Gets a value indicating whether the media behavior associated with the specified GUID is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>нтклосе</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-134">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9f5af-134">Deprecated.</span></span> <span data-ttu-id="9f5af-135">Эта функция используется для закрытия указанного маркера.</span><span class="sxs-lookup"><span data-stu-id="9f5af-135">This function is used to close the specified handle.</span></span> <span data-ttu-id="9f5af-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>Нтклосе</strong></a> заменяется <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="9f5af-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> is superseded by <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>нтдевицеиоконтролфиле</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-138">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9f5af-138">Deprecated.</span></span> <span data-ttu-id="9f5af-139">Создает дескрипторы для предоставляемых буферов и передает нетипизированные данные драйверу устройства, связанному с дескриптором файла.</span><span class="sxs-lookup"><span data-stu-id="9f5af-139">Builds descriptors for the supplied buffer(s) and passes the untyped data to the device driver associated with the file handle.</span></span> <span data-ttu-id="9f5af-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>Нтдевицеиоконтролфиле</strong></a> заменяется <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span><span class="sxs-lookup"><span data-stu-id="9f5af-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> is superseded by <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>нтваитфорсинглеобжект</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-142">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="9f5af-142">Deprecated.</span></span> <span data-ttu-id="9f5af-143">Ожидает, пока указанный объект не выйдет из состояния <code>signaled</code> .</span><span class="sxs-lookup"><span data-stu-id="9f5af-143">Waits until the specified object attains a state of <code>signaled</code>.</span></span> <span data-ttu-id="9f5af-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>Нтваитфорсинглеобжект</strong></a> заменяется объектом <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span><span class="sxs-lookup"><span data-stu-id="9f5af-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> is superseded by <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>ртлансистрингтауникодестринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-146">Преобразует указанную исходную строку ANSI в строку в Юникоде.</span><span class="sxs-lookup"><span data-stu-id="9f5af-146">Converts the specified ANSI source string into a Unicode string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>ртлчартоинтежер</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-148">Преобразует строку символов в целое число.</span><span class="sxs-lookup"><span data-stu-id="9f5af-148">Converts a character string to an integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>ртлформаткуррентусеркэйпас</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-150">Инициализирует указанный буфер строковым представлением идентификатора безопасности для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="9f5af-150">Initializes the supplied buffer with a string representation of the SID for the current user.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>ртлфриансистринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-152">Освобождает строковый буфер, выделенный <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>ртлуникодестрингтоансистринг</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9f5af-152">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>ртлфриоемстринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-154">Освобождает строковый буфер, выделенный <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>ртлуникодестрингтуемстринг</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="9f5af-154">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>ртлфриуникодестринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-156">Освобождает строковый буфер, выделенный <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>ртлансистрингтауникодестринг</strong></a> или <a href="https://msdn.microsoft.com/library/ms803011.aspx">ртлупкасеуникодестринг</a>.</span><span class="sxs-lookup"><span data-stu-id="9f5af-156">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> or by <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>ртлинитстринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-158">Инициализирует подсчитанную строку.</span><span class="sxs-lookup"><span data-stu-id="9f5af-158">Initializes a counted string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>ртлинитуникодестринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-160">Инициализирует подсчитанную строку Юникода.</span><span class="sxs-lookup"><span data-stu-id="9f5af-160">Initializes a counted Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>ртлуникодестрингтоансистринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-162">Преобразует указанную исходную строку Юникода в строку ANSI.</span><span class="sxs-lookup"><span data-stu-id="9f5af-162">Converts the specified Unicode source string into an ANSI string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>ртлуникодестрингтуемстринг</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-164">Эта функция преобразует указанную исходную строку Юникода в строку OEM.</span><span class="sxs-lookup"><span data-stu-id="9f5af-164">This functions converts the specified Unicode source string into an OEM string.</span></span> <span data-ttu-id="9f5af-165">Преобразование выполняется в соответствии с кодовой страницей OEM (OCP).</span><span class="sxs-lookup"><span data-stu-id="9f5af-165">The translation is done with respect to the OEM code page (OCP).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>ртлуникодетомултибитесизе</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-167">Определяет, сколько байтов необходимо для представления строки Юникода в виде строки ANSI.</span><span class="sxs-lookup"><span data-stu-id="9f5af-167">Determines how many bytes are needed to represent a Unicode string as an ANSI string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-169">Функция <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> преобразует указанную строку Юникода в новую символьную строку, используя 8-разрядную кодовую страницу формата преобразования Юникода (UTF-8).</span><span class="sxs-lookup"><span data-stu-id="9f5af-169">The <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> function translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-171">Функция <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> преобразует указанную исходную строку в строку в Юникоде, используя кодовую страницу UTF-8.</span><span class="sxs-lookup"><span data-stu-id="9f5af-171">The <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> function translates the specified source string into a Unicode string, using the UTF-8 code page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9f5af-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>сендимемессажеекс</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-173">Задает действие или обработку для редактора метода ввода (IME) с помощью указанной подфункции.</span><span class="sxs-lookup"><span data-stu-id="9f5af-173">Specifies an action or processing for the Input Method Editor (IME) through a specified subfunction.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f5af-174">Эта функция устарела и не должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="9f5af-174">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9f5af-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>виннлсенаблеиме</strong></a></span><span class="sxs-lookup"><span data-stu-id="9f5af-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span></span></td>
<td><span data-ttu-id="9f5af-176">Временно включает или отключает редактор IME и в то же время включает или отключает отображение всех окон, принадлежащих редактору IME.</span><span class="sxs-lookup"><span data-stu-id="9f5af-176">Temporarily enables or disables an IME and, at the same time, turns on or off the display of all windows owned by the IME.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="9f5af-177">Эта функция устарела и не должна использоваться.</span><span class="sxs-lookup"><span data-stu-id="9f5af-177">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a><span data-ttu-id="9f5af-178">Структуры</span><span class="sxs-lookup"><span data-stu-id="9f5af-178">Structures</span></span>



| <span data-ttu-id="9f5af-179">Раздел</span><span class="sxs-lookup"><span data-stu-id="9f5af-179">Topic</span></span>                                 | <span data-ttu-id="9f5af-180">Содержимое</span><span class="sxs-lookup"><span data-stu-id="9f5af-180">Contents</span></span>                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f5af-181">**иместрукт**</span><span class="sxs-lookup"><span data-stu-id="9f5af-181">**IMESTRUCT**</span></span>](/windows/win32/api/ime/ns-ime-imestruct) | <span data-ttu-id="9f5af-182">Используется функцией [**сендимемессажеекс**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) для указания подфункции, выполняемой в сообщении IME и его параметрах.</span><span class="sxs-lookup"><span data-stu-id="9f5af-182">Used by [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) to specify the subfunction to be executed in the IME message and its parameters.</span></span> <span data-ttu-id="9f5af-183">Эта структура также используется для получения возвращаемых значений из этих подфункций.</span><span class="sxs-lookup"><span data-stu-id="9f5af-183">This structure is also used to receive return values from those subfunctions.</span></span><br/> |
| [<span data-ttu-id="9f5af-184">**STRING**</span><span class="sxs-lookup"><span data-stu-id="9f5af-184">**STRING**</span></span>](/windows/desktop/api/Winternl/ns-winternl-string)       | <span data-ttu-id="9f5af-185">Эта структура используется с функцией [**ртлуникодестрингтуемстринг**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) .</span><span class="sxs-lookup"><span data-stu-id="9f5af-185">This structure is used with the [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) function.</span></span> <br/>                                                                                                              |



 

### <a name="compiler-routines"></a><span data-ttu-id="9f5af-186">Подпрограммы компилятора</span><span class="sxs-lookup"><span data-stu-id="9f5af-186">Compiler Routines</span></span>



| <span data-ttu-id="9f5af-187">Раздел</span><span class="sxs-lookup"><span data-stu-id="9f5af-187">Topic</span></span>                                                             | <span data-ttu-id="9f5af-188">Содержимое</span><span class="sxs-lookup"><span data-stu-id="9f5af-188">Contents</span></span>                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f5af-189">**\_\_Подпрограммы для \_ конкретного \_ обработчика C**</span><span class="sxs-lookup"><span data-stu-id="9f5af-189">**\_\_C\_specific\_handler Routine**</span></span>](--c-specific-handler2.md) | <span data-ttu-id="9f5af-190">[**\_ \_ \_ Специальный \_ обработчик c**](--c-specific-handler2.md) — это вспомогательная подпрограммы для компилятора C.</span><span class="sxs-lookup"><span data-stu-id="9f5af-190">[**\_\_C\_specific\_handler**](--c-specific-handler2.md) is a helper routine for the C compiler.</span></span><br/> |
| [<span data-ttu-id="9f5af-191">\_подпрограммы аллдив</span><span class="sxs-lookup"><span data-stu-id="9f5af-191">\_alldiv Routine</span></span>](-win32-alldiv.md)                             | <span data-ttu-id="9f5af-192">[ \_ подпрограммы аллдив](-win32-alldiv.md) — это вспомогательная подпрограммы для компилятора C.</span><span class="sxs-lookup"><span data-stu-id="9f5af-192">[\_alldiv Routine](-win32-alldiv.md) is a helper routine for the C compiler.</span></span><br/>                     |
| [<span data-ttu-id="9f5af-193">\_аллмул</span><span class="sxs-lookup"><span data-stu-id="9f5af-193">\_allmul</span></span>](-win32-allmul.md) | <span data-ttu-id="9f5af-194">Умножает два **лонглонг** или **улонглонг**.</span><span class="sxs-lookup"><span data-stu-id="9f5af-194">Multiplies two **LONGLONG** or **ULONGLONG**.</span></span> |
| [<span data-ttu-id="9f5af-195">\_ауллдив</span><span class="sxs-lookup"><span data-stu-id="9f5af-195">\_aulldiv</span></span>](-win32-aulldiv.md) | <span data-ttu-id="9f5af-196">Делит два целых числа **улонглонг** .</span><span class="sxs-lookup"><span data-stu-id="9f5af-196">Divides two **ULONGLONG** integers.</span></span> |
| [<span data-ttu-id="9f5af-197">\_подпрограммы чкстк</span><span class="sxs-lookup"><span data-stu-id="9f5af-197">\_chkstk Routine</span></span>](-win32-chkstk.md)                             | <span data-ttu-id="9f5af-198">[ \_ подпрограммы чкстк](-win32-chkstk.md) — это вспомогательная подпрограммы для компилятора C.</span><span class="sxs-lookup"><span data-stu-id="9f5af-198">[\_chkstk Routine](-win32-chkstk.md) is a helper routine for the C compiler.</span></span><br/>                     |
