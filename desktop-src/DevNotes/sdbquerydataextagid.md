---
description: Извлекает данные из указанных записей, принадлежащих записи EXE.
ms.assetid: 355eecd6-a0c9-4448-9aed-a9c3eb3b2071
title: Функция Сдбкуеридатаекстагид
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbQueryDataExTagID
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 8db16463d2923ce3c888de4f202e1ebc36584e99
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423206"
---
# <a name="sdbquerydataextagid-function"></a><span data-ttu-id="ae619-103">Функция Сдбкуеридатаекстагид</span><span class="sxs-lookup"><span data-stu-id="ae619-103">SdbQueryDataExTagID function</span></span>

<span data-ttu-id="ae619-104">Извлекает данные из указанных записей, принадлежащих записи EXE.</span><span class="sxs-lookup"><span data-stu-id="ae619-104">Retrieves data from the specified entries belonging to an EXE entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae619-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ae619-105">Syntax</span></span>


```C++
DWORD WINAPI SdbQueryDataExTagID(
  _In_        PDB     pdb,
  _In_        TAGID   tiExe,
  _In_opt_    LPCTSTR lpszDataName,
  _Out_opt_   LPDWORD lpdwDataType,
  _Out_       LPVOID  lpBuffer,
  _Inout_opt_ LPDWORD lpcbBufferSize,
  _Out_       TAGID   *ptiData
);
```



## <a name="parameters"></a><span data-ttu-id="ae619-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ae619-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae619-107">*pdb* \[ -файл окне\]</span><span class="sxs-lookup"><span data-stu-id="ae619-107">*pdb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae619-108">Маркер базы данных оболочек совместимости.</span><span class="sxs-lookup"><span data-stu-id="ae619-108">A handle to the shim database.</span></span>

</dd> <dt>

<span data-ttu-id="ae619-109">*тиексе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ae619-109">*tiExe* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae619-110">[**TAGID**](tagid.md) записи exe.</span><span class="sxs-lookup"><span data-stu-id="ae619-110">The [**TAGID**](tagid.md) of the EXE entry.</span></span>

</dd> <dt>

<span data-ttu-id="ae619-111">*лпсздатанаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="ae619-111">*lpszDataName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ae619-112">Имя возвращаемой записи данных.</span><span class="sxs-lookup"><span data-stu-id="ae619-112">The name of the data entry to be retrieved.</span></span> <span data-ttu-id="ae619-113">Чтобы указать несколько записей, разделяйте их символами обратной косой черты (" \\ ").</span><span class="sxs-lookup"><span data-stu-id="ae619-113">To specify multiple entries, separate the names with the backslash character ("\\").</span></span> <span data-ttu-id="ae619-114">Если этот параметр имеет **значение NULL**, функция пытается вернуть все записи данных.</span><span class="sxs-lookup"><span data-stu-id="ae619-114">If this parameter is **NULL**, the function attempts to return all data entries.</span></span>

</dd> <dt>

<span data-ttu-id="ae619-115">*лпдвдататипе* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="ae619-115">*lpdwDataType* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ae619-116">Тип данных возвращаемых записей.</span><span class="sxs-lookup"><span data-stu-id="ae619-116">The data type of the returned entries.</span></span> <span data-ttu-id="ae619-117">Этот параметр может принимать одно из следующих значений:</span><span class="sxs-lookup"><span data-stu-id="ae619-117">This parameter can be one of the following values:</span></span>

<dl><span id="REG_BINARY"></span><span id="reg_binary"></span><dt>

<span data-ttu-id="ae619-118">**\_двоичный файл REG**</span><span class="sxs-lookup"><span data-stu-id="ae619-118">**REG\_BINARY**</span></span>
</dt><span id="REG_DWORD"></span><span id="reg_dword"></span><dt>

<span data-ttu-id="ae619-119">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="ae619-119">**REG\_DWORD**</span></span>
</dt><span id="REG_MULTI_SZ"></span><span id="reg_multi_sz"></span><dt>

<span data-ttu-id="ae619-120">**REG \_ Multi \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="ae619-120">**REG\_MULTI\_SZ**</span></span>
</dt><span id="REG_NONE"></span><span id="reg_none"></span><dt>

<span data-ttu-id="ae619-121">**REG \_ None**</span><span class="sxs-lookup"><span data-stu-id="ae619-121">**REG\_NONE**</span></span>
</dt><span id="REG_QWORD"></span><span id="reg_qword"></span><dt>

<span data-ttu-id="ae619-122">**REG \_ QWORD**</span><span class="sxs-lookup"><span data-stu-id="ae619-122">**REG\_QWORD**</span></span>
</dt><span id="REG_SZ"></span><span id="reg_sz"></span><dt>

