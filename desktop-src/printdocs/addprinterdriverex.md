---
description: Функция Аддпринтердриверекс устанавливает локальный или удаленный драйвер принтера и связывает файлы конфигурации, данных и драйверов.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: Функция Аддпринтердриверекс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673636"
---
# <a name="addprinterdriverex-function"></a><span data-ttu-id="8185e-103">Функция Аддпринтердриверекс</span><span class="sxs-lookup"><span data-stu-id="8185e-103">AddPrinterDriverEx function</span></span>

<span data-ttu-id="8185e-104">Функция **аддпринтердриверекс** устанавливает локальный или удаленный драйвер принтера и связывает файлы конфигурации, данных и драйверов.</span><span class="sxs-lookup"><span data-stu-id="8185e-104">The **AddPrinterDriverEx** function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="8185e-105">Помимо возможностей [**аддпринтердривер**](addprinterdriver.md), у нее также есть параметры, обеспечивающие жесткое обновление, более пониженную версию, копирование только новых файлов и копирование всех файлов (независимо от отметки времени файла).</span><span class="sxs-lookup"><span data-stu-id="8185e-105">Besides having the capabilities of [**AddPrinterDriver**](addprinterdriver.md), it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="8185e-106">Установка драйвера принтера без пакета драйверов больше не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="8185e-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="8185e-107">Вместо этого используйте [**инсталлпринтердриверфромпаккаже**](installprinterdriverfrompackage.md) .</span><span class="sxs-lookup"><span data-stu-id="8185e-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="8185e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8185e-108">Syntax</span></span>


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8185e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8185e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8185e-110">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8185e-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8185e-111">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором должен быть установлен драйвер.</span><span class="sxs-lookup"><span data-stu-id="8185e-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span> <span data-ttu-id="8185e-112">Если этот параметр имеет **значение NULL**, функция устанавливает драйвер на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8185e-112">If this parameter is **NULL**, the function installs the driver on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8185e-113">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8185e-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8185e-114">Версия структуры, на которую указывает *пдриверинфо* .</span><span class="sxs-lookup"><span data-stu-id="8185e-114">The version of the structure to which *pDriverInfo* points.</span></span> <span data-ttu-id="8185e-115">Это значение может быть равно 2, 3, 4, 6 или 8.</span><span class="sxs-lookup"><span data-stu-id="8185e-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="8185e-116">*пдриверинфо* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="8185e-116">*pDriverInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8185e-117">Указатель на структуру, содержащую сведения о драйвере принтера.</span><span class="sxs-lookup"><span data-stu-id="8185e-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="8185e-118">Может быть одним из следующих.</span><span class="sxs-lookup"><span data-stu-id="8185e-118">It can be one of the following.</span></span>



| <span data-ttu-id="8185e-119">Значение уровня</span><span class="sxs-lookup"><span data-stu-id="8185e-119">Value of Level</span></span>                                                                                       | <span data-ttu-id="8185e-120">\_Структура сведений о драйвере \_ \*</span><span class="sxs-lookup"><span data-stu-id="8185e-120">DRIVER\_INFO\_\* Structure</span></span>                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <span data-ttu-id="8185e-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="8185e-122">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8185e-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="8185e-123"><dt>**3-5**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="8185e-124">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="8185e-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="8185e-125"><dt>**четырех**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="8185e-126">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8185e-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="8185e-127"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-127"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="8185e-128">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="8185e-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="8185e-129"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-129"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="8185e-130">**\_Сведения о драйвере \_ 8**</span><span class="sxs-lookup"><span data-stu-id="8185e-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

<span data-ttu-id="8185e-131">Если элемент **пенвиронмент** структуры, на который указывает *Пдриверинфо* , имеет **значение NULL**, функция использует текущую среду вызывающего или клиентского объекта, а не среду назначения или сервера.</span><span class="sxs-lookup"><span data-stu-id="8185e-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the function uses the current environment of the caller/client, not the environment of the destination/server.</span></span>

