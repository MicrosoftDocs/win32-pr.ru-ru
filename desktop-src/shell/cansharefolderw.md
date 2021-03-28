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
ms.openlocfilehash: cf7d0feb31666f3a918c0307a0b0983bff246fea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540562"
---
# <a name="cansharefolderw-function"></a><span data-ttu-id="74932-103">Функция Каншарефолдерв</span><span class="sxs-lookup"><span data-stu-id="74932-103">CanShareFolderW function</span></span>

<span data-ttu-id="74932-104">\[Эта функция доступна в Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="74932-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="74932-105">Он может быть изменен или недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="74932-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="74932-106">Используется для определения, следует ли отображать **этот параметр общей папки** в веб-представлении.</span><span class="sxs-lookup"><span data-stu-id="74932-106">Used to determine whether to show the **Share this folder** option in web view.</span></span>

## <a name="syntax"></a><span data-ttu-id="74932-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="74932-107">Syntax</span></span>


```C++
STDAPI CanShareFolderW(
  _In_ LPCWSTR pszPath
);
```



## <a name="parameters"></a><span data-ttu-id="74932-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="74932-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74932-109">*псзпас* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="74932-109">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74932-110">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="74932-110">Type: **LPCWSTR**</span></span>

<span data-ttu-id="74932-111">Указатель на строку, указывающую путь к проверяемой папке.</span><span class="sxs-lookup"><span data-stu-id="74932-111">A pointer to a string that specifies the path of the folder to test.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74932-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="74932-112">Return value</span></span>

<span data-ttu-id="74932-113">Тип: **стдапи**</span><span class="sxs-lookup"><span data-stu-id="74932-113">Type: **STDAPI**</span></span>

<span data-ttu-id="74932-114">К возвращаемым значениям относятся следующие.</span><span class="sxs-lookup"><span data-stu-id="74932-114">Return values include the following.</span></span>



| <span data-ttu-id="74932-115">Возвращаемый код и значение</span><span class="sxs-lookup"><span data-stu-id="74932-115">Return code/value</span></span>                                                                        | <span data-ttu-id="74932-116">Описание</span><span class="sxs-lookup"><span data-stu-id="74932-116">Description</span></span>                                                                           |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="74932-117"><dt>**\_ОК**</dt></span><span class="sxs-lookup"><span data-stu-id="74932-117"><dt>**S\_OK**</dt></span></span> </dl>     | <span data-ttu-id="74932-118">Путь, на который указывает *псзпас* , указывает папку, к которой можно предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="74932-118">The path pointed to by *pszPath* specifies a folder that can be shared.</span></span><br/>    |
| <dl> <span data-ttu-id="74932-119"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="74932-119"><dt>**S\_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="74932-120">Путь, на который указывает *псзпас* , указывает папку, к которой нельзя предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="74932-120">The path pointed to by *pszPath* specifies a folder that cannot be shared.</span></span><br/> |
| <dl> <span data-ttu-id="74932-121"><dt>Ошибка HRESULT</dt></span><span class="sxs-lookup"><span data-stu-id="74932-121"><dt>HRESULT error</dt></span></span> </dl> | <span data-ttu-id="74932-122">Произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="74932-122">An error has occurred.</span></span><br/>                                                     |



 

## <a name="remarks"></a><span data-ttu-id="74932-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="74932-123">Remarks</span></span>

<span data-ttu-id="74932-124">Эта функция не имеет связанного LIB файла.</span><span class="sxs-lookup"><span data-stu-id="74932-124">This function has no associated .lib file.</span></span> <span data-ttu-id="74932-125">Для его использования необходимо использовать [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="74932-125">You must use [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to use it.</span></span>

## <a name="requirements"></a><span data-ttu-id="74932-126">Требования</span><span class="sxs-lookup"><span data-stu-id="74932-126">Requirements</span></span>



| <span data-ttu-id="74932-127">Требование</span><span class="sxs-lookup"><span data-stu-id="74932-127">Requirement</span></span> | <span data-ttu-id="74932-128">Значение</span><span class="sxs-lookup"><span data-stu-id="74932-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="74932-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="74932-129">Minimum supported client</span></span><br/> | <span data-ttu-id="74932-130">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="74932-130">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="74932-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="74932-131">Minimum supported server</span></span><br/> | <span data-ttu-id="74932-132">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="74932-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="74932-133">DLL</span><span class="sxs-lookup"><span data-stu-id="74932-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74932-134"><dt>Ntshrui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74932-134"><dt>Ntshrui.dll</dt></span></span> </dl> |
| <span data-ttu-id="74932-135">Имя в кодировке Юникод и ANSI</span><span class="sxs-lookup"><span data-stu-id="74932-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="74932-136">**Каншарефолдерв** (Юникод)</span><span class="sxs-lookup"><span data-stu-id="74932-136">**CanShareFolderW** (Unicode)</span></span><br/>                                               |



## <a name="see-also"></a><span data-ttu-id="74932-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="74932-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74932-138">**шовшарефолдеруи**</span><span class="sxs-lookup"><span data-stu-id="74932-138">**ShowShareFolderUI**</span></span>](./showsharefolderui.md)
</dt> </dl>

 

 
