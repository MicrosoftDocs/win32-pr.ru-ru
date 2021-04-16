---
description: Перечисляет отдельные элементы файла в разделе Каталогфилес файла определения каталога (CDF).
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: Функция Крипткаткдфенуммемберсбикдфтажекс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541002"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a><span data-ttu-id="5b371-103">Функция Крипткаткдфенуммемберсбикдфтажекс</span><span class="sxs-lookup"><span data-stu-id="5b371-103">CryptCATCDFEnumMembersByCDFTagEx function</span></span>

<span data-ttu-id="5b371-104">\[Функция **крипткаткдфенуммемберсбикдфтажекс** доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="5b371-104">\[The **CryptCATCDFEnumMembersByCDFTagEx** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5b371-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="5b371-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="5b371-106">Функция **крипткаткдфенуммемберсбикдфтажекс** перечисляет отдельные элементы File в разделе **каталогфилес** файла определения каталога (CDF).</span><span class="sxs-lookup"><span data-stu-id="5b371-106">The **CryptCATCDFEnumMembersByCDFTagEx** function enumerates the individual file members in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="5b371-107">**Крипткаткдфенуммемберсбикдфтажекс** вызывается [макекат](makecat.md).</span><span class="sxs-lookup"><span data-stu-id="5b371-107">**CryptCATCDFEnumMembersByCDFTagEx** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="5b371-108">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="5b371-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="5b371-109">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="5b371-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5b371-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b371-110">Syntax</span></span>


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="5b371-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="5b371-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b371-112">*пкдф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b371-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b371-113">Указатель на структуру [**крипткаткдф**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="5b371-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5b371-114">*пвсзпревкдфтаг* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="5b371-114">*pwszPrevCDFTag* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b371-115">Указатель на строку, **завершающуюся нулем,** которая определяет элемент файла каталога.</span><span class="sxs-lookup"><span data-stu-id="5b371-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="5b371-116">*пфнпарсиррор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b371-116">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b371-117">Указатель на определяемую пользователем функцию для обработки ошибок синтаксического анализа файла.</span><span class="sxs-lookup"><span data-stu-id="5b371-117">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> <dt>

<span data-ttu-id="5b371-118">*ппмембер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b371-118">*ppMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b371-119">Указатель на структуру [**крипткатмембер**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) , содержащую сведения об элементе файла.</span><span class="sxs-lookup"><span data-stu-id="5b371-119">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the file member information.</span></span>

</dd> <dt>

<span data-ttu-id="5b371-120">*фконтинуеонеррор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b371-120">*fContinueOnError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b371-121">Значение типа, указывающее, следует ли размещать в памяти ссылку на последний перечислимый элемент.</span><span class="sxs-lookup"><span data-stu-id="5b371-121">A value that specifies whether to keep in memory a reference to the last enumerated member.</span></span>

</dd> <dt>

<span data-ttu-id="5b371-122">*пвресервед* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="5b371-122">*pvReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b371-123">Этот параметр зарезервирован; не используйте его.</span><span class="sxs-lookup"><span data-stu-id="5b371-123">This parameter is reserved; do not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b371-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b371-124">Return value</span></span>

<span data-ttu-id="5b371-125">После успешного выполнения эта функция возвращает указатель на строку, завершающуюся **нулем**, которая определяет элемент файла в разделе **каталогфилес** CDF.</span><span class="sxs-lookup"><span data-stu-id="5b371-125">Upon success, this function returns a pointer to a **null**-terminated string that identifies a file member in the **CatalogFiles** section of a CDF.</span></span> <span data-ttu-id="5b371-126">При сбое функция **крипткаткдфенуммемберсбикдфтажекс** возвращает **пустой** указатель.</span><span class="sxs-lookup"><span data-stu-id="5b371-126">The **CryptCATCDFEnumMembersByCDFTagEx** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b371-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5b371-127">Remarks</span></span>

<span data-ttu-id="5b371-128">Обычно эта функция вызывается в цикле для перечисления всех элементов файла каталога в CDF.</span><span class="sxs-lookup"><span data-stu-id="5b371-128">You typically call this function in a loop to enumerate all of the catalog file members in a CDF.</span></span> <span data-ttu-id="5b371-129">Перед входом в цикл задайте  для Пвсзпревкдфтаг **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="5b371-129">Before entering the loop, set *pwszPrevCDFTag* to **NULL**.</span></span> <span data-ttu-id="5b371-130">Функция возвращает указатель на первый элемент.</span><span class="sxs-lookup"><span data-stu-id="5b371-130">The function returns a pointer to the first member.</span></span> <span data-ttu-id="5b371-131">Задайте *пвсзпревкдфтаг* в качестве возвращаемого значения функции для последующих итераций цикла.</span><span class="sxs-lookup"><span data-stu-id="5b371-131">Set *pwszPrevCDFTag* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="5b371-132">Примеры</span><span class="sxs-lookup"><span data-stu-id="5b371-132">Examples</span></span>

<span data-ttu-id="5b371-133">В следующем примере показана правильная последовательность назначений для параметра *пвсзпревкдфтаг* ( `pwszMemberTag` ).</span><span class="sxs-lookup"><span data-stu-id="5b371-133">The following example shows the correct sequence of assignments for the *pwszPrevCDFTag* parameter (`pwszMemberTag`).</span></span>


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="5b371-134">Требования</span><span class="sxs-lookup"><span data-stu-id="5b371-134">Requirements</span></span>



| <span data-ttu-id="5b371-135">Требование</span><span class="sxs-lookup"><span data-stu-id="5b371-135">Requirement</span></span> | <span data-ttu-id="5b371-136">Значение</span><span class="sxs-lookup"><span data-stu-id="5b371-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b371-137">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5b371-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5b371-138">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="5b371-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5b371-139">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5b371-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5b371-140">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5b371-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5b371-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5b371-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b371-142"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b371-142"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b371-143">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5b371-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b371-144">макекат</span><span class="sxs-lookup"><span data-stu-id="5b371-144">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="5b371-145">**крипткаткдф**</span><span class="sxs-lookup"><span data-stu-id="5b371-145">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="5b371-146">**крипткатмембер**</span><span class="sxs-lookup"><span data-stu-id="5b371-146">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="5b371-147">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="5b371-147">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="5b371-148">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="5b371-148">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
