---
description: Начинает процесс отмены ожидающего асинхронного поиска.
title: 'Метод Ишеллфолдерсеарчабле:: Канцеласинксеарч'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.CancelAsyncSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5c920dca-fbca-48e1-9dce-38713cf1fcef
ms.openlocfilehash: e9e3231e8cc602a4e00b6ee79a25392717b6e68b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984637"
---
# <a name="ishellfoldersearchablecancelasyncsearch-method"></a><span data-ttu-id="00b7e-103">Метод Ишеллфолдерсеарчабле:: Канцеласинксеарч</span><span class="sxs-lookup"><span data-stu-id="00b7e-103">IShellFolderSearchable::CancelAsyncSearch method</span></span>

<span data-ttu-id="00b7e-104">Начинает процесс отмены ожидающего асинхронного поиска.</span><span class="sxs-lookup"><span data-stu-id="00b7e-104">Begins the process of canceling a pending asynchronous search.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b7e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="00b7e-105">Syntax</span></span>


```C++
HRESULT CancelAsyncSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="00b7e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00b7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00b7e-107">*пидлсеарч* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00b7e-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00b7e-108">Тип: **лпЦитемидлист**</span><span class="sxs-lookup"><span data-stu-id="00b7e-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="00b7e-109">Указатель на [**итемидлист**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) для поиска.</span><span class="sxs-lookup"><span data-stu-id="00b7e-109">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) for the search.</span></span>

</dd> <dt>

<span data-ttu-id="00b7e-110">*пдвфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="00b7e-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00b7e-111">Введите: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="00b7e-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="00b7e-112">Флаги в настоящее время не определены; Задайте значение _ \* NULL \* \*.</span><span class="sxs-lookup"><span data-stu-id="00b7e-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00b7e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="00b7e-113">Return value</span></span>

<span data-ttu-id="00b7e-114">Тип: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00b7e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="00b7e-115">Возвращает \_ значение s ОК при отмене или \_ false, если поиск не выполняется.</span><span class="sxs-lookup"><span data-stu-id="00b7e-115">Returns S\_OK if canceling, or S\_FALSE if search is not running.</span></span>

## <a name="remarks"></a><span data-ttu-id="00b7e-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="00b7e-116">Remarks</span></span>

<span data-ttu-id="00b7e-117">При фактическом отмене поиска будет вызван [**руненд**](ishellfoldersearchablecallback-runend.md) .</span><span class="sxs-lookup"><span data-stu-id="00b7e-117">When the search is actually canceled, [**RunEnd**](ishellfoldersearchablecallback-runend.md) will be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="00b7e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="00b7e-118">Requirements</span></span>



| <span data-ttu-id="00b7e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="00b7e-119">Requirement</span></span> | <span data-ttu-id="00b7e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="00b7e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00b7e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="00b7e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="00b7e-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00b7e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="00b7e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="00b7e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="00b7e-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="00b7e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="00b7e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="00b7e-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00b7e-126"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00b7e-126"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




