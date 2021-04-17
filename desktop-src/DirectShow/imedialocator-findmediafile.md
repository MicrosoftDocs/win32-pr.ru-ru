---
description: Метод Финдмедиафиле выполняет поиск файла и, в случае успешного выполнения, извлекает путь к файлу.
ms.assetid: ddfa2c75-e51f-4aad-afe6-8a60c46e8d35
title: 'Метод Имедиалокатор:: Финдмедиафиле (Кедит. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator.FindMediaFile
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3561b77873c90b2d4bd0202bed8e2da822a0362f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674974"
---
# <a name="imedialocatorfindmediafile-method"></a><span data-ttu-id="6bd6b-103">Метод Имедиалокатор:: Финдмедиафиле</span><span class="sxs-lookup"><span data-stu-id="6bd6b-103">IMediaLocator::FindMediaFile method</span></span>

> [!Note]  
> <span data-ttu-id="6bd6b-104">\[Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-104">\[Deprecated.</span></span> <span data-ttu-id="6bd6b-105">Этот API может быть удален из будущих выпусков Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6bd6b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="6bd6b-106">`FindMediaFile`Метод выполняет поиск файла и, при успешном выполнении, извлекает путь к файлу.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-106">The `FindMediaFile` method searches for a file and, if successful, retrieves the path to the file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bd6b-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bd6b-107">Syntax</span></span>


```C++
HRESULT FindMediaFile(
   BSTR Input,
   BSTR FilterString,
   BSTR *pOutput,
   long Flags
);
```



## <a name="parameters"></a><span data-ttu-id="6bd6b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bd6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bd6b-109">*Ввод*</span><span class="sxs-lookup"><span data-stu-id="6bd6b-109">*Input*</span></span> 
</dt> <dd>

<span data-ttu-id="6bd6b-110">Имя файла, включая путь, где находится файл, который был известен последним.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-110">File name, including path, where the file was last known to reside.</span></span> <span data-ttu-id="6bd6b-111">Для исходных объектов на временной шкале используйте текущее имя носителя.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-111">For source objects in the timeline, use the current media name.</span></span>

</dd> <dt>

<span data-ttu-id="6bd6b-112">*филтерстринг*</span><span class="sxs-lookup"><span data-stu-id="6bd6b-112">*FilterString*</span></span> 
</dt> <dd>

<span data-ttu-id="6bd6b-113">Строка **BSTR** , содержащая пары строк фильтра, отформатированные в соответствии с требованиями элемента **лпстрфилтер** структуры [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) .</span><span class="sxs-lookup"><span data-stu-id="6bd6b-113">A **BSTR** containing pairs of filter strings, formatted as required by the **lpstrFilter** member of the [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure.</span></span> <span data-ttu-id="6bd6b-114">Указатель мультимедиа использует этот фильтр, если он отображает диалоговое окно открытия файла.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-114">The media locator uses this filter if it displays a File Open dialog box.</span></span> <span data-ttu-id="6bd6b-115">Значение может быть **равно NULL** , если параметр *flags* не включает \_ \_ флаг всплывающего окна СФН валидатеф.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-115">The value can be **NULL** if the *Flags* parameter does not include the SFN\_VALIDATEF\_POPUP flag.</span></span>

</dd> <dt>

<span data-ttu-id="6bd6b-116">*паутпут*</span><span class="sxs-lookup"><span data-stu-id="6bd6b-116">*pOutput*</span></span> 
</dt> <dd>

<span data-ttu-id="6bd6b-117">Указатель на переменную, которая получает фактический путь к файлу, если он отличается от значения, содержащегося во *входных данных* , и если метод успешно найдет файл.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-117">Pointer to a variable that receives the actual path to the file, if it differs from the value contained in *Input* and if the method successfully locates the file.</span></span>

</dd> <dt>

<span data-ttu-id="6bd6b-118">*Флаги*</span><span class="sxs-lookup"><span data-stu-id="6bd6b-118">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="6bd6b-119">Битовая комбинация нуля или более флагов.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-119">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="6bd6b-120">Список возможных флагов см. в разделе [**Флаги проверки имени файла**](file-name-validation-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6bd6b-120">For a list of possible flags, see [**File Name Validation Flags**](file-name-validation-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bd6b-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bd6b-121">Return value</span></span>

<span data-ttu-id="6bd6b-122">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6bd6b-123">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6bd6b-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bd6b-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bd6b-124">Remarks</span></span>

<span data-ttu-id="6bd6b-125">Строка фильтра для диалогового окна открытия файла, заданная параметром *филтерстринг* , содержит внутренние символы NULL.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-125">The filter string for the File Open dialog, which is specified by the *FilterString* parameter, contains internal Null characters.</span></span> <span data-ttu-id="6bd6b-126">Например, видео \\ 0 \* . AVI \\ 0 \\ 0 является допустимой строкой фильтра.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-126">For example, Video\\0\*.avi\\0\\0 is a valid filter string.</span></span> <span data-ttu-id="6bd6b-127">Функцию **сисаллокстр** нельзя использовать для выделения строк BSTR, поскольку эта функция принимает строку, завершающуюся нулем, и усекает строку по первому пустому символу.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-127">You cannot use the **SysAllocStr** function to allocate the BSTR, because that function expects a Null-terminated string and will truncate the string at the first Null character.</span></span> <span data-ttu-id="6bd6b-128">Поэтому используйте функцию, такую как **сисаллокстринглен**, которая включает в себя явный параметр для длины:</span><span class="sxs-lookup"><span data-stu-id="6bd6b-128">Therefore, use a function such as **SysAllocStringLen**, which includes an explicit parameter for the length:</span></span>


```C++
BSTR filter = SysAllocStringLen(L"Video\0*.avi\0", 12);
// Note: SysAllocStringLen appends an additional '\0' to the string.
```



<span data-ttu-id="6bd6b-129">Если пользователь отменяет диалоговое окно открытия файла, метод возвращает \_ ошибку E.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-129">If the user cancels the File Open dialog, the method returns E\_FAIL.</span></span>

<span data-ttu-id="6bd6b-130">Метод выделяет память для **BSTR** в *паутпут*.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-130">The method allocates memory for the **BSTR** in *pOutput*.</span></span> <span data-ttu-id="6bd6b-131">Приложение должно вызвать **сисфристринг** для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-131">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="6bd6b-132">Файл заголовка Кедит. h несовместим с заголовками Direct3D позднее версии 7.</span><span class="sxs-lookup"><span data-stu-id="6bd6b-132">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="6bd6b-133">Чтобы получить Кедит. h, скачайте [обновление Microsoft Windows SDK для Windows Vista и платформа .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="6bd6b-133">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="6bd6b-134">Кедит. h недоступен в Microsoft Windows SDK для Windows 7 и платформа .NET Framework 3,5 с пакетом обновления 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="6bd6b-134">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6bd6b-135">Требования</span><span class="sxs-lookup"><span data-stu-id="6bd6b-135">Requirements</span></span>



| <span data-ttu-id="6bd6b-136">Требование</span><span class="sxs-lookup"><span data-stu-id="6bd6b-136">Requirement</span></span> | <span data-ttu-id="6bd6b-137">Значение</span><span class="sxs-lookup"><span data-stu-id="6bd6b-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6bd6b-138">Header</span><span class="sxs-lookup"><span data-stu-id="6bd6b-138">Header</span></span><br/>  | <dl> <span data-ttu-id="6bd6b-139"><dt>Кедит. h</dt></span><span class="sxs-lookup"><span data-stu-id="6bd6b-139"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="6bd6b-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6bd6b-140">Library</span></span><br/> | <dl> <span data-ttu-id="6bd6b-141"><dt>Стрмиидс. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6bd6b-141"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bd6b-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bd6b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bd6b-143">**Интерфейс Имедиалокатор**</span><span class="sxs-lookup"><span data-stu-id="6bd6b-143">**IMediaLocator Interface**</span></span>](imedialocator.md)
</dt> <dt>

[<span data-ttu-id="6bd6b-144">Коды ошибок и успешности</span><span class="sxs-lookup"><span data-stu-id="6bd6b-144">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 
