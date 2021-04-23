---
description: Функция Делетепринтердривер удаляет указанное имя драйвера принтера из списка имен поддерживаемых драйверов на сервере.
ms.assetid: b159bd8b-3416-44a5-91bf-c0447ed6b465
title: Функция Делетепринтердривер (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriver
- DeletePrinterDriverA
- DeletePrinterDriverW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 9e84730be0d20100c2da42aa357f35c08cfb0727
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663011"
---
# <a name="deleteprinterdriver-function"></a><span data-ttu-id="c461b-103">Функция Делетепринтердривер</span><span class="sxs-lookup"><span data-stu-id="c461b-103">DeletePrinterDriver function</span></span>

<span data-ttu-id="c461b-104">Функция **делетепринтердривер** удаляет указанное имя драйвера принтера из списка имен поддерживаемых драйверов на сервере.</span><span class="sxs-lookup"><span data-stu-id="c461b-104">The **DeletePrinterDriver** function removes the specified printer-driver name from the list of names of supported drivers on a server.</span></span>

<span data-ttu-id="c461b-105">Чтобы удалить файлы, связанные с драйвером, помимо удаления указанного имени драйвера принтера из списка имен поддерживаемых драйверов для сервера, используйте функцию [**делетепринтердриверекс**](deleteprinterdriverex.md) .</span><span class="sxs-lookup"><span data-stu-id="c461b-105">To delete the files associated with the driver in addition to removing the specified printer-driver name from the list of names of supported drivers for a server, use the [**DeletePrinterDriverEx**](deleteprinterdriverex.md) function.</span></span>

<span data-ttu-id="c461b-106">**Делетепринтердривер** удаляет драйвер, только если для указанной среды не используется ни одна версия драйвера.</span><span class="sxs-lookup"><span data-stu-id="c461b-106">**DeletePrinterDriver** deletes a driver only if no version of the driver is in use for the specified environment.</span></span> <span data-ttu-id="c461b-107">[**Делетепринтердриверекс**](deleteprinterdriverex.md) может удалять определенные версии драйвера.</span><span class="sxs-lookup"><span data-stu-id="c461b-107">[**DeletePrinterDriverEx**](deleteprinterdriverex.md) can delete specific versions of the driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="c461b-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c461b-108">Syntax</span></span>


```C++
BOOL DeletePrinterDriver(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pDriverName
);
```



## <a name="parameters"></a><span data-ttu-id="c461b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c461b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c461b-110">*pName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c461b-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c461b-111">Указатель на строку, завершающуюся нулем, которая указывает имя сервера, с которого должен быть удален драйвер.</span><span class="sxs-lookup"><span data-stu-id="c461b-111">A pointer to a null-terminated string that specifies the name of the server from which the driver is to be deleted.</span></span> <span data-ttu-id="c461b-112">Если этот параметр имеет **значение NULL**, имя драйвера принтера будет удалено локально.</span><span class="sxs-lookup"><span data-stu-id="c461b-112">If this parameter is **NULL**, the printer-driver name will be removed locally.</span></span>

</dd> <dt>

<span data-ttu-id="c461b-113">*пенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c461b-113">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c461b-114">Указатель на строку, завершающуюся нулем, которая указывает среду, из которой должен быть удален драйвер (например, Windows x86, Windows IA64 или Windows x64).</span><span class="sxs-lookup"><span data-stu-id="c461b-114">A pointer to a null-terminated string that specifies the environment from which the driver is to be deleted (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="c461b-115">Если этот параметр имеет **значение NULL**, имя драйвера удаляется из текущей среды вызывающего приложения и клиентского компьютера (не целевого приложения и сервера печати).</span><span class="sxs-lookup"><span data-stu-id="c461b-115">If this parameter is **NULL**, the driver name is deleted from the current environment of the calling application and client machine (not of the destination application and print server).</span></span>

</dd> <dt>

<span data-ttu-id="c461b-116">*пдривернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c461b-116">*pDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c461b-117">Указатель на строку с завершающим нулем, указывающую имя драйвера, который необходимо удалить.</span><span class="sxs-lookup"><span data-stu-id="c461b-117">A pointer to a null-terminated string specifying the name of the driver that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c461b-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c461b-118">Return value</span></span>

<span data-ttu-id="c461b-119">Если функция выполнена, возвращаемое значение будет ненулевым.</span><span class="sxs-lookup"><span data-stu-id="c461b-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c461b-120">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="c461b-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c461b-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c461b-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c461b-122">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="c461b-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c461b-123">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="c461b-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c461b-124">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="c461b-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c461b-125">Вызывающий объект должен иметь [селоаддриверпривилеже](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="c461b-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="c461b-126">Функция **делетепринтердривер** не удаляет связанные файлы, просто удаляет имя драйвера из списка, возвращенного функцией [**енумпринтердриверс**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="c461b-126">The **DeletePrinterDriver** function does not delete the associated files, it merely removes the driver name from the list returned by the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="c461b-127">Перед вызовом **делетепринтердривер** необходимо удалить все объекты принтера, использующие драйвер принтера.</span><span class="sxs-lookup"><span data-stu-id="c461b-127">Before calling **DeletePrinterDriver**, you must delete all printer objects that use the printer driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="c461b-128">Требования</span><span class="sxs-lookup"><span data-stu-id="c461b-128">Requirements</span></span>



| <span data-ttu-id="c461b-129">Требование</span><span class="sxs-lookup"><span data-stu-id="c461b-129">Requirement</span></span> | <span data-ttu-id="c461b-130">Значение</span><span class="sxs-lookup"><span data-stu-id="c461b-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c461b-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c461b-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c461b-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c461b-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c461b-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c461b-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c461b-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c461b-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c461b-135">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c461b-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="c461b-136"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c461b-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c461b-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="c461b-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="c461b-138"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c461b-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c461b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="c461b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c461b-140"><dt>Винспул. drv</dt></span><span class="sxs-lookup"><span data-stu-id="c461b-140"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="c461b-141">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="c461b-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c461b-142">**Делетепринтердриверв** (Юникод) и **делетепринтердривера** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c461b-142">**DeletePrinterDriverW** (Unicode) and **DeletePrinterDriverA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="c461b-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c461b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c461b-144">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="c461b-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c461b-145">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="c461b-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c461b-146">**делетепринтердриверекс**</span><span class="sxs-lookup"><span data-stu-id="c461b-146">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="c461b-147">**енумпринтердриверс**</span><span class="sxs-lookup"><span data-stu-id="c461b-147">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> </dl>

 