</dd> <dt>

<span data-ttu-id="8185e-132">*двфилекопифлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8185e-132">*dwFileCopyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8185e-133">Параметры для копирования файлов драйверов.</span><span class="sxs-lookup"><span data-stu-id="8185e-133">The options for copying the driver files.</span></span> <span data-ttu-id="8185e-134">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="8185e-134">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8185e-135">Значение</span><span class="sxs-lookup"><span data-stu-id="8185e-135">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="8185e-136">Значение</span><span class="sxs-lookup"><span data-stu-id="8185e-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <span data-ttu-id="8185e-137"><dt>**APD \_ Копировать \_ все \_ файлы**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-137"><dt>**APD\_COPY\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="8185e-138">Добавьте драйвер принтера и скопируйте все файлы в каталог драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="8185e-138">Add the printer driver and copy all the files in the printer-driver directory.</span></span> <span data-ttu-id="8185e-139">Метки времени файла игнорируются этим параметром.</span><span class="sxs-lookup"><span data-stu-id="8185e-139">The file time stamps are ignored with this option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <span data-ttu-id="8185e-140"><dt>**APD \_ Копировать \_ из \_ каталога**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-140"><dt>**APD\_COPY\_FROM\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="8185e-141">Добавьте драйвер принтера с полными именами файлов, указанными в структуре [**драйвера \_ \_ 6**](driver-info-6.md) .</span><span class="sxs-lookup"><span data-stu-id="8185e-141">Add the printer driver using the fully qualified file names specified in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure.</span></span> <span data-ttu-id="8185e-142">Этот флаг ORed в сочетании с одним из других флагов копирования.</span><span class="sxs-lookup"><span data-stu-id="8185e-142">This flag is ORed in conjunction with one of the other copy flags.</span></span> <span data-ttu-id="8185e-143">Если этот флаг установлен, **аддпринтердриверекс** завершится ошибкой, если файлы, где они указаны, существуют в структуре **драйвера \_ \_ 6** .</span><span class="sxs-lookup"><span data-stu-id="8185e-143">If this flag is set, **AddPrinterDriverEx** will fail if the files do not exist where they are specified to exist by the **DRIVER\_INFO\_6** structure.</span></span> <span data-ttu-id="8185e-144">Файлы не нужно копировать в каталог драйвера принтера системы.</span><span class="sxs-lookup"><span data-stu-id="8185e-144">The files do not need to be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="8185e-145">См. примечания.</span><span class="sxs-lookup"><span data-stu-id="8185e-145">See the Remarks.</span></span><br/> <span data-ttu-id="8185e-146">**Windows 2000:** Этот флаг не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="8185e-146">**Windows 2000:** This flag is not supported.</span></span><br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <span data-ttu-id="8185e-147"><dt>**APD \_ Копировать \_ новые \_ файлы**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-147"><dt>**APD\_COPY\_NEW\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="8185e-148">Добавьте драйвер принтера и скопируйте файлы в каталог драйвера принтера, который новее, чем все файлы, используемые в данный момент.</span><span class="sxs-lookup"><span data-stu-id="8185e-148">Add the printer driver and copy the files in the printer-driver directory that are newer than any corresponding files that are currently in use.</span></span> <span data-ttu-id="8185e-149">Этот флаг эмулирует поведение [**аддпринтердривер**](addprinterdriver.md).</span><span class="sxs-lookup"><span data-stu-id="8185e-149">This flag emulates the behavior of [**AddPrinterDriver**](addprinterdriver.md).</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <span data-ttu-id="8185e-150"><dt>**APD \_ с \_ пониженным уровнем**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-150"><dt>**APD\_STRICT\_DOWNGRADE**</dt></span></span> </dl>           | <span data-ttu-id="8185e-151">Добавьте драйвер принтера, только если все файлы в каталоге драйвера принтера старше всех файлов, используемых в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="8185e-151">Add the printer driver only if all the files in the printer-driver directory are older than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <span data-ttu-id="8185e-152"><dt>**APD с \_ четким \_ обновлением**</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-152"><dt>**APD\_STRICT\_UPGRADE**</dt></span></span> </dl>                 | <span data-ttu-id="8185e-153">Добавьте драйвер принтера, только если все файлы в каталоге драйвера принтера новее, чем все файлы, используемые в настоящее время.</span><span class="sxs-lookup"><span data-stu-id="8185e-153">Add the printer driver only if all the files in the printer-driver directory are newer than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8185e-154">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8185e-154">Return value</span></span>

