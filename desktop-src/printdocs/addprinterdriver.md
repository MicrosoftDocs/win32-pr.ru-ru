---
description: Функция Аддпринтердривер устанавливает локальный или удаленный драйвер принтера и связывает файлы конфигурации, данных и драйверов.
ms.assetid: 0f762800-f5a5-40ea-8be1-7fd8bda23788
title: Функция Аддпринтердривер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriver
- AddPrinterDriverA
- AddPrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: de5a9e9d16a47dfe8b9620edc9acdc5c5fd4d552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815504"
---
# <a name="addprinterdriver-function"></a><span data-ttu-id="b14b8-103">Функция Аддпринтердривер</span><span class="sxs-lookup"><span data-stu-id="b14b8-103">AddPrinterDriver function</span></span>

<span data-ttu-id="b14b8-104">Функция **аддпринтердривер** устанавливает локальный или удаленный драйвер принтера и связывает файлы конфигурации, данных и драйверов.</span><span class="sxs-lookup"><span data-stu-id="b14b8-104">The **AddPrinterDriver** function installs a local or remote printer driver and associates the configuration, data, and driver files.</span></span>

<span data-ttu-id="b14b8-105">Для большей гибкости при установке или обновлении драйверов принтеров используйте функцию [**аддпринтердриверекс**](addprinterdriverex.md) , так как она обеспечивает жесткое обновление, более пониженную версию, копирование только новых файлов и копирование всех файлов (независимо от отметки времени файла).</span><span class="sxs-lookup"><span data-stu-id="b14b8-105">For more flexibility in installing or upgrading printer drivers, use the [**AddPrinterDriverEx**](addprinterdriverex.md) function because it allows strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of the file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="b14b8-106">Установка драйвера принтера без пакета драйверов больше не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="b14b8-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="b14b8-107">Вместо этого используйте [**инсталлпринтердриверфромпаккаже**](installprinterdriverfrompackage.md) .</span><span class="sxs-lookup"><span data-stu-id="b14b8-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="b14b8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b14b8-108">Syntax</span></span>


```C++
BOOL AddPrinterDriver(
  _In_ LPTSTR pName,
  _In_ DWORD  Level,
  _In_ LPBYTE pDriverInfo
);
```



## <a name="parameters"></a><span data-ttu-id="b14b8-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b14b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b14b8-110">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b14b8-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b14b8-111">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, на котором должен быть установлен драйвер.</span><span class="sxs-lookup"><span data-stu-id="b14b8-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span>

<span data-ttu-id="b14b8-112">Если *pName* имеет **значение NULL**, драйвер будет установлен локально.</span><span class="sxs-lookup"><span data-stu-id="b14b8-112">If *pName* is **NULL**, the driver will be installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="b14b8-113">*Уровень* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b14b8-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b14b8-114">Версия структуры, на которую указывает *пдриверинфо* .</span><span class="sxs-lookup"><span data-stu-id="b14b8-114">The version of the structure to which *pDriverInfo* points.</span></span>

<span data-ttu-id="b14b8-115">Это значение может быть равно 2, 3, 4, 6 или 8.</span><span class="sxs-lookup"><span data-stu-id="b14b8-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="b14b8-116">*пдриверинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="b14b8-116">*pDriverInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b14b8-117">Указатель на структуру, содержащую сведения о драйвере принтера.</span><span class="sxs-lookup"><span data-stu-id="b14b8-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="b14b8-118">Это зависит от значения *Level*.</span><span class="sxs-lookup"><span data-stu-id="b14b8-118">This depends on the value of *Level*.</span></span>



