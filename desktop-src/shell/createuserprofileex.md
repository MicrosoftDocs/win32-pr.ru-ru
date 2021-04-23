---
description: Создает профиль пользователя для указанного пользователя.
ms.assetid: e4ea4032-d8d3-45c1-b2e5-7fef52a8a869
title: Функция Креатеусерпрофиликс
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateUserProfileEx
- CreateUserProfileExA
- CreateUserProfileExW
api_type:
- DllExport
api_location:
- Userenv.dll
ms.openlocfilehash: 8dbb76293fda769ec720221ca1bfa4474af1620c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987500"
---
# <a name="createuserprofileex-function"></a><span data-ttu-id="67f35-103">Функция Креатеусерпрофиликс</span><span class="sxs-lookup"><span data-stu-id="67f35-103">CreateUserProfileEx function</span></span>

<span data-ttu-id="67f35-104">\[Эта функция недоступна в Windows Vista.\]</span><span class="sxs-lookup"><span data-stu-id="67f35-104">\[This function is not available as of Windows Vista.\]</span></span>

<span data-ttu-id="67f35-105">Создает профиль пользователя для указанного пользователя.</span><span class="sxs-lookup"><span data-stu-id="67f35-105">Creates a user profile for a specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="67f35-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="67f35-106">Syntax</span></span>


```C++
BOOL WINAPI CreateUserProfileEx(
  _In_      PSID    pSid,
  _In_      LPCTSTR lpUserName,
  _In_opt_  LPCTSTR lpUserHive,
  _Out_opt_ LPTSTR  lpProfileDir,
  _In_      DWORD   dwDirSize,
  _In_      BOOL    bWin9xUpg
);
```



## <a name="parameters"></a><span data-ttu-id="67f35-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="67f35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67f35-108">*пустой pSid* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67f35-108">*pSid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67f35-109">Тип: **пустой pSid**</span><span class="sxs-lookup"><span data-stu-id="67f35-109">Type: **PSID**</span></span>

<span data-ttu-id="67f35-110">Идентификатор безопасности нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="67f35-110">The SID of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="67f35-111">*лпусернаме* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67f35-111">*lpUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67f35-112">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="67f35-112">Type: **LPCTSTR**</span></span>

<span data-ttu-id="67f35-113">Указатель на буфер, содержащий имя пользователя нового пользователя.</span><span class="sxs-lookup"><span data-stu-id="67f35-113">Pointer to a buffer that contains the user name of the new user.</span></span>

</dd> <dt>

<span data-ttu-id="67f35-114">*лпусерхиве* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="67f35-114">*lpUserHive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="67f35-115">Тип: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="67f35-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="67f35-116">Указатель на буфер, содержащий [куст реестра](../sysinfo/registry-hives.md) для использования.</span><span class="sxs-lookup"><span data-stu-id="67f35-116">Pointer to a buffer that contains the [registry hive](../sysinfo/registry-hives.md) to use.</span></span> <span data-ttu-id="67f35-117">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="67f35-117">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="67f35-118">*лппрофиледир* \[ out, необязательно\]</span><span class="sxs-lookup"><span data-stu-id="67f35-118">*lpProfileDir* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="67f35-119">Тип: **LPTSTR**</span><span class="sxs-lookup"><span data-stu-id="67f35-119">Type: **LPTSTR**</span></span>

<span data-ttu-id="67f35-120">Указатель на буфер, который при возврате этой функции получает путь к каталогу профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="67f35-120">Pointer to a buffer that, when this function returns, receives the user's profile directory path.</span></span> <span data-ttu-id="67f35-121">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="67f35-121">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="67f35-122">*двдирсизе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67f35-122">*dwDirSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67f35-123">Тип: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="67f35-123">Type: **DWORD**</span></span>

<span data-ttu-id="67f35-124">Размер буфера, заданного параметром *лппрофиледир*, в тчарс.</span><span class="sxs-lookup"><span data-stu-id="67f35-124">Size of the buffer specified by *lpProfileDir*, in TCHARs.</span></span>

</dd> <dt>

<span data-ttu-id="67f35-125">*bWin9xUpg* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="67f35-125">*bWin9xUpg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67f35-126">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="67f35-126">Type: **BOOL**</span></span>

