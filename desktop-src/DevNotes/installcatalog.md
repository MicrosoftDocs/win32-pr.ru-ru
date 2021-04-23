---
description: Устанавливает каталог в каталог.
ms.assetid: 9741f8e3-d9db-46cd-886d-587f332b0ab8
title: Функция Инсталлкаталог
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallCatalog
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 57b2a9d29b72db6c04673f30f41f26c44701c69c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669068"
---
# <a name="installcatalog-function"></a><span data-ttu-id="8ffd6-103">Функция Инсталлкаталог</span><span class="sxs-lookup"><span data-stu-id="8ffd6-103">InstallCatalog function</span></span>

<span data-ttu-id="8ffd6-104">\[Эта функция не поддерживается и не должна использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="8ffd6-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="8ffd6-105">Устанавливает каталог в каталог.</span><span class="sxs-lookup"><span data-stu-id="8ffd6-105">Installs a catalog in a directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffd6-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ffd6-106">Syntax</span></span>


```C++
DWORD InstallCatalog(
  _In_      LPCTSTR                  CatalogFullPath,
  _In_opt_  LPCTSTR                  NewBaseName,
  _Out_opt_ ecount_(MAX_Path) LPTSTR NewCatalogFullPath
);
```



## <a name="parameters"></a><span data-ttu-id="8ffd6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="8ffd6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ffd6-108">*Каталогфуллпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="8ffd6-108">*CatalogFullPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffd6-109">Указатель на строку, представляющую полный путь к каталогу перед установкой.</span><span class="sxs-lookup"><span data-stu-id="8ffd6-109">A pointer to a string that represents the full path of the catalog before installation.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd6-110">*Невбасенаме* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="8ffd6-110">*NewBaseName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffd6-111">Указатель на новое базовое имя.</span><span class="sxs-lookup"><span data-stu-id="8ffd6-111">A pointer to the new base name.</span></span>

</dd> <dt>

<span data-ttu-id="8ffd6-112">*Невкаталогфуллпас* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="8ffd6-112">*NewCatalogFullPath* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ffd6-113">Указатель на строку, представляющую полный путь к каталогу после установки.</span><span class="sxs-lookup"><span data-stu-id="8ffd6-113">A pointer to a string that represent the full path of the catalog after installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ffd6-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8ffd6-114">Return value</span></span>

<span data-ttu-id="8ffd6-115">Эта функция в настоящее время не реализована, поэтому она не возвращает фактическое значение.</span><span class="sxs-lookup"><span data-stu-id="8ffd6-115">This function is not currently implemented, so it does not return an actual value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ffd6-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ffd6-116">Remarks</span></span>

<span data-ttu-id="8ffd6-117">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8ffd6-117">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ffd6-118">Требования</span><span class="sxs-lookup"><span data-stu-id="8ffd6-118">Requirements</span></span>



| <span data-ttu-id="8ffd6-119">Требование</span><span class="sxs-lookup"><span data-stu-id="8ffd6-119">Requirement</span></span> | <span data-ttu-id="8ffd6-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8ffd6-120">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ffd6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="8ffd6-121">DLL</span></span><br/> | <dl> <span data-ttu-id="8ffd6-122"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ffd6-122"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