| <span data-ttu-id="b14b8-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b14b8-119">Value</span></span> | <span data-ttu-id="b14b8-120">Структура дисковода принтера</span><span class="sxs-lookup"><span data-stu-id="b14b8-120">Printer Drive Structure</span></span>                  |
|-------|------------------------------------------|
| <span data-ttu-id="b14b8-121">2</span><span class="sxs-lookup"><span data-stu-id="b14b8-121">2</span></span>     | [<span data-ttu-id="b14b8-122">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b14b8-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md) |
| <span data-ttu-id="b14b8-123">3</span><span class="sxs-lookup"><span data-stu-id="b14b8-123">3</span></span>     | [<span data-ttu-id="b14b8-124">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="b14b8-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md) |
| <span data-ttu-id="b14b8-125">4</span><span class="sxs-lookup"><span data-stu-id="b14b8-125">4</span></span>     | [<span data-ttu-id="b14b8-126">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="b14b8-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md) |
| <span data-ttu-id="b14b8-127">6</span><span class="sxs-lookup"><span data-stu-id="b14b8-127">6</span></span>     | [<span data-ttu-id="b14b8-128">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="b14b8-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md) |
| <span data-ttu-id="b14b8-129">8</span><span class="sxs-lookup"><span data-stu-id="b14b8-129">8</span></span>     | [<span data-ttu-id="b14b8-130">**\_Сведения о драйвере \_ 8**</span><span class="sxs-lookup"><span data-stu-id="b14b8-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md) |



 

<span data-ttu-id="b14b8-131">Если элемент **пенвиронмент** структуры, на который указывает *Пдриверинфо* , имеет **значение NULL**, используется текущая среда вызывающего или клиентского объекта (не целевого/сервера).</span><span class="sxs-lookup"><span data-stu-id="b14b8-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b14b8-132">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b14b8-132">Return value</span></span>

<span data-ttu-id="b14b8-133">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="b14b8-133">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b14b8-134">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="b14b8-134">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b14b8-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b14b8-135">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b14b8-136">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="b14b8-136">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b14b8-137">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="b14b8-137">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b14b8-138">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="b14b8-138">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b14b8-139">Вызывающий объект должен иметь [селоаддриверпривилеже](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="b14b8-139">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="b14b8-140">Прежде чем приложение вызовет функцию **аддпринтердривер** , все файлы, необходимые для драйвера, должны быть скопированы в каталог системного драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="b14b8-140">Before an application calls the **AddPrinterDriver** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="b14b8-141">Приложение может получить имя этого каталога, вызвав функцию [**жетпринтердривердиректори**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="b14b8-141">An application can retrieve the name of this directory by calling the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="b14b8-142">Приложение может определить, какие драйверы принтера в настоящее время установлены путем вызова функции [**енумпринтердриверс**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="b14b8-142">An application can determine which printer drivers are currently installed by calling the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b14b8-143">Требования</span><span class="sxs-lookup"><span data-stu-id="b14b8-143">Requirements</span></span>



| <span data-ttu-id="b14b8-144">Требование</span><span class="sxs-lookup"><span data-stu-id="b14b8-144">Requirement</span></span> | <span data-ttu-id="b14b8-145">Значение</span><span class="sxs-lookup"><span data-stu-id="b14b8-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b14b8-146">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b14b8-146">Minimum supported client</span></span><br/> | <span data-ttu-id="b14b8-147">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b14b8-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b14b8-148">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b14b8-148">Minimum supported server</span></span><br/> | <span data-ttu-id="b14b8-149">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b14b8-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b14b8-150">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b14b8-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="b14b8-151"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b14b8-151"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b14b8-152">Библиотека</span><span class="sxs-lookup"><span data-stu-id="b14b8-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="b14b8-153"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b14b8-153"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b14b8-154">DLL</span><span class="sxs-lookup"><span data-stu-id="b14b8-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b14b8-155"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b14b8-155"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b14b8-156">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="b14b8-156">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b14b8-157">**Аддпринтердриверв** (Юникод) и **аддпринтердривера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b14b8-157">**AddPrinterDriverW** (Unicode) and **AddPrinterDriverA** (ANSI)</span></span><br/>                               |



## <a name="see-also"></a><span data-ttu-id="b14b8-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b14b8-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b14b8-159">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="b14b8-159">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b14b8-160">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="b14b8-160">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b14b8-161">**аддпринтердриверекс**</span><span class="sxs-lookup"><span data-stu-id="b14b8-161">**AddPrinterDriverEx**</span></span>](addprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="b14b8-162">**\_Сведения о драйвере \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b14b8-162">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="b14b8-163">**\_Сведения о драйвере \_ 3**</span><span class="sxs-lookup"><span data-stu-id="b14b8-163">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="b14b8-164">**\_Сведения о драйвере \_ 4**</span><span class="sxs-lookup"><span data-stu-id="b14b8-164">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="b14b8-165">**\_Сведения о драйвере \_ 6**</span><span class="sxs-lookup"><span data-stu-id="b14b8-165">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="b14b8-166">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="b14b8-166">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="b14b8-167">**жетпринтердривердиректори**</span><span class="sxs-lookup"><span data-stu-id="b14b8-167">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

