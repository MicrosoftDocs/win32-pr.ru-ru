---
description: Создает разницу между исходным и целевым объектом (предоставленными в виде буферов) и возвращает выходной результат в виде буфера, выделенного Мсделта.
title: Функция CreateDeltaB
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721011"
---
# <a name="createdeltab-function"></a><span data-ttu-id="3d047-103">Функция CreateDeltaB</span><span class="sxs-lookup"><span data-stu-id="3d047-103">CreateDeltaB function</span></span>

<span data-ttu-id="3d047-104">Создает разницу между исходным и целевым объектом (предоставленными в виде буферов) и возвращает выходной результат в виде буфера, выделенного Мсделта.</span><span class="sxs-lookup"><span data-stu-id="3d047-104">Creates a delta between the source and target (provided as buffers) and returns the output delta as an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="3d047-105">Необходимо вызвать [делтафри](msdelta-deltafree.md) , чтобы освободить выходной буфер после завершения этой функции.</span><span class="sxs-lookup"><span data-stu-id="3d047-105">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d047-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d047-106">Syntax</span></span>

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a><span data-ttu-id="3d047-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d047-107">Parameters</span></span>

<span data-ttu-id="3d047-108">*филетипесет*</span><span class="sxs-lookup"><span data-stu-id="3d047-108">*FileTypeSet*</span></span>

<span data-ttu-id="3d047-109">окне Значение [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) , указывающее тип файла, который должен использоваться для процесса создания.</span><span class="sxs-lookup"><span data-stu-id="3d047-109">[in] The [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) value that indicates the file type set to be used for the create process.</span></span>

<span data-ttu-id="3d047-110">*сетфлагс*</span><span class="sxs-lookup"><span data-stu-id="3d047-110">*SetFlags*</span></span>

