---
description: Перечисляет атрибуты файлов элементов в разделе Каталогфилес файла определения каталога (CDF).
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: Функция Крипткаткдфенуматтрибутесвискдфтаг
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540999"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a><span data-ttu-id="1fe6b-103">Функция Крипткаткдфенуматтрибутесвискдфтаг</span><span class="sxs-lookup"><span data-stu-id="1fe6b-103">CryptCATCDFEnumAttributesWithCDFTag function</span></span>

<span data-ttu-id="1fe6b-104">\[Функция **крипткаткдфенуматтрибутесвискдфтаг** доступна для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-104">\[The **CryptCATCDFEnumAttributesWithCDFTag** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="1fe6b-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="1fe6b-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="1fe6b-106">Функция **крипткаткдфенуматтрибутесвискдфтаг** перечисляет атрибуты файлов элементов в разделе **каталогфилес** файла определения каталога (CDF).</span><span class="sxs-lookup"><span data-stu-id="1fe6b-106">The **CryptCATCDFEnumAttributesWithCDFTag** function enumerates the attributes of member files in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="1fe6b-107">**Крипткаткдфенуматтрибутесвискдфтаг** вызывается [макекат](makecat.md).</span><span class="sxs-lookup"><span data-stu-id="1fe6b-107">**CryptCATCDFEnumAttributesWithCDFTag** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="1fe6b-108">Эта функция не имеет связанного файла заголовка или библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="1fe6b-109">Чтобы вызвать эту функцию, необходимо создать файл заголовка, определяемый пользователем, и использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) для динамической привязки к Mssign32.dll.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="1fe6b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fe6b-110">Syntax</span></span>


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a><span data-ttu-id="1fe6b-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="1fe6b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fe6b-112">*пкдф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fe6b-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe6b-113">Указатель на структуру [**крипткаткдф**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) .</span><span class="sxs-lookup"><span data-stu-id="1fe6b-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1fe6b-114">*пвсзмембертаг* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fe6b-114">*pwszMemberTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe6b-115">Указатель на строку, **завершающуюся нулем,** которая определяет элемент файла каталога.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="1fe6b-116">*пмембер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fe6b-116">*pMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe6b-117">Указатель на структуру [**крипткатмембер**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) , содержащую сведения об элементе.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-117">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the member information.</span></span>

</dd> <dt>

<span data-ttu-id="1fe6b-118">*ппреваттр* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fe6b-118">*pPrevAttr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe6b-119">Указатель на структуру [**крипткататтрибуте**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) для атрибута элемента файла в CDF, на который указывает *пкдф*.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-119">A pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure for a file member attribute in the CDF pointed to by *pCDF*.</span></span>

</dd> <dt>

<span data-ttu-id="1fe6b-120">*пфнпарсиррор* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fe6b-120">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fe6b-121">Указатель на определяемую пользователем функцию для обработки ошибок синтаксического анализа файла.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-121">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fe6b-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1fe6b-122">Return value</span></span>

<span data-ttu-id="1fe6b-123">После успешного выполнения эта функция возвращает указатель на структуру [**крипткататтрибуте**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) .</span><span class="sxs-lookup"><span data-stu-id="1fe6b-123">Upon success, this function returns a pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure.</span></span> <span data-ttu-id="1fe6b-124">При сбое функция **крипткаткдфенуматтрибутесвискдфтаг** возвращает **пустой** указатель.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-124">The **CryptCATCDFEnumAttributesWithCDFTag** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fe6b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1fe6b-125">Remarks</span></span>

<span data-ttu-id="1fe6b-126">Обычно эта функция вызывается в цикле для перечисления всех атрибутов члена файла каталога в CDF.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-126">You typically call this function in a loop to enumerate all of the catalog file member attributes in a CDF.</span></span> <span data-ttu-id="1fe6b-127">Перед входом в цикл задайте  для Ппреваттр **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-127">Before entering the loop, set *pPrevAttr* to **NULL**.</span></span> <span data-ttu-id="1fe6b-128">Функция возвращает указатель на первый атрибут.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-128">The function returns a pointer to the first attribute.</span></span> <span data-ttu-id="1fe6b-129">Задайте *ппреваттр* в качестве возвращаемого значения функции для последующих итераций цикла.</span><span class="sxs-lookup"><span data-stu-id="1fe6b-129">Set *pPrevAttr* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="1fe6b-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="1fe6b-130">Examples</span></span>

<span data-ttu-id="1fe6b-131">В следующем примере показана правильная последовательность назначений для параметра *ппреваттр* ( `pAttr` ).</span><span class="sxs-lookup"><span data-stu-id="1fe6b-131">The following example shows the correct sequence of assignments for the *pPrevAttr* parameter (`pAttr`).</span></span>


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="1fe6b-132">Требования</span><span class="sxs-lookup"><span data-stu-id="1fe6b-132">Requirements</span></span>



| <span data-ttu-id="1fe6b-133">Требование</span><span class="sxs-lookup"><span data-stu-id="1fe6b-133">Requirement</span></span> | <span data-ttu-id="1fe6b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="1fe6b-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fe6b-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1fe6b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1fe6b-136">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1fe6b-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1fe6b-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1fe6b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1fe6b-138">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fe6b-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1fe6b-139">DLL</span><span class="sxs-lookup"><span data-stu-id="1fe6b-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fe6b-140"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fe6b-140"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fe6b-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fe6b-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fe6b-142">макекат</span><span class="sxs-lookup"><span data-stu-id="1fe6b-142">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="1fe6b-143">**крипткататтрибуте**</span><span class="sxs-lookup"><span data-stu-id="1fe6b-143">**CRYPTCATATTRIBUTE**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[<span data-ttu-id="1fe6b-144">**крипткаткдф**</span><span class="sxs-lookup"><span data-stu-id="1fe6b-144">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="1fe6b-145">**крипткатмембер**</span><span class="sxs-lookup"><span data-stu-id="1fe6b-145">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="1fe6b-146">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="1fe6b-146">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="1fe6b-147">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="1fe6b-147">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
