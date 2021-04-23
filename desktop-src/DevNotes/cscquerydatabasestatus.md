---
description: Получает состояние кэша автономные файлы.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: Функция Ксккуеридатабасестатус
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648978"
---
# <a name="cscquerydatabasestatus-function"></a><span data-ttu-id="79127-103">Функция Ксккуеридатабасестатус</span><span class="sxs-lookup"><span data-stu-id="79127-103">CSCQueryDatabaseStatus function</span></span>

<span data-ttu-id="79127-104">\[Эта функция не поддерживается и не должна использоваться.\]</span><span class="sxs-lookup"><span data-stu-id="79127-104">\[This function is not supported and should not be used.\]</span></span>

<span data-ttu-id="79127-105">Получает состояние кэша автономные файлы.</span><span class="sxs-lookup"><span data-stu-id="79127-105">Retrieves the status of the Offline Files cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="79127-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="79127-106">Syntax</span></span>


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a><span data-ttu-id="79127-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="79127-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79127-108">*пулстатус*</span><span class="sxs-lookup"><span data-stu-id="79127-108">*pulStatus*</span></span> 
</dt> <dd>

<span data-ttu-id="79127-109">Состояние.</span><span class="sxs-lookup"><span data-stu-id="79127-109">The status.</span></span> <span data-ttu-id="79127-110">Этот параметр может принимать одно из указанных ниже значений.</span><span class="sxs-lookup"><span data-stu-id="79127-110">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="79127-111">Значение</span><span class="sxs-lookup"><span data-stu-id="79127-111">Value</span></span>                                                                                                                                                                                                                                                                                                               | <span data-ttu-id="79127-112">Значение</span><span class="sxs-lookup"><span data-stu-id="79127-112">Meaning</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <span data-ttu-id="79127-113"><dt>**Флаг \_ DATABASESTATUS, \_ зашифрованный**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="79127-113"><dt>**FLAG\_DATABASESTATUS\_ENCRYPTED**</dt> <dt>0x00000002</dt></span></span> </dl>                                      | <span data-ttu-id="79127-114">Кэш помечен для шифрования, и все файлы в кэше шифруются.</span><span class="sxs-lookup"><span data-stu-id="79127-114">The cache is marked for encryption and all files in the cache are encrypted.</span></span><br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <span data-ttu-id="79127-115"><dt>**Флаг \_ DATABASESTATUS с \_ частичным \_ шифрованием**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="79127-115"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_ENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl>       | <span data-ttu-id="79127-116">Кэш помечен для шифрования, но некоторые файлы в кэше не шифруются.</span><span class="sxs-lookup"><span data-stu-id="79127-116">The cache is marked for encryption, but some files in the cache are not encrypted.</span></span><br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <span data-ttu-id="79127-117"><dt>**Флаг \_ DATABASESTATUS \_ частично без \_ шифрования**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="79127-117"><dt>**FLAG\_DATABASESTATUS\_PARTIALLY\_UNENCRYPTED**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="79127-118">Кэш не помечен для шифрования, но не все файлы в кэше были расшифрованы.</span><span class="sxs-lookup"><span data-stu-id="79127-118">The cache is not marked for encryption, but not all files in the cache have been decrypted.</span></span><br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <span data-ttu-id="79127-119"><dt>**Флаг \_ DATABASESTATUS без \_ шифрования**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="79127-119"><dt>**FLAG\_DATABASESTATUS\_UNENCRYPTED**</dt> <dt>0x00000000</dt></span></span> </dl>                                | <span data-ttu-id="79127-120">Кэш не помечен для шифрования, и все файлы в кэше были расшифрованы.</span><span class="sxs-lookup"><span data-stu-id="79127-120">The cache is not marked for encryption and all files in the cache have been decrypted.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="79127-121">*пулеррорс*</span><span class="sxs-lookup"><span data-stu-id="79127-121">*pulErrors*</span></span> 
</dt> <dd>

<span data-ttu-id="79127-122">Этот параметр имеет ненулевое значение, если возникла внутренняя ошибка базы данных или 0 в противном случае.</span><span class="sxs-lookup"><span data-stu-id="79127-122">This parameter is a nonzero value if there is an internal database error or 0 otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79127-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="79127-123">Return value</span></span>

<span data-ttu-id="79127-124">Эта функция возвращает **значение true** , если она выполнена. в противном случае возвращается **значение false**.</span><span class="sxs-lookup"><span data-stu-id="79127-124">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="79127-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79127-125">Remarks</span></span>

<span data-ttu-id="79127-126">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="79127-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="79127-127">Требования</span><span class="sxs-lookup"><span data-stu-id="79127-127">Requirements</span></span>



| <span data-ttu-id="79127-128">Требование</span><span class="sxs-lookup"><span data-stu-id="79127-128">Requirement</span></span> | <span data-ttu-id="79127-129">Значение</span><span class="sxs-lookup"><span data-stu-id="79127-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79127-130">DLL</span><span class="sxs-lookup"><span data-stu-id="79127-130">DLL</span></span><br/> | <dl> <span data-ttu-id="79127-131"><dt>Cscmig.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79127-131"><dt>Cscmig.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79127-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79127-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79127-133">**ксЦисксценаблед**</span><span class="sxs-lookup"><span data-stu-id="79127-133">**CSCIsCSCEnabled**</span></span>](csciscscenabled.md)
</dt> </dl>

 

 