<span data-ttu-id="3d047-111">окне Одно или несколько значений [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , указывающих флаги, которые будут использоваться в процессе создания, а также флаги по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3d047-111">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the flags to be used during the create process, in addition to the default flags.</span></span>

<span data-ttu-id="3d047-112">*ресетфлагс*</span><span class="sxs-lookup"><span data-stu-id="3d047-112">*ResetFlags*</span></span>

<span data-ttu-id="3d047-113">окне Одно или несколько значений [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) , указывающих флаги по умолчанию, которые будут сброшены во время процесса создания.</span><span class="sxs-lookup"><span data-stu-id="3d047-113">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the default flags to be reset during the create process.</span></span>

<span data-ttu-id="3d047-114">*Источник*</span><span class="sxs-lookup"><span data-stu-id="3d047-114">*Source*</span></span>

<span data-ttu-id="3d047-115">окне Структура [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) , содержащая указатель на буфер, содержащий исходные данные.</span><span class="sxs-lookup"><span data-stu-id="3d047-115">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="3d047-116">*Целевой объект*</span><span class="sxs-lookup"><span data-stu-id="3d047-116">*Target*</span></span>

<span data-ttu-id="3d047-117">окне Структура [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) , содержащая указатель на буфер, содержащий целевые данные.</span><span class="sxs-lookup"><span data-stu-id="3d047-117">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the target data.</span></span>

<span data-ttu-id="3d047-118">*саурцеоптионс*</span><span class="sxs-lookup"><span data-stu-id="3d047-118">*SourceOptions*</span></span>

<span data-ttu-id="3d047-119">[in] Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3d047-119">[in] Reserved.</span></span> <span data-ttu-id="3d047-120">Передайте [DELTA_INPUTную](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) структуру с *редактируемым* значением **false**, для *Лпстарт* задайте **значение NULL** , а для *усизе* — значение 0.</span><span class="sxs-lookup"><span data-stu-id="3d047-120">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="3d047-121">*таржетоптионс*</span><span class="sxs-lookup"><span data-stu-id="3d047-121">*TargetOptions*</span></span>

<span data-ttu-id="3d047-122">[in] Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3d047-122">[in] Reserved.</span></span> <span data-ttu-id="3d047-123">Передайте [DELTA_INPUTную](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) структуру с *редактируемым* значением **false**, для *Лпстарт* задайте **значение NULL** , а для *усизе* — значение 0.</span><span class="sxs-lookup"><span data-stu-id="3d047-123">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="3d047-124">*GlobalOptions*</span><span class="sxs-lookup"><span data-stu-id="3d047-124">*GlobalOptions*</span></span>

<span data-ttu-id="3d047-125">[in] Зарезервировано.</span><span class="sxs-lookup"><span data-stu-id="3d047-125">[in] Reserved.</span></span> <span data-ttu-id="3d047-126">Передайте [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) структуру с параметром *лпстарт* , имеющим значение **null** , а *усизе* значение 0.</span><span class="sxs-lookup"><span data-stu-id="3d047-126">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="3d047-127">*лптаржетфилетиме*</span><span class="sxs-lookup"><span data-stu-id="3d047-127">*lpTargetFileTime*</span></span>

<span data-ttu-id="3d047-128">окне Метка времени, заданная для целевого файла после применения разностной разницы.</span><span class="sxs-lookup"><span data-stu-id="3d047-128">[in] The time stamp set on the target file after delta apply.</span></span> <span data-ttu-id="3d047-129">Если **значение равно NULL**, то конечная отметка времени будет текущим временем в процессе создания.</span><span class="sxs-lookup"><span data-stu-id="3d047-129">If **NULL**, the target timestamp will be the current time during the create process.</span></span>

<span data-ttu-id="3d047-130">*хашалгид*</span><span class="sxs-lookup"><span data-stu-id="3d047-130">*HashAlgId*</span></span>

<span data-ttu-id="3d047-131">окне ALG_ID алгоритм, используемый для создания целевой сигнатуры.</span><span class="sxs-lookup"><span data-stu-id="3d047-131">[in] ALG_ID of the algorithm to be used to generate the target signature.</span></span> <span data-ttu-id="3d047-132">Некоторые специальные значения:</span><span class="sxs-lookup"><span data-stu-id="3d047-132">Some special values are:</span></span>

- <span data-ttu-id="3d047-133">0 = нет подписи</span><span class="sxs-lookup"><span data-stu-id="3d047-133">0 = No signature</span></span>
- <span data-ttu-id="3d047-134">32 = 32-разрядная CRC, определенная в msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="3d047-134">32 = 32-bit CRC defined in msdelta.dll</span></span>

<span data-ttu-id="3d047-135">*лпделта*</span><span class="sxs-lookup"><span data-stu-id="3d047-135">*lpDelta*</span></span>

<span data-ttu-id="3d047-136">заполняет Указатель на структуру [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) , в которой будет записана Дельта.</span><span class="sxs-lookup"><span data-stu-id="3d047-136">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the delta is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d047-137">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3d047-137">Return value</span></span>

<span data-ttu-id="3d047-138">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="3d047-138">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="3d047-139">Если функция возвращает **значение false**, можно вызвать [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) , чтобы получить соответствующий код системной ошибки Win32.</span><span class="sxs-lookup"><span data-stu-id="3d047-139">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d047-140">Требования</span><span class="sxs-lookup"><span data-stu-id="3d047-140">Requirements</span></span>

| <span data-ttu-id="3d047-141">Требование</span><span class="sxs-lookup"><span data-stu-id="3d047-141">Requirement</span></span> | <span data-ttu-id="3d047-142">Значение</span><span class="sxs-lookup"><span data-stu-id="3d047-142">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d047-143">Header</span><span class="sxs-lookup"><span data-stu-id="3d047-143">Header</span></span> | <span data-ttu-id="3d047-144">мсделта. h</span><span class="sxs-lookup"><span data-stu-id="3d047-144">msdelta.h</span></span> |
| <span data-ttu-id="3d047-145">DLL</span><span class="sxs-lookup"><span data-stu-id="3d047-145">DLL</span></span> | <span data-ttu-id="3d047-146">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="3d047-146">msdelta.dll</span></span> |
| <span data-ttu-id="3d047-147">Юникод</span><span class="sxs-lookup"><span data-stu-id="3d047-147">Unicode</span></span> | <span data-ttu-id="3d047-148">Неприменимо</span><span class="sxs-lookup"><span data-stu-id="3d047-148">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="3d047-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3d047-149">See also</span></span>

[<span data-ttu-id="3d047-150">мсделта</span><span class="sxs-lookup"><span data-stu-id="3d047-150">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="3d047-151">делтафри</span><span class="sxs-lookup"><span data-stu-id="3d047-151">DeltaFree</span></span>](msdelta-deltafree.md)
