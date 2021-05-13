---
description: Используется для определения, следует ли отображать этот параметр общей папки в веб-представлении.
title: Функция Каншарефолдерв
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CanShareFolderW
- CanShareFolderW
api_type:
- DllExport
api_location:
- Ntshrui.dll
ms.assetid: 5fd28a14-53e7-4016-9c49-9bb14ce7808b
ms.openlocfilehash: 46df03208ecc468aac366fb0b4cfb33e1a68157e
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841685"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="e9db4-103">Функция Каншарефолдерв</span><span class="sxs-lookup"><span data-stu-id="e9db4-103">CanShareFolderW function</span></span>

<span data-ttu-id="e9db4-104">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e9db4-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="e9db4-105">Он может быть изменен или недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e9db4-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e9db4-106">Используется для определения, следует ли отображать **этот параметр общей папки** в веб-представлении.</span><span class="sxs-lookup"><span data-stu-id="e9db4-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9db4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9db4-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="e9db4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e9db4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9db4-109">*псзпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e9db4-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9db4-110">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="e9db4-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="e9db4-111">Указатель на строку, указывающую путь к проверяемой папке.</span><span class="sxs-lookup"><span data-stu-id="e9db4-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9db4-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e9db4-112">Return value</span></span>

<span data-ttu-id="e9db4-113">Тип: **стдапи**</span><span class="sxs-lookup"><span data-stu-id="e9db4-113">Type: **STDAPI**</span></span>

<span data-ttu-id="e9db4-114">К возвращаемым значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="e9db4-114">Return values include the following.</span></span>



| <span data-ttu-id="e9db4-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="e9db4-115">Return code/value</span></span>                                                                        | <span data-ttu-id="e9db4-116">Описание</span><span class="sxs-lookup"><span data-stu-id="e9db4-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e9db4-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="e9db4-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="e9db4-118">Путь, на который указывает *псзпас* , указывает папку, к которой можно предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="e9db4-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="e9db4-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e9db4-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="e9db4-120">Путь, на который указывает *псзпас* , указывает папку, к которой нельзя предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="e9db4-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="e9db4-121"><dt>Ошибка HRESULT</dt></span><span class="sxs-lookup"><span data-stu-id="e9db4-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="e9db4-122">Произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="e9db4-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="e9db4-123">Remarks</span><span class="sxs-lookup"><span data-stu-id="e9db4-123">Remarks</span></span>

<span data-ttu-id="e9db4-124">Эта функция не имеет связанного LIB файла.</span><span class="sxs-lookup"><span data-stu-id="e9db4-124">This function has no associated .lib file.</span></span> <span data-ttu-id="e9db4-125">Для его использования необходимо использовать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="e9db4-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9db4-126">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="e9db4-126">Requirements</span></span>



| <span data-ttu-id="e9db4-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e9db4-127">Requirement</span></span> | <span data-ttu-id="e9db4-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e9db4-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9db4-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e9db4-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e9db4-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e9db4-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e9db4-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e9db4-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e9db4-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e9db4-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e9db4-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e9db4-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9db4-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9db4-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9db4-135">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="e9db4-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e9db4-136">**Каншарефолдерв** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="e9db4-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="e9db4-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9db4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9db4-138">**шовшарефолдеруи**</span><span class="sxs-lookup"><span data-stu-id="e9db4-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
