---
description: Удаляет пакет драйвера принтера из хранилища драйверов.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: Функция Делетепринтердриверпаккаже (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702201"
---
# <a name="deleteprinterdriverpackage-function"></a><span data-ttu-id="23db2-103">Функция Делетепринтердриверпаккаже</span><span class="sxs-lookup"><span data-stu-id="23db2-103">DeletePrinterDriverPackage function</span></span>

<span data-ttu-id="23db2-104">Удаляет пакет драйвера принтера из хранилища драйверов.</span><span class="sxs-lookup"><span data-stu-id="23db2-104">Deletes a printer driver package from the driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="23db2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23db2-105">Syntax</span></span>


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a><span data-ttu-id="23db2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="23db2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23db2-107">*псзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23db2-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23db2-108">Указатель на константу, завершающуюся нулем строку, указывающую имя сервера печати, с которого удаляется пакет драйверов.</span><span class="sxs-lookup"><span data-stu-id="23db2-108">A pointer to a constant, null-terminated string that specifies the name of the print server from which the driver package is being deleted.</span></span> <span data-ttu-id="23db2-109">Значение указателя **null** означает локальный компьютер.</span><span class="sxs-lookup"><span data-stu-id="23db2-109">A **NULL** pointer value means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="23db2-110">*псзинфпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23db2-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23db2-111">Указатель на константу, заканчивающуюся нулем строкой, которая указывает путь к INF-файлу драйвера \* .</span><span class="sxs-lookup"><span data-stu-id="23db2-111">A pointer to a constant, null-terminated string that specifies the path to the driver's \*.inf file.</span></span>

</dd> <dt>

<span data-ttu-id="23db2-112">*псзенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="23db2-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23db2-113">Указатель на константу, заканчивающуюся нулем строкой, которая указывает архитектуру процессора (например, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="23db2-113">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="23db2-114">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="23db2-114">This can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23db2-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="23db2-115">Return value</span></span>

<span data-ttu-id="23db2-116">\_ОК, если операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="23db2-116">S\_OK, if the operation succeeds.</span></span>

<span data-ttu-id="23db2-117">E \_ ACCESSDENIED, если пакет поставлялся вместе с Windows.</span><span class="sxs-lookup"><span data-stu-id="23db2-117">E\_ACCESSDENIED, if the package was shipped with Windows.</span></span>

<span data-ttu-id="23db2-118">\_Код HRESULT (ошибка \_ при \_ \_ использовании пакета драйвера печати \_ \_ ), если пакет используется.</span><span class="sxs-lookup"><span data-stu-id="23db2-118">HRESULT\_CODE(ERROR\_PRINT\_DRIVER\_PACKAGE\_IN\_USE), if the package is being used.</span></span>

<span data-ttu-id="23db2-119">В противном случае **HRESULT** будет содержать код ошибки.</span><span class="sxs-lookup"><span data-stu-id="23db2-119">Otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="23db2-120">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="23db2-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="23db2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23db2-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="23db2-122">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="23db2-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="23db2-123">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="23db2-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="23db2-124">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="23db2-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="23db2-125">Обычно хранилище драйверов —% WINDIR% \\ INF или% WINDIR% \\ system32 \\ дриверсторе \\ филерепоситори.</span><span class="sxs-lookup"><span data-stu-id="23db2-125">The driver store is typically %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="23db2-126">Пакет драйверов, поставляемый вместе с Windows, нельзя удалить с помощью этой функции.</span><span class="sxs-lookup"><span data-stu-id="23db2-126">A driver package that shipped with Windows cannot be removed with this function.</span></span>

<span data-ttu-id="23db2-127">Пользователь должен иметь права администратора принтера.</span><span class="sxs-lookup"><span data-stu-id="23db2-127">The user must have printer administration privileges.</span></span>

## <a name="requirements"></a><span data-ttu-id="23db2-128">Требования</span><span class="sxs-lookup"><span data-stu-id="23db2-128">Requirements</span></span>



| <span data-ttu-id="23db2-129">Требование</span><span class="sxs-lookup"><span data-stu-id="23db2-129">Requirement</span></span> | <span data-ttu-id="23db2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="23db2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23db2-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="23db2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="23db2-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23db2-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="23db2-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="23db2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="23db2-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23db2-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="23db2-135">Header</span><span class="sxs-lookup"><span data-stu-id="23db2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="23db2-136"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="23db2-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="23db2-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="23db2-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="23db2-138"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="23db2-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="23db2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="23db2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23db2-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="23db2-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="23db2-141">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="23db2-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="23db2-142">**Делетепринтердриверпаккажев** (Юникод) и **делетепринтердриверпаккажеа** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="23db2-142">**DeletePrinterDriverPackageW** (Unicode) and **DeletePrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="23db2-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="23db2-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23db2-144">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="23db2-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="23db2-145">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="23db2-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

