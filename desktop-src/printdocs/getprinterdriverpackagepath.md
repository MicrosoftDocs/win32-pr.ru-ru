---
description: Извлекает путь к указанному пакету драйвера принтера на сервере печати.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: Функция Жетпринтердриверпаккажепас (Винспул. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703135"
---
# <a name="getprinterdriverpackagepath-function"></a><span data-ttu-id="740c2-103">Функция Жетпринтердриверпаккажепас</span><span class="sxs-lookup"><span data-stu-id="740c2-103">GetPrinterDriverPackagePath function</span></span>

<span data-ttu-id="740c2-104">Извлекает путь к указанному пакету драйвера принтера на сервере печати.</span><span class="sxs-lookup"><span data-stu-id="740c2-104">Retrieves the path to the specified printer driver package on a print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="740c2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="740c2-105">Syntax</span></span>


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a><span data-ttu-id="740c2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="740c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="740c2-107">*псзсервер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="740c2-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="740c2-108">Указатель на константу, заканчивающуюся нулем строкой, которая указывает имя сервера печати.</span><span class="sxs-lookup"><span data-stu-id="740c2-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="740c2-109">Для локального компьютера используйте **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="740c2-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="740c2-110">*псзенвиронмент* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="740c2-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="740c2-111">Указатель на константу, заканчивающуюся нулем строкой, которая указывает архитектуру процессора (например, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="740c2-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="740c2-112">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="740c2-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="740c2-113">*псзлангуаже* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="740c2-113">*pszLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="740c2-114">Указатель на константу, заканчивающуюся нулем строкой, которая указывает язык [многоязычного пользовательского интерфейса](/windows/desktop/Intl/mui-resource-management) для устанавливаемого драйвера.</span><span class="sxs-lookup"><span data-stu-id="740c2-114">A pointer to a constant, null-terminated string that specifies the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) language for the driver being installed.</span></span> <span data-ttu-id="740c2-115">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="740c2-115">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="740c2-116">*псзпаккажеид* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="740c2-116">*pszPackageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="740c2-117">Указатель на константу, заканчивающуюся нулем строкой, которая указывает идентификатор пакета драйвера.</span><span class="sxs-lookup"><span data-stu-id="740c2-117">A pointer to a constant, null-terminated string that specifies the ID of the driver package.</span></span>

</dd> <dt>

<span data-ttu-id="740c2-118">*псздриверпаккажекаб* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="740c2-118">*pszDriverPackageCab* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="740c2-119">Указатель на строку, завершающуюся нулем, которая указывает путь к CAB-файлу для пакета драйверов.</span><span class="sxs-lookup"><span data-stu-id="740c2-119">A pointer to a null-terminated string that specifies the path to the cabinet file for the driver package.</span></span> <span data-ttu-id="740c2-120">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="740c2-120">This can be **NULL**.</span></span> <span data-ttu-id="740c2-121">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="740c2-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="740c2-122">*кчдриверпаккажекаб* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="740c2-122">*cchDriverPackageCab* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="740c2-123">Размер (в символах) буфера *псздриверпаккажекаб* .</span><span class="sxs-lookup"><span data-stu-id="740c2-123">The size, in characters, of the *pszDriverPackageCab* buffer.</span></span> <span data-ttu-id="740c2-124">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="740c2-124">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="740c2-125">*пкчрекуиредсизе* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="740c2-125">*pcchRequiredSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="740c2-126">Указатель на требуемый размер буфера *псздриверпаккажекаб* .</span><span class="sxs-lookup"><span data-stu-id="740c2-126">A pointer to the required size of the *pszDriverPackageCab* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="740c2-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="740c2-127">Return value</span></span>

<span data-ttu-id="740c2-128">Если операция выполнена успешно, возвращается значение S \_ ОК, в противном случае **HRESULT** будет содержать код ошибки.</span><span class="sxs-lookup"><span data-stu-id="740c2-128">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="740c2-129">Дополнительные сведения о кодах ошибок COM см. в разделе [Обработка ошибок](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="740c2-129">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="740c2-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="740c2-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="740c2-131">Это блокирующая или синхронная функция, которая может не возвращать значение немедленно.</span><span class="sxs-lookup"><span data-stu-id="740c2-131">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="740c2-132">Скорость возврата этой функцией зависит от факторов времени выполнения, таких как состояние сети, Конфигурация сервера печати и факторы реализации драйвера принтера, которые трудно предсказать при написании приложения.</span><span class="sxs-lookup"><span data-stu-id="740c2-132">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="740c2-133">Вызов этой функции из потока, который управляет взаимодействием с пользовательским интерфейсом, может привести к невозможности реагирования приложения.</span><span class="sxs-lookup"><span data-stu-id="740c2-133">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="740c2-134">Чтобы получить значение для *кчдриверпаккажекаб*, вызовите функцию со значением **null** в качестве значения параметра *псздриверпаккажекаб*.</span><span class="sxs-lookup"><span data-stu-id="740c2-134">To obtain a value for *cchDriverPackageCab*, call the function with **NULL** as the value of *pszDriverPackageCab*.</span></span> <span data-ttu-id="740c2-135">Используйте значение, возвращенное в *пкчрекуиредсизе* , как значение *кчдриверпаккажекаб* , и снова вызовите функцию.</span><span class="sxs-lookup"><span data-stu-id="740c2-135">Use the value returned in *pcchRequiredSize* as the value of *cchDriverPackageCab* and call the function again.</span></span>

<span data-ttu-id="740c2-136">*Псзпаккажеид* обычно получается из вызова [**жеткорепринтердриверс**](getcoreprinterdrivers.md).</span><span class="sxs-lookup"><span data-stu-id="740c2-136">The *pszPackageID* is typically obtained from a call to [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="740c2-137">Требования</span><span class="sxs-lookup"><span data-stu-id="740c2-137">Requirements</span></span>



| <span data-ttu-id="740c2-138">Требование</span><span class="sxs-lookup"><span data-stu-id="740c2-138">Requirement</span></span> | <span data-ttu-id="740c2-139">Значение</span><span class="sxs-lookup"><span data-stu-id="740c2-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="740c2-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="740c2-140">Minimum supported client</span></span><br/> | <span data-ttu-id="740c2-141">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="740c2-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="740c2-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="740c2-142">Minimum supported server</span></span><br/> | <span data-ttu-id="740c2-143">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="740c2-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="740c2-144">Header</span><span class="sxs-lookup"><span data-stu-id="740c2-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="740c2-145"><dt>Винспул. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="740c2-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="740c2-146">Библиотека</span><span class="sxs-lookup"><span data-stu-id="740c2-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="740c2-147"><dt>Винспул. lib</dt></span><span class="sxs-lookup"><span data-stu-id="740c2-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="740c2-148">DLL</span><span class="sxs-lookup"><span data-stu-id="740c2-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="740c2-149"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="740c2-149"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="740c2-150">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="740c2-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="740c2-151">**Жетпринтердриверпаккажепасв** (Юникод) и **жетпринтердриверпаккажепаса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="740c2-151">**GetPrinterDriverPackagePathW** (Unicode) and **GetPrinterDriverPackagePathA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="740c2-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="740c2-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="740c2-153">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="740c2-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="740c2-154">Функции API очереди печати принтера</span><span class="sxs-lookup"><span data-stu-id="740c2-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

