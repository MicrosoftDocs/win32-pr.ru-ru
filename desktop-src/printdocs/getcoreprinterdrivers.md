---
description: Извлекает GUID, версию и дату указанных основных драйверов принтера и путь к их пакетам.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: Функция Жеткорепринтердриверс (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345285"
---
# <a name="getcoreprinterdrivers-function"></a><span data-ttu-id="da6bb-103">Функция Жеткорепринтердриверс</span><span class="sxs-lookup"><span data-stu-id="da6bb-103">GetCorePrinterDrivers function</span></span>

<span data-ttu-id="da6bb-104">Извлекает GUID, версию и дату указанных основных драйверов принтера и путь к их пакетам.</span><span class="sxs-lookup"><span data-stu-id="da6bb-104">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span>

## <a name="syntax"></a><span data-ttu-id="da6bb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da6bb-105">Syntax</span></span>


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a><span data-ttu-id="da6bb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da6bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da6bb-107">*псзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da6bb-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da6bb-108">Указатель на константу, заканчивающуюся нулем строкой, которая указывает имя сервера печати.</span><span class="sxs-lookup"><span data-stu-id="da6bb-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="da6bb-109">Для локального компьютера используйте **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="da6bb-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="da6bb-110">*псзенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da6bb-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da6bb-111">Указатель на константу, заканчивающуюся нулем строкой, которая указывает архитектуру процессора (например, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="da6bb-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="da6bb-112">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="da6bb-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="da6bb-113">*псззкоредривердепенденЦиес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da6bb-113">*pszzCoreDriverDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da6bb-114">Указатель на многострочную строку, завершающуюся нулем, которая указывает идентификаторы GUID основных драйверов принтера.</span><span class="sxs-lookup"><span data-stu-id="da6bb-114">A pointer to a null-terminated multi-string that specifies the GUIDs of the core printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="da6bb-115">*ккорепринтердриверс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da6bb-115">*cCorePrinterDrivers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da6bb-116">Количество строк в *псззкоредривердепенденЦиес*.</span><span class="sxs-lookup"><span data-stu-id="da6bb-116">The number of strings in *pszzCoreDriverDependencies*.</span></span>

</dd> <dt>

<span data-ttu-id="da6bb-117">*пкорепринтердриверс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="da6bb-117">*pCorePrinterDrivers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da6bb-118">Указатель на массив из одной или нескольких основных структур [**\_ \_ драйвера принтера**](core-printer-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="da6bb-118">A pointer to an array of one or more [**CORE\_PRINTER\_DRIVER**](core-printer-driver.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da6bb-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da6bb-119">Return value</span></span>

<span data-ttu-id="da6bb-120">Если операция выполнена успешно, возвращается значение S \_ ОК, в противном случае **HRESULT** будет содержать код ошибки.</span><span class="sxs-lookup"><span data-stu-id="da6bb-120">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="da6bb-121">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="da6bb-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="da6bb-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="da6bb-122">Remarks</span></span>

<span data-ttu-id="da6bb-123">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="da6bb-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="da6bb-124">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="da6bb-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="da6bb-125">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="da6bb-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

## <a name="requirements"></a><span data-ttu-id="da6bb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="da6bb-126">Requirements</span></span>



| <span data-ttu-id="da6bb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="da6bb-127">Requirement</span></span> | <span data-ttu-id="da6bb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="da6bb-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da6bb-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="da6bb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="da6bb-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="da6bb-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="da6bb-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="da6bb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="da6bb-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="da6bb-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="da6bb-133">Header</span><span class="sxs-lookup"><span data-stu-id="da6bb-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="da6bb-134"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="da6bb-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="da6bb-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da6bb-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="da6bb-136"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da6bb-136"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="da6bb-137">DLL</span><span class="sxs-lookup"><span data-stu-id="da6bb-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="da6bb-138"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da6bb-138"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="da6bb-139">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="da6bb-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="da6bb-140">**Жеткорепринтердриверсв** (Юникод) и **жеткорепринтердриверса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="da6bb-140">**GetCorePrinterDriversW** (Unicode) and **GetCorePrinterDriversA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="da6bb-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da6bb-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da6bb-142">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="da6bb-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="da6bb-143">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="da6bb-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

