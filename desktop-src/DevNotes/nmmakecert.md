---
description: Создает сертификат пользователя для использования с Конференцией NetMeeting.
ms.assetid: 22acdcbe-c9c9-4f1b-a62d-44a35e101eec
title: Функция Нммакецерт
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NmMakeCert
api_type:
- DllExport
api_location:
- Nmmkcert.dll
ms.openlocfilehash: f90af11ada2bca330bbabeb83f4a8aa94e611630
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648847"
---
# <a name="nmmakecert-function"></a><span data-ttu-id="8506b-103">Функция Нммакецерт</span><span class="sxs-lookup"><span data-stu-id="8506b-103">NmMakeCert function</span></span>

<span data-ttu-id="8506b-104">Создает сертификат пользователя для использования с Конференцией NetMeeting.</span><span class="sxs-lookup"><span data-stu-id="8506b-104">Creates a user certificate for use with NetMeeting conferencing.</span></span>

## <a name="syntax"></a><span data-ttu-id="8506b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8506b-105">Syntax</span></span>


```C++
void NmMakeCert(
   LPCSTR szFirstName,
   LPCSTR szLastName,
   LPCSTR szEmailName,
   LPCSTR szCity,
   LPCSTR szCountry,
   DWORD  dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8506b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8506b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8506b-107">*сзфирстнаме*</span><span class="sxs-lookup"><span data-stu-id="8506b-107">*szFirstName*</span></span> 
</dt> <dd>

<span data-ttu-id="8506b-108">Имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="8506b-108">The user's first name.</span></span>

</dd> <dt>

<span data-ttu-id="8506b-109">*сзластнаме*</span><span class="sxs-lookup"><span data-stu-id="8506b-109">*szLastName*</span></span> 
</dt> <dd>

<span data-ttu-id="8506b-110">Фамилия пользователя.</span><span class="sxs-lookup"><span data-stu-id="8506b-110">The user's last name.</span></span>

</dd> <dt>

<span data-ttu-id="8506b-111">*сземаилнаме*</span><span class="sxs-lookup"><span data-stu-id="8506b-111">*szEmailName*</span></span> 
</dt> <dd>

<span data-ttu-id="8506b-112">Имя электронной почты пользователя.</span><span class="sxs-lookup"><span data-stu-id="8506b-112">The user's email name.</span></span>

</dd> <dt>

<span data-ttu-id="8506b-113">*сзЦити*</span><span class="sxs-lookup"><span data-stu-id="8506b-113">*szCity*</span></span> 
</dt> <dd>

<span data-ttu-id="8506b-114">Город пользователя.</span><span class="sxs-lookup"><span data-stu-id="8506b-114">The user's city.</span></span>

</dd> <dt>

<span data-ttu-id="8506b-115">*сзкаунтри*</span><span class="sxs-lookup"><span data-stu-id="8506b-115">*szCountry*</span></span> 
</dt> <dd>

<span data-ttu-id="8506b-116">Страна или регион пользователя.</span><span class="sxs-lookup"><span data-stu-id="8506b-116">The user's country/region.</span></span>

</dd> <dt>

<span data-ttu-id="8506b-117">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="8506b-117">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="8506b-118">Значение, указывающее, как должен быть создан сертификат.</span><span class="sxs-lookup"><span data-stu-id="8506b-118">A value that indicates how the certificate should be created.</span></span> <span data-ttu-id="8506b-119">Может принимать любое из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="8506b-119">Values can be any of the following.</span></span>



| <span data-ttu-id="8506b-120">Значение</span><span class="sxs-lookup"><span data-stu-id="8506b-120">Value</span></span>                                                                                                                                                                                                                                                            | <span data-ttu-id="8506b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="8506b-121">Meaning</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="NMMKCERT_F_CLEANUP_ONLY"></span><span id="nmmkcert_f_cleanup_only"></span><dl> <span data-ttu-id="8506b-122"><dt>**Нммкцерт \_ F \_ Очистка \_ только**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="8506b-122"><dt>**NMMKCERT\_F\_CLEANUP\_ONLY**</dt> <dt>0x00000004</dt></span></span> </dl>    | <span data-ttu-id="8506b-123">Удалите старый сертификат, не создавая новый.</span><span class="sxs-lookup"><span data-stu-id="8506b-123">Delete the old certificate without creating a new one.</span></span> <br/>            |
| <span id="NMMKCERT_F_DELETEOLDCERT"></span><span id="nmmkcert_f_deleteoldcert"></span><dl> <span data-ttu-id="8506b-124"><dt>**Нммкцерт \_ F \_ делетеолдцерт**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="8506b-124"><dt>**NMMKCERT\_F\_DELETEOLDCERT**</dt> <dt>0x00000001</dt></span></span> </dl>  | <span data-ttu-id="8506b-125">Удалите старый сертификат, созданный ранее с помощью этой функции.</span><span class="sxs-lookup"><span data-stu-id="8506b-125">Delete the old certificate previously created with this function.</span></span> <br/> |
| <span id="NMMKCERT_F_LOCAL_MACHINE"></span><span id="nmmkcert_f_local_machine"></span><dl> <span data-ttu-id="8506b-126"><dt>**Нммкцерт \_ \_Локальный \_ компьютер F**</dt> ( <dt>0x00000002</dt> )</span><span class="sxs-lookup"><span data-stu-id="8506b-126"><dt>**NMMKCERT\_F\_LOCAL\_MACHINE**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="8506b-127">Создайте сертификат в хранилище сертификатов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="8506b-127">Create the certificate in the local machine certificate store.</span></span> <br/>    |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8506b-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8506b-128">Return value</span></span>

<span data-ttu-id="8506b-129">Возвращает значение 1, если функция завершается успешно, и – 1, если функция завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="8506b-129">Returns 1 if the function succeeds and –1 if the function fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="8506b-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8506b-130">Remarks</span></span>

<span data-ttu-id="8506b-131">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8506b-131">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8506b-132">Требования</span><span class="sxs-lookup"><span data-stu-id="8506b-132">Requirements</span></span>



| <span data-ttu-id="8506b-133">Требование</span><span class="sxs-lookup"><span data-stu-id="8506b-133">Requirement</span></span> | <span data-ttu-id="8506b-134">Значение</span><span class="sxs-lookup"><span data-stu-id="8506b-134">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8506b-135">DLL</span><span class="sxs-lookup"><span data-stu-id="8506b-135">DLL</span></span><br/> | <dl> <span data-ttu-id="8506b-136"><dt>Nmmkcert.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8506b-136"><dt>Nmmkcert.dll</dt></span></span> </dl> |



 

 