<span data-ttu-id="67f35-127">**Значение true** , если профиль пользователя создается в ходе миграции профиля из Windows 9x; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="67f35-127">**TRUE** if the user profile is being created as part of a profile migration from Windows 9x; otherwise, **FALSE**.</span></span>

<span data-ttu-id="67f35-128">Если **значение равно true**, профиль пользователя настраивается в каталоге профиля по умолчанию — обычно C: \\ Documents and Settings \\ *username*.</span><span class="sxs-lookup"><span data-stu-id="67f35-128">When **TRUE**, the user profile is set up in the default profile directory—normally C:\\Documents and Settings\\*UserName*.</span></span> <span data-ttu-id="67f35-129">Если этот каталог уже существует, он используется.</span><span class="sxs-lookup"><span data-stu-id="67f35-129">If that directory already exists, it is used.</span></span> <span data-ttu-id="67f35-130">В противном случае он будет создан.</span><span class="sxs-lookup"><span data-stu-id="67f35-130">If it does not, it is created.</span></span>

<span data-ttu-id="67f35-131">Если задано **значение false**, каталог профиля по умолчанию создается, если он не существует.</span><span class="sxs-lookup"><span data-stu-id="67f35-131">If **FALSE**, the default profile directory is created if it does not exist.</span></span> <span data-ttu-id="67f35-132">Если каталог профиля по умолчанию уже существует, для этого профиля пользователя создается новый каталог.</span><span class="sxs-lookup"><span data-stu-id="67f35-132">If the default profile directory already exists, a new directory is created for this user profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67f35-133">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="67f35-133">Return value</span></span>

<span data-ttu-id="67f35-134">Тип: **bool** .</span><span class="sxs-lookup"><span data-stu-id="67f35-134">Type: **BOOL**</span></span>

<span data-ttu-id="67f35-135">Возвращает **значение true** , если новый профиль пользователя успешно создан; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="67f35-135">Returns **TRUE** if the new user profile was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="67f35-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="67f35-136">Remarks</span></span>

<span data-ttu-id="67f35-137">Эта функция не объявлена в заголовках пакета средств разработки программного обеспечения и не имеет связанной библиотеки импорта.</span><span class="sxs-lookup"><span data-stu-id="67f35-137">This function is not declared in the software development kit (SDK) headers and has no associated import library.</span></span> <span data-ttu-id="67f35-138">Для связи с Userenv.dll необходимо использовать функции [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="67f35-138">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to link to Userenv.dll.</span></span> <span data-ttu-id="67f35-139">Версия ANSI функции **креатеусерпрофиликса** упоминается из Userenv.dll как порядковый номер 153.</span><span class="sxs-lookup"><span data-stu-id="67f35-139">The ANSI version of the function, **CreateUserProfileExA** is referenced from Userenv.dll as ordinal 153.</span></span> <span data-ttu-id="67f35-140">Версия Юникода, **креатеусерпрофиликсв** , упоминается как порядковый номер 154.</span><span class="sxs-lookup"><span data-stu-id="67f35-140">The Unicode version, **CreateUserProfileExW** is referenced as ordinal 154.</span></span>

## <a name="requirements"></a><span data-ttu-id="67f35-141">Требования</span><span class="sxs-lookup"><span data-stu-id="67f35-141">Requirements</span></span>



| <span data-ttu-id="67f35-142">Требование</span><span class="sxs-lookup"><span data-stu-id="67f35-142">Requirement</span></span> | <span data-ttu-id="67f35-143">Значение</span><span class="sxs-lookup"><span data-stu-id="67f35-143">Value</span></span> |
|-----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="67f35-144">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="67f35-144">End of client support</span></span><br/>  | <span data-ttu-id="67f35-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="67f35-145">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="67f35-146">DLL</span><span class="sxs-lookup"><span data-stu-id="67f35-146">DLL</span></span><br/>                    | <dl> <span data-ttu-id="67f35-147"><dt>Userenv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67f35-147"><dt>Userenv.dll</dt></span></span> </dl> |
| <span data-ttu-id="67f35-148">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="67f35-148">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="67f35-149">**Креатеусерпрофиликсв** (Юникод) и **креатеусерпрофиликса** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="67f35-149">**CreateUserProfileExW** (Unicode) and **CreateUserProfileExA** (ANSI)</span></span><br/>      |



 

 
