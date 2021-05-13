---
description: Создает массив дескрипторов для значков, извлеченных из указанного файла.
title: Функция Шекстрактиконсв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840915"
---
# <a name="shextracticonsw-function"></a><span data-ttu-id="13261-103">Функция Шекстрактиконсв</span><span class="sxs-lookup"><span data-stu-id="13261-103">SHExtractIconsW function</span></span>

<span data-ttu-id="13261-104">\[**Шекстрактиконсв** доступен в Windows XP с пакетом обновления 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="13261-104">\[**SHExtractIconsW** is available through Windows XP Service Pack 2 (SP2).</span></span> <span data-ttu-id="13261-105">Он может быть изменен или недоступен в последующих версиях.\]</span><span class="sxs-lookup"><span data-stu-id="13261-105">It might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="13261-106">Создает массив дескрипторов для значков, извлеченных из указанного файла.</span><span class="sxs-lookup"><span data-stu-id="13261-106">Creates an array of handles to icons extracted from a specified file.</span></span>

## <a name="syntax"></a><span data-ttu-id="13261-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="13261-107">Syntax</span></span>


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a><span data-ttu-id="13261-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="13261-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13261-109">*pszFileName* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13261-109">*pszFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13261-110">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="13261-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="13261-111">Указатель на имя файла, из которого извлекаются значки.</span><span class="sxs-lookup"><span data-stu-id="13261-111">A pointer to the file name from which to extract the icons.</span></span>

</dd> <dt>

<span data-ttu-id="13261-112">*никониндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13261-112">*nIconIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13261-113">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="13261-113">Type: **int**</span></span>

<span data-ttu-id="13261-114">Индекс первого значка, извлекаемого из ресурса с именем в *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="13261-114">The index of the first icon to extract from the resource named in *pszFileName*.</span></span>

</dd> <dt>

<span data-ttu-id="13261-115">*кксикон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13261-115">*cxIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13261-116">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="13261-116">Type: **int**</span></span>

<span data-ttu-id="13261-117">Требуемая ширина значка.</span><span class="sxs-lookup"><span data-stu-id="13261-117">The desired width of the icon.</span></span> <span data-ttu-id="13261-118">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="13261-118">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="13261-119">*циикон* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13261-119">*cyIcon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13261-120">Тип: **int**</span><span class="sxs-lookup"><span data-stu-id="13261-120">Type: **int**</span></span>

<span data-ttu-id="13261-121">Желаемая высота значка.</span><span class="sxs-lookup"><span data-stu-id="13261-121">The desired height of the icon.</span></span> <span data-ttu-id="13261-122">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="13261-122">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="13261-123">*фикон* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="13261-123">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13261-124">Тип: **Хикон \***</span><span class="sxs-lookup"><span data-stu-id="13261-124">Type: **HICON\***</span></span>

<span data-ttu-id="13261-125">При возврате этой функции содержит указатель на массив дескрипторов значков.</span><span class="sxs-lookup"><span data-stu-id="13261-125">When this function returns, contains a pointer to the array of icon handles.</span></span>

</dd> <dt>

<span data-ttu-id="13261-126">*пиконид* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="13261-126">*pIconId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13261-127">Тип: **uint \***</span><span class="sxs-lookup"><span data-stu-id="13261-127">Type: **UINT\***</span></span>

<span data-ttu-id="13261-128">При возврате этой функции содержит указатель на идентификатор ресурса извлеченного значка, который лучше подходит для текущего устройства вывода.</span><span class="sxs-lookup"><span data-stu-id="13261-128">When this function returns, contains a pointer to the resource identifier of the extracted icon that best fits the current display device.</span></span> <span data-ttu-id="13261-129">Если для этого формата нет доступных идентификаторов, он содержит значение 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="13261-129">If there is no identifier available for this format, it contains 0xFFFFFFFF.</span></span> <span data-ttu-id="13261-130">Если идентификатор не может быть получен по какой либо другой причине, возвращает нуль.</span><span class="sxs-lookup"><span data-stu-id="13261-130">If no identifier can be obtained for any other reason, returns zero.</span></span>

</dd> <dt>

<span data-ttu-id="13261-131">*никонс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13261-131">*nIcons* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13261-132">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="13261-132">Type: **UINT**</span></span>

<span data-ttu-id="13261-133">Число значков, извлекаемых из ресурса с именем в *pszFileName*.</span><span class="sxs-lookup"><span data-stu-id="13261-133">The number of icons to extract from the resource named in *pszFileName*.</span></span> <span data-ttu-id="13261-134">Этот параметр допустим только в том случае, если ресурс является файлом EXE или DLL.</span><span class="sxs-lookup"><span data-stu-id="13261-134">This parameter is valid only when the resource is a .exe or .dll file.</span></span>

</dd> <dt>

<span data-ttu-id="13261-135">*Флаги* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="13261-135">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13261-136">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="13261-136">Type: **UINT**</span></span>

<span data-ttu-id="13261-137">Флаги, управляющие этой функцией.</span><span class="sxs-lookup"><span data-stu-id="13261-137">The flags that control this function.</span></span> <span data-ttu-id="13261-138">Возможные значения см. в описании параметра *фулоад* функции [**лоадимаже**](/windows/win32/api/winuser/nf-winuser-loadimagea) .</span><span class="sxs-lookup"><span data-stu-id="13261-138">For possible values, see the *fuLoad* parameter of the [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13261-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="13261-139">Return value</span></span>

<span data-ttu-id="13261-140">Тип: **uint**</span><span class="sxs-lookup"><span data-stu-id="13261-140">Type: **UINT**</span></span>

<span data-ttu-id="13261-141">Ненулевое значение в случае успеха; в противном случае — нуль.</span><span class="sxs-lookup"><span data-stu-id="13261-141">A nonzero value if successful; otherwise, zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="13261-142">Remarks</span><span class="sxs-lookup"><span data-stu-id="13261-142">Remarks</span></span>

<span data-ttu-id="13261-143">**Шекстрактиконсв** извлекает из следующих типов файлов.</span><span class="sxs-lookup"><span data-stu-id="13261-143">**SHExtractIconsW** extracts from the following file types.</span></span>

-   <span data-ttu-id="13261-144">Исполняемый файл (.EXE)</span><span class="sxs-lookup"><span data-stu-id="13261-144">Executable (.exe)</span></span>
-   <span data-ttu-id="13261-145">DLL (DLL)</span><span class="sxs-lookup"><span data-stu-id="13261-145">DLL (.dll)</span></span>
-   <span data-ttu-id="13261-146">Значок (ICO)</span><span class="sxs-lookup"><span data-stu-id="13261-146">Icon (.ico)</span></span>
-   <span data-ttu-id="13261-147">Курсор (CUR)</span><span class="sxs-lookup"><span data-stu-id="13261-147">Cursor (.cur)</span></span>
-   <span data-ttu-id="13261-148">Анимированный курсор (. ANI)</span><span class="sxs-lookup"><span data-stu-id="13261-148">Animated cursor (.ani)</span></span>
-   <span data-ttu-id="13261-149">Растровое изображение (.bmp)</span><span class="sxs-lookup"><span data-stu-id="13261-149">Bitmap (.bmp)</span></span>

<span data-ttu-id="13261-150">Извлечения из Windows 3. также поддерживаются *16-* разрядные исполняемые файлы (exe или DLL).</span><span class="sxs-lookup"><span data-stu-id="13261-150">Extractions from Windows 3.*x* 16-bit executable files (.exe or .dll) are also supported.</span></span>

<span data-ttu-id="13261-151">Параметры *кксикон* и *циикон* определяют размер извлекаемых значков.</span><span class="sxs-lookup"><span data-stu-id="13261-151">The *cxIcon* and *cyIcon* parameters specify the size of the icons to extract.</span></span> <span data-ttu-id="13261-152">Два размера можно извлечь с помощью каждого параметра, разделив значение между его ЛОВОРД и HIWORD.</span><span class="sxs-lookup"><span data-stu-id="13261-152">Two sizes can be extracted through each parameter by splitting the value between its LOWORD and HIWORD.</span></span> <span data-ttu-id="13261-153">Установите первый требуемый размер в ЛОВОРД параметра и второй размер в HIWORD.</span><span class="sxs-lookup"><span data-stu-id="13261-153">Put the first desired size in the LOWORD of the parameter and the second size in the HIWORD.</span></span> <span data-ttu-id="13261-154">Например, [**макелонг**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) для *кксикон* и *циикон* извлекает значки размером 24 и 48.</span><span class="sxs-lookup"><span data-stu-id="13261-154">For example, [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85))(24, 48) for both *cxIcon* and *cyIcon* extracts both 24 and 48 sized icons.</span></span>

<span data-ttu-id="13261-155">Вызывающий процесс отвечает за уничтожение всех значков, извлеченных с помощью этой функции, путем вызова функции [**дестройикон**](/windows/win32/api/winuser/nf-winuser-destroyicon) .</span><span class="sxs-lookup"><span data-stu-id="13261-155">The calling process is responsible for destroying all icons extracted through this function by calling the [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) function.</span></span>

<span data-ttu-id="13261-156">**Шекстрактиконсв** не экспортируется по имени или объявлено в общедоступном файле заголовка.</span><span class="sxs-lookup"><span data-stu-id="13261-156">**SHExtractIconsW** is not exported by name or declared in a public header file.</span></span> <span data-ttu-id="13261-157">Чтобы использовать его, необходимо объявить соответствующий прототип и использовать [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для запроса указателя на функцию от Shell32.dll, который можно использовать для вызова этой функции.</span><span class="sxs-lookup"><span data-stu-id="13261-157">To use it, you must declare a matching prototype and use [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to request a function pointer from Shell32.dll that can be used to call this function.</span></span>

## <a name="requirements"></a><span data-ttu-id="13261-158">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="13261-158">Requirements</span></span>



| <span data-ttu-id="13261-159">Требование</span><span class="sxs-lookup"><span data-stu-id="13261-159">Requirement</span></span> | <span data-ttu-id="13261-160">Значение</span><span class="sxs-lookup"><span data-stu-id="13261-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13261-161">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="13261-161">Minimum supported client</span></span><br/> | <span data-ttu-id="13261-162">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="13261-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="13261-163">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="13261-163">Minimum supported server</span></span><br/> | <span data-ttu-id="13261-164">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="13261-164">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="13261-165">DLL</span><span class="sxs-lookup"><span data-stu-id="13261-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13261-166"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="13261-166"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="13261-167">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="13261-167">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="13261-168">**Шекстрактиконсв** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="13261-168">**SHExtractIconsW** (Unicode)</span></span><br/>                                                                      |



 

 