<span data-ttu-id="ae619-123">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="ae619-123">**REG\_SZ**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="ae619-124">*лпбуффер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ae619-124">*lpBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae619-125">Буфер, который получает данные.</span><span class="sxs-lookup"><span data-stu-id="ae619-125">The buffer that receives the data.</span></span> <span data-ttu-id="ae619-126">Если буфер недостаточно велик для хранения данных, функция завершается ошибкой и возвращает **ошибку \_ недостаточного размера \_ буфера**.</span><span class="sxs-lookup"><span data-stu-id="ae619-126">If buffer is not large enough to contain the data, the function fails and returns **ERROR\_INSUFFICIENT\_BUFFER**.</span></span>

</dd> <dt>

<span data-ttu-id="ae619-127">*лпкббуфферсизе* \[ в, out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="ae619-127">*lpcbBufferSize* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ae619-128">Размер буфера *лпбуффер* в байтах.</span><span class="sxs-lookup"><span data-stu-id="ae619-128">The size of the *lpBuffer* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ae619-129">*птидата* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ae619-129">*ptiData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae619-130">[**TAGID**](tagid.md) ввода данных.</span><span class="sxs-lookup"><span data-stu-id="ae619-130">The [**TAGID**](tagid.md) of the data entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae619-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ae619-131">Return value</span></span>

<span data-ttu-id="ae619-132">Эта функция возвращает одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ae619-132">This function returns one of the following values.</span></span>



| <span data-ttu-id="ae619-133">Код возврата</span><span class="sxs-lookup"><span data-stu-id="ae619-133">Return code</span></span>                                                                                                    | <span data-ttu-id="ae619-134">Описание</span><span class="sxs-lookup"><span data-stu-id="ae619-134">Description</span></span>                                                            |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ae619-135"><dt>**Ошибка \_ недопустимого \_ параметра**</dt></span><span class="sxs-lookup"><span data-stu-id="ae619-135"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>       | <span data-ttu-id="ae619-136">Один или несколько входных параметров неверны.</span><span class="sxs-lookup"><span data-stu-id="ae619-136">One or more input parameters is incorrect.</span></span><br/>                  |
| <dl> <span data-ttu-id="ae619-137"><dt>**Ошибка \_ внутреннего \_ повреждения базы данных \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ae619-137"><dt>**ERROR\_INTERNAL\_DB\_CORRUPTION**</dt></span></span> </dl> | <span data-ttu-id="ae619-138">Не найдены записи данных для записи EXE.</span><span class="sxs-lookup"><span data-stu-id="ae619-138">No data entries were found for the EXE entry.</span></span><br/>               |
| <dl> <span data-ttu-id="ae619-139"><dt>**Ошибка \_ недостаточного \_ буфера**</dt></span><span class="sxs-lookup"><span data-stu-id="ae619-139"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl>     | <span data-ttu-id="ae619-140">Буфер недостаточно велик для хранения записей данных.</span><span class="sxs-lookup"><span data-stu-id="ae619-140">The buffer is not large enough to contain the data entries.</span></span><br/> |
| <dl> <span data-ttu-id="ae619-141"><dt>**Ошибка \_ не \_ хватает \_ памяти**</dt></span><span class="sxs-lookup"><span data-stu-id="ae619-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>      | <span data-ttu-id="ae619-142">Сбой выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="ae619-142">The memory allocation failed.</span></span><br/>                               |
| <dl> <span data-ttu-id="ae619-143"><dt>**Ошибка \_ не \_ найдена**</dt></span><span class="sxs-lookup"><span data-stu-id="ae619-143"><dt>**ERROR\_NOT\_FOUND**</dt></span></span> </dl>               | <span data-ttu-id="ae619-144">Не найдена запись данных с именем *лпсздатанаме* .</span><span class="sxs-lookup"><span data-stu-id="ae619-144">A data entry with the name *lpszDataName* was not found.</span></span><br/>    |
| <dl> <span data-ttu-id="ae619-145"><dt>**Ошибка при \_ успешном выполнении**</dt></span><span class="sxs-lookup"><span data-stu-id="ae619-145"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>                  | <span data-ttu-id="ae619-146">Функция успешно завершена.</span><span class="sxs-lookup"><span data-stu-id="ae619-146">The function completed successfully.</span></span><br/>                        |



 

## <a name="requirements"></a><span data-ttu-id="ae619-147">Требования</span><span class="sxs-lookup"><span data-stu-id="ae619-147">Requirements</span></span>



| <span data-ttu-id="ae619-148">Требование</span><span class="sxs-lookup"><span data-stu-id="ae619-148">Requirement</span></span> | <span data-ttu-id="ae619-149">Значение</span><span class="sxs-lookup"><span data-stu-id="ae619-149">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae619-150">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ae619-150">Minimum supported client</span></span><br/> | <span data-ttu-id="ae619-151">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ae619-151">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ae619-152">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ae619-152">Minimum supported server</span></span><br/> | <span data-ttu-id="ae619-153">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ae619-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ae619-154">DLL</span><span class="sxs-lookup"><span data-stu-id="ae619-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ae619-155"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae619-155"><dt>Apphelp.dll</dt></span></span> </dl> |



 

 