<span data-ttu-id="8185e-155">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="8185e-155">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="8185e-156">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="8185e-156">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="8185e-157">Если известно, что драйвер принтера не работает с операционной системой, **аддпринтердриверекс** завершится с одним из следующих кодов ошибок:</span><span class="sxs-lookup"><span data-stu-id="8185e-157">If the printer driver is known to have problems working with the operating system, **AddPrinterDriverEx** will fail with one of the following error codes:</span></span>



| <span data-ttu-id="8185e-158">Код ошибки</span><span class="sxs-lookup"><span data-stu-id="8185e-158">Error Code</span></span>                      | <span data-ttu-id="8185e-159">Значение</span><span class="sxs-lookup"><span data-stu-id="8185e-159">Meaning</span></span>                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8185e-160">\_драйвер принтера \_ ошибок \_ заблокирован</span><span class="sxs-lookup"><span data-stu-id="8185e-160">ERROR\_PRINTER\_DRIVER\_BLOCKED</span></span> | <span data-ttu-id="8185e-161">Драйвер не работает в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="8185e-161">The driver does not work on the operating system.</span></span>                                                                                                         |
| <span data-ttu-id="8185e-162">предупреждение об ОШИБКе \_ \_ драйвера принтера \_</span><span class="sxs-lookup"><span data-stu-id="8185e-162">ERROR\_PRINTER\_DRIVER\_WARNED</span></span>  | <span data-ttu-id="8185e-163">Драйвер не является надежным в операционной системе.</span><span class="sxs-lookup"><span data-stu-id="8185e-163">The driver is unreliable on the operating system.</span></span> <span data-ttu-id="8185e-164">Однако если \_ \_ указан драйвер предупреждения установки APD \_ , драйвер устанавливается и предупреждение не выдается.</span><span class="sxs-lookup"><span data-stu-id="8185e-164">However, if APD\_INSTALL\_WARNED\_DRIVER is specified, the driver is installed and no warning is given.</span></span> |



 

