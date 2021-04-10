---
description: Функция Аддпринтер добавляет принтер в список поддерживаемых принтеров для указанного сервера.
ms.assetid: ffc4fee8-46c6-47ad-803d-623bf8efdefd
title: Функция Аддпринтер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinter
- AddPrinterA
- AddPrinterW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 51416ed59bc1c6df1d2c69de87d61bdecab522f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104264345"
---
# <a name="addprinter-function"></a><span data-ttu-id="354e7-103">Функция Аддпринтер</span><span class="sxs-lookup"><span data-stu-id="354e7-103">AddPrinter function</span></span>

<span data-ttu-id="354e7-104">Функция **аддпринтер** добавляет принтер в список поддерживаемых принтеров для указанного сервера.</span><span class="sxs-lookup"><span data-stu-id="354e7-104">The **AddPrinter** function adds a printer to the list of supported printers for a specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="354e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="354e7-105">Syntax</span></span>


```C++
HANDLE AddPrinter(
  _In_ LPTSTR *pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="354e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="354e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="354e7-107">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="354e7-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="354e7-108">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором должен быть установлен принтер.</span><span class="sxs-lookup"><span data-stu-id="354e7-108">A pointer to a null-terminated string that specifies the name of the server on which the printer should be installed.</span></span> <span data-ttu-id="354e7-109">Если эта строка имеет **значение NULL**, принтер устанавливается локально.</span><span class="sxs-lookup"><span data-stu-id="354e7-109">If this string is **NULL**, the printer is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="354e7-110">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="354e7-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="354e7-111">Версия структуры, на которую указывает *ппринтер* .</span><span class="sxs-lookup"><span data-stu-id="354e7-111">The version of the structure to which *pPrinter* points.</span></span> <span data-ttu-id="354e7-112">Это значение должно быть равно 2.</span><span class="sxs-lookup"><span data-stu-id="354e7-112">This value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="354e7-113">*ппринтер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="354e7-113">*pPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="354e7-114">Указатель на структуру [**\_ \_ 2 принтера**](printer-info-2.md) , содержащий сведения о принтере.</span><span class="sxs-lookup"><span data-stu-id="354e7-114">A pointer to a [**PRINTER\_INFO\_2**](printer-info-2.md) structure that contains information about the printer.</span></span> <span data-ttu-id="354e7-115">Перед вызовом **аддпринтер** необходимо указать значения, отличные от **null** , для элементов **ппринтернаме**, **ппортнаме**, **пдривернаме** и **ппринтпроцессор** этой структуры.</span><span class="sxs-lookup"><span data-stu-id="354e7-115">You must specify non-**NULL** values for the **pPrinterName**, **pPortName**, **pDriverName**, and **pPrintProcessor** members of this structure before calling **AddPrinter**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="354e7-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="354e7-116">Return value</span></span>

<span data-ttu-id="354e7-117">Если функция выполнена, возвращаемое значение является обработчиком (непотокобезопасным) для нового объекта принтера.</span><span class="sxs-lookup"><span data-stu-id="354e7-117">If the function succeeds, the return value is a handle (not thread safe) to a new printer object.</span></span> <span data-ttu-id="354e7-118">По завершении работы с маркером передайте его в функцию [**клосепринтер**](closeprinter.md) , чтобы закрыть его.</span><span class="sxs-lookup"><span data-stu-id="354e7-118">When you are finished with the handle, pass it to the [**ClosePrinter**](closeprinter.md) function to close it.</span></span>

<span data-ttu-id="354e7-119">Если функция завершается ошибкой, возвращается значение **null**.</span><span class="sxs-lookup"><span data-stu-id="354e7-119">If the function fails, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="354e7-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="354e7-120">Remarks</span></span>

<span data-ttu-id="354e7-121">Не вызывайте этот метод в [**DllMain**](/windows/desktop/Dlls/dllmain).</span><span class="sxs-lookup"><span data-stu-id="354e7-121">Do not call this method in [**DllMain**](/windows/desktop/Dlls/dllmain).</span></span>

> [!Note]  
> <span data-ttu-id="354e7-122">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="354e7-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="354e7-123">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="354e7-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="354e7-124">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="354e7-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="354e7-125">Вызывающий объект должен иметь [селоаддриверпривилеже](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="354e7-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="354e7-126">Возвращенный маркер не является потокобезопасным.</span><span class="sxs-lookup"><span data-stu-id="354e7-126">The returned handle is not thread safe.</span></span> <span data-ttu-id="354e7-127">Если вызывающие объекты должны одновременно использовать его в нескольких потоках, они должны предоставить настраиваемый доступ к обработке принтера с помощью [функций синхронизации](/windows/desktop/Sync/synchronization-functions).</span><span class="sxs-lookup"><span data-stu-id="354e7-127">If callers need to use it concurrently on multiple threads, they must provide custom synchronization access to the printer handle using the [Synchronization Functions](/windows/desktop/Sync/synchronization-functions).</span></span> <span data-ttu-id="354e7-128">Чтобы избежать написания пользовательского кода, приложение может по мере необходимости открывать маркеры принтера в каждом потоке.</span><span class="sxs-lookup"><span data-stu-id="354e7-128">To avoid writing custom code the application can open a printer handle on each thread, as needed.</span></span>

<span data-ttu-id="354e7-129">Ниже приведены элементы структуры « [**\_ сведения о принтере \_ 2**](printer-info-2.md) », которые можно задать до вызова функции **аддпринтер** .</span><span class="sxs-lookup"><span data-stu-id="354e7-129">The following are the members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure that can be set before the **AddPrinter** function is called:</span></span>

-   <span data-ttu-id="354e7-130">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="354e7-130">**Attributes**</span></span>
-   <span data-ttu-id="354e7-131">**ппринтпроцессор**</span><span class="sxs-lookup"><span data-stu-id="354e7-131">**pPrintProcessor**</span></span>
-   <span data-ttu-id="354e7-132">**дефаултприорити**</span><span class="sxs-lookup"><span data-stu-id="354e7-132">**DefaultPriority**</span></span>
-   <span data-ttu-id="354e7-133">**Приоритет**</span><span class="sxs-lookup"><span data-stu-id="354e7-133">**Priority**</span></span>
-   <span data-ttu-id="354e7-134">**пкоммент**</span><span class="sxs-lookup"><span data-stu-id="354e7-134">**pComment**</span></span>
-   <span data-ttu-id="354e7-135">**псекуритидескриптор**</span><span class="sxs-lookup"><span data-stu-id="354e7-135">**pSecurityDescriptor**</span></span>
-   <span data-ttu-id="354e7-136">**пдататипе**</span><span class="sxs-lookup"><span data-stu-id="354e7-136">**pDatatype**</span></span>
-   <span data-ttu-id="354e7-137">**псепфиле**</span><span class="sxs-lookup"><span data-stu-id="354e7-137">**pSepFile**</span></span>
-   <span data-ttu-id="354e7-138">**пдевмоде**</span><span class="sxs-lookup"><span data-stu-id="354e7-138">**pDevMode**</span></span>
-   <span data-ttu-id="354e7-139">**пшаренаме**</span><span class="sxs-lookup"><span data-stu-id="354e7-139">**pShareName**</span></span>
-   <span data-ttu-id="354e7-140">**плокатион**</span><span class="sxs-lookup"><span data-stu-id="354e7-140">**pLocation**</span></span>
-   <span data-ttu-id="354e7-141">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="354e7-141">**StartTime**</span></span>
-   <span data-ttu-id="354e7-142">**ппараметерс**</span><span class="sxs-lookup"><span data-stu-id="354e7-142">**pParameters**</span></span>
-   <span data-ttu-id="354e7-143">**унтилтиме**</span><span class="sxs-lookup"><span data-stu-id="354e7-143">**UntilTime**</span></span>

<span data-ttu-id="354e7-144">Элементы **Status**, **кжобс** и **Аверажеппм** структуры " [**\_ сведения о \_ принтере**](printer-info-2.md) " зарезервированы для использования функцией [**PrintOut**](getprinter.md) .</span><span class="sxs-lookup"><span data-stu-id="354e7-144">The **Status**, **cJobs**, and **AveragePPM** members of the [**PRINTER\_INFO\_2**](printer-info-2.md) structure are reserved for use by the [**GetPrinter**](getprinter.md) function.</span></span> <span data-ttu-id="354e7-145">Их не следует задавать перед вызовом **аддпринтер**.</span><span class="sxs-lookup"><span data-stu-id="354e7-145">They must not be set before calling **AddPrinter**.</span></span>

<span data-ttu-id="354e7-146">Если **псекуритидескриптор** имеет **значение NULL**, система присваивает принтеру дескриптор безопасности по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="354e7-146">If **pSecurityDescriptor** is **NULL**, the system assigns a default security descriptor to the printer.</span></span> <span data-ttu-id="354e7-147">Дескриптор безопасности по умолчанию имеет следующие разрешения.</span><span class="sxs-lookup"><span data-stu-id="354e7-147">The default security descriptor has the following permissions.</span></span>



| <span data-ttu-id="354e7-148">Значение</span><span class="sxs-lookup"><span data-stu-id="354e7-148">Value</span></span>                          | <span data-ttu-id="354e7-149">Описание</span><span class="sxs-lookup"><span data-stu-id="354e7-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354e7-150">Администраторы и опытные пользователи.</span><span class="sxs-lookup"><span data-stu-id="354e7-150">Administrators and Power Users</span></span> | <span data-ttu-id="354e7-151">Полный доступ к очереди печати.</span><span class="sxs-lookup"><span data-stu-id="354e7-151">Full control on the print queue.</span></span> <span data-ttu-id="354e7-152">Это означает, что члены этих групп могут печатать, управлять очередью (может удалять очередь, изменять любые параметры очереди, включая дескриптор безопасности) и управлять заданиями печати всех пользователей (удаление, приостановка, возобновление и перезапуск заданий). Обратите внимание, что опытные пользователи не существуют до Windows XP Professional.</span><span class="sxs-lookup"><span data-stu-id="354e7-152">This means members of these groups can print, manage the queue (can delete the queue, change any setting of the queue, including the security descriptor), and manage the print jobs of all users (delete, pause, resume, restart jobs).Note that Power Users do not exist before Windows XP Professional.</span></span><br/> |
| <span data-ttu-id="354e7-153">Создатель/владелец</span><span class="sxs-lookup"><span data-stu-id="354e7-153">Creator/Owner</span></span>                  | <span data-ttu-id="354e7-154">Может управлять собственными заданиями.</span><span class="sxs-lookup"><span data-stu-id="354e7-154">Can manage own jobs.</span></span> <span data-ttu-id="354e7-155">Это означает, что пользователь, отправивший задания, может управлять своими заданиями (удалять, приостанавливать, возобновлять, перезапускать).</span><span class="sxs-lookup"><span data-stu-id="354e7-155">This means that user who submit jobs can manage (delete, pause, resume, restart) their own jobs.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="354e7-156">Все</span><span class="sxs-lookup"><span data-stu-id="354e7-156">Everyone</span></span>                       | <span data-ttu-id="354e7-157">Выполнение и Стандартный контроль чтения.</span><span class="sxs-lookup"><span data-stu-id="354e7-157">Execute and standard read control.</span></span> <span data-ttu-id="354e7-158">Это означает, что члены группы «все» могут печатать и читать свойства очереди печати.</span><span class="sxs-lookup"><span data-stu-id="354e7-158">This means that members of the everyone group can print and read properties of the print queue.</span></span>                                                                                                                                                                                                                     |



 

<span data-ttu-id="354e7-159">После того как приложение создает объект принтера с помощью функции **аддпринтер** , он должен использовать функцию [**принтерпропертиес**](printerproperties.md) для указания правильных параметров драйвера принтера, связанного с объектом Printer.</span><span class="sxs-lookup"><span data-stu-id="354e7-159">After an application creates a printer object with the **AddPrinter** function, it must use the [**PrinterProperties**](printerproperties.md) function to specify the correct settings for the printer driver associated with the printer object.</span></span>

<span data-ttu-id="354e7-160">Функция **аддпринтер** возвращает ошибку, если объект принтера с таким именем уже существует, если этот объект не помечен как ожидающий удаления.</span><span class="sxs-lookup"><span data-stu-id="354e7-160">The **AddPrinter** function returns an error if a printer object with the same name already exists, unless that object is marked as pending deletion.</span></span> <span data-ttu-id="354e7-161">В этом случае существующий принтер не удаляется, а параметры создания **аддпринтер** используются для изменения существующих параметров принтера (как если бы приложение использовало функцию [**сетпринтер**](setprinter.md) ).</span><span class="sxs-lookup"><span data-stu-id="354e7-161">In that case, the existing printer is not deleted, and the **AddPrinter** creation parameters are used to change the existing printer settings (as if the application had used the [**SetPrinter**](setprinter.md) function).</span></span>

<span data-ttu-id="354e7-162">Используйте функцию [**енумпринтпроцессорс**](enumprintprocessors.md) для перечисления набора обработчиков печати, установленных на сервере.</span><span class="sxs-lookup"><span data-stu-id="354e7-162">Use the [**EnumPrintProcessors**](enumprintprocessors.md) function to enumerate the set of print processors installed on a server.</span></span> <span data-ttu-id="354e7-163">Используйте функцию [**енумпринтпроцессордататипес**](enumprintprocessordatatypes.md) для перечисления набора типов данных, поддерживаемых обработчиком печати.</span><span class="sxs-lookup"><span data-stu-id="354e7-163">Use the [**EnumPrintProcessorDatatypes**](enumprintprocessordatatypes.md) function to enumerate the set of data types that a print processor supports.</span></span> <span data-ttu-id="354e7-164">Используйте функцию [**енумпортс**](enumports.md) для перечисления набора доступных портов.</span><span class="sxs-lookup"><span data-stu-id="354e7-164">Use the [**EnumPorts**](enumports.md) function to enumerate the set of available ports.</span></span> <span data-ttu-id="354e7-165">Используйте функцию [**енумпринтердриверс**](enumprinterdrivers.md) для перечисления установленных драйверов принтера.</span><span class="sxs-lookup"><span data-stu-id="354e7-165">Use the [**EnumPrinterDrivers**](enumprinterdrivers.md) function to enumerate the installed printer drivers.</span></span>

<span data-ttu-id="354e7-166">Вызывающая функция **аддпринтер** должна иметь доступ к серверу \_ для \_ администрирования доступа к серверу, на котором будет создан принтер.</span><span class="sxs-lookup"><span data-stu-id="354e7-166">The caller of the **AddPrinter** function must have SERVER\_ACCESS\_ADMINISTER access to the server on which the printer is to be created.</span></span> <span data-ttu-id="354e7-167">Маркер, возвращаемый функцией, будет иметь \_ \_ разрешение на доступ к принтеру и может использоваться для выполнения административных операций на принтере.</span><span class="sxs-lookup"><span data-stu-id="354e7-167">The handle returned by the function will have PRINTER\_ALL\_ACCESS permission, and can be used to perform administrative operations on the printer.</span></span>

<span data-ttu-id="354e7-168">Если функции **дрвпринтеревент** передается \_ флаг события принтера \_ \_ без \_ флага пользовательского интерфейса, драйвер не должен использовать вызов пользовательского интерфейса во время **дрвпринтеревент**.</span><span class="sxs-lookup"><span data-stu-id="354e7-168">If the **DrvPrinterEvent** function is passed the PRINTER\_EVENT\_FLAG\_NO\_UI flag, the driver should not use a UI call during **DrvPrinterEvent**.</span></span> <span data-ttu-id="354e7-169">Чтобы выполнять задания, связанные с пользовательским интерфейсом, установщик должен либо использовать запись **вендорсетуп** в INF-файле принтера, либо, для устройств Самонастраивающийся, установщик может использовать соустановщик для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="354e7-169">To do UI-related jobs, the installer should either use the **VendorSetup** entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="354e7-170">Дополнительные сведения о **вендорсетуп** см. в пакете средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="354e7-170">For more information about **VendorSetup**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

<span data-ttu-id="354e7-171">Брандмауэр подключения к Интернету (ICF) блокирует порты принтера по умолчанию, но при запуске **аддпринтер** включается исключение для общего доступа к файлам и принтерам.</span><span class="sxs-lookup"><span data-stu-id="354e7-171">The Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing is enabled when you run **AddPrinter**.</span></span>

## <a name="requirements"></a><span data-ttu-id="354e7-172">Требования</span><span class="sxs-lookup"><span data-stu-id="354e7-172">Requirements</span></span>



| <span data-ttu-id="354e7-173">Требование</span><span class="sxs-lookup"><span data-stu-id="354e7-173">Requirement</span></span> | <span data-ttu-id="354e7-174">Значение</span><span class="sxs-lookup"><span data-stu-id="354e7-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="354e7-175">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="354e7-175">Minimum supported client</span></span><br/> | <span data-ttu-id="354e7-176">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="354e7-176">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="354e7-177">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="354e7-177">Minimum supported server</span></span><br/> | <span data-ttu-id="354e7-178">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="354e7-178">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="354e7-179">Заголовок</span><span class="sxs-lookup"><span data-stu-id="354e7-179">Header</span></span><br/>                   | <dl> <span data-ttu-id="354e7-180"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="354e7-180"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="354e7-181">Библиотека</span><span class="sxs-lookup"><span data-stu-id="354e7-181">Library</span></span><br/>                  | <dl> <span data-ttu-id="354e7-182"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="354e7-182"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="354e7-183">DLL</span><span class="sxs-lookup"><span data-stu-id="354e7-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="354e7-184"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="354e7-184"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="354e7-185">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="354e7-185">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="354e7-186">**Аддпринтерв** (Юникод) и **аддпринтера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="354e7-186">**AddPrinterW** (Unicode) and **AddPrinterA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="354e7-187">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="354e7-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="354e7-188">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="354e7-188">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="354e7-189">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="354e7-189">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="354e7-190">**клосепринтер**</span><span class="sxs-lookup"><span data-stu-id="354e7-190">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="354e7-191">**делетепринтер**</span><span class="sxs-lookup"><span data-stu-id="354e7-191">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="354e7-192">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="354e7-192">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="354e7-193">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="354e7-193">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="354e7-194">**енумпринтпроцессорс**</span><span class="sxs-lookup"><span data-stu-id="354e7-194">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="354e7-195">**енумпринтпроцессордататипес**</span><span class="sxs-lookup"><span data-stu-id="354e7-195">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md)
</dt> <dt>

[<span data-ttu-id="354e7-196">**Наложение**</span><span class="sxs-lookup"><span data-stu-id="354e7-196">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="354e7-197">**\_Сведения о принтере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="354e7-197">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="354e7-198">**принтерпропертиес**</span><span class="sxs-lookup"><span data-stu-id="354e7-198">**PrinterProperties**</span></span>](printerproperties.md)
</dt> <dt>

[<span data-ttu-id="354e7-199">**сетпринтер**</span><span class="sxs-lookup"><span data-stu-id="354e7-199">**SetPrinter**</span></span>](setprinter.md)
</dt> </dl>

 

