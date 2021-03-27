---
description: Начинает поиск указанной строки поиска.
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'Метод Ишеллфолдерсеарчабле:: FindString (MMC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810948"
---
# <a name="ishellfoldersearchablefindstring-method"></a><span data-ttu-id="acaa0-103">Метод Ишеллфолдерсеарчабле:: FindString</span><span class="sxs-lookup"><span data-stu-id="acaa0-103">IShellFolderSearchable::FindString method</span></span>

<span data-ttu-id="acaa0-104">Начинает поиск указанной строки поиска.</span><span class="sxs-lookup"><span data-stu-id="acaa0-104">Begins a search for a specified search string.</span></span>

## <a name="syntax"></a><span data-ttu-id="acaa0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acaa0-105">Syntax</span></span>


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="acaa0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="acaa0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acaa0-107">*пвсзтаржет* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="acaa0-107">*pwszTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acaa0-108">Тип: **лпквстр**</span><span class="sxs-lookup"><span data-stu-id="acaa0-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="acaa0-109">Указатель на строку, указывающую ключевое слово поиска.</span><span class="sxs-lookup"><span data-stu-id="acaa0-109">A pointer to a string that specifies the search keyword.</span></span>

</dd> <dt>

<span data-ttu-id="acaa0-110">*пдвфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="acaa0-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acaa0-111">Введите: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="acaa0-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="acaa0-112">Флаги в настоящее время не определены; Задайте значение _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="acaa0-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="acaa0-113">*пунконасинксеарч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="acaa0-113">*punkOnAsyncSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="acaa0-114">Тип: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="acaa0-114">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="acaa0-115">Указатель на объект типа [_ *IUnknown* \*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span><span class="sxs-lookup"><span data-stu-id="acaa0-115">A pointer to an object of type [_ *IUnknown*\*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="acaa0-116">Этот объект должен поддерживать интерфейс [**ишеллфолдерсеарчаблекаллбакк**](ishellfoldersearchablecallback.md) .</span><span class="sxs-lookup"><span data-stu-id="acaa0-116">This object must support the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface.</span></span> <span data-ttu-id="acaa0-117">Если обратный вызов не требуется, задайте значение **null** .</span><span class="sxs-lookup"><span data-stu-id="acaa0-117">Set to **NULL** if no callback is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="acaa0-118">*ппидлаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="acaa0-118">*ppidlOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="acaa0-119">Тип: **лпитемидлист**</span><span class="sxs-lookup"><span data-stu-id="acaa0-119">Type: **LPITEMIDLIST**</span></span>

<span data-ttu-id="acaa0-120">Указатель на структуру [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) для папки поиска.</span><span class="sxs-lookup"><span data-stu-id="acaa0-120">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acaa0-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acaa0-121">Return value</span></span>

<span data-ttu-id="acaa0-122">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="acaa0-122">Type: **HRESULT**</span></span>

<span data-ttu-id="acaa0-123">Если этот метод завершается успешно, возвращается значение **S \_ ОК**.</span><span class="sxs-lookup"><span data-stu-id="acaa0-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="acaa0-124">В противном случае возвращается код ошибки **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="acaa0-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="acaa0-125">Требования</span><span class="sxs-lookup"><span data-stu-id="acaa0-125">Requirements</span></span>



| <span data-ttu-id="acaa0-126">Требование</span><span class="sxs-lookup"><span data-stu-id="acaa0-126">Requirement</span></span> | <span data-ttu-id="acaa0-127">Значение</span><span class="sxs-lookup"><span data-stu-id="acaa0-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="acaa0-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acaa0-128">Minimum supported client</span></span><br/> | <span data-ttu-id="acaa0-129">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="acaa0-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="acaa0-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acaa0-130">Minimum supported server</span></span><br/> | <span data-ttu-id="acaa0-131">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="acaa0-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="acaa0-132">Заголовок</span><span class="sxs-lookup"><span data-stu-id="acaa0-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="acaa0-133"><dt>MMC. h</dt></span><span class="sxs-lookup"><span data-stu-id="acaa0-133"><dt>Mmc.h</dt></span></span> </dl>       |
| <span data-ttu-id="acaa0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="acaa0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acaa0-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acaa0-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