<span data-ttu-id="8185e-165">Дополнительные сведения см. в разделе «Примечания».</span><span class="sxs-lookup"><span data-stu-id="8185e-165">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="8185e-166">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8185e-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8185e-167">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="8185e-167">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8185e-168">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="8185e-168">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8185e-169">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="8185e-169">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8185e-170">Вызывающий объект должен иметь [селоаддриверпривилеже](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="8185e-170">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="8185e-171">Перед вызовом функции **аддпринтердриверекс** все файлы, необходимые для драйвера, должны быть скопированы в каталог системного драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="8185e-171">Before calling the **AddPrinterDriverEx** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="8185e-172">Чтобы получить имя этого каталога, вызовите функцию [**жетпринтердривердиректори**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="8185e-172">To retrieve the name of this directory, call the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="8185e-173">Чтобы определить, какие драйверы принтера в настоящий момент установлены, вызовите функцию [**енумпринтердриверс**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="8185e-173">To determine which printer drivers are currently installed, call the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="8185e-174">Если драйвер принтера был успешно добавлен, функция вызывает функцию Дрвдриверевент ( \_ Инициализация события драйвера, \_ уровень, \_ сведения о драйвере \_ \* , lParam), чтобы разрешить драйверу выполнять инициализацию, необходимую во время установки драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="8185e-174">If the printer driver has been successfully added, the function calls the DrvDriverEvent (DRIVER\_EVENT\_INITIALIZE, Level, DRIVER\_INFO\_\*, lparam ) function to allow the driver to perform any initializations required during the installation of a printer driver.</span></span> <span data-ttu-id="8185e-175">Дополнительные сведения о **дрвдриверевент** см. в пакете средств разработки драйверов Microsoft Windows (DDK).</span><span class="sxs-lookup"><span data-stu-id="8185e-175">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK)</span></span>

<span data-ttu-id="8185e-176">Драйвер не должен использовать вызов пользовательского интерфейса во время вызова **дрвдриверевент**.</span><span class="sxs-lookup"><span data-stu-id="8185e-176">The driver should not use a UI call during the call to **DrvDriverEvent**.</span></span> <span data-ttu-id="8185e-177">Чтобы выполнять задания, связанные с пользовательским интерфейсом, установщик должен либо использовать запись Вендорсетуп в INF-файле принтера, либо, для устройств самонастраивающийся, установщик может использовать соустановщик для конкретного устройства.</span><span class="sxs-lookup"><span data-stu-id="8185e-177">To do UI-related jobs, the installer should either use the VendorSetup entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="8185e-178">Дополнительные сведения о Вендорсетуп см. в пакете DDK.</span><span class="sxs-lookup"><span data-stu-id="8185e-178">For more information about VendorSetup, see the DDK.</span></span>

<span data-ttu-id="8185e-179">Файлы, на которые ссылается структура [**драйвера \_ \_ 6**](driver-info-6.md) , должны быть локальными для компьютера, на котором выполняется вызов.</span><span class="sxs-lookup"><span data-stu-id="8185e-179">The files that are referenced in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure must be local to the machine from which the call is made.</span></span> <span data-ttu-id="8185e-180">Имя файла может представлять собой UNC-имя, если имя UNC является локальным компьютером.</span><span class="sxs-lookup"><span data-stu-id="8185e-180">A file name can be a UNC name as long as the UNC name is the local machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="8185e-181">Требования</span><span class="sxs-lookup"><span data-stu-id="8185e-181">Requirements</span></span>



| <span data-ttu-id="8185e-182">Требование</span><span class="sxs-lookup"><span data-stu-id="8185e-182">Requirement</span></span> | <span data-ttu-id="8185e-183">Значение</span><span class="sxs-lookup"><span data-stu-id="8185e-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8185e-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8185e-184">Minimum supported client</span></span><br/> | <span data-ttu-id="8185e-185">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8185e-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="8185e-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8185e-186">Minimum supported server</span></span><br/> | <span data-ttu-id="8185e-187">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8185e-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8185e-188">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8185e-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="8185e-189"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-189"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8185e-190">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8185e-190">Library</span></span><br/>                  | <dl> <span data-ttu-id="8185e-191"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-191"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8185e-192">DLL</span><span class="sxs-lookup"><span data-stu-id="8185e-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8185e-193"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="8185e-193"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="8185e-194">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="8185e-194">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8185e-195">**Аддпринтердриверексв** (Юникод) и **аддпринтердриверекса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8185e-195">**AddPrinterDriverExW** (Unicode) and **AddPrinterDriverExA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="8185e-196">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8185e-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8185e-197">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="8185e-197">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8185e-198">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="8185e-198">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="8185e-199">**аддпринтердривер**</span><span class="sxs-lookup"><span data-stu-id="8185e-199">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="8185e-200">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="8185e-200">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="8185e-201">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="8185e-201">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="8185e-202">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="8185e-202">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="8185e-203">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="8185e-203">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="8185e-204">**делетепринтердриверекс**</span><span class="sxs-lookup"><span data-stu-id="8185e-204">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="8185e-205">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="8185e-205">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="8185e-206">**жетпринтердривердиректори**</span><span class="sxs-lookup"><span data-stu-id="8185e-206">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

