---
description: Функция Корепринтердриверинсталлед сообщает, установлен ли основной драйвер принтера с указанными GUID, датой и версией.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: Функция Корепринтердриверинсталлед (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081162"
---
# <a name="coreprinterdriverinstalled-function"></a><span data-ttu-id="43dfc-103">Функция Корепринтердриверинсталлед</span><span class="sxs-lookup"><span data-stu-id="43dfc-103">CorePrinterDriverInstalled function</span></span>

<span data-ttu-id="43dfc-104">Функция **корепринтердриверинсталлед** сообщает, установлен ли основной драйвер принтера с указанными GUID, датой и версией.</span><span class="sxs-lookup"><span data-stu-id="43dfc-104">The **CorePrinterDriverInstalled** function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="43dfc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43dfc-105">Syntax</span></span>


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="43dfc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43dfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43dfc-107">*псзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43dfc-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43dfc-108">Указатель на константу, заканчивающуюся нулем строкой, которая указывает имя сервера печати.</span><span class="sxs-lookup"><span data-stu-id="43dfc-108">Pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="43dfc-109">Для локального компьютера используйте **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="43dfc-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="43dfc-110">*псзенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43dfc-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43dfc-111">Указатель на константу, заканчивающуюся нулем строкой, которая указывает архитектуру процессора (например, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="43dfc-111">Pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="43dfc-112">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="43dfc-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="43dfc-113">*Коредривергуид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43dfc-113">*CoreDriverGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43dfc-114">Идентификатор GUID основного драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="43dfc-114">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="43dfc-115">*фтдривердате* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43dfc-115">*ftDriverDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43dfc-116">Дата основного драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="43dfc-116">The date of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="43dfc-117">*двлдриверверсион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="43dfc-117">*dwlDriverVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43dfc-118">Версия основного драйвера принтера.</span><span class="sxs-lookup"><span data-stu-id="43dfc-118">The version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="43dfc-119">*пбдриверинсталлед* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="43dfc-119">*pbDriverInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43dfc-120">Указатель на **значение true** , если установлен драйвер или более новая версия, и **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="43dfc-120">A pointer to **TRUE** if the driver, or a newer version, is installed, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43dfc-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="43dfc-121">Return value</span></span>

<span data-ttu-id="43dfc-122">Если операция выполнена успешно, возвращается значение S \_ ОК, в противном случае **HRESULT** будет содержать код ошибки.</span><span class="sxs-lookup"><span data-stu-id="43dfc-122">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="43dfc-123">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="43dfc-123">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="43dfc-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43dfc-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="43dfc-125">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="43dfc-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="43dfc-126">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="43dfc-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="43dfc-127">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="43dfc-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43dfc-128">Требования</span><span class="sxs-lookup"><span data-stu-id="43dfc-128">Requirements</span></span>



| <span data-ttu-id="43dfc-129">Требование</span><span class="sxs-lookup"><span data-stu-id="43dfc-129">Requirement</span></span> | <span data-ttu-id="43dfc-130">Значение</span><span class="sxs-lookup"><span data-stu-id="43dfc-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43dfc-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43dfc-131">Minimum supported client</span></span><br/> | <span data-ttu-id="43dfc-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43dfc-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="43dfc-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43dfc-133">Minimum supported server</span></span><br/> | <span data-ttu-id="43dfc-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43dfc-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="43dfc-135">Header</span><span class="sxs-lookup"><span data-stu-id="43dfc-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="43dfc-136"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43dfc-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="43dfc-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="43dfc-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="43dfc-138"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="43dfc-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="43dfc-139">DLL</span><span class="sxs-lookup"><span data-stu-id="43dfc-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43dfc-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43dfc-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="43dfc-141">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="43dfc-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="43dfc-142">**Корепринтердриверинсталледв** (Юникод) и **корепринтердриверинсталледа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="43dfc-142">**CorePrinterDriverInstalledW** (Unicode) and **CorePrinterDriverInstalledA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="43dfc-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43dfc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43dfc-144">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="43dfc-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="43dfc-145">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="43dfc-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

