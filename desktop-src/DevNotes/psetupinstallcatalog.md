---
description: Устанавливает файл каталога.
ms.assetid: bea74e91-1a87-4785-b983-5fec87e03499
title: Функция Псетупинсталлкаталог
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupInstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 1fc3948233fe2716bd4a0a6d720a3f285a5476cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648873"
---
# <a name="psetupinstallcatalog-function"></a><span data-ttu-id="666b2-103">Функция Псетупинсталлкаталог</span><span class="sxs-lookup"><span data-stu-id="666b2-103">pSetupInstallCatalog function</span></span>

<span data-ttu-id="666b2-104">\[Эта функция больше не поддерживается корпорацией Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="666b2-104">\[This function is no longer supported by Microsoft.</span></span> <span data-ttu-id="666b2-105">Разработчики должны использовать **крипткатадминаддкаталог**.\]</span><span class="sxs-lookup"><span data-stu-id="666b2-105">Developers should use **CryptCATAdminAddCatalog**.\]</span></span>

<span data-ttu-id="666b2-106">Устанавливает файл каталога.</span><span class="sxs-lookup"><span data-stu-id="666b2-106">Installs a catalog file.</span></span>

## <a name="syntax"></a><span data-ttu-id="666b2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="666b2-107">Syntax</span></span>


```C++
DWORD pSetupInstallCatalog(
  _In_      LPCTSTR CatalogFullPath,
  _In_      LPCTSTR NewBaseName,
  _Out_opt_ LPTSTR  NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="666b2-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="666b2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="666b2-109">*Каталогфуллпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="666b2-109">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="666b2-110">Полный путь к каталогу, который должен быть установлен в системе.</span><span class="sxs-lookup"><span data-stu-id="666b2-110">The fully qualified path of the catalog to be installed on the system.</span></span>

</dd> <dt>

<span data-ttu-id="666b2-111">*Невбасенаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="666b2-111">*NewBaseName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="666b2-112">Новое базовое имя, используемое при копировании файла каталога в хранилище каталога.</span><span class="sxs-lookup"><span data-stu-id="666b2-112">The new base name to use when the catalog file is copied into the catalog store.</span></span>

</dd> <dt>

<span data-ttu-id="666b2-113">*Невкаталогфуллпас* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="666b2-113">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="666b2-114">При необходимости получает полный путь к файлу каталога в хранилище каталога.</span><span class="sxs-lookup"><span data-stu-id="666b2-114">Optionally receives the fully qualified path of the catalog file within the catalog store.</span></span> <span data-ttu-id="666b2-115">Этот буфер должен содержать по крайней мере **максимальный размер \_ пути** (версия ANSI) или символы (версия Юникода).</span><span class="sxs-lookup"><span data-stu-id="666b2-115">This buffer should be at least **MAX\_PATH** bytes (ANSI version) or chars (Unicode version).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="666b2-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="666b2-116">Return value</span></span>

<span data-ttu-id="666b2-117">Если функция завершается успешно, она **не возвращает \_ ошибку**. в противном случае она возвращает код ошибки Win32, указывающий на причину сбоя.</span><span class="sxs-lookup"><span data-stu-id="666b2-117">If the function succeeds, it returns **NO\_ERROR**; otherwise, it returns a Win32 error code that indicates the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="666b2-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="666b2-118">Remarks</span></span>

<span data-ttu-id="666b2-119">Файл копируется системой в специальный каталог и при необходимости переименовывается.</span><span class="sxs-lookup"><span data-stu-id="666b2-119">The file is copied by the system into a special directory and is optionally renamed.</span></span>

<span data-ttu-id="666b2-120">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="666b2-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="666b2-121">Требования</span><span class="sxs-lookup"><span data-stu-id="666b2-121">Requirements</span></span>



| <span data-ttu-id="666b2-122">Требование</span><span class="sxs-lookup"><span data-stu-id="666b2-122">Requirement</span></span> | <span data-ttu-id="666b2-123">Значение</span><span class="sxs-lookup"><span data-stu-id="666b2-123">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="666b2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="666b2-124">DLL</span></span><br/> | <dl> <span data-ttu-id="666b2-125"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="666b2-125"><dt>Setupapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="666b2-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="666b2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="666b2-127">**крипткатадминаддкаталог**</span><span class="sxs-lookup"><span data-stu-id="666b2-127">**CryptCATAdminAddCatalog**</span></span>](/windows/win32/api/mscat/nf-mscat-cryptcatadminaddcatalog)
</dt> </dl>

 

 
